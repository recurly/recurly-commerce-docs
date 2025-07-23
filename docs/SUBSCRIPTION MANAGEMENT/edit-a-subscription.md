---
title: Edit a customer subscription
excerpt: >-
  Step-by-step instructions for merchants to modify any aspect of an active
  subscriber’s contract—from status and contact info to billing cadence,
  pricing, add-ons, shipping, and cancellation—while preserving continuity.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

The **Edit a Customer Subscription** screen in Recurly Commerce empowers you to manage every facet of an individual subscriber’s contract in real time: update their status, contact details, next-billing date, frequency, pricing, discounts, add-ons, shipping and more, or pause, skip, cancel, and even re-activate—all without code.

export const PrerequisitesLimitations = ({ header }) => {
  return (
    <div className="flex justify-start">
      <div className="rounded-md p-6 m-4 max-w-lg shadow-md border border-gray-300 dark:bg-gray-800 dark:border-gray-600">
        <p className="text-lg font-bold">{header}</p>
        <p>
          <i className="fa-solid fa-check mr-2" />
          The subscriber must already have an active contract.
        </p>
      </div>
    </div>
  );
};

<PrerequisitesLimitations header="Prerequisites & limitations" />

# Definition

Editing a subscription contract lets you tailor an individual customer’s upcoming renewals and deliveries—updating their billing schedule, quantities, product selections, pricing, discounts, shipping, and status—while existing subscribers continue uninterrupted.

# Key benefits

* **Immediate adjustments**: Apply changes on the spot for any single subscriber’s contract.
* **Subscriber retention**: Pause, skip, or modify schedules to keep customers engaged and satisfied.
* **Personalized service**: Offer one-off add-ons, custom discounts, and gifting directly on their contract.

# Key details

## Accessing a subscriber’s contract

1. **Go** to **Customers** → **Active** (or **Inactive**) tab.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/2465e345e7995b90ec60b3bea0fef15c2ca88a23c915655eef7adc34934d5667-image.png" />

2. **Find** the subscriber in the list and click anywhere on their row.
3. The contract detail page opens, showing name, email, phone and status badge.

**Statuses**:

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/e80e529203b09b3af6e8d56445a200a4773351f95fcdb6b8ffb7ffecb7f332ef-image.png" />

* **Active:** This means the contract is active with no issues found.
* **Inactive:** This means the contract is cancelled.
  * (**Click** the “Reactivate” button to reactivate a subscription contract)
* **Failed (in dunning):** This means the contract’s payment method is currently being re-tried through a process called dunning.
  * (Pause and unpause the contract to stop dunning and bring the contract back to an active state)

***

## Edit Phone Number

1. In the contract header, click the ✎ icon beside **Phone**.

<Image align="center" src="https://files.readme.io/43753f0a143cc6e1a870512991dfa6e3a98fd54bba777aad5cca057c7ea4e48b-image.png" />

2. Enter the new number and click **Save**.

***

## Edit email

Change a subscriber’s email address.

1. **Navigate** to **Subscribers**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/550f1d8edbe55ffb87782d9af99b95a223e6e46d14c4f6f3a172983959f32c9b-image.png" />

2. **Locate** and **select** the subscriber.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/dad537371948e469a21491c1d3ff8e817b20c4d87597d0fc9f0f70c31a44269c-image.png" />

3. **Click** **Change** beside the email field.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/b43754ffc82fde0ebc8207ba95c6820dd505435edb7e9119cdf3774ec8778b77-image.png" />

4. **Enter** the new email address and **click** **Update**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/a2b5ac87ba923e98c85913535c1a65328347d57fd27104fc02aa23d0735df584-image.png" />

5. The change is applied immediately.

***

## Set delivery / renewal date

Adjust when this subscriber’s payment method is charged—and all future renewals follow.

1. **Click** **Set Delivery**.

