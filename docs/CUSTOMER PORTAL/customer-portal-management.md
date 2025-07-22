---
title: Customer portal management
excerpt: Configure subscriber permissions and styling in the Customer Portal.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

The Customer Portal is where your subscribers manage and view their subscription contracts. From here, merchants can control which self-service actions are available and customize the look and feel of the portal.

export const PrerequisitesLimitations = ({ header }) => {
  return (
    <div className="flex justify-start">
      <div className="rounded-md p-6 m-4 max-w-lg shadow-md border border-gray-300 dark:bg-gray-800 dark:border-gray-600">
        <p className="text-lg font-bold">{header}</p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          You must have the Customer Portal feature enabled in your Recurly Commerce plan.
        </p>
        <p>
          <i className="fa-solid fa-exclamation-triangle mr-4" />
          Permissions toggles apply immediately—double-check your settings before saving.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

Customer Portal Management lets you turn merchant-approved self-service actions on or off for your subscribers (skip, swap, pause, etc.) and tailor the portal’s branding, copy, and layout to match your store.

# Key benefits

* **Empower your subscribers**: Let customers skip, pause, swap, and more—reducing support tickets and churn.
* **Maintain brand consistency**: Match portal colors, borders, and text to your storefront for a seamless experience.
* **Control subscriber experience**: Enable or disable exactly the actions you want customers to take—no surprises.

# Key details

## Customer Portal Permissions

Navigate to **Customer Portal** in the Recurly Commerce app to toggle subscriber actions:

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/94504e4d299d29c56018307a441a38174bb6d9f175aa55c48f8d7e35a2eb323f-image.png" />

1. **Shoppers can skip**\
   Allow customers to skip their next delivery without canceling their subscription—perfect for vacations or paused usage.
2. **Shoppers can change renewal date**\
   Let customers move their next charge/delivery date up to their upcoming shipment.
3. **Shoppers can change quantity**\
   Enable quantity adjustments—special discounts recalc automatically.
4. **Shoppers can change cadence**\
   Allow delivery frequency changes within the plan’s available options, so customers adapt to their lifestyle.
5. **Shoppers can swap products**\
   Give subscribers the ability to swap SKUs within the same subscription plan, driving experimentation without churn.
6. **Shoppers can pause / un-pause**\
   Offer indefinite or limited-cycle pause functionality, configured by you, to retain customers during gaps in need.
7. **Shoppers can gift next delivery**\
   Turn on gifting so subscribers can send an upcoming order to a friend instead of themselves.

## Stylize the Customer Portal

Under the same **Customer Portal** tab, select a template and adjust:

* **Colors & borders**: Align portal UI with your branding.
* **Copy edits**: Update button text or instructions—reach out to your CSM for deep copy changes.
* **Live preview**: Click **Save and set live** to instantly apply updates.

<Image align="center" className="border" border={true} width="60% " src="https://files.readme.io/160fc76046efb56414d40de7b45c7461725971b7b1a62736236af0c5a0eda399-image.png" />

Still need help or have questions about further customizations? Contact <a href="mailto:support@recurly.com" target="_blank">[support@recurly.com](mailto:support@recurly.com)</a>.