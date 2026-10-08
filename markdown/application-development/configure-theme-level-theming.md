---
title: Configure theme-level theming
description: Configure brand colors, shape, theme-owned fonts, logos, favicons, and mobile color mappings in a theme.js module. Theme-level values can vary by tenant or user without a change to component code or an app rebuild.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/configure-theme-level-theming.html
release: zurich
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 3
keywords: [Configure theme-level theming, Declare the theme in theme.js, Connect the theme to the app, Register a theme-owned font, Verify, Examples, Next steps]
breadcrumb: [Theming with Lux, Configure experiences, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Configure theme-level theming

Configure brand colors, shape, theme-owned fonts, logos, favicons, and mobile color mappings in a `theme.js` module. Theme-level values can vary by tenant or user without a change to component code or an app rebuild.

## Before you begin

Role required: admin

## About this task

If a value must stay fixed for every deployment of the app, configure it at the app level instead. For instructions, see [Configure app-level theming](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/configure-app-level-theming.md).

## Procedure

1.  Declare the theme in `theme.js`

    Create `theme.js` at the app root, alongside `aiux.json`, and export an object literal.

    The following example includes the theme's fields. Replace the sample attachment sys IDs and font paths with values from your instance and app.

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
      },
    
      fonts: [
        {
          name: 'Demo Grotesk',
          faces: [
            {
              src: 'public/fonts/DemoGrotesk.woff2',
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
              display: 'swap',
              preload: false
            }
          ]
        }
      ],
    
      mobile_color_variables: {
        'text-primary': '--color-text-primary',
        'surface-primary': '--primary-600',
        'text-on-primary': '--matched-primary-content',
        'custom-background': '#ffffff'
      },
    
      light_logo: 'aaaaaaaa11111111bbbbbbbb22222222',
      dark_logo: 'cccccccc33333333dddddddd44444444',
      light_favicon: 'eeeeeeee55555555ffffffff66666666',
      dark_favicon: '11111111aaaaaaaa22222222bbbbbbbb'
    };
    ```

    For the values each field accepts and what it generates, see [Theme field reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/theme-field-reference.md).

    **Important:** Use a `theme.js` module that exports an object literal, not `theme.json`. The build parses this module to produce the app's `sys_aix_theme` record, and it doesn't read a `theme.json` file in a Lux app.

2.  Connect the theme to the app

    Import the theme in `application.js` and export it as `appTheme`:

    ```
    // application.js
    import {AppTheme} from './theme.js';
    
    export default {
      appTheme: AppTheme,
      applicationLayout: 'aiux-nav-layout'
    };
    ```

    If the app has no lifecycle module, set the theme on the layout class instead:

    ```
    // pages/layout.js
    import {AIUXAppLayoutElement} from '@servicenow/aiux-components-core';
    import {AppTheme} from '../theme.js';
    
    export default class AppLayout extends AIUXAppLayoutElement {
      static appTheme = AppTheme;
    }
    ```

    A theme provisioned on the instance takes precedence over the file-based app theme. For file-based configuration, `application.js` takes precedence over the layout static. If none is configured, Lux uses its default theme.

3.  Register a theme-owned font

    Use `fonts` when a typeface belongs to the tenant's brand and should be replaceable without a change to app source. Declare each family with one or more faces:

    ```
    fonts: [
      {
        name: 'Demo Grotesk',
        faces: [
          {
            src: 'https://cdn.example.com/fonts/DemoGrotesk.woff2',
            format: 'woff2',
            weight: '100 900',
            preload: true
          }
        ]
      }
    ]
    ```

    The `fonts` field registers font faces but doesn't select a family for components.

    For a font that ships with the app and is identical for every tenant, register it in `head.app.css` instead, as described in [Configure app-level theming](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/configure-app-level-theming.md).


## Verify

-   Build and deploy the app, then confirm that a primary-colored control uses the configured brand color.
-   Switch between light and dark modes and verify that text, surfaces, logos, and controls keep sufficient contrast.
-   If the theme doesn't appear, confirm that `theme.js` is exported as `appTheme` before checking individual fields.
-   For a custom font, confirm that the face loaded and that any expected preload was emitted.
-   For a mobile mapping, inspect the mobile theme response and confirm that the semantic name resolves to light and dark values.

## Examples

The `examples/custom-font-theme` app demonstrates a font supplied by the theme.

