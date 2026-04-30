---
title: Blueprint, configurable product, and field UI
description: View a list of updates and changes made in April 202\(3\)
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 4
breadcrumb: [ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Blueprint, configurable product, and field UI

View a list of updates and changes made in April 202\(3\)

Improvements in Admin usability and readability. No changes in functionality.

Revamped field, configurable product, and blueprint UIs.

Improved navigation. Breadcrumb links are used more extensively in the UI and dialogs.

Enhanced field association experience from the Blueprint page.

Field and set pages are consolidated into a single view.

Support for creating sets in the New Field dialog.

## Updated blueprint UI

The relationship between the ServiceNow CPQ items and the blueprint can now be easily accessed via the tiles in the left column and the number of associated items is visible at a glance.

Each tile displays the appropriate UI for its object on the right of the screen.

![Blueprint screen](../images/cpq-2023-release-notes-1.png)

\(1\) Edit: The blueprint variable name is displayed in parentheses. The blueprint name and description can be edited by clicking the pencil icon.

\(2\) Associated Fields: Fields for blueprint use the updated field UI with grouping.

\(3\) Related Rules: Rules that are related to the blueprint.

\(4\) Layouts: Layouts for this blueprint.

\(5\) Configurable Product: Configurable products that use this blueprint.

\(6\) Enrichments: The enrichment scripts for the blueprint.

\(7\) Associate Fields: Opens field association for the blueprint.

## Updated navigation

In the updated UI for blueprints and configurable products, the navigation and editing experience has changed. When clicking a field or a rule, an editing page slides into the page instead of a dialog appearing. Additionally, there are now breadcrumbs for navigation and context.

![Navigation screen](../images/cpq-2023-release-notes-2.png)

\(1\) Navigation breadcrumb: Breadcrumb links are placed on the header to help maintain context and provide navigation.

\(2\) Edit page: The editing page replaces the table view of items in context, instead of the dialog view used previously.

\(3\) Relationship links: Maintaining consistency with editing a field through the main fields tab, the page layout and relationship links are shown.

## Updated field association in blueprints

Field association to blueprints has also received a makeover. From the blueprint UI, with the Associated Fields tile selected, click the **Associate Fields** button to launch the new panel experience.

![Updated field Association in blueprints](../images/cpq-2023-release-notes-3.png)

\(1\) Filter Categories: Fields can be filtered to “Standard” or “Sets” using the drop-down menu. The filter applies to both the results list and the selected list.

\(2\) Search: Fields can be searched and filtered using the search bar.

\(3\) Results: Field results appear on the left. Fields can be added by clicking the **+** icon. Selecting a field removes it from the results column and add it to the selected column.

\(4\) Selected: Selected fields and their details are displayed on the right. Click the check mark icon removes the field from the selected list.

\(5\) Actions: Two actions are available at the bottom of the panel, Cancel and Done. To save the changes and associate the fields to the blueprint, click Done. To close the panel without adding any fields, click Cancel. The panel can also be closed without adding fields by clicking the arrow at the top left of the panel \(6\).

Depending on the size of the browser window, you may see a stacked view of the Results \(1, below\) and Selected \(2\) field lists. The functionality remains the same.

![Associate additional fields](../images/cpq-2023-release-notes-4.png)

## Updated configurable product UI

The configurable product UI has also received an update, to align with the blueprint UI and utilize the updated field UI.

![Updated configurable product UI](../images/cpq-2023-release-notes-5.png)

Similar to the blueprint UI, tiles on the left control what is displayed on the right.

\(1\) Associated Fields: fields for configurable product.

\(2\) Related Rules: Rules that are related to the configurable product.

\(3\) Layouts: Layouts for this configurable product.

\(4\) Hyperjump: Launches Hyperjump for this configurable product.

5. UI Content: Displays content from whichever tile is currently selected.

## Updated field UI

The updated field UI provides a unified view of fields and sets and is also used in the update blueprint and configurable products UI.

![Updated field UI](../images/cpq-2023-release-notes-6.png)

Fields are now grouped into three types: Standard, Sets, and System. By default the “Standard” section is open.

\(1\) Standard section: Displays standard field types \(Text, Number, Picklist, Boolean\)

\(2\) Sets section: Displays all Sets \(See more below\)

\(3\) System section: Displays system fields.

\(4\) Open/Close section: Each section can be expanded using the arrow icon to the left of the grouping name. Only one section is open at a time.

With the inclusion of sets in the field UI, the display of sets has also been updated.

![Updated field UI](../images/cpq-2023-release-notes-7.png)

\(1\) Set grouping section: an expanded view of all sets.

\(2\) Individual sets can be expanded or collapsed in the table using the arrow icon on the left. By default, the view is expanded. Multiple sets can be expanded at once.

\(3\) When a set is expanded, the fields and details are also displayed.

The New Field window provides a unified way to create both standard field types and sets.

![Updated field UI](../images/cpq-2023-release-notes-8.png)

Field types can be selected by either picking the appropriate tile or by using the arrows to scroll through the display examples.

\(1\) Sets are available in addition to the four standard field types.

\(2\) Each field type has a display example showing different ways that the field can appear on a layout. The example is not exhaustive.

