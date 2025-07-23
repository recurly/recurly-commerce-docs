---
title: Email and SMS integrations
excerpt: >-
  Easily connect your favorite email and SMS platforms to automate subscriber
  communications directly from Recurly Commerce.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

Seamlessly integrate Klaviyo, Postscript, or Attentive with Recurly Commerce to power your email and SMS messaging workflows—no developer required.

export const PrerequisitesLimitations = ({ header }) => {
  return (
    <div className="flex justify-start">
      <div className="rounded-md p-6 m-4 max-w-lg shadow-md border border-gray-300 dark:bg-gray-800 dark:border-gray-600">
        <p className="text-lg font-bold">{header}</p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          A valid account with the tool you wish to connect (Klaviyo, Postscript, or Attentive).
        </p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          Admin access to the Recurly Commerce app.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

Email & SMS integrations let you forward Recurly Commerce subscription events and subscriber data into third-party platforms. Once connected, you can build tailored automations, segments, and campaigns based on real-time subscription lifecycle events.

# Key benefits

* **Unified subscriber data**: Sync Recurly Commerce events and tags into your messaging platform for accurate segmentation.
* **Timely automations**: Trigger emails or SMS when subscriptions start, renew, fail, or cancel.
* **No-code setup**: Connect in minutes via the Integrations tab—no engineering overhead.

# Key details

To integrate one of the following tools with Recurly Commerce:

1. Open the **Integrations** tab in the Recurly Commerce app.
2. Click **Connect** on the card of your desired platform.
3. Follow the on-screen guide to authenticate and enable the integration.

<Cards columns={3}>
  <Card title="Klaviyo" icon="fa-envelope" target="_blank" href="https://docs.recurly.com/docs/klaviyo-integration#/">
    Build advanced email automations and segments using Recurly Commerce subscription events in Klaviyo.
  </Card>

  <Card title="Postscript" icon="fa-comment-dots" target="_blank" href="https://docs.recurly.com/docs/postcript-integration#/">
    Trigger SMS flows for subscription starts, cancellations, billing retries, and more in Postscript.
  </Card>

  <Card title="Attentive" icon="fa-bell" target="_blank" href="https://docs.attentive.com/pages/authentication/">
    Integrate Attentive to send personalized SMS messages based on real-time subscription lifecycle events.
  </Card>
</Cards>

Still need help? Contact <a href="mailto:support@recurly.com" target="_blank">[support@recurly.com](mailto:support@recurly.com)</a>