---
title: Subscriber activity
excerpt: >-
  Track every purchase and update on a subscription contract with Recurly
  Commerce’s order history and activity log.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

### Prerequisites & limitations

* Requires that your Shopify store is connected to Recurly Commerce.

# Definition

Recurly Commerce surfaces two essential tools at the bottom of each subscription contract—**Order History** and the **Customer Activity Log**—so you can see exactly what’s happened on that subscription and who made each change.

* **Order History**: a chronological list of each successful renewal or one-off invoice, with full financial details.
* **Customer Activity Log**: an audit trail showing every change to the subscription contract, who performed it (merchant, customer, or system), and when.

# Key benefits

* **Full financial transparency**: Instantly review order amounts, taxes, shipping, and totals without jumping between systems.
* **End-to-end audit trail**: Know exactly who made what change and when—crucial for support and compliance.
* **Faster issue resolution**: With all activity exposed in one place, you can diagnose billing or contract questions in seconds.

# Key details

## Order history

Recurly Commerce logs each renewal or one-off invoice as its own line item, displaying:

* **Order Number** (clickable to open in Shopify)
* **Date** of the transaction
* **Subtotal**, **Tax**, **Shipping**, and **Total**

Click the order number to jump straight to Shopify’s Orders page and perform further actions like [refunds](https://docs.recurly.com/recurly-docs-commerce/docs/refund-a-subscription-in-shopify#/) or [fulfillments](fulfill-a-subscription-in-shopify) .

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/9d7b3e15528d56e95fcbef09ae84f56fe5c22bddf018c6e94d33ca778690b121-image.png" />

## Customer activity log

Every action on the subscription contract is recorded with:

* **Actor**

  * **Store Admin**: Changes made by your team in the Recurly Commerce app
  * **Customer**: Updates made via the customer portal
  * **Recurly Commerce System**: Automated or back-end updates
* **Action Details**: exactly what changed
* **Timestamp**: when it happened

Use this log to handle support tickets, verify subscription updates, and maintain complete visibility into your customer relationships.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/021d947e9632bd5120e476e0186894f616bd71aedac930aeb881fc9930ad6593-image.png" />