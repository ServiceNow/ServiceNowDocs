---
title: Quote transaction views
description: Views control how users with specific personas can view and modify fields and events at each stage of a quote in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-views.html
release: australia
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Quote transaction views

Views control how users with specific personas can view and modify fields and events at each stage of a quote in ServiceNow CPQ.

Views allow ServiceNow Quote Experience administrators to control how users with various personas can view and modify fields and events at various stages of a transaction. A persona can be assigned to only one view. The Views list page in the administration interface shows all configured views. Selecting a view's name displays its defined access privileges.

## Field access

The **Fields** tab in a view shows the field access privileges for that view. The leftmost column lists all field names at both transaction level and transaction line level. Stages appear in the top row, enabling per-stage access to be defined for each field. Use the **Filter** field to filter by field name or variable name, and use the adjacent menu to show all fields, transaction-level only, or transaction line-level only.

Field access values are:

-   Editable \(Read/Write\)
-   Read Only
-   No Access

Persona assignment is managed by selecting the pencil icon next to **Associated Personas**. A persona can only be assigned to one view.

**Note:** Field and event access values cannot be modified in the administration interface. They can only be modified by importing a `blueprints.zip` file containing updated CSV files.

## Event access

The **Events** tab shows the access privileges for each event in the blueprint. As with fields, event access is defined per stage. Event access values are Active or No Access.

## View configuration files

Views are created and modified using three files included in the `blueprints.zip` file.

-   **Fields CSV file**

    Defines the field access rights for each transaction-level and transaction line-level field at each stage. The file is located in the `blueprints/default/views` folder of the blueprint ZIP file. Modified values are entered without an asterisk \(\*\); original values include an asterisk.

-   **Events CSV file**

    Defines the event access rights for each transaction-level and line-level event at each stage. Located in the same `blueprints/default/views` folder. Modified values are entered without an asterisk.

-   **Views YAML file**

    Defines the view name, variable name, the variable names of any associated personas, and the locations of the field and event CSV files within the blueprint ZIP. If multiple views are defined, the information for each view is repeated in this file.


