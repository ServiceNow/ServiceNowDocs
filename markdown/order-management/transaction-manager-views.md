---
title: Transaction Manager: Views
description: Understand how to set rules for access to fields and events according to user persona.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Transaction Manager, CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Views

Understand how to set rules for access to fields and events according to user persona.

Views allow Transaction Manager admins to control how users with various personas can view and modify fields and events at various stages of a transaction.

To work with views, click **Views** in the Admin menu. The views list page shows the views you have configured for your transaction environment. Clicking a view’s name in the list displays the access privileges defined in the view.

![Transaction Manager: Views](../images/cpq-txn-mgr-views.jpeg)

## Field access

When you click a view name, the view’s field and event access privileges are shown in a table.

Clicking **Fields** in the top left corner shows the field access privileges defined for the view. The leftmost column in the table displays all of the field names, both transaction level and transaction line level.

Using the **Filter** field lets you filter the display by field name or variable name. An adjacent menu lets you decide whether you want to see all the fields, only transaction level fields, or only transaction line level fields.

The stages appear in the top row of the table. This helps you define the access to each field in each stage of your sales process for the personas assigned to the view.

Clicking the pencil icon for **Associated Personas** lets you choose the personas assigned to the view. A menu shows all the personas. A persona can only be assigned to one view.

The values in the display cannot be modified in the Admin UI. They can be modified only by importing a blueprints.zip file in CSV format.

![Transaction Manager: Views](../images/cpq-txn-mgr-views-fields.jpeg)

## Events access

The **Events** tab shows the access privileges defined for each event in the Transaction Manager blueprint.

As with the fields display, these values cannot be modified in the Admin UI. They can only be modified via CSV file import.

![Transaction Manager: Views](../images/cpq-txn-mgr-views-events.jpeg)

## Creating views

To create a new view or modify an existing view, use CSV and YAML files.

-   The Fields CSV file defines the field access for a persona or set of personas at each stage.
-   The Events CSV file defines the event access for a persona or set of personas at each stage.
-   The views.yaml file defines the name of the view being added or modified and the location of the two CSV files.

By default, Transaction Manager provides a copy of each of these files for the default view. To create new views, you can use the default view files, modify them, and save them under new file names. Including the new files in the blueprint.zip file eanbles you to import the new views into your Transaction Manager blueprint.

## Fields CSV file

The fields CSV file contains the field access rights to each transaction-level and transaction line-level field in each stage. For each field, you can define one of the following access levels:

-   Editable \(Read/Write\)
-   Read Only
-   No Access

In the blueprint.zip file, the file should be located in the following folder hierarchy: `blueprints/default/views`

When you modify a view field file, modified values are entered without the asterisk \(\*\).

Original fields CSV file:

![CSV file](../images/cpq-txn-mgr-views-fields-original.jpeg)

Modified fields CSV file:

![CSV file](../images/cpq-txn-mgr-views-fields-modified.jpeg)

## Events CSV file

The events CSV file contains the event access rights to each transaction-level and transaction line-level event in each stage.

Each field can be defined as Active or No Access.

In the blueprint.zip file, the file should be located in the following folder hierarchy: `blueprints/default/views`

When you modify a view event file, modified values are entered without the asterisk \(\*\).

Original events CSV file:

![CSV file](../images/cpq-txn-mgr-views-events-original.jpeg)

Modified events CSV file:

![CSV file](../images/cpq-txn-mgr-views-events-modified.jpeg)

## YAML file

The views YAML file defines the view. Information in the views YAML file includes:

-   The name and variable name of the view
-   The variable name of any personas assigned to the view
-   The location of the field and event CSV files in the blueprint.zip file

If you have multiple views defined for your Transaction Manager blueprint, this information is repeated for each defined view in your blueprint.

![Yaml file](../images/cpq-txn-mgr-views-yaml.jpeg)

When all three files have been modified, they can be placed in the views folder of the blueprints.zip file and imported into Transaction Manager via the Matrix Loader. Assuming that there are no issues with any of the files, changes to any views take effect when the blueprint is deployed.

**Related topics**  


[Transaction Manager: Personas](transaction-manager-personas.md)

[Transaction Manager: Stages](transaction-manager-stages.md)

[Transaction Manager: Events](transaction-manager-events.md)

[Transaction Manager: Rules and rule groupings](transaction-manager-rules-and-rule-groupings.md)

