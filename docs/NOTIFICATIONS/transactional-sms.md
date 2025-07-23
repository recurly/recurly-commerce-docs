---
title: Transactional SMS
excerpt: >-
  Keep subscribers in the loop on the go with concise, event-driven SMS
  alerts—no extra cost, no spam.
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
          You must have a valid mobile number on file for each subscriber.
        </p>
        <p>
          <i className="fa-solid fa-exclamation-triangle mr-4" />
          If a subscriber opts out of SMS, they cannot opt back in unless you update their phone number on the subscription contract.
        </p>
        <p>
          <i className="fa-solid fa-exclamation-triangle mr-4" />
          Limit to three active SMS notifications per subscriber to avoid over-messaging.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

Transactional SMS are short text messages sent automatically when key subscription events occur, such as order confirmations, payment failures, and upcoming renewals.

# Key benefits

* **Instant engagement:** Deliver real-time updates directly to your customers’ devices for higher open rates.
* **Lower support load:** Proactively notify subscribers of issues (like payment failures) before they reach out.
* **Seamless customization:** Edit message templates with our built-in editor—no coding required.

# Key details

## Enabling transactional SMS

We recommend toggling on no more than three notifications to cover the most critical touchpoints:

1. **Subscription created**: Confirms that a new subscription order has been created.
2. **Order placed**: Confirms that an order has been successfully placed.
3. **Failed payment method** *(highly recommended)*: Alerts customers when their payment could not be processed.
4. **Subscription cancelled**: Confirms that a subscription contract has been cancelled.
5. **Product out of stock** *(highly recommended)*: Notifies customers when one or more subscribed products are unavailable.
6. **Upcoming order** *(highly recommended)*: Sends a reminder 3 days before the next renewal.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/019f716569a5bcac3123db4601505d1a805544703d2953cd6392ac06d30809e3-image.png" />

## Customizing SMS content

Use our simple text editor to tailor each SMS template:

* Personalize greetings or add your brand name
* Adjust message copy to match your tone
* Preview before enabling to ensure clarity

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/b67ce5551bf6821f6f9c7f3ce8a6b55983f9426dc3c9f4bdb3e27f2cd61fbfd8-image.png" />