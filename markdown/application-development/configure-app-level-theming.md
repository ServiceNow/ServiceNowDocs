---
title: Configure app-level theming
description: Configure app-level CSS for styles that belong to the app and must stay the same regardless of the tenant or user-resolved theme. Lux supports two optional files for this, tailwind.app.css and head.app.css.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/configure-app-level-theming.html
release: australia
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 3
keywords: [Configure app-level theming, Extend component styles with tailwind.app.css, Register document-wide CSS with head.app.css, Verify, Next steps]
breadcrumb: [Theming with Lux, Configure experiences, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Configure app-level theming

Configure app-level CSS for styles that belong to the app and must stay the same regardless of the tenant or user-resolved theme. Lux supports two optional files for this, `tailwind.app.css` and `head.app.css`.

## Before you begin

Role required: admin

## About this task

Both files sit at the app root, alongside `aiux.json`. The `aiux build` command discovers both files automatically, so they require no manifest entry or manual import.

The following table compares the two files.

|File|Scope|Use it for|
|----|-----|----------|
|`tailwind.app.css`|Every app component's shadow root|New or overriding utilities, dynamic-class safelists, and app-specific animations|
|`head.app.css`|The document `<head>`|CSS that must be registered once for the whole document, especially `@font-face`|

For colors, shape, or fonts that a tenant theme should be able to change, use `theme.js` instead. For instructions, see [Configure theme-level theming](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configure-theme-level-theming.md).

## Procedure

1.  Extend component styles with `tailwind.app.css`

    The app's Tailwind build compiles `tailwind.app.css`, and the compiled sheet is adopted into every app component's shadow root. Use this file when a rule must be available inside components.

    The file supports Tailwind directives and standard CSS, including the items in the following table.

    |Directive or rule|Use|
    |-----------------|---|
    |`@source inline("…")`|Safelist class names that can't be discovered statically|
    |`@layer utilities { … }`|Add or override utility classes|
    |`@keyframes … { … }`|Define app-specific animations|

    Declare overrides in a named layer so that their precedence doesn't depend only on stylesheet order:

    ```
    /* tailwind.app.css */
    @layer utilities, your-app;
    
    @layer your-app {
      .aiux-btn {
        border-radius: 50px;
      }
    }
    ```

    **Important:**

    Leave the following two things out of `tailwind.app.css`:

    -   Don't add `@import "tailwindcss"`. The build entry already imports Tailwind, and another import duplicates generated styles.
    -   Don't add an `@theme { … }` block. The app build removes the generated theme layer so that it can't replace the platform's customized tokens.
2.  Register document-wide CSS with `head.app.css`

    The `head.app.css` file isn't processed by Tailwind or PostCSS, and it's linked directly in the document `<head>`. Its content is preserved except for supported `public/...` URLs inside `@font-face` rules, which the build prefixes with the app basename.

    Use this file for CSS that must be registered once outside component shadow roots. The primary use case is `@font-face`:

    ```
    /* head.app.css */
    @font-face {
      font-family: 'Inter';
      font-style: normal;
      font-weight: 400 700;
      font-display: swap;
      src: url(https://cdn.example.com/fonts/inter.woff2) format('woff2');
    }
    ```

    Inside an `@font-face` rule, a path beginning with `public/` is rewritten to `/aiux/<basename>/public/...`. Other URLs, URLs outside `@font-face`, and `@import` values are preserved as authored. For those references, use an `https:` URL, a `data:` URI, or an already-served root-relative path.

    The `head.app.css` pipeline doesn't copy local assets, so files under `public/` must also be included by the app's static-content configuration.


## Verify

-   Build and deploy the app. No additional manifest configuration is required.
-   Inspect the document `<head>` and confirm that `head.app.css` is linked after the platform's base `aiux-theme-variables` style block.
-   Inspect an app component's shadow root and confirm that the compiled app Tailwind sheet is present.
-   For a custom font, confirm that the font file loads once.

## What to do next

-   [Configure app-level theming](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configure-app-level-theming.md) — configure rebrandable colors, shape, and fonts.
-    — available tokens and their default values.

