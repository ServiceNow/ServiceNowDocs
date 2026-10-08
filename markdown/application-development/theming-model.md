---
title: Theming model
description: Lux generates every color, radius, and font token from a small brand configuration, and a theme record can override any of those tokens per tenant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/theming-model.html
release: brazil
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 3
keywords: [Theming model, Brand config instead of component CSS, Token pipeline, Token override hooks, Override precedence, Color scheme and density attributes, Related]
breadcrumb: [Theming with Lux, Configure experiences, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Theming model

Lux generates every color, radius, and font token from a small brand configuration, and a theme record can override any of those tokens per tenant.

Identify which side a given change belongs to before making it:

-   `theme.js` and `tailwind.app.css` are developer work. They ship with the app's source, are the same for every tenant, and changing either requires a rebuild.
-   The `token_overrides` field on a `sys_aix_theme` record and the multi-theme rows that control which theme a given user gets are admin configuration. They change what a tenant sees without an app source change or a redeploy.

Both are combined in the same generated CSS, which is why one topic covers them.

## Brand config instead of component CSS

You don't restyle a Lux app by overriding component CSS. You declare a brand config and the framework generates every color, radius, and font token from it. A scaffolded Lux app's whole theme file is a handful of lines of brand input:

```
// theme.js
export const AppTheme = {
  primary_color: '#032D42',
  accent_color: '#63DF4E',
  neutral_colors: {
    use_hex_value: true,
    hex_value: '#F8F7F4'
  },
  shape: {
    selector_radius: '0.75rem',
    field_radius: '0.5rem',
    boxes_radius: '1rem',
    border_width: '1px'
  }
};
```

`primary_color`, `accent_color`, and `neutral_colors` are base colors, not tokens. Each expands into an 11-stop scale from `50` through `950`, generated once for light mode and once for dark, so contrast holds in both. Semantic tokens map to those stops and are what components consume.

In component styles, use a semantic token instead of a raw stop. Semantic tokens survive a rebrand; raw stops do not.

## Token pipeline

Theming is a pipeline of CSS custom properties that flows from brand configuration into every shadow root:

1.  Brand config in. The theme object's colors, shape, fonts, and token overrides are read. They come from the theme record on the instance at request time, or from the app's own theme module.
2.  Generation. A generator turns them into accessible color scales, validated `@font-face` rules, up to four font preload links, and a token-override block.
3.  Into the document head. Those blocks are emitted as inline `<style>` elements in the server-rendered document, alongside the framework's static token mappings.
4.  Into Tailwind. A Tailwind plugin registers the same tokens as base CSS and as prefixed component overrides. The tokens are then reachable as utility classes rather than only as `var()` calls.
5.  Into every shadow root. The compiled stylesheet is adopted into each `AIUXElement`'s shadow root. CSS custom properties inherit through shadow boundaries, so a token registered at the document root is readable by every component that adopted the sheet.

**Note:** If required theme values aren't provided, the generator falls back to the corresponding values from `DEFAULT_THEME`. This verifies the generated CSS has the color scales needed to resolve semantic tokens correctly. For primary and accent colors, this applies when values are omitted or `undefined`; the neutral scale also falls back when its configuration cannot be resolved.

## Color scheme and density attributes

Light, dark, and density are attributes rather than themes. Color scheme lives on `data-theme` on the document element, and density on `data-density`. Both are orthogonal to which theme record resolved.

The Lux framework exposes a service for flipping color scheme at runtime, and the user's choice persists across reloads. Most apps don't write that themselves, the nav layout ships a theme toggle you turn on with a feature flag.

Density scales spacing, item heights, and sidebar widths globally, because every Tailwind spacing utility resolves through one spacing unit token. Switching density rescales the whole UI with no component-level change. The three modes and their values can be found in .

**Important:** A component that needs to react to color scheme rather than set it should reflect its own attribute onto its host and style against that. The generated theme CSS declares `[data-theme]` rules at the document level, which outrank a `:host` rule for the same token. An override written against `data-theme` inside a shadow root does not apply.

**Related topics**  


[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/design-tokens.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/design-tokens.md)

[theme.js configuration reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/theme-js-configuration-reference.md)

[Configuration model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/configuration-model.md)