![](https://files.readme.io/61803eae4434fadd437f9dc14b0a618e728e2c477154f486f49c9ac17fa25049-image.png)

2. **Select** your new billing date.

<Image align="center" className="border" border={true} width="60% " src="https://files.readme.io/7259ddf8ee27f3bbaa4f49daffa6d0dd8d1f12f5eaf8fab59aef194dd341aa45-image.png" />

3. **Click** **Update** to apply.

***

## Process now

Charge the subscriber immediately—no waiting for the next scheduled date.

1. **Click** **Process Now** to trigger an on-demand payment.

![](https://files.readme.io/92b011924d257926ba60fb8cefac655dc9b58423708c1a1df11f4e710b411444-image.png)

***

## Edit frequency

Change how often this subscriber is billed going forward.

1. **Click** **Edit Frequency**.

![](https://files.readme.io/f0729cd660a0ff7c669868be2ba46717e3bcfaae933a0ca3d4843be81a060dbb-image.png)

2. **Choose** a new cadence from the list of your configured options.

<Image align="center" width="60% " src="https://files.readme.io/ec3a998f6e8a30bdf5522e4ed496394bf33e8a9e684ce2fb3aef5dbe0b58205d-image.png" />

3. **Click** **Update** to save—it applies to all upcoming renewals.

***

## Change price

Update the per-renewal cost for this subscriber’s contract—future renewals will charge the new amount without affecting any other subscribers.

1. **Click** **Change Price**.

![](https://files.readme.io/66dccf75868d9cfbdadeb6b6b0b2d8815344bbfb6bddd1a1e817bd7ef71104dd-image.png)

2. **Enter** the new subscription price for this contract only.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/fe50ad810dc5fbf937a342df8c10e821d6df2153ac97849401f1566abf5cd8fa-image.png" />

3. **Click** **Apply** to confirm the new price.

***

## Pause contract

Temporarily halt a subscriber’s renewals—either indefinitely or for a predefined number of deliveries.

1. **Click** **Pause**.

![](https://files.readme.io/ba39e69e836b3f2ec5cbd8111890d03b648ec99a34df3b52bb21a18729c8b914-image.png)

1. **Choose** between pausing indefinitely or specifying a number of upcoming deliveries (if your plan supports it).

***

## Skip next

Skip one or more upcoming orders without cancelling the subscription; the schedule will pick up after the skipped delivery.

1. **Click** **Skip Next**.

![](https://files.readme.io/00bfc039d87d36923442af5752dcee8753ee4e8047a2c44907ad6a08217b0c17-image.png)

2. **Select** the orders you want to skip.
3. **Click** **Confirm**—all future renewals resume once those orders have been skipped.

***

## Update quantity

Adjust the number of items your subscriber receives on each renewal.

1. **Click** **Update Quantity**.

![](https://files.readme.io/5738bf05f51b78bdaf844980df316ea58e44511abfd7c7198b3e5b81c586957b-image.png)

2. **Enter** the new quantity for all future deliveries.

<Image align="center" width="80% " src="https://files.readme.io/c32aa566d8bdffa6d126c8215782eb99100e3b08214349767312b9ed429aedfd-image.png" />

3. **Click** **Apply** to save the updated quantity.

***

## Apply coupon / discount code

Attach a Shopify coupon code directly to a subscriber’s contract to apply promotional pricing on all future renewals.

1. **Click** **Coupon Code**.

![](https://files.readme.io/b78fd515467a4eb3b15ec8f1dbf2f2f15ebe855f74996bd37c7e2feb05903309-image.png)

2. **Enter** a valid Shopify coupon code.

<Image align="center" width="80% " src="https://files.readme.io/3d27a32157260922d8e6b844fb81e6a7ddf0f86bf0096860c03b4c990a9be836-image.png" />

3. **Click** **Apply** to activate the discount for this subscription contract.

***

## Swap product

Replace the current subscription item with a different SKU you’ve pre-configured in your plan’s swap list.

1. **Click** **Swap Product**.

![](https://files.readme.io/6fe491aacae79f89409287b6d2a317c872fe801c04072de41b2a7c44e68775d6-image.png)

2. **Select** a replacement SKU from the enabled swap list.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/6f7585a8dd52437d4f1b2785960e99b7aa9178db28cd74584ad48016dc43cf7b-image.png" />

3. **Click** **Swap & Save** to update the contract.

***

## Add-on subscription product

Include an extra product on every delivery to boost order value and subscriber satisfaction.

1. **Click** **Add-on Subscription Product to all Deliveries**.

![](https://files.readme.io/1b83551dc32b5ad2c958886d115fec4b2aecb8ac741b6d6591e762815a333e36-image.png)

2. **Choose** the add-on SKU to include on each renewal.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/cf71f14540e667cd3dff6dfdd61e66be3996e0b8d7767e3152389d2172e5220c-image.png" />

3. **Save** your changes to lock in the add-on for all future deliveries.

***

## One-time add-on product

A subscription product will be added once to a specific renewal/delivery of choice.

1. **Click** **Select One-Time Add-On**.

![](https://files.readme.io/d51f0e48131a349e29a271bb85fade171d8d1750a38490accbe11dc154141d21-image.png)

2. **Select** the SKU and specify which upcoming renewal.

<Image align="center" className="border" border={true} width="70% " src="https://files.readme.io/ad267487bf391edaebfbd9b362b11fb01fd835b5c482844b1a154e0aa126ab1e-image.png" />

3. **Save** your changes.

***

## Cancel subscription

Cancelling the subscription will immediately stop all subsequent renewals/deliveries in the contract and push the contract status to an “inactive” state.

1. **Click** **Cancel Subscription**.

![](https://files.readme.io/73a94ff26c936edbedafbfe0f2717ec01338573825b8a738dd08d7f7e8cdd073-image.png)

2. Confirm in the pop-up to stop all future renewals and set status to **Inactive**.

![](https://files.readme.io/caf03f940a65a4e783885faca2128e981faa6277f0091bdd081e635842d38c92-image.png)

***

## Reactivate subscription

Bring a cancelled subscription contract back to life in three easy steps:

1. **Switch** to the **Inactive** tab in the **Customers** section and find the subscriber.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/1715fdc88b964559864e2b505c2a6d4d40c53c9713b00956f7ec2beb0fb7e57a-image.png" />

2. **Click** **Reactivate** next to their contract.

![](https://files.readme.io/03c16f07ee5172dca7d58b1c3f73e242db552806e874ac45ed053e40dd7c354b-image.png)

3. **Confirm** the action in the pop-up. Their status will immediately revert to **Active**, and they’ll reappear in the **Active** list.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/7b8abf13562797bb5f42b394aa9dc5f51ae31a7ebd978cf5501198bed150b7c5-image.png" />

***

## Update shipping information

Adjust the subscriber’s delivery address on file to ensure future orders ship to the correct location:

1. In the **Shipping Information** panel, **click** **Edit**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/9fa36508fb8f10f302d3463c0433deac908e9775c47453a074f29c80fe935e6c-image.png" />

2. **Modify** any of the fields—name, street address, city, state, postal code, or country—to the new values.

<Image align="center" className="border" border={true} width="60% " src="https://files.readme.io/909a1d2de214cb65fe019c05eaf1fdf2fe00a514d3f2b021d66e81a237326366-image.png" />

3. **Click** **Update** to save the new shipping information. All future renewals and deliveries will use this updated address.

***

## Update billing information

When a customer needs to change their payment method on file, trigger a secure reset through Shopify Payments:

> **Note**: For security and PCI compliance, merchants cannot directly edit a customer’s payment details. You must send a reset link.

1. In the **Billing & Shipping** section, **click** **Send reset email**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/506b3b70c9c5d3c2a525c0dad8d0d90c564f07acad96196823f0e60718a849b1-image.png" />

1. The subscriber receives an email with a link to update their payment details via the Shopify Payments gateway.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/043e181c421c08cf83218993a7621899e2862f85cc8600fd69d652191818b8ab-image.png" />

1. Once the customer completes the update in Shopify, Recurly Commerce automatically syncs the new billing information into the subscription contract.

<Image align="center" className="border" border={true} width="50% " src="https://www.gitbook.com/cdn-cgi/image/dpr=2,width=2400,onerror=redirect,format=auto/https%3A%2F%2Ffiles.gitbook.com%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F8fL56bv4OV5TqEAqXpvt%252Fuploads%252Fpx9UxrCPhCzsijb7Ue6W%252Fezgif.com-gif-maker.gif%3Falt%3Dmedia%26token%3D6273e900-9c2d-417d-8764-bc8e42eef1ee" />

> **Note**: This reset process ensures you never handle raw payment data directly, keeping both you and your customers secure.

***

## Create a new subscription contract

Use this flow to add a brand-new contract for a customer who already has at least one active subscription under their email:

1. **Navigate** to **Subscriptions** → **Create Contract** in the top right corner.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/7adcc1328f1ba211db4f01195e2fe1bbfb5237ba34ade9062b0c98e639c121ba-image.png" />

2. **Complete** the contract form—select the customer, plan, start date, and any options—then click **Create**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/e80a9096c8dadf1b949b438f03528d226654e26e18bb900bf7b7fa0797e723ef-image.png" />

> **Note**: Shopify merges all subscriptions by email. To issue a separate contract under the same store account, the customer must checkout with a different email address.

***

Still need help? Contact [support@recurly.com](mailto:support@recurly.com).