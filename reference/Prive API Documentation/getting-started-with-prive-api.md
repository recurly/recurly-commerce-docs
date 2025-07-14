---
title: Getting Started with Prive API
excerpt: Streamline you subscription workflows
deprecated: false
hidden: false
metadata:
  title: Getting Started with Prive API
  description: ''
  robots: noindex
next:
  description: ''
---
Welcome to our comprehensive guide to getting started with Prive APIs. We provide a suite of robust APIs that will empower you to seamlessly manage your subscriptions, subscribers, and orders with Prive.

## Authentication

All our API endpoints require the use of private API keys to authenticate requests. This is a security measure that ensures only authorized users have access to the API functionalities, thereby keeping your data secure.

To get your unique API key, please contact our support team. You can reach out to us via email at [cs@tryprive.com](mailto:cs@tryprive.com) or through the support section of your account dashboard. Once you receive your API key, ensure that you store it securely and never expose it in public spaces, as it gives full access to your data.

Remember, each API request you make must include your API key in the headers as follows:

```javascript
const headers = {
  "Content-Type": "application/json",
  "Authorization": `Bearer ${API_KEY}`
};
```

## Rate limiting

In order to maintain optimal performance and security of our services, Prive API endpoints are subject to rate limiting. 

Prive API rate limit policy is scoped to each API key generated for a merchant. 

Prive API uses a leaky bucket algorithm for the rate limit policy.

The rate limit bucket size is 50 with a leak rate of 2 per second. 

With this policy:

* If you burst requests, the total requests you can make per burst will be 50 and every second after this you restore 2 points to the bucket.
* You can consistently make 2 requests per second and it will be regenerated each second.
* If the bucket limit is exceeded the API will return a 429 error code will be returned.

## Pagination

To make data retrieval more manageable, our APIs support pagination in responses. You can control pagination through the page and limit query parameters in your API requests.

```
GET /subscriptions?page=2&limit=5
```

## Webhook Verification

Prive webhooks use standard hmac verification. Prive will provide merchant a secret token. Prive uses the secret token to generate the hmac and is passed in the 'x-prive-hmac-sha256'  header. The webhook receiving service will run a verification check by obtaining the raw request body (if you are using node, you can use something like 'body-parser' npm package), 'x-prive-hmac-sha256' header, webhook merchant secret token.

```typescript type
// function to verify webhook payload
const verifyWebhook = (body: any, hmac: string, webhookVerificationSecret: string): boolean => {
  const genHmac = crypto.createHmac('sha256', webhookVerificationSecret).update(body, 'utf8', 'hex').digest('base64');
  return genHmac === hmac;
};

// should put in middleware function and run before endpoint business logic
const hmac = req.headers['x-prive-hmac-sha256'];
if (!hmac) throw new UnauthorizedException();

verifyWebhook(req.rawBody, req.headers['x-prive-hmac-sha256'], '<webhookVerificationSecret>')
```
