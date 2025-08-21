---
title: Order tagging
excerpt: >-
  Automatically label and filter subscription orders in Shopify using Recurly
  Commerce’s built-in tagging system.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

Recurly Commerce tags every subscription order in Shopify—so you can instantly spot, filter, and analyze subscriptions alongside one-time purchases.

### Video

<Embed typeOfEmbed="iframe" url="https://www.loom.com/embed/5f9882b2fca94287b34bf53f93e37df2" href="https://www.loom.com/embed/5f9882b2fca94287b34bf53f93e37df2" html="false" iframe="true" />

export const PrerequisitesLimitations = ({ header }) => {
  return (
    <div className="flex justify-start">
      <div className="rounded-md p-6 m-4 max-w-lg shadow-md border border-gray-300 dark:bg-gray-800 dark:border-gray-600">
        <p className="text-lg font-bold">{header}</p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          Only subscription orders are tagged; one-time purchase orders remain untagged.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

Order tagging is the automatic assignment of Shopify tags to subscription orders, letting you differentiate, filter, and report on them with precision.

# Key benefits

* **Clear differentiation**: Tags mark subscription purchases so you can instantly distinguish them from one-time orders.
* **Powerful filtering**: Leverage Shopify’s tag filters to segment and search your order history.
* **Analytics-ready**: Use tags in your reports, dashboards, or integrations for deeper insights.

# Key details

## Subscription tag types

Recurly Commerce applies these standard tags to subscription orders:

| Tag                              | Description                                                                                                                                     |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **Subscription order**           | Applied to every subscription order—use it to separate subscription orders from one-time purchases.                                             |
| **Subscription order \<number>** | Sequential tag per subscription: initial purchase is “Subscription order 1,” renewals increment the number (e.g. “Subscription order 2,” etc.). |
| **First time subscriber**        | Marks a customer’s very first subscription order. (Migrated subscribers will not receive this tag.)                                             |
| **Recurring subscription order** | Applied to all renewal orders after the first—signifies returning subscribers.                                                                  |
| **Shipping Profile**             | Reflects the Shopify shipping profile selected for that order (e.g., economy, free shipping), enabling fulfillment or reporting logic.          |
| **Gift subscription order**      | When the order is a gifted subscription, initial and recurring orders will have this tag.                                                       |
| **Prepaid subscription order**   | If the contract is a prepaid contract initial and recurring orders will have this tag.                                                          |

## Filter by tags

To locate tagged subscription orders in Shopify:

1. **Navigate** to **Orders** in your Shopify admin.
2. **Click** **Filter** above the order list.
3. **Select** **Tagged with** from the dropdown.
4. **Type** the tag you wish to filter by (e.g., “Subscription order 1”).
5. **Add** multiple tags to compare or combine filter criteria.

Now you can view, export, or act on subscription orders with ease.