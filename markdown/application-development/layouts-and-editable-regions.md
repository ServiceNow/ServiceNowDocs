---
title: Layouts and editable regions
description: A layout wraps every page in your app's chrome \(header, sidebar, footer\) while pages render only their own content. Within a page, a region composes widgets into a structured arrangement that a visual editor can rearrange later.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/layouts-and-editable-regions.html
release: australia
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 16
keywords: [Layouts and editable regions, The app layout, Choosing a base class, Configuring navigation, App lifecycle hooks, Toolbar actions, Reading layout data in a page, Customizing NavLayout without subclassing, Composing widgets inside a page with the region DSL, The regions/ directory is mandatory, Rows, columns, and the nesting cap, One rule explains every restriction, Spacing is one value, and it isn't admin-editable, The region wrapper, Editing a region visually, Rendering a layout on the server, See also]
breadcrumb: [Build with Lux, Lux Development, Building pro-code applications, Developing your application, Classic app development, Building applications]
---

# Layouts and editable regions

A layout wraps every page in your app's chrome \(header, sidebar, footer\) while pages render only their own content. Within a page, a region composes widgets into a structured arrangement that a visual editor can rearrange later.

## The app layout

A Lux app has one root layout, `pages/layout.js`; you can add nested layouts in route folders \(`pages/<route>/layout.js`\). The build identifies it as the layout, not a page, and wraps every page inside it. Pages shouldn't contain `<header>`, `<nav>`, or global footer elements; all app-wide chrome belongs in the layout.

## Choosing a base class

```
AIUXElement
  └─ AIUXAppLayoutElement       (client-side routing, navigate())
       ├─ AIUXLayout             (header/main/footer structure)
       └─ AIUXStructuredLayout   (header, aside-start, main, aside-end, footer)
            └─ NavLayout          (sidebar, menus, user avatar, preferences)
                 └─ YourLayout    (your sidebar items, app-specific tweaks)
```

Most apps extend `NavLayout` from `@servicenow/aiux-components-nav`, which provides the standard ServiceNow sidebar, header, and L1/L2/L3 navigation. Extending `AIUXAppLayoutElement` directly gives you a fully custom shell, but you give up the sidebar, menus, and breadcrumbs the platform otherwise provides.

A bare custom layout implements `renderLayout()` for the chrome and calls `this.renderPage()` at the point where the current page should render:

```
// pages/layout.js
import {html} from 'lit';
import {customElement} from 'lit/decorators.js';
import {AIUXAppLayoutElement} from '@servicenow/aiux-components-core';

@customElement('my-app-layout')
export default class AppLayout extends AIUXAppLayoutElement {
  renderLayout() {
    return html`
      <header>My App</header>
      <main>${this.renderPage()}</main>
    `;
  }
}
```

## Configuring navigation

`NavLayout`'s sidebar items are set through `navLayoutContext`, typically from the layout's own loader:

```
import {NavLayout, navLayoutContext} from '@servicenow/aiux-components-nav';
import {customElement} from 'lit/decorators.js';

@customElement('my-app-layout')
export default class AppLayout extends NavLayout {
  static async loader(ctx) {
    await super.loader(ctx); // let NavLayout populate menus, prefs, origin, etc.

    navLayoutContext.set({
      ...navLayoutContext.get(),
      items: [
        {icon: 'home', title: 'Home', action: {type: 'navigate', path: '/home'}},
        {icon: 'gear', title: 'Settings', action: {type: 'navigate', path: '/settings'}}
      ]
    });
  }
}
```

Each item is a plain object with `icon`, `title`, and an `action`: `{type: 'navigate', path: '/route'}` for in-app navigation, or `{type: 'event', name: '...'}` for a non-navigation action. `action.path` must correspond to an actual page file; selecting an item whose path has no matching `pages/<route>/page.js` returns a 404 error.

Add an `l2Nav` array to an item for sub-pages, and an `l3Nav` array on an L2 item for tab-style sub-views. Each L2/L3 entry needs its own page file. The layout renders L3 items as a tab bar automatically and highlights the active tab from the current URL.

To change nav items after the initial load \(for example behind a feature flag\), use the imperative helpers instead of rewriting the whole array:

```
import {appendL1Nav, removeL1Nav} from '@servicenow/aiux-components-nav';

appendL1Nav({icon: 'shield', title: 'Risk', action: {type: 'navigate', path: '/risk'}});
removeL1Nav('/risk');
```

These write directly to `navLayoutContext`, so the sidebar re-renders automatically. `appendL1Nav` and `removeL1Nav` carry no `window` guard, so you can call them from `application.js`'s `setup(ctx)` hook and from the layout's loader.

`prependL1Nav` is also available, and all three helpers accept a single item \(or path\) or an array. The older names, `addNavItem` and `removeNavItem`, still work but log a deprecation warning.

## App lifecycle hooks

An optional `application.js` at the app root defines lifecycle hooks independent of the layout. The hooks are described in the following table.

|Hook|Runs|Typical use|
|----|----|-----------|
|`setup(ctx)`|Once, when the app is entered|Configure nav items, set contexts, initialize app state|
|`navigate(navCtx, ctx)`|Before every in-app navigation commits \(client only\)|Rewrite a route, guard/redirect|
|`teardown(ctx)`|When leaving the app \(client only\)|Clean up subscriptions, reset nav state|

All hooks are optional, and `application.js` itself is optional; omit it entirely if your app has no app-level lifecycle logic.

A fourth hook, `notFound()`, runs when no route matches. For its full contract, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/component-lifecycle.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/component-lifecycle.md).

