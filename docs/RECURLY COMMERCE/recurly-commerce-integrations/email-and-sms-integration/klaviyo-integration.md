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

### Prerequisites & limitations

* You must have an active Klaviyo account and the Recurly Commerce (Prive) Klaviyo integration enabled in your merchant admin.
* Data backfill populates historical customer properties but does **not** retroactively fire subscription events—only new events after integration will trigger metrics.

# Definition

The Klaviyo integration pushes Prive-specific metrics (e.g., subscription started, billing attempt failed) and customer properties (e.g., active subscriber count, pause status) into Klaviyo. These enrich your Klaviyo profiles and enable bespoke, event-driven flows and segments.

# Key benefits

* **Granular subscriber signals**: Fire events for every lifecycle milestone—starts, pauses, cancellations, upcoming orders, and more.
* **Rich customer profile**: Surface counts of active, cancelled, paused, and skipped subscriptions for precise segmentation.
* **Quick Actions**: Embed actionable links (skip next order, reactivate) directly in emails to drive self-service and reduce support tickets.

# Key details

## Available Recurly Commerce metrics / events

Below is the complete list of Recurly Commerce metrics/events that will be sent to Klaviyo in real time:

| Prive Metric in Klaviyo      | When is it triggered?                                                                                                            |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| Recurly Commerce Subscription Started   | This metric is triggered when a subscription is created/purchased by the shopper.                                                |
| Recurly Commerce Subscription Cancelled | This metric is triggered when a subscription is canceled by you in the merchant admin or by the customer in the customer portal. |
| Recurly Commerce Subscription Paused    | This metric is triggered when a subscription is paused by you in the merchant admin or by the customer in the customer portal.   |
| Recurly Commerce Status Update          | This metric is triggered when a subscription’s status changes.                                                                   |
| Recurly Commerce Billing Attempt Failed | This metric is triggered when a billing attempt failed.                                                                          |
| Recurly Commerce Upcoming Order         | This metric is triggered **3 calendar days** before the scheduled upcoming order.                                                |
| Recurly Commerce Gift Confirmation      | This metric is triggered when a gift subscription is created/purchased by the shopper.                                           |
| Recurly Commerce Out of Stock           | This metric is triggered when a product variant is deleted or has 0 quantity left.                                               |
| Recurly Commerce Order Placed           | This metric is triggered when a renewal order has successfully been placed.                                                      |

### Recurly Commerce metric / event properties

Each event is accompanied by a rich set of properties for granular segmentation:

| Metric(s)                      | Property                      | Type             | Description                                                                           |
| ------------------------------ | ----------------------------- | ---------------- | ------------------------------------------------------------------------------------- |
| Recurly Commerce Subscription Started     | charge\_amount                | Number (e.g. 50) | Total amount the shopper paid when the subscription started (includes shipping, tax). |
| …                              | product\_title                | String           | Shopify product title.                                                                |
| …                              | product\_id                   | Number           | Shopify product ID.                                                                   |
| …                              | variant\_id                   | Number           | Shopify variant ID.                                                                   |
| …                              | variant\_title                | String           | Shopify variant title.                                                                |
| …                              | line\_items                   | Array\<object>   | Subscription contract line items.                                                     |
| …                              | next\_billing\_date           | String           | Subscription contract next billing date.                                              |
| …                              | order\_interval\_frequency    | Number           | Number relating to “Order Interval Unit” for subscription renewal cadence.            |
| …                              | order\_interval\_unit         | String           | “DAY”, “WEEK”, “MONTH”, or “YEAR”.                                                    |
| …                              | order\_interval\_days         | Number           | Number of days between renewals.                                                      |
| …                              | is\_prepaid                   | Boolean          | True if the subscription is prepaid; false otherwise.                                 |
| …                              | value                         | Number           | Subscription contract total charged amount (inc. taxes & shipping).                   |
| …                              | price                         | Number           | Subscription contract price before discounts.                                         |
| – Recurly Commerce Subscription Cancelled | cancel\_reason                | String           | Reason captured from the cancellation survey.                                         |
| – Recurly Commerce Billing Attempt Failed | total\_retries                | Number           | Number of dunning retry attempts (excludes the initial failure).                      |
| – Recurly Commerce Upcoming Order         | is\_prepaid\_upcoming\_charge | Boolean          | True if the upcoming order is a fulfillment only; false if it includes a charge.      |
| – Recurly Commerce Gift Confirmation      | order\_number                 | Number           | The number of completed orders at the time the gift confirmation metric fires.        |
| – Recurly Commerce Out of Stock           | (same as above properties)    | …                | …                                                                                     |
| – Recurly Commerce Order Placed           | order\_number                 | Number           | The number of completed orders at the time the order placed metric fires.             |

> **Use Case:** Leverage these events to create custom segments in Klaviyo (e.g., “All subscribers with paused subscriptions AND billing failures in the last 7 days”) and trigger tailored flows.

## Available Recurly Commerce Customer properties

These properties are written to each Klaviyo profile under **Custom Properties**:

| Recurly Commerce Customer Property      | Type    | Description                                                       |
| --------------------------------------- | ------- | ----------------------------------------------------------------- |
| prive\_is\_active\_subscriber           | Boolean | True if the customer has ≥1 active subscription; false otherwise. |
| prive\_active\_subscription\_count      | Number  | Total number of active subscriptions for this customer.           |
| prive\_status\_active\_subscriptions    | Number  | Alias for active subscription count.                              |
| prive\_status\_cancelled\_subscriptions | Number  | Total number of cancelled subscriptions for this customer.        |
| prive\_status\_paused\_subscriptions    | Number  | Total number of paused subscriptions for this customer.           |
| prive\_status\_skipped\_subscriptions   | Number  | Total number of skipped subscriptions for this customer.          |

## Quick actions

Embed “Quick Action” links in Klaviyo emails to let subscribers self-serve common tasks (skip next order, reactivate subscription, add add-ons, etc.).

1. In the Recurly Commerce merchant admin, configure a quicklink with a **name** and an **action**.
2. After the next Recurly Commerce metric fires (e.g., upcoming order or cancelled), the quicklink appears in the customer’s Klaviyo profile.
3. Reference the quicklink in a Klaviyo flow using the variable syntax `{{ event.extra.quicklink_name }}`.

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