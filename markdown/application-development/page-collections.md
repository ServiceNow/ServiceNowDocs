---
title: Lux Page variants
description: A page collection lets more than one page module claim the same route. Lux determines which one to serve, per request, per user, instead of you branching a single render\(\) on role checks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/page-collections.html
release: australia
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 6
keywords: [Page collections, The \_variants/ convention, Declaring a candidate, How resolution works, Switching between siblings, Schema, How a page becomes sys\_aix\_page in general, See also]
breadcrumb: [Build with Lux, Lux Development, Building pro-code applications, Developing your application, Classic app development, Building applications]
---

# Lux Page variants

A page collection lets more than one page module claim the same route. Lux determines which one to serve, per request, per user, instead of you branching a single `render()` on role checks.

Use a page collection when a route needs a structurally different page for different audiences \(different widgets, different layout, different loader\), not just a conditionally hidden section. A hidden section is simpler to express as a widget ACL or a reactive property.

Page variants make it a deliberate, authored pattern. A variant is one or more candidate pages in a `_variants/` folder, plus an optional base page at the normal route. Each sibling is optionally gated by role or access control list \(ACL\), and ranked by an explicit order.

**Note:** There's no admin interface for reordering or disabling a page variant; **order** and **active** are edited directly on the installed `sys_aix_page` record.

## The \_collections/ convention

Put a base page at the normal route, then add a `_variants/` sibling folder next to it with one subfolder per candidate:

```
pages/dashboard/
├── page.js                    ← base page, order 100 (default), no ACL
└── _variants/
    └── admin/
        └── page.js            ← candidate, ranked ahead of the base page
```

`_variants/` is reserved and contributes no route segment of its own. Every `page.js`/`page.ts` under it, at any nesting depth, resolves to the same route as the sibling base page. A `_variants/` folder that contains no `page.js`/`page.ts` fails the build. A base page next to it is optional; without one, the route comes from the parent folder.

The older folder name, `_collections/`, still builds but logs a deprecation warning. A folder that contains both `_variants/` and `_collections/` fails the build.

## Declaring a candidate

Gate and rank a candidate with two build-time decorators from `@servicenow/aiux-components-core`:

```
// pages/dashboard/_variants/admin/page.js
import {html} from 'lit';
import {customElement} from 'lit/decorators.js';
import {AIUXElement, decorators} from '@servicenow/aiux-components-core';

const {acl, order} = decorators;

@customElement('collections-demo-dashboard-admin-page')
@order(10)
@acl([{decision: 'allow_if', roles: ['admin']}])
export default class DashboardAdminPage extends AIUXElement {
  render() {
    return html`<h1>Dashboard (admin)</h1>`;
  }
}
```

The decorators for gating and ranking a collection candidate are described in the following table.

|Decorator|Effect|
|---------|------|
|`@order(N)`|Integer; lower wins. A page with no `@order()` gets the default, 100 \(pages contributed by an extension default to 10\).|
|`@acl([{decision?, roles?, securityAttribute?, id?}])`|`decision` is `'allow_if'` \(the default\) or `'deny_unless'`. Each rule needs a non-empty `roles` array of role names, a non-empty `securityAttribute` string, or both. `id` is optional. A rule set made only of `deny_unless` rules fails the build. The build emits one ACL record per rule.|

**Warning:** An ungated candidate must not sort ahead of gated siblings, or it wins for everyone. A missing ACL record is read leniently, accessible to all, so an undecorated \(or `@order()`-only\) page with a lower order than its gated siblings permanently shadows them. Leave an intentional fallback page at the default order \(100\) or higher.

`@acl()` and a legacy `@roles()` decorator are mutually exclusive for a variant candidate. A page carrying both still gets its ACL record generated, but only the `roles` check runs during resolution.

## How resolution works

1.  Every `sys_aix_page` candidate whose `path_pattern` matches the requested path is collected.
2.  Candidates are sorted by URL specificity first, then by `order` ascending; a base page and its `_variants/` siblings share one route, so `order` alone decides among them.
3.  Each candidate is checked, in that sorted order, by whichever access mechanism its own record declares. A legacy `roles` check fails closed on an infrastructure error. An ACL check runs against the candidate's own ACL records and fails open, so an undecorated page with no ACL record is accessible to everyone.
4.  The first accessible candidate wins and is served, unless the request names an accessible sibling \(the viewer's switcher choice or the URL\), which is served instead. The rest are offered as alternatives, which is what the two pickers in the Switching between siblings section render from.

Variant candidates are resolved live, per request. A route with more than one page variant doesn't use the identity-blind on-disk fast path, so switching identity mid-session picks up the correct candidate on the next request.

## Switching between siblings

Two surfaces render the sibling pool, for two different audiences.

|Aspect|`<aiux-page-variant-switcher>`|The config editor's collection picker|
|------|------------------------------|-------------------------------------|
|Package|`@servicenow/aiux-components-nav`|`@servicenow/aiux-components-config-editor`|
|Audience|Viewer|Admin, while configuring|
|Mount|`horizontal-contextual-nav`, through `nav-layout`|The config editor's toolbar|
|Gate|`features.pageVariantSwitcher`, default `true`, and the `aiux.nav.page_variant_switcher.enabled` system property, default `true`; both must allow it|Only while editing|

Switching page variants while configuring is an authoring action rather than a viewer action, so the editor gets its own control labeled "Editing:" followed by the page variant title. An app that wants only the authoring control turns the shell control off per app:

```
navLayoutContext.set({
  ...(navLayoutContext.get() ?? {}),
  features: {...(navLayoutContext.get()?.features ?? {}), pageVariantSwitcher: false}
});
await super.loader(ctx);
```

**Warning:** NavLayout.loader takes only `ctx`. A second options argument is silently dropped, so feature opt-outs must be written onto `navLayoutContext` before `super.loader` runs, as the preceding example shows.

Both pickers run the switch through the router's **beforeNavigate** pipeline rather than assigning `location.href`, so a dirty-state guard goes first and switching can't silently discard unsaved work. Either way the sibling is chosen during server route resolution; a switch re-resolves the route server-side rather than swapping client state.

The config editor's entry point appears for config admins when the page has a configurable component or more than one page variant.

## Schema

`sys_aix_page` carries three fields for this feature.

|Column|Type|Default|Purpose|
|------|----|-------|-------|
|`variant_name`|string| |Identifies a collection page relative to its base page. The build derives it from the folder segment\(s\) under `_variants/<name>/` and writes it onto the record \(e.g. `_variants/admin/page.js` → `admin`\); no manual authoring step.|
|`order`|integer|`100` \(`10` for extension pages\)|Evaluation precedence when multiple candidates match the same route. Lower wins.|
|`active`|boolean|`true`|Lets an admin disable a page variant without deleting it.|

There's no `parent_page_id` link back to the base page and no `variant_name`/`is_default` flag; a page variant is identified purely by sharing its base page's `path_pattern`.

## How a page becomes sys\_aix\_page in general

Outside the variants feature specifically, every page under `pages/` maps to a `sys_aix_page` record the same way.

|Source|Field|Derivation|
|------|-----|----------|
|Folder path under `pages/`|`path_pattern`|`[param]` converts to `:param`; the `page.js`/`page.ts` filename is not part of the route|
|`@title()` decorator|`title`|Decorator value on the default export class|
|`@global(false)` decorator|`private_experience`|Restricts the page to the app's own experience. Build error if `aiux.json` has no `basename`|
|`@roles([...])` decorator|`roles`|Legacy role gate, distinct from `@acl()`|

**Related topics**  


[Create a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/create-a-page.md)

[metadata-and-configuration]

