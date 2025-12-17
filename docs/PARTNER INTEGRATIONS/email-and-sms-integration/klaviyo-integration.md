---
title: Klaviyo integration
excerpt: >-
  Extend your Klaviyo flows with bespoke Recurly Commerce subscription events
  and customer properties—unlock powerful segmentation and personalized
  messaging.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

export const PrerequisitesLimitations = ({ header }) => {
  return (
    <div className="flex justify-start">
      <div className="rounded-md p-6 m-4 max-w-lg shadow-md border border-gray-300 dark:bg-gray-800 dark:border-gray-600">
        <p className="text-lg font-bold">{header}</p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          You must have an active Klaviyo account and the Recurly Commerce (Prive) Klaviyo integration enabled in your merchant admin.
        </p>
        <p>
          <i className="fa-solid fa-exclamation-triangle mr-4" />
          Data backfill populates historical customer properties but does <strong>not</strong> retroactively fire subscription events—only new events after integration will trigger metrics.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

The Klaviyo integration pushes Prive-specific metrics (e.g., subscription started, billing attempt failed) and customer properties (e.g., active subscriber count, pause status) into Klaviyo. These enrich your Klaviyo profiles and enable bespoke, event-driven flows and segments.

# Key benefits

* **Granular subscriber signals**: Fire events for every lifecycle milestone—starts, pauses, cancellations, upcoming orders, and more.
* **Rich customer profile**: Surface counts of active, cancelled, paused, and skipped subscriptions for precise segmentation.
* **Quick Actions**: Embed actionable links (skip next order, reactivate) directly in emails to drive self-service and reduce support tickets.

# Key details

## Available Recurly Commerce metrics / events

Below is the complete list of Recurly Commerce metrics/events that will be sent to Klaviyo in real time:

| Prive Metric in Klaviyo           | When is it triggered?                                                                            |
| --------------------------------- | ------------------------------------------------------------------------------------------------ |
| Prive Billing Attempt Failed      | Billing attempt failed                                                                           |
| Prive Contract Order Skipped      |                                                                                                  |
| Prive Gift Confirmation           | Gift subscription is created/purchased by the shopper.                                           |
| Prive Gift Confirmation Recipient |                                                                                                  |
| Prive Gift Opened                 |                                                                                                  |
| Prive Gift Order Placed           |                                                                                                  |
| Prive One Time Addon Created      |                                                                                                  |
| Prive One Time Addon Removed      |                                                                                                  |
| Prive Order Placed                | Renewal order has successfully been placed.                                                      |
| Prive Out Of Stock                | Product variant is deleted or has 0 quantity left.                                               |
| Prive Revoked Payment Method      |                                                                                                  |
| Prive Status Update               | Subscription’s status changes.                                                                   |
| Prive Subscription Cancelled      | Subscription is canceled by you in the merchant admin or by the customer in the customer portal. |
| Prive Subscription Started        | Subscription is created/purchased by the shopper.                                                |
| Prive Upcoming Order              | **3 calendar days** before the scheduled upcoming order.                                         |

### Recurly Commerce metric / event properties

Each event is accompanied by a rich set of properties for granular segmentation:

| Metric(s)                                              | Property                   | Type             | Description                                                                           |
| :----------------------------------------------------- | :------------------------- | :--------------- | :------------------------------------------------------------------------------------ |
| All metrics include the following properties           | charge_amount              | Number (e.g. 50) | Total amount the shopper paid when the subscription started (includes shipping, tax). |
| …                                                      | product_title              | String           | Shopify product title.                                                                |
| …                                                      | product_id                 | Number           | Shopify product ID.                                                                   |
| …                                                      | variant_id                 | Number           | Shopify variant ID.                                                                   |
| …                                                      | variant_title              | String           | Shopify variant title.                                                                |
| …                                                      | line_items                 | Array\<object>   | Subscription contract line items.                                                     |
| ...                                                    | addonItems                 | Array\<object>   | Subscription contract add-on items.                                                   |
| …                                                      | nextBillingDate            | String           | Subscription contract next billing date.                                              |
| …                                                      | order_interval_frequency   | Number           | Number relating to “Order Interval Unit” for subscription renewal cadence.            |
| …                                                      | order_interval_unit        | String           | “DAY”, “WEEK”, “MONTH”, or “YEAR”.                                                    |
| …                                                      | order_interval_days        | Number           | Number of days between renewals.                                                      |
| …                                                      | isPrepaid                  | Boolean          | True if the subscription is prepaid; false otherwise.                                 |
| ...                                                    | isGift                     | Boolean          | True if the subscription is a gift; false otherwise.                                  |
| …                                                      | $value                     | Number           | Subscription contract total charged amount (inc. taxes & shipping).                   |
| …                                                      | price                      | Number           | Subscription contract price before discounts.                                         |
| Additional property for "Prive Subscription Cancelled" | cancel_reason              | String           | Reason captured from the cancellation survey.                                         |
| Additional property for "Prive Status Update"          | new_status                 | String           | The new status of the subscription                                                    |
| Additional property for "Prive Billing Attempt Failed" | total_retries              | Number           | Number of dunning retry attempts (excludes the initial failure).                      |
| Additional property for "Prive Upcoming Order"         | isPrepaidUpcomingCharge    | Boolean          | True if the upcoming order is a fulfillment only; false if it includes a charge.      |
| Additional property for "Prive Upcoming Order"         | daysBeforeBilling          | Number           | Number of days before the next order                                                  |
| Prive Out of Stock                                     | (same as above properties) | …                | …                                                                                     |
| Prive Order Placed                                     | order_number               | Number           | The number of completed orders at the time the order placed metric fires.             |

Gift confirmation has several additional properties, which are shown in the below table

| Metric(s)               | Property             | Type | Description |
| :---------------------- | :------------------- | :--- | :---------- |
| Prive Gift Confirmation | sender_email         |      |             |
| …                       | sender_first_name    |      |             |
| …                       | sender_last_name     |      |             |
| …                       | sender_phone         |      |             |
| …                       | recipient_email      |      |             |
| …                       | recipient_first_name |      |             |
| ...                     | recipient_last_name  |      |             |
| …                       | recipient_phone      |      |             |
| …                       | number_of_deliveries |      |             |
| …                       | gift_message         |      |             |
| …                       | order_number         |      |             |
| …                       | order_name           |      |             |
| ...                     | order_internal_id    |      |             |
| …                       | shipping_method      |      |             |
| …                       | shipping_price       |      |             |
| ...                     | shipping_address     |      |             |

**Use Case:** Leverage these events to create custom segments in Klaviyo (e.g., “All subscribers with paused subscriptions AND billing failures in the last 7 days”) and trigger tailored flows.

## Available Recurly Commerce Customer properties

These properties are written to each Klaviyo profile under **Custom Properties**:

| Recurly Commerce Customer Property   | Type    | Description                                                       |
| ------------------------------------ | ------- | ----------------------------------------------------------------- |
| prive_is_active_subscriber           | Boolean | True if the customer has ≥1 active subscription; false otherwise. |
| prive_active_subscription_count      | Number  | Total number of active subscriptions for this customer.           |
| prive_status_active_subscriptions    | Number  | Alias for active subscription count.                              |
| prive_status_cancelled_subscriptions | Number  | Total number of cancelled subscriptions for this customer.        |
| prive_status_paused_subscriptions    | Number  | Total number of paused subscriptions for this customer.           |
| prive_status_skipped_subscriptions   | Number  | Total number of skipped subscriptions for this customer.          |

## Quick actions

Embed “Quick Action” links in Klaviyo emails to let subscribers self-serve common tasks (skip next order, reactivate subscription, add add-ons, etc.).

1. In the Recurly Commerce merchant admin, configure a quicklink with a **name** and an **action**.
2. After the next Recurly Commerce metric fires (e.g., upcoming order or cancelled), the quicklink appears in the customer’s Klaviyo profile.
3. Reference the quicklink in a Klaviyo flow using the variable syntax `{{ event.quicklink_name }}`.

   Once clicked, the action executes immediately and the subscriber sees a confirmation message.

## Data backfill

Customer properties are backfilled automatically for all existing subscription customers (including migrated).

> 🚧 Backfilling **does not** retroactively fire subscription events; only new events post-integration will trigger.

## Testing Klaviyo locally

To trial Klaviyo events in your local environment:

1. Request access to your merchant’s Klaviyo account for testing.
2. Copy the `accounts` row from production into your local database and extend the `expires_at` timestamp.
3. Update `merchantId` to your local merchant’s ID.
4. Trigger subscription events locally—they will appear in the test Klaviyo account.
