---
title: Transactional emails
excerpt: >-
  Keep subscribers informed and engaged at every subscription milestone with
  fully customizable transactional emails—no extra cost, no coding required.
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
          <i className="fa-solid fa-exclamation-triangle mr-4" />
          Emails cannot be used for promotional content; they must remain informational.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

Transactional emails are automated, event-driven messages sent to subscribers to confirm subscription actions (orders, renewals, failures, etc.) and keep them up to date on their subscription status.

# Key benefits

* **Reduce support tickets**: Proactively inform customers of order statuses, failures, and upcoming renewals so they don’t have to reach out.
* **Improve retention**: Remind subscribers of upcoming orders and out-of-stock items before issues arise.
* **Full customization**: Edit subject lines, body copy, styling, and even insert HTML for a brand-consistent experience.

# Key details

## Enabling transactional email

We recommend toggling on at least four notifications to cover the critical touchpoints and minimize support overhead.

1. **Subscription created**: Confirms that a subscription order has been created.
2. **Order placed** _(highly recommended)_: Confirms that an order has successfully been placed.
3. **Failed payment method** _(highly recommended)_: Alerts customers when their payment couldn’t be processed.
4. **Subscription cancelled**: Confirms that a subscription contract has been cancelled.
5. **Product out of stock** _(highly recommended)_: Warns customers when one or more subscribed products are unavailable.
6. **Upcoming order** _(highly recommended)_: Notifies customers 3 days before their next renewal.
7. **Gift subscription created**: Confirms that a gift subscription order has been processed.

<Image align="center" border={true} width="80% " src="https://files.readme.io/f97fa96568ec6cd3537191572727535d81d08a6254041b8ad9885ba2e0c8040d-Notifications.png" className="border" />

## Customizing email content

Use our built-in rich text editor to tailor each template:

* Insert and resize images
* Adjust fonts, colors, and spacing
* Switch to HTML source view for advanced customizations

<Image align="center" border={true} width="80% " src="https://files.readme.io/48c4c5678a2979a9694bce42e285c19536f78e011bad51e266a9f34f925af420-Subsccription_created_email.png" className="border" />
