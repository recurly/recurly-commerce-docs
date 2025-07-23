---
title: Advanced analytics
excerpt: >-
  Export your subscription contracts and historical events as CSVs to power
  custom analyses and reporting.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

### Prerequisites & limitations

export const PrerequisitesLimitations = ({ header }) => {
  return (
    <div className="flex justify-start">
      <div className="rounded-md p-6 m-4 max-w-lg shadow-md border border-gray-300 dark:bg-gray-800 dark:border-gray-600">
        <p className="text-lg font-bold">{header}</p>
        <p>
          <i className="fa-solid fa-exclamation-triangle mr-4" />
          Exports may include large volumes of data—consider filtering by date where possible.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

Advanced Data Exporting provides two categories of reports—General and Historical—that you can select and download from the Recurly Commerce admin, giving you full visibility into your subscription business both now and over time.

# Key benefits

* **Current-state exports**: Instantly grab a snapshot of every active subscription contract and their product breakdowns.
* **Historical reports**: Pull comprehensive order and contract-event histories for deep-dive BI analyses.
* **Flexible date ranges**: Filter historical exports by custom date windows to focus on the periods that matter.

# Key details

## Accessing exports

1. In the Recurly Commerce app, **go** to **Settings**.
2. **Scroll** to the **Reports Available for Export** section.
3. **Select** one or more report checkboxes on the right.
4. **Click** **Download CSV**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/4e404c629949cc1e2a3531508f7ca55fcde186b8bdd72c700d343b3c8929b034-image.png" />

Reports are organized into two categories: **General** and **Historical**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/96ca7f232aa706b4993e70dacbb803c5e44cabc2cfe81df3ecb06ac2c7ea7dc3-image.png" />

***

## General reports

Reflect the current state of your subscription business.

| Report                                       | Description                                                                                                                                                                                      |
| -------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **All subscription contracts**               | A snapshot of every contract (each row = one `contractId`) including customer IDs, emails, next order dates, delivery & billing cadences, and more.                                              |
| **Subscription contracts product breakdown** | A detailed breakdown of each product in every contract (each row = one `contractLineItem` linked to a `contractId`), letting you analyze SKU popularity and cadence across your subscriber base. |

***

## Historical reports

Contain a source-of-truth history of past events. Select your desired date range before exporting.

| Report                                      | Description                                                                                                                                                           |
| ------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Orders (Historical)**                     | Each row = one past order by `orderId`, linked to a contract. Includes `chargeAmount` (price + shipping + tax) to help you calculate AOV and revenue over any period. |
| **Subscription Contract Activity**          | Each row = one contract event (`event_id`) for a `contractId`. Track when contracts were created, canceled, etc.                                                      |
| **Subscription Contract Detailed Activity** | Like Contract Activity but includes granular events—pauses, skips, swaps. Note: detailed events are only available for activity after April 29, 2022.                 |
| **Cancellation Survey (Historical)**        | Records of shopper cancellation reasons and related fields.                                                                                                           |
| **Retention Strategy Results (Historical)** | Shopper responses to your retention offers (e.g., discounts or incentives presented during cancellation flows).                                                       |
| **Billing Failures (Historical)**           | All failed billing attempts, including gateway error messages and retry counts.                                                                                       |

***

> **Note:** Historical exports can be large; use date filters to limit file size when possible.