## Toolbar actions

A page contributes buttons to the sticky toolbar by calling `setPageActions(host, actions)` from `@servicenow/aiux-components-nav`, typically from `firstUpdated()`. The toolbar shows up to three actions directly; the rest collapse into a "More actions" menu, sooner on narrow screens. Actions clear automatically when the user navigates away.

## Reading layout data in a page

A page reads data the layout's loader produced with `getLayoutData(key)` \(`key` is the layout's tag name\), available on every `AIUXElement` subclass:

```
render() {
  const user = this.getLayoutData('my-app-layout')?.user;
  return html`<h1>Welcome, ${user?.name}</h1>`;
}
```

`getLayoutData()` is deprecated in favor of the Context API for new cross-component data sharing, but it remains in use in existing code.

## Customizing NavLayout without subclassing

If your app uses the stock `NavLayout` but needs app-specific AI context or client tools, declare a `layoutOverrides` block in `application.js` instead of subclassing:

```
// application.js
export default {
  layoutOverrides: {
    aiContext: {
      description: 'The core UI navigation layout',
      bestFor: 'When the user asks to navigate to a page or section'
    },
    client_tools: {
      navigateToMenuItem: {
        description: 'Navigate to a menu item by its visible title',
        arguments: [{name: 'title', type: 'string', required: true, description: 'The menu item title'}],
        // Must be a regular function; arrow functions break `this` binding
        definition: async function ({title} = {}) {
          const items = await this.getNavigableMenuItems();
          // ...
        }
      }
    }
  }
};
```

Only `aiContext` and `client_tools` are overridable this way; `styles` is not. Extend `NavLayout` and spread `NavLayout.styles` for additional styles. If you subclass `NavLayout` and declare your own `static aiContext` or `static client_tools`, your subclass's own declaration wins over the `application.js` override for that property.

**Warning:** Layout overrides \(`layoutOverrides` in `application.js`\) are loaded from your app's lifecycle bundle. The bundle exists only after the app has been built. If the bundle is missing or fails to load, the page still renders, but your layout overrides are not applied. No error or warning is shown. If an override has no effect after a build, confirm that your app has an `application.js` and that the bundle request succeeds in your browser's network tools.

## Composing widgets inside a page with the region DSL

Separately from `pages/layout.js`, Lux provides a `region` tagged template \(from `@servicenow/aiux-components-core`\) for composing widgets within a page. It's a constrained, HTML-like domain-specific language \(DSL\); only `row`, `column`, `raw`, and hyphenated widget tags are valid. It's built so that a visual editor can parse, manipulate, and serialize the arrangement, and that visual editing surface is what makes a region "editable."

## The regions/ directory is mandatory

