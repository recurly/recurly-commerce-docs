---
title: Installing and onboarding to Recurly Commerce
excerpt: >-
  Step-by-step guide to installing and onboarding Recurly Commerce in your
  Shopify store—covering app installation, plan selection, subscription
  creation, storefront setup, and communications configuration.
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
          A Shopify or Shopify Plus store is required.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

The Installing & Onboarding workflow guides you through adding the Recurly Commerce app to Shopify and configuring your first subscriptions, storefront, and notifications.

# Key benefits

* **Rapid launch**: Get subscriptions up and running in minutes.
* **Plan flexibility**: Choose or upgrade plans to match your business needs.
* **Native integration**: Manage everything directly within Shopify’s interface.

# Key detail

<Cards columns={3}>
  <Card title="Download App" icon="fa-download" target="_blank" href="https://apps.shopify.com/prive-subscriptions">
    Recurly Commerce is supported on Shopify and Shopify Plus.<br />
    Install it from the Shopify App Store.
  </Card>

  <Card title="Choose a Plan" icon="fa-list" target="_blank" href="https://www.tryprive.com/pricing">
    1. Open the Recurly Commerce app.
    2. Select one of two plans (upgrade anytime)
    3. Complete checkout via Shopify<br />
       [Compare plans](https://www.tryprive.com/pricing)
  </Card>

  <Card title="Create Subscription Plan" icon="fa-plus-circle" target="_blank" href="https://docs.recurly.com/recurly-commerce-docs/docs/create-a-subscription-plan#/">
    Define your subscription offers—these feed directly into your storefront widget.<br />
    [Create a subscription plan](https://docs.recurly.com/recurly-commerce-docs/docs/create-a-subscription-plan#/)
  </Card>

  <Card title="Set Up Storefront" icon="fa-store" target="_blank" href="https://docs.recurly.com/recurly-commerce-docs/docs/storefront-setup#/">
    Ensure the subscription purchase widget displays on your product pages.<br />
    [Storefront setup guide](https://docs.recurly.com/recurly-commerce-docs/storefront-setup#/)
  </Card>

  <Card title="Configure Comms" icon="fa-envelope" target="_blank" href="https://docs.recurly.com/recurly-commerce-docs/docs/transactional-emails">
    Free transactional email & SMS keep subscribers informed at every stage.<br />
    [Configure transactional emails](https://docs.recurly.com/recurly-commerce-docs/docs/transactional-emails)
  </Card>
</Cards>