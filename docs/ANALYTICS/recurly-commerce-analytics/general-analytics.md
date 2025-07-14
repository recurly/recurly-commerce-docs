---
title: General analytics
excerpt: >-
  The General Analytics dashboard provides an at-a-glance view of your
  subscription business performance, with flexible date ranges, comparison
  periods, and detailed executive reports.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

General Analytics surfaces high-level subscription health metrics—revenue, order volume, average order value—and empowers you to dive into monthly and daily breakdowns via the Executive Report and daily summaries.

# Key benefits

* **Holistic performance view**: See total gross sales, average order value, and order volume all in one place.
* **Flexible comparisons**: Compare current data against any prior period to spot trends and anomalies.
* **Deep drill-downs**: Access a comprehensive Executive Report and daily summaries for granular KPI insights.

# Key details

## Total gross sales during selected period

A line chart of subscription gross sales over time. The solid line reflects the current period; the dotted line shows the previous comparison period.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/a136c4d9bb1959ccf266daf761337f4dca1bb77bc229dbf1d51f60073feadeb1-image.png" />

## Average order value

Tracks the average dollar amount per subscription order (including initial purchases), helping you monitor changes in cart size over time.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/1b45129d690bc4d59d0fde7d5c7eef0d62f3ee4c238b96d01ce8c791699166b1-image.png" />

## Subscription orders processed

Displays the total number of subscription orders—both new and renewals—processed in the selected period.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/e6da7fd91451fc35b24e0c5df374512ff54220fccb71db28169592807982a056-image.png" />

## Monthly executive report

| Metric                                                         | Definition                                                                                               |
| -------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| **Gross Subscription Sales**                                   | Total gross sales (in merchant local currency, including tax and shipping) from all subscription orders. |
| **Subscription Sales (from first orders)**                     | Gross sales (including tax and shipping) from initial subscription purchase orders only.                 |
| **Subscription Sales (from recurring orders)**                 | Gross sales (including tax and shipping) from all subscription renewals, excluding initial purchases.    |
| **Subscription Orders**                                        | The count of subscription orders processed in the month (initial orders plus renewals).                  |
| **Gross Subscription Sales (from one-time add-ons)**           | Sum of gross sales from one-time add-on items purchased alongside subscriptions.                         |
| **Subscription Orders (with one-time add-ons)**                | Count of subscription orders that included at least one one-time add-on item.                            |
| **New Subscriptions**                                          | Number of initial subscription purchase orders processed in the month.                                   |
| **New Migrated Subscriptions**                                 | Number of initial subscription orders that were migrated into Recurly Commerce from another platform.    |
| **New Subscribers**                                            | Count of unique shoppers who purchased a new subscription in the month.                                  |
| **New Migrated Subscribers**                                   | Count of unique shoppers migrated into Recurly Commerce who had at least one subscription.               |
| **Active Subscriptions (including paused & dunning) (ending)** | Number of subscriptions in an active, paused, or dunning state at month-end.                             |
| **Cancelled Subscriptions (ending)**                           | Number of subscriptions in a cancelled state (excluding paused or dunning) at month-end.                 |
| **Actively Cancelled Subscriptions (ending)**                  | Subscriptions cancelled by either customer or merchant action at month-end.                              |
| **Passively Cancelled Subscriptions (ending)**                 | Subscriptions cancelled automatically due to failed payments & dunning policies at month-end.            |
| **Migrated Cancelled Subscriptions (ending)**                  | Subscriptions migrated into Recurly Commerce already in a cancelled state at month-end.                  |
| **Paused Subscriptions (ending)**                              | Subscriptions in a paused state at month-end, whether indefinitely or for a set number of deliveries.    |
| **Failed/Dunning Subscriptions (ending)**                      | Subscriptions in a failed payment state undergoing dunning management at month-end.                      |
| **All Subscriptions (ending)**                                 | Total subscriptions at month-end (active + paused + dunning + cancelled).                                |
| **Active Subscribers (including paused & dunning) (ending)**   | Unique subscribers with at least one active, paused, or dunning subscription at month-end.               |
| **Churned Subscribers (ending)**                               | Subscribers with zero active, paused, or dunning subscriptions at month-end.                             |
| **Actively Churned Subscribers (ending)**                      | Subscribers who churned by direct cancellation (customer or merchant) at month-end.                      |
| **Passively Churned Subscribers (ending)**                     | Subscribers who churned due to passive cancellation (failed payments & dunning) at month-end.            |
| **All Subscribers (ending)**                                   | Sum of Active Subscribers and Churned Subscribers at month-end.                                          |

## Subscription daily summary

Provides a day-by-day breakdown of each Executive Report metric for the selected period. Refer to the monthly definitions above for metric meanings.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/62910208917ca12c6e67b2b0111713b52e7d1f19529ff9b38b9c2110458a1c19-image.png" />

## Subscriber daily summary

Offers a daily view of subscriber counts—new, active, churned—matching the Executive Report definitions.

> **Note:** All data is shown in your store’s timezone and may differ from Shopify analytics due to differing aggregation methods.