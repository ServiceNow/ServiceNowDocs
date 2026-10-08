---
title: Theme field reference
description: The fields of a theme.js theme object set brand colors, neutral colors, shape, fonts, mobile color mappings, logos, and favicons. Each field's value determines the tokens and document resources that the theme generates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/theme-field-reference.html
release: australia
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 6
keywords: [Theme field reference, Theme fields, Brand colors, Neutral colors, Shape, Logos and favicons, Mobile color mappings, Font family fields, Font face fields, Font URLs and preloading, Font registration]
breadcrumb: [Theming with Lux, Configure experiences, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Theme field reference

The fields of a `theme.js` theme object set brand colors, neutral colors, shape, fonts, mobile color mappings, logos, and favicons. Each field's value determines the tokens and document resources that the theme generates.

For the procedure that uses these fields, see [Configure theme-level theming](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configure-theme-level-theming.md).

## Theme fields

The following table lists the fields of the theme object.

|Field|Required|Value example|What it controls|
|-----|--------|-------------|----------------|
|`primary_color`|Yes|`'#032D42'`|Primary brand scale, primary actions, links, and focus states|
|`accent_color`|No|`'#63DF4E'`|Accent scale and secondary or AI-focused emphasis|
|`neutral_colors`|No|`'sand'` or `{use_hex_value: true, hex_value: '#F8F7F4'}`|Neutral scale used by surfaces, text, borders, and dark backgrounds|
|`shape`|No|`{field_radius: '0.5rem', …}`|Selector, field, container, and border shape tokens|
|`fonts`|No|`[{name: 'Demo Grotesk', faces: […]}]`|Font families registered as document-wide `@font-face` rules|
|`mobile_color_variables`|No|`{'text-primary': '--color-text-primary'}`|Mobile semantic names resolved to light and dark hex values by the server|
|`light_logo`|No|A `db_image` sys ID|Navigation logo for light mode|
|`dark_logo`|No|A `db_image` sys ID|Navigation logo for dark mode|
|`light_favicon`|No|A `db_image` sys ID|Browser favicon for light mode|
|`dark_favicon`|No|A `db_image` sys ID|Browser favicon for dark mode|

## Brand colors

The `primary_color` field is the main brand input and should be a hex color. Lux expands it into an 11-stop scale from `50` through `950` for both light and dark modes. Semantic tokens then map buttons, links, focus rings, text, and surfaces to appropriate stops in that scale.

The `accent_color` field generates a separate 11-stop accent scale. Use it for secondary emphasis rather than as a replacement for the primary brand color. If `accent_color` is omitted, Lux uses its default accent color.

```
primary_color: '#032D42',
accent_color: '#63DF4E'
```

In components, use semantic tokens such as `--color-primary` instead of using `--primary-600` directly. Semantic tokens can select different scale stops when the color scheme changes.

## Neutral colors

The neutral scale underpins most backgrounds, text colors, and borders. You can configure it in one of two ways.

Reference a shipped neutral swatch by name:

```
neutral_colors: 'sand'
```

The shipped swatches are `sand`, `granite`, `stone`, `zinc`, `dune`, and `slate`. Names are case-insensitive, and an unknown name fails the metadata build.

Alternatively, generate a custom neutral scale from one hex value:

```
neutral_colors: {
  use_hex_value: true,
  hex_value: '#F8F7F4'
}
```

The object form creates an app-specific `sys_aix_color_swatch` record. The generated light and dark neutral scales feed tokens such as `--neutral-300`, `--color-text-secondary`, and `--color-border-subtle`. If no usable neutral configuration resolves at runtime, Lux generates the default neutral scale so that these tokens aren't left undefined.

## Shape

The `shape` object maps directly to four component-level custom properties.

|Field|CSS token|Applies to|Example values|
|-----|---------|----------|--------------|
|`selector_radius`|`--radius-selector`|Checkboxes, radios, and toggles|`'0'`, `'0.25rem'`, `'9999px'`|
|`field_radius`|`--radius-field`|Inputs, buttons, selects, and text areas|`'0.5rem'`|
|`boxes_radius`|`--radius-box`|Cards, panels, and other containers|`'1rem'`|
|`border_width`|`--border`|Default component borders|`'0'`, `'1px'`, `'2px'`|

Values are CSS lengths. The generated declarations apply under the active `[data-theme]` selector, so all components receive the same shape settings.

## Logos and favicons

The `light_logo`, `dark_logo`, `light_favicon`, and `dark_favicon` fields are ServiceNow `db_image` reference sys IDs, not image URLs:

```
light_logo: 'aaaaaaaa11111111bbbbbbbb22222222',
dark_logo: 'cccccccc33333333dddddddd44444444',
light_favicon: 'eeeeeeee55555555ffffffff66666666',
dark_favicon: '11111111aaaaaaaa22222222bbbbbbbb'
```

The light and dark logo fields populate the theme's mode-specific logo value. The favicon fields produce mode-specific favicon URLs in the document head. Provide both variants when the same asset doesn't have sufficient contrast in both schemes.

## Mobile color mappings

Native mobile clients don't run the browser's color-generation pipeline. The `mobile_color_variables` field maps names that the mobile client expects to design tokens or direct values, which the server resolves for light and dark modes:

```
mobile_color_variables: {
  'text-primary': '--color-text-primary',
  'surface-primary': '--primary-600',
  'text-on-primary': '--matched-primary-content',
  'custom-background': '#ffffff'
}
```

Each key is the semantic name returned to the mobile client. Each value can reference a generated palette token, a semantic color token, or a direct color value. Theme entries are merged over the platform's default mobile mappings, so you only need to declare values that differ from those defaults.

## Font family fields

The `fonts` field is an array of font families, and each family contains one or more faces:

```
fonts: [
  {
    name: 'Demo Grotesk',
    faces: [
      {
        src: '/aiux/your-app/public/fonts/DemoGrotesk.woff2',
        format: 'woff2',
        weight: '100 900',
        style: 'normal',
        display: 'swap',
        unicode_range: 'U+0000-00FF',
        preload: true
      },
      {
        src: 'https://cdn.example.com/fonts/DemoGrotesk-Italic.woff2',
        format: 'woff2',
        weight: '400',
        style: 'italic',
        display: 'swap'
      }
    ]
  }
]
```

The fields of each family are described in the following table.

|Field|Required|Accepted values|Effect|
|-----|--------|---------------|------|
|`name`|Yes|A family name up to 64 letters, numbers, spaces, `.`, `_`, or `-`|Becomes the `font-family` value in generated `@font-face` rules|
|`faces`|Yes|An array of face descriptors|Registers weights, styles, ranges, or files belonging to the family|

A theme can register up to eight usable families and twelve faces per family. Families without a valid name or at least one usable face are omitted.

## Font face fields

The fields of each face descriptor are described in the following table.

|Field|Required|Accepted values|Effect|
|-----|--------|---------------|------|
|`src`|Yes|An `https:` URL, an already-served root-relative path, or an app asset under `public/`|Identifies the font file|
|`format`|No|`'woff2'`, `'woff'`, `'ttf'`, or `'otf'`|Adds the CSS `format()` hint and determines the preload MIME type|
|`weight`|No|`'normal'`, `'bold'`, a number such as `'400'`, or a range such as `'100 900'`|Sets `font-weight`; ranges describe variable fonts|
|`style`|No|`'normal'`, `'italic'`, or `'oblique'`|Sets `font-style`|
|`display`|No|`'auto'`, `'block'`, `'swap'`, `'fallback'`, or `'optional'`|Sets `font-display`; defaults to `'swap'`|
|`unicode_range`|No|A CSS Unicode range such as `'U+0000-00FF'` or a comma-separated list|Limits the characters served by that face|
|`preload`|No|`true` or `false`|Requests an early `<link rel="preload" as="font">` for the face|

Prefer `woff2` for modern browsers, because it normally provides the smallest transfer size. Declare separate faces for distinct static weights and styles, or one weight range for a variable font.

## Font URLs and preloading

Font URLs are validated before CSS is generated. The following URL forms are dropped:

-   `http:` URLs
-   `data:` URLs
-   Protocol-relative URLs, such as `//cdn.example.com/font.woff2`
-   Unsupported relative paths, such as `./fonts/font.woff2`

For a font under the app's `public/` directory, author a path such as `public/fonts/DemoGrotesk.woff2`. The build rewrites it to `/aiux/<basename>/public/fonts/DemoGrotesk.woff2`. The file must also be included by the app's static-content configuration. An `https:` URL or an already-served root-relative path can be used without that rewrite.

At most four faces are preloaded per theme, in declaration order. A preloaded face must include a supported `format`. Without one, Lux can't emit a reliable MIME type and skips that preload. Reserve preloading for faces needed during first paint.

## Font registration

The `fonts` field registers font faces but doesn't select a family for components. During theme generation, valid faces become one `theme-font-faces` style block in the document head. This block registers each family once for the page rather than duplicating `@font-face` rules in every shadow root.