All `region` DSL must live in a file under `<srcDir>/regions/` \(the configured source root, or the project root if `srcDir` isn't set\). Using `region` as a tagged template directly in a page's `render()` is a build error. The page imports a thunk from `regions/` and calls it; the `region` import never appears in a page file.

```
// regions/home/body.js: the DSL lives here
import {region} from '@servicenow/aiux-components-core';
import '../../widgets/stat-card/index.js';
import '../../widgets/activity-feed/index.js';

// Thunk form: the tagged template is invoked per render, so the override
// lookup reads the current request's registry, not the empty module-load
// one. The region name is derived from this file's path by the SDK.
export default () => region`
  <row>
    <column span=${8}>
      <stat-card aiux-config-id="hero" .label=${'Open Incidents'} .value=${'142'} />
    </column>
    <column span=${4}>
      <activity-feed .title=${'Recent Activity'} />
    </column>
  </row>
`;
```

```
// pages/home/page.js: the page imports the thunk, never imports region
import {html} from 'lit';
import {AIUXElement} from '@servicenow/aiux-components-core';
import body from '../../regions/home/body.js';

export default class HomePage extends AIUXElement {
  render() {
    return html`
      <h1>Dashboard</h1>
      ${body()}
    `;
  }
}
```

Call `body()` on every `render()` and don't cache its result. That is what makes the runtime consult the current request's `sys_aix_page_region` override registry rather than a module-load-time snapshot.

The build enforces this, and there is no opt-out. The build fails on any file outside `regions/` that imports `region` or uses it as a tagged template. The required file shape is described in the following list.

-   The default export is a nullary, non-async, non-generator function: arrow, function expression, or declaration.
-   It returns a bare `region`…`` tagged template, either directly or as the sole statement of a block body. It uses the exact local name the file imported `region` as.
-   Every `${…}` interpolation is a literal: string, number, boolean, `null`, or an array of those. Object literals aren't allowed. A variable, ternary, or function call fails with `region interpolation must be a literal value`.
-   A string value can't contain a `}` character.
-   Widget imports go in the region file, with paths relative to it.
-   No `<scope:tag>` elements; that prefix is only for admin-saved layouts.
-   Every hyphenated tag must be a widget: one of the app's own widgets \(`widgets/<name>/index.js`\) or a published widget imported from `@servicenow/glide-widgets/<scope>/<tag>`. A plain component fails the build.

The region's name comes from its file path, relative to `regions/`, extension stripped, `/` replaced with `-`: `regions/home/body.js` registers as `home-body`. That name is what the visual editor writes into `sys_aix_page_region.region`, and what the runtime looks up overrides by. There is no decorator for it, and writing it by hand \(the curried `region('my-name')`…`` form\) is also a build error. Folder and file segments must match `^[A-Za-z_][A-Za-z0-9._-]*$`. The derived name can't be `default`, `none`, `auto`, `and`, `or`, or `not`.

## Rows, columns, and the nesting cap

|Tag|Role|Holds|
|---|----|-----|
|`row`|The arrangement: a 12-column grid|One or more `column`s, nothing else|
|`column`|The slot: addressable, lockable, position-bearing, and a vertical flex column|Widgets, `raw`, and nested `row`s in any mix; never a `column` directly|
|`raw`|Escape hatch for static author-written markup|An opaque HTML string; no attributes, no `${}`|

A region's top level holds only `row`s, and a `column` is always inside a `row`. The one-column case has exactly one spelling, `<row><column span=${12}>`. With the nesting cap, a region can take exactly two shapes: `row > column > widget`, and `row > column > row > column > widget`. A third level of `row` is a parse error, and the visual editor refuses a deeper edit up front with "Max nesting reached."

An empty `row` is refused, not seeded. A column-less row is a parse error at any depth. Nothing in it can hold a widget, so it is not a layout. A stored or code-authored region holding one doesn't parse, the editor never loads it, and the region's blocked reason carries the parser's message.

Several top-level rows are fine. Multiple widgets in one `column` already stack vertically, so there is no separate "stack" primitive; `<stack>` is deprecated and rewrites to `<row><column span=${12}>`, carrying none of its attributes across.

## One rule explains every restriction

**Note:** A widget receives only its own declared properties. Every value is a whole `${}` hole of a serializable kind. Nothing reaches the element as raw source text.

That's why there's no `class`, `style`, `@event` or arbitrary-attribute support. A widget's entire vocabulary is `.prop=${…}`, `?bool=${…}`, and the editor metadata `aiux-pinned` / `aiux-order` / `aiux-config-id`. `name="hello"` without the dot is invalid; write `.name=${'hello'}` even for a plain string. A widget is always a leaf: it cannot contain children, another widget, or text. If part of the page needs slotted composition, write it in plain Lit `html` in the page.

|Tag|Attribute|Values|Notes|
|---|---------|------|-----|
|any widget|`.prop=${value}`|Any serializable value|Live property binding|
|any widget|`?bool=${value}`|Any value|Boolean attribute, present when truthy|
|any widget|`aiux-pinned`|Bare|The visual editor can't remove it|
|any widget|`aiux-order`|`${n}` or literal|Display-order metadata|
|any widget|`aiux-config-id="id"`|Non-empty string, required if present|Stamps `data-aiux-element-id` + `aiux-config-data`|
|`column`|`span=${n}`|Integer 1–12, default 12|Grid width in its `row`|
|`column`|`span-sm`…`span-2xl=${n}`|Integer 1–12|Breakpoint override, ascending emission|
|`column`|`locked`|Bare|The visual editor fixes its position|
|`column`|`scroll=${'sm'|'md'|'lg'}`|Closed token|Bounds block size and makes the column independently scrollable|
|`row`|`container`|Bare|Switches child `span-{bp}` from the viewport axis to a container-query axis|
|`raw`|none| |Takes zero attributes|

`container`'s viewport `md` \(`48rem`\) and container `@md` \(`28rem`\) are different physical widths under the same `span-md` attribute name. That's Tailwind's design, not a DSL quirk.

Values must arrive through `${}` for escaping reasons, not expressiveness. A `Date`, class instance, `NaN` or `Infinity` binds live, but round-trips through storage as an ISO string, a plain object or `null`. The widget has to cast it back. Several kinds throw at parse time instead, because a stored layout's JSON round trip destroys them. Those kinds are a function, a `nothing`/`noChange` sentinel, a directive \(`ifDefined`, `classMap`, `ref`\), a nested `html`/`region` template, a `bigint`, and a `Map`/`Set`/`RegExp`. To omit a property conditionally, pass `undefined` or `null`.

## Spacing is one value, and it isn't admin-editable

A region has one spacing value: the gutter `gap-layout` puts between every row's columns, every column's children, and the region's own top-level rows. There is no padding and no per-instance override, so the space between any two adjacent widgets is the same however deeply they nest.

`gap` and `padding` are deprecated. Both are still parsed and still consumed by the region, so they never reach the rendered element. They are ignored on any tag and with any value, and warned one time per attribute/tag pair. Build-time warnings are source-located per region file; runtime warnings fire once per page load per distinct notice. Remove them. `margin` was considered and deliberately left out. A child owning its own outer spacing, alongside a container that already owns spacing between children, produces uneven or doubled gaps.

To retune the gutter, set the `--layout-gap` custom property at `:root`, or set `--spacing-layout` on an ancestor to scope one subtree. A `--layout-gap` set on a descendant of `:root` isn't read, because the `var()` in the token's definition is substituted where it's declared.

## The region wrapper

**Note:**

Every rendered region is enclosed in exactly one wrapper element: `<div data-aiux-region="{name}" class="flex flex-col gap-layout overflow-hidden">`. The wrapper is part of the rendered-output contract, so query `data-aiux-region` as a literal.

The wrapper is a real layout box that stacks the region's top-level rows as a flex column on `gap-layout`. This is the same theme-able gutter a `row` puts between its columns and a `column` puts between its children. Two top-level rows sit exactly one gutter apart, the same distance as two widgets in a column. It carries `overflow-hidden` because it is the region's outermost box, the one the page's layout places. The layout consequence for the page: a region is one item of the page's own grid or flex parent, rather than each of its rows being one.

The following consequences matter when you query or test a region.

-   Measuring a region means measuring the union of the wrapper's children, not the wrapper's own rect; the page's layout can stretch the wrapper past the rows it holds.
-   Inner nodes carry no marker: one `<div>` per primitive, one element per widget, in AST order. Map DOM back to AST by walking both in parallel from the wrapper. The one exception is a `scroll`-bearing `column`, which emits two elements \(`data-aiux-scroll-root` around `data-aiux-scroll`\), with the grid placement on the outer one.

**Note:** Widget-inside-widget composition isn't supported by the DSL.

## Editing a region visually

Every region a page renders with `region` can be edited directly on the live page by a config admin, without touching code. Opening the admin configuration mode unlocks every region on the page at one time; there's no separate "edit layout" step to enter. An admin can then do the following:

-   Add or remove widgets from a searchable widget picker, or drag one in from a "Recents" list
-   Resize a column's grid span, or move a widget beside or below another one
-   Turn on `scroll` to bound a column's height and make it independently scrollable
-   Restore a region to the layout the app ships in code, discarding the admin's override

The first edit to a region creates a new row in `sys_aix_page_region`, keyed on `(widget, region)` \(the page's widget and the path-derived region name\). From that point, the region's layout stops taking upgrades from new app versions. The widgets inside it keep taking theirs, but the arrangement is now the admin's to maintain. "Restore defaults" deletes the override row, and the app-shipped layout takes over again.

Repositioning a widget needs nothing from you. Making a widget inside a region individually configurable needs an `aiux-config-id` on that widget in the region file. Configurable means the admin can edit its properties, not just move it. The `regions/home/body.js` example sets one on `<stat-card>`. See  for what that attribute stamps and how a component reads its slice.

Some regions can't be opened in the editor. In each case the admin gets the reason on the region's outline rather than an error.

-   A `<raw>` block. Author it in code, or don't use `<raw>` in a region you expect admins to reconfigure.
-   A region the parser rejects \(most commonly a column-less `row`\). The editor never loads it and surfaces the parser's own message as the blocked reason.

A region rendered by one of the page's child widgets is also refused rather than reassigned upwards. A region is the page's own layout, and an override keyed on the page would claim the page owns something its child authored.

## Rendering a layout on the server

Every page request renders as a nested tree of Lit components: the page component wrapped inside its layout. Both the layout's and the page's loaders run in parallel on the server.

If your app defines no custom layout, Lux falls back to the layout named by `applicationLayout` in `application.js` \(`aiux-nav-layout` or `aiux-layout`; default `aiux-layout`\).

**Related topics**  


[Create a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/create-a-page.md)

[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/component-lifecycle.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/component-lifecycle.md)

[metadata-and-configuration]

[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/reusable-components.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/reusable-components.md)

