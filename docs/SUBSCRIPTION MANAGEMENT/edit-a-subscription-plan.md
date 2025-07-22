---
title: Edit a subscription plan
excerpt: >-
  Comprehensive guide to updating every aspect of an existing subscription plan
  in Recurly Commerce, including products, purchase modes, discounts, add-ons,
  gifting, shipping, and plan archiving.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

### Video

<Embed typeOfEmbed="iframe" url="https://www.loom.com/embed/898c9b96d39a42f9921285096bd21e97" href="https://www.loom.com/embed/898c9b96d39a42f9921285096bd21e97" html="false" iframe="true" />

export const PrerequisitesLimitations = ({ header }) => {
  return (
    <div className="flex justify-start">
      <div className="rounded-md p-6 m-4 max-w-lg shadow-md border border-gray-300 dark:bg-gray-800 dark:border-gray-600">
        <p className="text-lg font-bold">{header}</p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          You must have at least one live subscription plan to edit.
        </p>
        <p>
          <i className="fa-solid fa-exclamation-triangle mr-4" />
          Only products not already tied to another subscription offer will appear when selecting SKUs.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

Editing a subscription plan allows you to modify all live offer settings—products, purchase modes, billing cadences, discounts, gifting, add-ons, and shipping—without affecting current subscriber contracts. Changes apply prospectively, ensuring seamless continuity for your customers.

# Key benefits

* **Real-time control**: Instantly update products, pricing, and perks to respond to inventory changes or promotions.
* **Subscriber continuity**: All edits take effect on future renewals—active subscribers remain uninterrupted.
* **Holistic management**: Centralize every aspect of your subscription offer in one intuitive interface.

# Key details

## Accessing the edit screen

1. Navigate to **Subscription Plans** in the left sidebar.
2. Locate the plan you wish to update.
3. Click the **⋮** menu on its card and select **Edit**.

***

## Add or Remove Products

1. Scroll to the **Details** section and click the purple **Edit** button.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/2aebb5a4416113d9634c50df72b0231638da434fdaae8a66719f543a0fabdd14-image.png" />

2. (Optional) **Update** the internal **Name** and **Description** for clarity—these labels are for your team only.
3. **Click** **+ Select Products** to open your full Shopify SKU catalog.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/a5867979940d8892500e62e229934834e0b7c290c1eead0f43827826b4ceb6a2-image.png" />

4. **Check** boxes next to SKUs to add, or uncheck to remove.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/6c4491e678495f72c1b3ae9c8f82ce6bcbbf430091786b90b251ce95a2dcc80b-image.png" />

5. **Click** **Confirm**, then be sure to **hit** **Save Changes** at the top to apply your updates.

> **Note:** Only products without an existing subscription offer are listed.

***

## Edit purchase options and discounts

1. In the **Options** section, **click** **Edit**.
2. **View** each purchase mode (e.g., One-time & Subscribe & Save, Subscription Only, Pre-Paid). You’ll see delivery cadence and current subscriber counts.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/d9c7021a51a7421419a119720ce3c3b682b7c5075014f1294b1906ba137d375c-image.png" />

3. **Reorder** options by dragging to control display priority on your widget.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/ef9a70b573f8e7e674bbca8ee6dcf0aa7960d66a69298bf5125bf2a482971ef3-image.png" />

4. **Archive** any unwanted purchase modes to remove them from new signups.
5. **Toggle** **Add Gift Option** on or off to prompt “Is this a gift?” during checkout.
6. **Click** **Save Changes** to lock in your revised purchase options.

***

## Edit Product Swaps & Add-ons

1. **Scroll** to **Product Swap and Add-Ons** and **click** **Edit**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/31a564c55d34c35983d4d499f623b0d9ebdebe5555c42f7a2382c1d963a3a705-image.png" />

2. By default, your selected subscription products are available for swaps and add-ons.
3. **Click** **+ Select Products** to include additional SKUs for:

   * **Swap** – let customers swap one SKU for another at renewal.
   * **One-Time Add-On** – enable single delivery extras (e.g., tote bags).
   * **Subscription Add-On** – include add-ons on every renewal cycle.
4. **Check** or **uncheck** each SKU’s boxes to configure.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/a1a783d40969367070c69067932ed4760e4bc347e4e80a14daf4cc1074c2326c-image.png" />

5. **Click** **Confirm**, then **Save Changes**.

***

## Edit special discounts

1. Find the **Special Discounts** section and click **Edit**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/de282c89a319da610117c38d275be200710b1e60e6309c534921c256b898f9b6-image.png" />

2. You’ll see existing discounts by:

* **By Order** – a percentage off the first N orders.
* **By Quantity** – a discount based on item quantity per order.

3. **Adjust** the values, or select **None** to disable special discounts.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/8ea50ec213b7433b2f9296c941c12a7ec45a4511ea4f1b9810c3cfe7e90ad62e-image.png" />

4. **Click** **Save Changes**.

> **Note:** Special discounts override any frequency-based discounts until they expire.

***

## Edit free shipping

1. **Scroll** to the **Free Shipping** section and click **Edit**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/15fa5ce353fa164e093a993c7fe5b69fc02a40687b017594d1d225cecea9cf68-image.png" />

2. **Toggle** free shipping **On** or **Off**.
3. **Configure**:

   * **Countries** where free shipping applies.
   * **Minimum spend** or **minimum quantity** thresholds.
   * **Apply** to **first order only** or **every renewal**.

   <br />

   <Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/8774a6685ed75503009dee71fbefb3b792eb0e77911c27f7b64db6bdf84f6fb3-image.png" />

   <br />
4. **Click** **Save Changes**.

> **Note:** If your Shopify shipping profiles already cover subscription orders, omit this step to avoid conflicts.

***

## Archive a subscription plan

1. On the plan’s card, **click** the **⋮** menu and **select** **Archive**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/46cfe3a7838cd46b80088dba779656d9d50b6cf14cd8d7d4e9f378ea27e96a77-image.png" />

2. **Confirm** to deactivate the offer—archived plans move into the **Archived** tab.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/147616f8854cf369b9012fce86022cef169345becf2f369ba97a4d601ee613ba-image.png" />

> **Warning:** Archiving does **not** cancel active subscriptions; those contracts continue to renew. Archived plans cannot be reactivated.

***

Still need help? Contact [support@recurly.com](mailto:support@recurly.com).