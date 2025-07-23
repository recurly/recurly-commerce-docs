---
title: Gorgias integration
excerpt: >-
  Integrate Recurly Commerce with Gorgias to surface subscriber details and
  manage subscriptions right from your support tickets.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

### Video

<Embed typeOfEmbed="iframe" url="https://www.loom.com/embed/1f8b9b9e05584c87bf8665fa4f42e47d" href="https://www.loom.com/embed/1f8b9b9e05584c87bf8665fa4f42e47d" html="false" iframe="true" />

export const PrerequisitesLimitations = ({ header }) => {
  return (
    <div className="flex justify-start">
      <div className="rounded-md p-6 m-4 max-w-lg shadow-md border border-gray-300 dark:bg-gray-800 dark:border-gray-600">
        <p className="text-lg font-bold">{header}</p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          Requires a Gorgias account with API access and a Recurly Commerce subscription.
        </p>
        <p>
          <i className="fa-solid fa-exclamation-triangle mr-4" />
          Subscription data refreshes only when a ticket is updated (e.g., by sending a message or toggling a tag).
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

The Gorgias integration pulls Recurly Commerce subscriber and subscription contract data into the Gorgias ticket sidebar. Agents can inspect subscriber properties, review contract details, and invoke common subscription actions directly from the support interface.

# Key benefits

* **Faster support resolution**: See subscriber history and next order dates without leaving Gorgias.
* **In-ticket subscription controls**: Skip orders, change delivery dates, or jump to the contract in Recurly with one click.
* **Seamless data syncing**: Subscriber and subscription details stay up to date whenever the ticket is refreshed.

# Key details

## Available Recurly Commerce properties

### Subscriber Properties

Below is a list of Recurly Commerce subscriber properties available in the Gorgias “Subscriber” widget:

| Property                       | Description                                      |
| ------------------------------ | ------------------------------------------------ |
| **Customer Since**             | Earliest date the customer became a subscriber   |
| **Email**                      | Subscriber’s email address                       |
| **First Name**                 | Subscriber’s first name                          |
| **Id**                         | Unique subscriber identifier                     |
| **Last Name**                  | Subscriber’s last name                           |
| **Last Order**                 | Date of the last processed order                 |
| **Next Order**                 | Date of the next scheduled order                 |
| **Phone**                      | Subscriber’s phone number                        |
| **Total Active Subscriptions** | Count of active subscriptions for the subscriber |
| **Total Orders**               | Total number of orders the shopper has placed    |

![Gorgias subscriber widget](https://files.readme.io/3cff9280d25a1f28c54899c0b247017e74bb1bcddb960513889e66a43ed848be-image.png)

### Subscription Properties

The “Subscription” widget displays contract-specific properties:

| Property                     | Description                                  |
| ---------------------------- | -------------------------------------------- |
| **Contract id**              | Unique subscription contract identifier      |
| **Product Title**            | Title of the subscribed product              |
| **Status**                   | Contract state: ACTIVE, PAUSED, or CANCELLED |
| **Updated at**               | Timestamp of the last contract update        |
| **Order Interval Frequency** | Numeric frequency of renewals                |
| **Order Interval Unit**      | Unit of frequency (DAY, WEEK, MONTH)         |
| **Next Order Date**          | Date of the next renewal                     |
| **Cancellation Reason**      | Reason provided at cancellation              |

### Subscription Actions

Agents can trigger these actions directly from the sidebar:

| Action                   | Description                                                            |
| ------------------------ | ---------------------------------------------------------------------- |
| **Skip Subscription**    | Skip the next scheduled order                                          |
| **Change Delivery Date** | Set a new date for the upcoming delivery                               |
| **Manage Subscription**  | Open the full subscription in Recurly Commerce (requires portal login) |

![Gorgias subscription actions](https://files.readme.io/d9a02f6815a530855942f406237f87d47d05843c94c926ebffe9ec08eb36c4d3-image.png)

## Data refresh

All subscriber and contract data appears for migrated and new customers. Because Gorgias only reloads sidebar data on ticket updates (not on simple page load), perform an action like sending a message or adding/removing a tag to force a refresh.

## Setup

1. In your Recurly Commerce admin, go to **Integrations → Gorgias** or visit:\
   [https://admin.tryprive.com/integrations/gorgias](https://admin.tryprive.com/integrations/gorgias)
2. Copy the Gorgias **API URL** and **API Key** from your Gorgias dashboard (Settings → API).
3. Paste them into Recurly Commerce and click **Connect**.

![](https://files.readme.io/ae0f23457f5e288ec934e5f953cec169ad6444d58105216bbc1ae2c80b819d38-image.png)\
![](https://files.readme.io/8d153beb5939badb4a0f59ac4e8fc3a18235482f7cef28a736a6ccb4b55e3755-image.png)