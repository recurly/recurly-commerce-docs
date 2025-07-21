---
title: Free trial
excerpt: >-
  Use Recurly Commerce to configure a free trial experience using product
  variants, subscription offers, and automation for product swaps.
deprecated: false
hidden: true
metadata:
  robots: index
---
# Overview

### Prerequisites & limitations

* Each **subscription offer** can only have one option/cadence if using a product swap for free trials.
* If multiple free trial durations are needed (e.g., 7, 14, or 21 days), you must create **separate subscription offers** for each.
* This setup requires support from the Engineering team to complete the backend configuration.

# Definition

**Free trial**: A promotional subscription period where the user is not charged before being automatically enrolled in a paid plan.

**Product swap**: A feature that allows subscriptions to transition from one offer (e.g., free) to another (e.g., paid) automatically.

# Key benefits

* Enables automated transition from a free to paid subscription with minimal customer effort.
* Allows full customization of the trial period and post-trial cadence.
* Maintains a seamless Shopify experience by hiding paid options until the free trial ends.

***

# Key details

## Step 1: Create your Shopify product with two variants

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/940afd3a77f7a02cd3b09f50998807db90c56a9cdd58ef93c147b85e36036ff0-image.png" />

* One variant for the free trial (e.g., $0). The trial price will be $0 due to the 100% discount, regardless of how it's configured. However, whether the variant itself is priced at $0 or not depends on how you want the pricing to appear on the product display page.
* One variant for the paid subscription.

> **Note:** Label the variants clearly for internal reference.

***

## Set up the free trial offer in Recurly Commerce

1. Go to **Subscription Plans** and **press** **Create offer**.

<Image align="center" className="border" border={true} src="https://files.readme.io/48c12fe99d37b541f093cae58c5cd0a96c1ccac1fd6c1d2a669d8482a7486ded-image.png" />

2. **Create** a new offer for the **free** variant.

* Name and add a description for the offer group

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/5af3d65a8c8f52dd2db4e9ccca6560a70d7a6f7d67e5b07f8e3eb1e056f12308-image.png" />

* Select **ONLY** the free product variant and **press** **Confirm**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/a8bd70c93774a20a5f941e1a3c06e84c2c77df8339e4beb827d340056c1cd357-image.png" />

* **Choose** **Subscription Only**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/dce7707d7e70f4e4c0636340a02d7c7635d8e9d75f0804dc41f7c75ee9bd8e29-image.png" />

* Set up one cadence/option with **100% off** (this defines the trial length)

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/5882df6acb38198d0dd9872ba516f18a4e78427e993608732df47a36b1753279-image.png" />

* In **Product Swap and Add-ons**, **choose** the paid variant, **click** **Swap** and **confirm.**

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/d063f124f7ed8c249bc97c873e0153489b6077a800766dac9991686d5e49ec84-image.png" />

* Set **Special Discounts** to **None**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/96294f07acea29a8ddfe0a945520b6c21af6f6cd2b12c875045e01bd4930d7e4-image.png" />

* **Publish** the offer.

2. Edit the offer in **Subscription Plans**

   * Under **Options**, change the text to something like. :*“Delivered monthly for $24.99 after trial”*.
   * This is what customers will see in Shopify

## Set up the paid offer

1. Create another subscription offer for the **paid** variant

   * Name the offer group
   * Select the paid product variant
   * Choose **Subscription Only**
   * Define the cadence (e.g., 1 month)
   * No product swap required
   * Set **Special Discounts** to **None**

## Request engineering assistance

Provide the following to Support:

* Your Shopify store URL prefix (from **Settings > top-left**)
* The name of the paid offer

Engineering will:

* **Hide the paid offer** from the Shopify product display page (set visibility to `MERCHANT_PORTAL`)
* **Enable`swapOfferEnabled`** to allow cadence to update during the swap

## Create the automation

1. Go to **Automations**, create a new one using **Swap Automation**
2. Name the automation (e.g., *Culinary Crate – Free Trial Swap*)
3. Set trigger: Initial purchase of the **free variant**
4. In **Conditions**:

   * Set **On renewal** = 1
   * Select the **paid variant**
   * Check **Use this product’s plan** to apply the cadence from the paid offer
   * Leave discount at 0%
   * Save

## Test the full experience

1. Complete a test subscription from your Shopify store using the **free variant**
2. In Recurly Commerce:

   * Go to **Subscribers**, open the subscriber
   * Check **Manage Subscription Contracts**
   * Note the current frequency (e.g., every 7 days) and price ($0.00)
3. Click **Process Now** to trigger the renewal
4. After a few seconds, verify the swap:

   * Subscription cadence and price should update to the paid version
   * No refresh needed
   * Example: “Every month for $24.99”