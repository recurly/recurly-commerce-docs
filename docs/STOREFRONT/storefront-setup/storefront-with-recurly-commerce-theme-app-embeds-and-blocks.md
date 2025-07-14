---
title: Storefront with Recurly Commerce theme app embeds and blocks
excerpt: >-
  Guide to adding, removing, and customizing the Recurly Commerce Subscriptions
  app embed and inline app blocks via the Shopify Theme Editor.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

Use Shopify’s Theme Editor to enable the mandatory Recurly Commerce Subscriptions embed block for core functionality—and optionally add inline app blocks for precise widget placement on OS 2.0 themes.

### Prerequisites & limitations

* **Embed block** is required on **all** themes.
* **Inline app blocks** are only available on Shopify Operating System 2.0 themes.
* Customization options for both embed and app blocks are coming soon.

# Definition

* **App Embed Block**: A global toggle in Theme Settings that injects Recurly Commerce’s subscription widget scripts across your storefront.
* **Inline App Block**: A draggable block you can place within a theme section (e.g. Product information) to control exactly where the widget appears on [OS 2.0 themes](https://help.shopify.com/en/manual/online-store/themes/managing-themes/upgrading-themes).

# Key benefits

* **Zero-code installation**: Enable or disable the embed with a single toggle—no theme file editing required.
* **Flexible placement**: For [OS 2.0 themes](https://help.shopify.com/en/manual/online-store/themes/managing-themes/upgrading-themes), use app blocks to position the widget anywhere within your product template.
* **Future-proof**: Blocks and embeds inherit your theme’s styles and support upcoming customization features.

# Key details

## Mandatory app embed block

Whether you’re on a vintage theme or a Shopify OS 2.0 theme, you must enable the embed block to power all Recurly Commerce storefront features.

### Adding the embed block

1. **Open** your Shopify Theme Editor (Online Store → Themes → Customize).
2. In the left sidebar, click **Theme Settings** → **App Embeds**.
3. Toggle **Recurly Commerce Subscriptions Widget** on.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/135c716f1242ad4b10f942180d079fa7d14a33499fec881e5af32223cf13b4bf-App_embeds.gif" />

4. Click **Save** (top right) to publish.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/28777881cbee1ab15331985762f0aac8db0833a62a00fbc76d8c957a0b2cea2b-image.png" />

### Removing the embed block

1. In **Theme Settings** → **App Embeds**, **toggle** **Recurly Commerce Subscriptions Widget** off.
2. **Click** **Save** to remove all storefront subscription components.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/71414dfec365a655df4b96a3a688dfe4d6621bb40c5a3160ed6cb2506b82d170-image.png" />

### Customizing the embed block

> We don’t currently offer custom styling options for the embed block—stay tuned for future updates!

## Optional inline app blocks

OS 2.0 themes support inline app blocks, giving you granular control over widget placement on your product pages.

### Adding an inline app block

1. **Open** the Theme Editor and navigate to a **Product page** with an active subscription offer.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/d9b0e14ed5c133080967b145d11c85edc84b5cd908de42657aab6679d720adaa-image.png" />

2. In the left sidebar, **expand** **Product Information**, then click **Add block**.
3. Under **APPS**, **select** **Recurly Commerce Subscriptions Widget**.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/3560be608ce4ca60e5315db2cdd1a5a60884572ef8b123a41124c0b196a0989b-image.png" />

4. **Drag** the block above your **Buy button** to set its position.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/604e06f8e775adb9e178f18b50781ebf0d86c816783929b0566e86354aefd918-image.png" />

5. **Click** **Save** (top right) to publish.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/ec6e334daeff0ac15e415aca2af53f893b4442be3b2ebd072d1e97f7cf96648a-image.png" />

### Removing an inline app block

1. In your product template, **select** the **Recurly Commerce Subscriptions Widget** block.
2. **Click** **Remove block** (bottom left).
3. **Click** **Save** to publish.

<Image align="center" className="border" border={true} width="80% " src="https://files.readme.io/32d52b6a7fa47f7fc50214ebeed0830cb0fc6d94cba87ba12dcdc4dbb855e641-image.png" />

### Customizing the inline app block

> Custom styling for app blocks is not yet supported—watch this space for upcoming features!