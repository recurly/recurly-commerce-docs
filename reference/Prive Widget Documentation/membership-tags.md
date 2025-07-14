---
title: Membership Tags in Shopify Liquid
excerpt: >-
  Prive allows merchants to configure subscriptions specific to membership
  experience. Merchants can rely on these Shopify customer tags to surface up
  different web content in their Shopify Liquid template files.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
| Tag                                                  | Description                                                                                             |
| ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| Member\_status: enum \{active,inactive,failed}       | Membership status of customer.                                                                          |
| Membership\_type: string\[]                          | Configured in the subscription offer. A list of membership types that is configured by the merchant.    |
| Membership\_trial\_conversion: boolean               | Membership is converted from trial.                                                                     |
| Membership\_duration: enum\{monthly,annual,lifetime} | Configured in the subscription offer. This is the duration of the membership before it is set to renew. |
| Member\_last\_cancelled\_date: string                | Date the member last cancelled.                                                                         |
