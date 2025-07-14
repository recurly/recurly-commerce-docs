---
title: Intelligent retries
excerpt: >-
  Intelligently recover failed payments with AI-driven retry logic tailored for
  Shopify merchants.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Recurly Commerce: Intelligent retries

Intelligent Retries is an automated retry engine that blends Shopify’s detailed gateway decline codes and payment metadata with Recurly’s proprietary AI/ML models, honed over years across 2,000+ merchants, to determine the optimal timing and frequency for successful payment recovery.

# Key benefits

* **Higher recovery rates**: Maximize involuntary churn reduction by retrying at the precise moments most likely to succeed.
* **Data-driven timing**: Leverage an AI/ML engine trained on extensive historical patterns—both Shopify-specific and cross-merchant—to pick the best retry schedule, independent of traditional dunning settings.
* **Transparent reporting**: Every retry is recorded in your subscription’s activity log and exportable via the **Subscription Contract Activity** report for full visibility.

# Key details

## How intelligent retries works

Recurly collects Shopify’s payment failure codes and available payment metadata, and combines that with patterns learned from thousands of merchants. Our AI/ML engine analyzes each failure reason and customer context to select the ideal retry window, whether hours, days, or weeks later, maximizing the likelihood of success.

## AI/ML engine

Built on years of data from 2,000+ merchants, these models continuously learn which timing, cadence, and conditions convert declined attempts into successful payments, resulting in fewer manual interventions and more recovered revenue.

## Retry decision logic

Unlike static schedules, Intelligent Retries dynamically adapts to each failure type. It assesses factors such as gateway error category, customer behavior, and historical outcomes—all while preserving your original renewal date.

## Enabling intelligent retries

For new merchants to Recurly Commerce, Intelligent Retries is already active. For existing merchants that may have another Payment Failure Experience selected, navigate to **Settings** -> **Payment Failure Experience**. From there, use the dropdown (shown below) to select **Intelligent Retries**.

<Image align="center" className="border" border={true} width="50% " src="https://files.readme.io/6a3e8f9edb4e88cb1c221d92d774ca8b71be10131c5fa20cb5aaeacc57fbbc80-image.png" />

## Activity logging & reporting

* **Subscription Activity Log**: Each retry attempt appears as an entry, showing timestamp, outcome, and the next scheduled retry.
* **Exportable Data**: Use the **Subscription Contract Activity** report in Settings to analyze retry patterns and outcomes at scale.

## Cancellation if payment issue remains unresolved

If no retry succeeds after the AI-determined maximum attempts, the subscription is automatically canceled—closing the loop on recovery and preventing endless billing attempts.

# FAQs

**Q: How many times will Intelligent Retries try?**\
A: The engine determines the optimal number of retries per failure type—typically between 3 and 7—based on historical success rates.

**Q: Where can I see retry history?**\
A: Every retry is recorded in the subscription’s activity log. You can also export **Subscription Contract Activity** to review timestamps and outcomes.

**Q: Will retries affect my renewal schedule?**\
A: No—successful retries simply process the payment and renew the subscription as originally scheduled.

**Q: Can I disable Intelligent Retries for certain plans or customers?**\
A: No—Intelligent Retries is enabled at the account level. If you’d like to discuss exceptions, please contact your Recurly account manager.

Still need help? Contact <a href="mailto:support@recurly.com" target="_blank">[support@recurly.com](mailto:support@recurly.com)</a>.