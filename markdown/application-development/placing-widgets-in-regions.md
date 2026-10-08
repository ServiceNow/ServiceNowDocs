---
title: Placing Lux widgets in regions
description: A seam is a placement point in a region, the edge of a widget or the gap between two widgets. Use seams to add widgets from the toolbox and configure widgets placed inside a region.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/placing-widgets-in-regions.html
release: zurich
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 6
keywords: [Placing widgets in regions, Seams and widget placement, Adding a widget from the toolbox, Configuring a widget inside a region, One surface per element, Related]
breadcrumb: [Layout configuration, Configure experiences, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Placing Lux widgets in regions

A seam is a placement point in a region, the edge of a widget or the gap between two widgets. Use seams to add widgets from the toolbox and configure widgets placed inside a region.

## Seams and widget placement

A seam is a placement point in a region, the edge of a widget or the gap between two widgets. It is not an address. An administrator points at a widget, not at the container around it. Both the `+` affordances and drag-and-drop resolve through the same function, so the two gestures produce the same structure for the same intent.

A widget's top and bottom edges insert directly into the column the widget is already in. No container is created, and the widget stays mounted. A widget's side edges behave differently depending on whether the widget shares its column:

|The pointed-at widget|The placement|Why|
|---------------------|-------------|---|
|Alone in its column|A new cell of the enclosing row, on that side|The cell is the widget, so "beside this" and "beside this cell" are the same request — and the flat shape says it with one fewer invisible container. It costs the row's width rather than a nesting level, so it works at the depth cap where a wrap can't.|
|Sharing its column|The widget's own slot is wrapped in a nested row of two even cells|Adding a cell to the row would move the widget's stacked siblings too, which is not what pointing at one of them means. The stack stays; the row appears between the two widgets it was already between.|

A container boundary is the gap between two siblings, or an empty box. It resolves to whatever chain the grammar needs, outside in. A region's top level takes rows only, so a widget dropped there gets a row and a column. A row takes columns only, so a widget dropped between two cells gets one column. A column takes widgets, so nothing is synthesized.

Where corridors overlap, an interior seam, one sitting in a real gap between two siblings, wins over an end seam sitting on its container's own edge. Only then does the deepest win. Depth alone was wrong in exactly the case the gutters are for. A full-height column's own bottom edge is also its row's bottom edge, so aiming at the gap between two bands appended to the preceding band instead.

## Adding a widget from the toolbox

The toolbox is a panel anchored to the specific `+` that was pressed. One search runs per term and three tabs narrow its result client-side, so switching tabs is not a network round trip for an answer already in memory.

|Tab|What it shows|Ordering|
|---|-------------|--------|
|**All widgets**|The search result verbatim|Name, A-Z or Z-A|
|**Recents**|The intersection with a stored tag list|Recency; the name sort is inactive|
|**My widgets**|Widgets whose scope row is an application built on this instance|Name, A-Z or Z-A|

**My widgets** can't be answered from the scope name. An app authored on the instance and one installed from the ServiceNow Store are both prefixed the same way. The question is which table the scope row sits on.

**Recents** lives in the browser's local storage, holds the most recent twelve, and writes on the pick rather than on Apply or Save. Re-adding a widget already in the list moves it to the front. The stored value validates on read rather than trusted, and a remembered tag with no row in the current catalog drops. So a stale entry can't offer a widget that no longer exists.

A thumbtack keeps the panel open after an add, advancing the insertion point so successive picks stack in order. It is skipped when the placement needed a container to be built. Subdividing or wrapping restructures the tree, and every path the plan named can be stale the instant it is applied.

## Configuring a widget inside a region

A region controls a widget's layout, not its properties.

Configuration is an override of a property, so there is one system, and `aiux-config-id` is what opts a widget into it. The attribute compiles to exactly the binding a hand-written `elementId(host, 'id')` produces, and that stamps `data-aiux-element-id` on the rendered element. A region widget carrying one is therefore an ordinary configuration entry. It is found by the same DOM scan, stored in `sys_aix_configuration` under `<id>.<prop>`, read back by the same `@config` getter, and reset by the same call. See [Configurable properties for Lux experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/configurable-properties.md) for the attribute itself.

Four consequences follow:

-   A widget without an `aiux-config-id` has no address, so keys cannot be saved or retrieved. Its surface shows a chevron instead of a split button.
-   Every widget the editor adds gets one, deterministically. New nodes are stamped `<tag>__<nonce>`, using the lowest unused nonce across the region. Colliding IDs would give two widgets the same configuration address, so the rule avoids all existing IDs, not just those of the same tag. IDs the region arrived with are never changed; renumbering one would orphan its stored configuration.
-   Widget and region configuration are always available together, and neither is exclusive to a mode. The widget's pencil opens its properties pane, while the region's tab and canvas are its own controls. These are distinct affordances, so suppressing the widget's pencil inside a region would override the author's intent.
-   Property overrides are staged on the page component's resolved configuration payload and applied on the next render. No layout remounts between keystrokes, and the region's template shape is unchanged, so only the affected attribute updates.

## One surface per element

Two layers can draw a box over the same element, and each answers a question the other can't. The outline layer draws per configuration entry; the region canvas draws per node of a loaded region. A region widget carrying `aiux-config-id` is both, and used to wear both. Each element now gets exactly one surface:

|The element|Deep links|Pencil|Chevron|Resize brackets|Dashed outline|Drawn by|
|-----------|----------|------|-------|---------------|--------------|--------|
|Widget in a loaded region, with an `aiux-config-id`|One per link|Yes|Yes|Yes|No|Canvas|
|Widget in a loaded region, without one|One per link|No|Yes|Yes|No|Canvas|
|Widget outside any region|One per link|Yes|No|No|Yes|Overlay|
|Configurable element inside a region widget|One per link|Yes|No|No|Yes|Overlay|
|The region wrapper|—|—|Its tab's gear|No|Yes|Canvas box plus overlay tab|

The canvas owns the widget's surface because it is the only layer that handles layout edits and resize. Both operations are addressed by node path. A region widget without an `aiux-config-id` has a path but no configuration entry.

External configuration deep links appear on whichever surface the widget has. A widget whose configuration lives in a platform tool returns one or more label-and-URL pairs. Each pair renders as a leading button on the same control as the pencil: labeled on an outline box corner, icon-only on the canvas toolbar. A deep link does not require an `aiux-config-id` because it is a URL into another tool, not a stored override. A region widget with a deep link and no `aiux-config-id` displays the link and the chevron.

The region wrapper tab displays the word `Region`, not the region's name. The name identifies a slot in a template for authors. Administrators cannot place or act on it. Displaying the name caused the tab to read as a label for the content inside the box rather than a description of the box itself. Administrators need to know the kind, not the name. The name remains the tab's accessible name and the heading the gear menu opens with, where **Restore defaults** must identify which region it restores.

