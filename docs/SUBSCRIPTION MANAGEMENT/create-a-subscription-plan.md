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

<br />

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

   * **Name**: an internal label for your team.
   * **Description**: internal notes—your customers never see these.
3. Click **+ Select Products**. Your entire Shopify SKU catalog loads in a modal.

   * Check the box next to each product you wish to include in this plan.
   * Uncheck to remove. These selections determine which product detail pages (PDPs) display the subscription widget.
4. Click **Confirm** at the bottom to save your product selection.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/6cbcdd748375a8be4bbcfc74b7e6a5cb1d569b9cf0d657872159ee86a87394c4-image.png" />

> **Note:** Only products that do not currently have a subscription offer are available for selection.

***

## Choosing purchasing options

Once your products are chosen, select how they’ll be offered to customers:

* **One-time & Subscribe & Save**

  * Customers can either purchase once or subscribe on a recurring schedule.
* **Subscription Only**

  * The product is available exclusively as a subscription.
* **Pre-Paid Subscription Only**

  * Customers pay upfront for the entire subscription term (e.g., full year) and receive deliveries at each interval.
* **One-time, Subscribe & Save, and Prepaid Subscription**

  * All three options appear in the widget, letting customers choose among one-time purchase, recurring billing, or prepaid plans.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/0c3562de13c54df346e4311943672b0b1c76378536ece3c7373ad4b34ce13004-image.png" />

***

## Add subscription options & discounts

1. Use the **Offer Discounts** toggle to enable or disable promotional pricing.
2. Click **+ Add Option** to define each delivery frequency (e.g., every 4 weeks, every 8 weeks).
3. For each frequency, enter the discount percentage you wish to apply (e.g., 10% off every 4 weeks).

> **Note:** Offering larger discounts for more frequent deliveries incentivizes subscriptions and boosts customer retention.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/53b6b70e3476393b720119f426d940765154f9b28a181907d4019b06a0c0ccba-image.png" />

***

## Gifting option

Toggle **Add Gift Option** on to include an “Is this a gift?” prompt below the subscription choices. This adds a radio button customers can select to flag their order as a gift.

***

## Product swaps and add-ons

For each product in your plan, you can configure:

* **Swap**

  * Allow subscribers to swap this SKU for any other plan product at renewal.
* **One-Time Add-On**

  * Let subscribers select this (or other store) SKU as an optional extra on a single delivery. Great for accessories like tote bags or water bottles.
* **Subscription Add-On**

  * Automatically include this SKU on every renewal—for staples your subscribers always need.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/a7fa49c9a5894858ec0592e4ec126ba845f1bc15f1b49870b55fbede076018ae-image.png" />

> **Note:** By default, only the products you selected for this subscription are available to swap or add-on—but you can extend add-on availability to any store product.

***

## Special discounts

In addition to recurring frequency discounts, you can grant one-time promotions based on order count or quantity:

* **By Order**

  * Apply a special discount to the first N deliveries (e.g., 50% off the first 3 orders) to win initial sign-ups.
* **By Quantity**

  * Discount based on the total quantity of product (e.g., 20% off when ordering 3+ units per delivery) to encourage larger baskets.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/de4d7decca07c55fc2b9f8af6b694fe539d1eb3864576f484fb1010511cccb0e-image.png" />

> **Note:** Discounts don’t stack. Special discounts override the recurring frequency discount until they expire—for example, a “first 3 orders 50% off” runs first, then the “10% off every 4 weeks” takes over.

***

## Free shipping

Define your subscription shipping rules:

* **Countries** where free shipping applies.
* **Minimum spend** or **minimum quantity** threshold.
* **First-order only** vs. **every renewal** toggle.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/97262007e0b799bfa8569cbeb2ecd05bfd50cbb3d17d0b825328afd9c9df40b5-image.png" />

> **Note:** If your Shopify store’s existing shipping profile already handles subscriptions, skip this section to avoid conflicting rules.

***

## Publish offer

When you’re satisfied with your selections, click **Publish Offer** in the top-right corner. Your subscription plan is now live on the product pages you configured.

***

Still need help? Contact [support@recurly.com](mailto:support@recurly.com).