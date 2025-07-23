---
title: Manage shipping profiles
excerpt: >-
  Learn how Recurly Commerce uses your Shopify shipping profiles to configure
  free shipping for subscriptions without duplicating rules.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

export const PrerequisitesLimitations = ({ header }) => {
  return (
    <div className="flex justify-start">
      <div className="rounded-md p-6 m-4 max-w-lg shadow-md border border-gray-300 dark:bg-gray-800 dark:border-gray-600">
        <p className="text-lg font-bold">{header}</p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          Requires Shopify shipping profiles to be properly configured under <strong>Settings → Shipping and delivery</strong>.
        </p>
        <p>
          <i className="fa-solid fa-exclamation-triangle mr-4" />
          If your Shopify profile already covers subscriptions, <strong>do not</strong> enable free shipping in Recurly Commerce to avoid rule conflicts.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

Managing shipping profiles means using Shopify’s built-in shipping settings to determine which countries, order values, or quantities qualify for free shipping on subscription orders.

# Key benefits

* **Zero duplication of work**: Use the same shipping profiles you’ve already set up in Shopify—no separate configuration in Recurly Commerce.
* **Granular control**: Specify countries, minimum purchase amounts, or quantity thresholds for free shipping on subscription renewals.
* **Flexible application**: Choose whether free shipping applies to every renewal or only the first N orders.

# Key details

## Viewing your Shopify shipping profiles

Recurly Commerce does not host shipping rules itself—it reads from Shopify. To view or edit your profiles:

1. In Shopify admin, go to **Settings** → **Shipping and delivery**.
2. Locate the profile you want to use for subscriptions.

> **Note:** If a Shopify profile already applies to subscription orders, skip the free-shipping setup in Recurly Commerce to prevent overlapping rules.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/bdcc67d6dac1fd0c6b01f25f9d00de643bb3383b0d962d8f0b2de02ba628ee66-image.png" />

## Configuring free shipping in Recurly Commerce

1. In the Recurly Commerce app, navigate to **Subscription Plans**, then select **Edit** on your plan and scroll to **Free Shipping**.
2. Toggle **Free Shipping** on.
3. Set your parameters:

   * **Countries**: Which regions qualify.
   * **Minimum order amount** or **quantity**: The spend or item count threshold.
   * **Applies to**: Choose **All renewals** or **First N orders only**.

> **Note**: Only enable if you need different shipping rules for subscriptions than your standard Shopify profile.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/9a720811174fb29a30065ed7626135490342edb6a4d992145c0683837f3911ab-image.png" />