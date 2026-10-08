---
title: Regions and the wrapper contract
description: A config admin can restructure a page's layout directly on the rendered page and persist the result as an admin override. Config admins can add and remove rows, columns, and widgets, resize column spans, change scrolling, and move containers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/regions-and-the-wrapper-contract.html
release: australia
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 5
keywords: [Regions and the wrapper contract, Region wrapper contract, Region spacing, Which element owns a region, Round-trip to storable text, Related]
breadcrumb: [Layout configuration, Configure experiences, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Regions and the wrapper contract

A config admin can restructure a page's layout directly on the rendered page and persist the result as an admin override. Config admins can add and remove rows, columns, and widgets, resize column spans, change scrolling, and move containers.

A region is a named, addressable area of a page. A region is authored in code with the `region` template and rendered inside a wrapper element that contains the region. The preceding topics in this series cover admin overrides for property values. This topic covers admin overrides for layouts, including how to edit an already-rendered region and the persistence path that makes an edit stick.

## Region wrapper contract

Every rendered region is enclosed in exactly one wrapper element. The wrapper is part of the rendered-output contract and uses a specific data attribute for identification.

A region's name is the thing an override is keyed on.

## Region spacing

A region's spacing is not something the editor exposes. The runtime emits one uniform gutter between all widgets and no padding. Spacing is retuned through the `--layout-gap` custom property, or `--spacing-layout` for one subtree, rather than through the DSL. The paddings-and-gaps popover that used to write `gap` and `padding` is gone with them.

`gap` and `padding` are deprecated on the authoring side too. Both are still parsed and consumed by the region, so they never reach the rendered element. But they are ignored on any tag, with any value, and warned once per attribute and tag pair. They existed to tune spacing per container, which is exactly what a uniform gutter cannot allow. A `padding` on a column, or a smaller `gap` on a nested row, doubles or breaks the gutter at that nesting boundary. `margin` was considered for the same purpose and deliberately left out.

## Which element owns a region

One element per page owns its regions, and which one depends on the kind of page.

|Page|Region owner|Row keyed on|
|----|------------|------------|
|A normal custom page \(anything an app author wrote\)|The page widget, and nothing else|The page's widget record, read from the manifest with no round trip|
|A core-ui page \(a list page or a record page\)|The view widget, and never the page|That widget's `sys_aix_widget` row, read from the instance|

The page is the outermost tag in the region's custom-element ancestor chain that the client manifest carries a widget record for. Layouts and app-level lifecycle modules aren't in that set, so they are skipped without a test of their own.

Two consequences follow:

-   A normal page's child widgets are not searched for regions. A region is the page's own layout. A widget that renders one is describing a layout it does not own. An override keyed on the page would claim the page owns something its child authored. Such a region is refused rather than reassigned upward; no session, nothing to save; and the widget entries inside it are untouched.
-   On a core-ui page, being the page widget is not enough. The page itself is platform chrome nobody configures. The page body is a view widget resolved per request. That widget is what an admin is rearranging, so it is the only element on the page allowed to own a region. Several views can be configured and only the one the platform's view-rule engine picked is on the page, so the DOM settles which one it was.

## The printer

The printer converts an edited tree to storable text. Before it returns the text, it verifies its own output. The printer splits, decodes, and re-parses the text it printed. It then compares the two trees. If the trees do not match, the printer throws an error.

This behavior is necessary, not cautious. The renderer catches render errors and falls back to the code-authored template without warning. A mis-printed edit does not cause an error. It causes an edit that appears to do nothing. The printer throws an error at the print step to prevent this.

## What the printer rejects

The printer rejects these three items:

-   Object-valued interpolations
-   Strings that contain `}`
-   `<raw>` blocks

The platform save-time splitter treats the first `}` after a `${` as the end of an interpolation. This is why the printer rejects object-valued interpolations and strings that contain `}`. An admin can trigger the second condition by typing an ordinary label.

Stored DSL rejects `<raw>` blocks as a cross-site scripting risk. A region that contains a `<raw>` block is not editable.

## Unstored regions

Unstored regions are editable. Override rows exist only for regions that an admin has already overridden. A region that has never been modified has no row.

The renderer records the code-authored tree it walked. This gives the editor a starting point when no stored row exists. Under server-side rendering, this recording does nothing. This is correct because the editor runs client-side.

## The deprecated &lt;stack&gt; tag

The deprecated `<stack>` tag does not reach the editor. Both editor inputs go through the same parser. The parser rewrites every `<stack>` tag before validation runs. It converts each `<stack>` into a `row` that holds one full-width `column`. The parser drops all attributes on the `<stack>` tag and writes a named console warning for each one. The first time an admin saves a region that contained a `<stack>` tag, the stored text uses rows and columns.

**Related topics**  


[Editing and persisting layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/editing-and-persisting-layouts.md)

[Placing Lux widgets in regions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/placing-widgets-in-regions.md)

[layouts-and-editable-regions]

[Configurable properties for Lux experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configurable-properties.md)

[Configuration model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configuration-model.md)

