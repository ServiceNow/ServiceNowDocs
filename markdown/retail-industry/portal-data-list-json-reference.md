---
title: Portal Data List widget JSON parameters
description: JSON parameters control what data categories appear on the Retail Org Details page in the Retail portal.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-31"
reading_time_minutes: 1
breadcrumb: [Add and configure the Retail KPI widget, Set up Retail Portal, Configure, Retail]
---

# Portal Data List widget JSON parameters

JSON parameters control what data categories appear on the Retail Org Details page in the Retail portal.

Each object in the Portal Data List widget JSON array defines one data category tile on the Retail Org Details page. Categories are rendered as cards and filtered at runtime to the viewing user's service organization.

**Note:** This information assumes that you are familiar with JSON format.

<table id="table_data_list_params"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Example value

</th></tr></thead><tbody><tr><td>

category

</td><td>

Display name for the data category tile as it appears to portal users.

</td><td>

`Store Equipment`

</td></tr><tr><td>

ID

</td><td>

Unique string identifier for this category within the JSON array. Must be unique across all entries.

</td><td>

`store_equipment`

</td></tr><tr><td>

table

</td><td>

API name of the ServiceNow table from which records are retrieved for this category.

</td><td>

`sn_install_base_item`

</td></tr><tr><td>

view

</td><td>

Name of the table view used to render the card fields. Use a view that has been configured for portal display.

</td><td>

`blsp`

</td></tr><tr><td>

card\_view\_primary\_column

</td><td>

Field name displayed as the primary \(title\) line on each card.

</td><td>

`number`

</td></tr><tr><td>

card\_view\_secondary\_column

</td><td>

Field name displayed as the secondary line on each card, below the primary column.

</td><td>

`name`

</td></tr><tr><td>

card\_view\_additional\_columns

</td><td>

Pipe-delimited list of additional field names shown on the card below the secondary column.

</td><td>

`location|state`

</td></tr><tr><td>

glyph

</td><td>

Icon name from the ServiceNow icon library displayed on the category tile.

</td><td>

`calculator`

</td></tr><tr><td>

target\_page\_id

</td><td>

Service Portal page ID to navigate to when a user selects a card. The record sys\_id is passed as a URL parameter.

</td><td>

`instance_detail`

</td></tr><tr><td>

run\_time\_filters

</td><td>

Array of filter objects applied at runtime to scope records to the user's service organization. Each object has two keys: -   **column**

The table field used for filtering \(for example, `service_organization`\).

-   **selection\_type**

The filter strategy. Use `current_org` to filter to the service organization of the portal user's current context.


</td><td>

```
[{"column":"service_organization","selection_type":"current_org"}]
```

</td></tr></tbody>
</table>