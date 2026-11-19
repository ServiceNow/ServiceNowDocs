---
title: theme.js configuration reference
description: A Lux application declares its brand in one file at the project root, and the framework generates every color, radius, and font token from it. Restyling a Lux application goes through that file rather than through component CSS.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/theme-js-configuration-reference.html
release: zurich
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 5
keywords: [theme.js configuration reference, Scaffolded theme file, Fields, Applying the theme, Precedence, Generated color scales, Custom fonts, token\_overrides, Key to selector, Key resolution, Application CSS precedence, Storage and request flow, Switching light and dark at runtime, Reacting to the theme mode, Related]
breadcrumb: [Lux Reference, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# theme.js configuration reference

A Lux application declares its brand in one file at the project root, and the framework generates every color, radius, and font token from it. Restyling a Lux application goes through that file rather than through component CSS.

**Important:** Two files carry the name `theme.js`, and this page is about your application's own root `theme.js`, which holds four keys of brand input. The framework's internal token-definitions module, `libraries/theme-generation/src/algorithm/theme.js`, is documented in [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/design-tokens.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/design-tokens.md). If you are looking for `ROOT_TOKENS`, look there.

## Scaffolded theme file

A scaffolded application ships with the following file.

```
// theme.js
export const AppTheme = {
  primary_color: '#032D42',
  neutral_colors: {use_hex_value: true, hex_value: '#F8F7F4'},
  shape: {
    selector_radius: '0.75rem',
    field_radius: '0.5rem',
    boxes_radius: '1rem',
    border_width: '1px'
  }
};
```

That is the whole file. The generated palette propagates to every component in the application.

## theme.js Fields

|Field|Type|What it controls|
|-----|----|----------------|
|`primary_color`|Hex string|Brand color. Drives the `--primary-*` scale, buttons, links, and focus rings.|
|`accent_color`|Hex string|Secondary calls to action, through the `--accent-*` scale.|
|`neutral_colors`|`{use_hex_value: true, hex_value: '#…'}`|Base for the `--neutral-*` scale, which most surface, text, and border tokens resolve through.|
|`shape`|Object|Four radius and width keys: `selector_radius` for check boxes, radios, and toggles, `field_radius` for inputs and buttons, `boxes_radius` for cards and panels, and `border_width`.|
|`fonts`|Array|Font families to register as `@font-face`.|
|`light_logo` / `dark_logo`|Attachment reference|Per-scheme logo shown in the nav header.|
|`light_favicon_url` / `dark_favicon_url`|URL|Per-scheme favicon.|
|`token_overrides`|Object|Override for individual token values.|

Only `primary_color` is required. Every other field falls back to a Lux default.

The four `shape` keys map onto the tokens documented in .

## Applying the theme

Export the theme from your application's lifecycle module. Nothing else is required.

```
// application.js
import {AppTheme} from './theme.js';

export default {
  appTheme: AppTheme,
  applicationLayout: 'aiux-nav-layout'
};
```

When your application has no lifecycle module, set the theme as a static on your layout class instead.

```
// pages/layout.js
import {AIUXAppLayoutElement} from '@servicenow/aiux-components-core';
import {AppTheme} from '../theme.js';

export default class AppLayout extends AIUXAppLayoutElement {
  static appTheme = AppTheme;
}
```

## Precedence

The following table lists the four theme sources, highest precedence first.

|Source|Notes|
|------|-----|
|A theme provisioned on the instance|Wins over everything in code, so an admin can rebrand the same application without a code change|
|`application.js`'s `appTheme` export|Wins over the layout static|
|`static appTheme` on an `AIUXAppLayoutElement` subclass|Fallback when there is no lifecycle module|
|The framework default theme|Applies when none of the other sources is present|

## Generated color scales

`primary_color`, `accent_color`, and `neutral_colors` are base colors rather than tokens. Each is expanded into an 11-stop scale, `50` through `950`, generated twice, once for light mode and once for dark, so contrast holds in both. The semantic tokens are defined in terms of those stops.

That expansion is why one hex value is enough to rebrand an application, and why component styles should use a semantic token rather than a raw stop. See .

## token\_overrides

`token_overrides` sets any design token without a change to component code. Every built-in token is defined with an override hook already in place, so a key matching a known token replaces that token's value everywhere it is consumed. A key matching nothing is emitted as a new custom property you can `var()` yourself.

Keys at the top level apply everywhere. Nest them under `light`, `dark`, `comfy`, or `cozy` to scope an override to one color scheme or density mode.

```
export const AppTheme = {
  primary_color: '#032D42',
  token_overrides: {
    '--radius-lg': '1.5rem',        // known token: every card gets rounder
    '--font-sans': '"Demo Grotesk"',
    '--brand-glow': '0 0 12px #63DF4E', // unknown key: new property, use via var()

    light: {'--color-primary': '#032D42'},
    dark: {'--color-primary': '#63DF4E'},
    comfy: {'--space-unit': '0.4rem'},
    cozy: {'--space-unit': '0.1rem'}
  }
};
```

## Key to selector

|Source key|Selector emitted|
|----------|----------------|
|Root-level keys|`:root`|
|`light`|`[data-theme="light"]`|
|`dark`|`[data-theme="dark"]`|
|`comfy`|`[data-density="comfy"]`|
|`cozy`|`[data-density="cozy"]`|

A theme with no `token_overrides`, or with an empty object, emits no override block.

## Key resolution

`generateTokenOverrideBlocks()` checks each key against `ROOT_TOKENS`, `DATAVIS_ROOT_TOKENS`, `LIGHT_THEME_TOKENS`, `DARK_THEME_TOKENS`, `DENSITY_COMFY`, and `DENSITY_COZY`. A match is renamed to `--theme-level-<name>`, which feeds the `var(--theme-level-<name>, <default>)` indirection already baked into that token. A non-match passes through unprefixed.

## Application CSS precedence

Tokens declared in your application's `tailwind.app.css` sit above the theme in the cascade, so a value pinned there isn't affected by whatever a theme sets. Use `token_overrides` for what a rebrand should be able to change, and `tailwind.app.css` for what it should not.

## Storage and request flow

The field is stored as a JSON blob on the `sys_aix_theme` record. It is an empty string, rather than `null` or `undefined`, when a theme declares no overrides.

A theme's `theme.js`, or an admin-authored theme record, declares `token_overrides`. `collectThemeRecords()` stringifies it into the `sys_aix_theme.token_overrides` column at build time, and `theme-reader.js` parses it back on every request. `getAppThemeCSS()` calls `generateThemeCSS()`, which includes the override block in the server-rendered `<style id="theme-token-overrides">` tag. On a client-side theme change, `applyTheme()` regenerates and swaps the same block without a full reload.

The mechanism is implemented, with the font route noted in the preceding note.

## Switching light and dark at runtime

Theme mode lives on the `data-theme` attribute. The framework exposes a service for flipping it, and the user's choice persists across reloads.

```
import {
  setThemeMode,
  getThemeMode,
  themeContext
} from '@servicenow/aiux-components-core';

_toggleTheme() {
  setThemeMode(getThemeMode() === 'dark' ? 'light' : 'dark');
}
```

Most applications don't need to write that code, because the nav layout ships a theme toggle that you turn on with `features.themeToggle`.

## Reacting to the theme mode

Consume `themeContext` and reflect the value onto your own host as `theme-variant`.

```
static contexts = [themeContext];

willUpdate() {
  this.setAttribute('theme-variant', themeContext.get()?.mode ?? 'light');
}

static styles = css`
  :host([theme-variant='dark']) .panel {
    box-shadow: none;
  }
`;
```

Use `theme-variant` on the host rather than `data-theme`. The generated theme CSS declares `[data-theme]` rules at the document level, and those outrank a `:host` rule for the same token. Reflecting your own attribute keeps the override inside your shadow root, where it applies.

