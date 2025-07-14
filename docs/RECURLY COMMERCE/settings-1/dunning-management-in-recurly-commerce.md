---
title: Dunning management in Recurly Commerce
excerpt: >-
  Configure your retry schedules, notifications, and recovery actions to turn
  payment failures into successful renewals.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

Dunning is an automated payment management process that allows you to set up retries for failed payment methods on a specific schedule and send reminders about outstanding dues after a declined payment.

# Key benefits

* **Maximize collections**: Customize retry intervals and counts to capture more successful payments.
* **Proactive communication**: Automatically notify customers of failures and guide them to update billing.
* **Flexible outcomes**: Choose to pause or cancel subscriptions when retries exhaust to match your business policy.

# Key details

## What is dunning?

Dunning is the retry-and-remind workflow for failed subscription payments. When a payment method declines, Recurly Commerce can retry the charge on your chosen schedule and send alerts to subscribers about the outstanding balance.

## Dunning configuration

In the **Settings > Dunning** section of the Recurly Commerce app, choose one of three built-in dunning strategies:

**Recurly Commerce's standard dunning setting**: Subscription contracts automatically cancel if all retries fail. By default, the system retries every 2 days up to 5 times.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/3bf5832600003bd3b17e282c64e971bfa1f39b855cec40f27f8e237e8810ca0a-image.png" />

**Retry after failed billing**: Specify how many days—and how many retry attempts—to schedule **after** the renewal date, and decide whether to pause or cancel once retries complete.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/af06f66ba65c9cbc0dcfd02450a5fa2edc05b99c51cdbda69a470a8f756f9046-image.png" />

**Retry before failed billing**: Define retry attempts **before** the renewal date, plus pause-or-cancel behavior post-retries.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/e42f13d781adc8e6abba25442334c698dc1c6ad63279f0b9700b9b85ab657d78-image.png" />

## Payment failure notification

Enable the **Failed payment method** email in **Notifications** to alert customers immediately when a charge fails. The message includes a link to their portal to update payment details.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/6b7f0ec80fa3dbde857f2708efc35c769674f6c576da4ea56bc51d44a037fc56-image.png" />

## Reset billing information

Merchants can’t edit payment details directly, but you can prompt a reset email:

1. Go to **Customers**, select a subscriber, and scroll to **Billing & Shipping**.
2. Click **Send email to reset** to trigger a Shopify-hosted billing update flow.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/b320e86d113266aa9acb2cfb4a106ac6ceb882de0f94865aa9b716080bd45f21-image.png" />

## Process failed payment

After a subscriber updates their payment method, click **Process Now** on their contract to immediately re-charge and, on success, resume the next renewal without altering the schedule.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/fe4a69f7fba47c5ab1fdff5e35f3a3093106bb827a4b5dc0fc014303222eb956-image.png" />