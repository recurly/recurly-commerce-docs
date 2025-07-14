---
title: Postcript Integration
excerpt: >-
  Enable Postscript to use Recurly Commerce subscriber events and tags for
  powerful SMS automations—no code required.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

### Prerequisites & limitations

* A Postscript account with Admin access.
* Recurly Commerce merchant admin access to configure the integration.
* No limitations on subscriber volume; tags and triggers fire in real time.

# Definition

The Postscript integration writes Recurly Commerce-specific subscriber tags and fires custom triggers into Postscript. Use these to build segments and automations that reach your subscribers at key moments—starts, cancellations, failed payments, and upcoming orders.

# Key benefits

* **Automated segmentation**: Tag subscribers as “active” or “inactive” in Postscript without manual work.
* **Event-driven automations**: Trigger SMS flows on subscription starts, cancellations, billing failures, or upcoming renewals.
* **Seamless setup**: Configure in minutes via API key—no developer resources needed.

# Key details

## Integrating Postscript into Recurly Commerce

### **Create a Postscript API Key**

1. In your [Postscript dashboard](https://app.postscript.io/dashboard), select your **Shop Name** → **API**.
2. Click **Create Security Key Pair**, then confirm with **Yes**.
3. Under **Private Key**, click **Show** and copy your new API key.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/af2c4db2c6e2196e750e668de94e98b90511b90fac76d573b985c384c0180f42-CreateAPIKey.gif" />

4. **Paste the API Key**:  In Recurly Commerce → Settings → Integrations → Postscript, enter the API key and save.

## After integration

### Available Recurly Commerce filters

Use these Subscriber Tags in Postscript to segment your audience:

| Tag name                                    | Description                                                                           |
| ------------------------------------------- | ------------------------------------------------------------------------------------- |
| SUBSCRIBER\_IS\_PRIVE\_ACTIVE\_SUBSCRIBER   | Applied if the customer has ≥ 1 active Recurly Commerce subscription.                 |
| SUBSCRIBER\_IS\_PRIVE\_INACTIVE\_SUBSCRIBER | Applied if the customer has no active subscriptions but was a subscriber in the past. |

> **Use Case:** Build a Segment of inactive subscribers for win-back SMS campaigns.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/0ecd26943a880d2f938f052c33079d2393ba4fd7a5a0649c39fee18db90406d7-image.png" />

### Available Recurly Commerce triggers

Fire these Postscript triggers in real time to power automations:

| Trigger Name                  | Description                                                                                   |
| ----------------------------- | --------------------------------------------------------------------------------------------- |
| Recurly Commerce: Subscription Started   | Fires when a subscription is created/purchased by the shopper.                                |
| Recurly Commerce: Subscription Canceled  | Fires when a subscription is canceled in the merchant admin or by the customer in the portal. |
| Recurly Commerce: Billing Attempt Failed | Fires when a billing attempt fails for a renewal order.                                       |
| Recurly Commerce: Upcoming Order         | Fires **3 days** before the next scheduled renewal order.                                     |

> **Use Case:** Send an SMS reminder for upcoming orders or recovery texts for failed payments.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/33394d0cb8a149a0ac9fa349d763e8610bf79cf1866a19cb7e85d5724dca6c11-image.png" />