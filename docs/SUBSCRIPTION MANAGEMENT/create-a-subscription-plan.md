---
title: Create a subscription plan
excerpt: >-
  Learn how to create and configure a subscription plan in Recurly Commerce—from
  product selection and purchasing options to discounts, gifting, and shipping
  rules—so you can launch offers in minutes.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

### Video

<Embed typeOfEmbed="iframe" url="https://www.loom.com/embed/6d76a0c604b2499788f2d7c398f989da" href="https://www.loom.com/embed/6d76a0c604b2499788f2d7c398f989da" html="false" iframe="true" />

export const PrerequisitesLimitations = ({ header }) => {
  return (
    <div className="flex justify-start">
      <div className="rounded-md p-6 m-4 max-w-lg shadow-md border border-gray-300 dark:bg-gray-800 dark:border-gray-600">
        <p className="text-lg font-bold">{header}</p>
        <p>
          <i className="fa-solid fa-exclamation-triangle mr-4" />
          Only products without an existing subscription offer can be selected.
        </p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          Your Shopify catalog must be synced to Recurly Commerce.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

A subscription plan in Recurly Commerce defines which products customers can subscribe to, how often they’re billed, and any discounts, gifting options, add-ons, or shipping rules that apply.

# Key benefits

* **Launch in minutes**: Spin up subscription offers without touching code or waiting on engineering.
* **Flexible pricing & discounts**: Configure one-time, subscription-only, prepaid, or hybrid offers with tiered discounts and special promotions.
* **Rich add-ons & gifting**: Enable product swaps, one-time or recurring add-ons, and gift-option prompts to boost average order value and delight customers.

# Key details

## Creating a subscription plan

With Recurly Commerce, you can create a subscription offer in minutes, which will feed into your storefront widget where your customers can add a subscription product to cart.

***

## Subscription Information

1. In the Recurly Commerce admin, navigate to **Subscription Plans** and click **+ Create Offer** in the top-right.
2. In **Subscription Information**, enter:

   * **Subscription offer group name**: an internal name for your team to reference.
   * **Description**: internal notes—your customers never see these.
3. Click **+ Select Products**. Your entire Shopify SKU catalog loads in a modal.

   * Check the box next to each product you wish to include in this plan.
   * Uncheck to remove. These selections determine which product detail pages (PDPs) display the subscription widget.
4. Click **Confirm** at the bottom to save your product selection.

<Image align="center" border={true} width="80% " src="https://files.readme.io/5c2549766a6b2e0a8dd67f5c7bea1116cef0cc396e5c0b7b0a26a61d4b220a87-Screenshot_2025-09-26_at_9.25.00_AM.png" className="border" />

> **Note:** Only products that do not currently have a subscription offer are available for selection.

***

## Choosing purchasing options

Once your products are chosen, select how they’ll be offered to customers:

* **One-time & Subscribe & Save**

  * Customers can either purchase once or subscribe on a recurring schedule.
* **Subscription only**

  * The product is available exclusively as a subscription.
* **Pre-paid subscription only**

  * Customers pay upfront for the entire subscription term (e.g., full year) and receive deliveries at each interval.
* **One-time, subscribe & save, and prepaid subscription**

  * All three options appear in the widget, letting customers choose among one-time purchase, recurring billing, or prepaid plans.
* **Membership**
  * Offer the product as a membership subscription.

<Image align="center" border={true} width="80% " src="https://files.readme.io/dd6d4f1d03626768caf8db315ff226aaca23978fe427df8d65d33cf5e74bf9c8-Screenshot_2025-09-26_at_9.40.21_AM.png" className="border" />

***

## Add subscription options & discounts

1. Select **Offer discounts**  or **Do not offer discounts** to enable or disable promotional pricing.
2. Click **+ Add Option** to define each delivery frequency (e.g., every 1 month, every 2 months).
3. For each frequency, enter the discount percentage you wish to apply (e.g., 15% off every month, 10% off every 2 months).

> **Note:** Offering larger discounts for more frequent deliveries incentivizes subscriptions and boosts customer retention.

<Image align="center" border={true} width="80% " src="https://files.readme.io/c9dd086c9c900a959aaa9d97a47fb5cb2eb70e97a27d8b0f2530f40bab9043f2-Screenshot_2025-09-26_at_9.58.59_AM.png" className="border" />

***

## Gifting option

Toggle **Add gift option** on to include an “Is this a gift?” prompt below the subscription choices. This adds a radio button customers can select to flag their order as a gift.

<Image align="center" border={true} width="80% " src="https://files.readme.io/7e2e3843cf56a7eebe97a26db391251913ef36382bc53e91ccbce1d7d2fe15d8-Screenshot_2025-09-26_at_10.03.26_AM.png" className="border" />

***

## Product swaps and add-ons

For each product in your plan, you can configure:

* **Swap**

  * Allow subscribers to swap this SKU for any other plan product at renewal.
* **One-time Add-on**

  * Let subscribers select this (or other store) SKU as an optional extra on a single delivery. Great for accessories like tote bags or water bottles.
* **Subscription Add-On**

  * Automatically include this SKU on every renewal—for staples your subscribers always need.

<Image align="center" border={true} width="80% " src="https://files.readme.io/523b7050db9899125e33be8aa2f8e576cbd3778af6fff08bd045a091b5c4f04b-Screenshot_2025-09-26_at_10.07.24_AM.png" className="border" />

> **Note:** By default, only the products you selected for this subscription are available to swap or add-on—but you can extend add-on availability to any store product.

***

## Special discounts

In addition to recurring frequency discounts, you can grant one-time promotions based on order count or quantity:

* **By Order**

  * Apply a special discount to the first N deliveries, e.g., 50% off the first 3 orders to win initial sign-ups or 100% off the first order to offer a free trial.
* **By Quantity**

  * Discount based on the total quantity of products (e.g., 10% off when ordering 2 products, 15% off when ordering 3 products) to encourage larger carts.
  * Click **+ Add Discount Tier** to add additional discount tiers by quantity.

<Image align="center" border={true} width="80% " src="https://files.readme.io/c5167b3a17daedc94062642d3eab75436ef7a3f1647b8733cf9a7ba049545dc6-Screenshot_2025-09-26_at_10.12.04_AM.png" className="border" />

> **Note:** Discounts don’t stack. Special discounts override the recurring frequency discount until they expire—for example, a “first 3 orders 50% off” runs first, then the “10% off every 1 month” takes over.

***

## Free shipping

Define your subscription shipping rules:

* Toggle **Free shipping** to define the Countries where free shipping applies.
* Select **All countries available** or **Selected countries available** to select where free shipping applies.

<Image align="center" border={true} width="80% " src="https://files.readme.io/338bb146030c9ecf54b839764e33fd7f9567b53f636e50cb201ed274c3d192b6-Screenshot_2025-09-26_at_12.58.06_PM.png" className="border" />

> **Note:** If your Shopify store’s existing shipping profile already handles subscriptions, skip this section to avoid conflicting rules.

***

## Contract Type

The Contract Type determines if the subscription plan requires a term commitment and allows for charging a cancellation fee.

* **Flexible (default)**
  * No term commitment, the customer can cancel anytime free of charge
* **Committed**

  * Add a term commitment and cancellation fees

  <br />

  <Image align="center" border={true} width="80% " src="https://files.readme.io/c62e8f65cbf229838ab885856829e7aec46a2ffc8901c376324a8f0b07013e17-Contract_Terms.png" className="border" />

> **Note:** A Committed Contract Term is not available on Prepaid or Membership Subscription Plans.

To set a term commitment, define the Term Commitment Length. This is the total number of deliveries your customer agrees to as a part of the Plan.  The delivery length must be at least 1 delivery.

To enable an early cancellation fee:

* Select the corresponding checkbox.
* Choose the Fee Product you have configured in Shopify.
* Choose whether to **Prorate** the cancellation fee. If prorated, the fee is based on the remaining term. For example, if 40% of the term is left, the customer pays 40% of the maximum cancellation fee.

### Creating the fee product in Shopify

The Cancellation Fee must be set up as a standard Shopify product. Follow these steps in your Shopify admin:

1. Go to Products > Add Product.
2. Set a clear Title for the product (e.g., "Cancellation Fee").
3. Under Price, ensure the product is **not taxable**.
4. Under Inventory, either disable tracking inventory or ensure you have adequate stock to charge the fee.
5. Under Publishing, set the "Online Store" sales channel to **Unpublished**.
6. Set the product Status to **Active**.

<Image align="center" border={true} width="80% " src="https://files.readme.io/3b559ae9f4dc354acb55cd8c006a7fe3fde56ceda87da1cff7524d20f33552d4-Cancellation_Fee.png" className="border" />

> **Note:** Only one cancellation product can be selected per subscription plan.

***

## Cancellation flow

Finally, set up your desired Cancellation Flow.  With tailored cancellation flows, you can configure flows that:

* Prevent cancellations with timely incentives or suggesting alternative products
* Gather critical customer feedback with custom, on-brand surveys and
* Personalize the subscriber experience with relevant messaging and upsells

Click **None** in the Cancellation Flow drop down to select from your list of Cancellation Flows.

To learn more about creating a Cancellation Flow, check out the [Cancellation and churn prevention flows overview.](https://docs.recurly.com/recurly-commerce/docs/cancellation-and-churn-prevention-flows#/intelligent-cancellation-flows)

<Image align="center" border={true} width="80% " src="https://files.readme.io/6f7593c5bf4cd59ec2b02af2e0fec8dd8dcfc1be683125938c7e799242ebae8d-Screenshot_2025-09-26_at_1.09.39_PM.png" className="border" />

<br />

***

## Publish offer

When you’re satisfied with your selections, click **Publish Offer** in the top-right corner. Your subscription plan is now live on the product pages you configured.

***

Still need help? Contact [support@recurly.com](mailto:support@recurly.com).
