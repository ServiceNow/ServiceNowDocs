---
title: Transaction Manager: Views
description: Understand how to define access rules to fields and events according to the user persona.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-10"
reading_time_minutes: 4
breadcrumb: [Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Views

Understand how to define access rules to fields and events according to the user persona.

Views allow Transaction Manager administrators to define access rules for fields and events for different personas at various stages of the transaction life cycle.

Views, personas, and stages work together to allow the admin to control who can access various transaction level and transaction line level fields and events within the transaction at any point in the sales process.

Views can be used to control field access \(Read/Write vs. Read-Only\) and event access \(Active vs. No Access\) at various stages of the transaction process for various personas the you have defined in your sales organization.

To work with views, click the **Views** option in the Admin menu to the left side of the Admin UI. The Views List page will show you the views the you have configured for your transaction environment. Clicking a view’s name in the list will display the access privileges defined in the view.

![Transaction Manager: Views](../images/cpq-txn-mgr-views.jpeg)

## Field access

When you click a view name in the Views List page, the view’s defined field and event access privileges are shown.

The view and its access privileges are displayed in a table. Clicking **Fields** in the top left corner of the table will display the field access privileges defined for the view. The leftmost column in the table will display all of the field names, both transaction level and transaction line level.

Using the Filter field below the fields tab lets you filter the display by field name or variable name. A menu to the right of the Filter field allows you to show all the fields, only transaction level fields, or only transaction line level fields.

The stages are displayed in the top row of the table starting in second column from the left. This allows you to define the field access for each field in each stage of your sales process for the personas assigned to the view.

In the top right of the fields display is the Associated Personas list. Clicking the pencil icon lets you choose the personas assigned to this view. A menu displaying all the personas is shown. A persona can only be assigned to one view.

The values on the display cannot be modified in the Admin UI. They can only be modified in the Blueprints.zip file via CSV file import.

![Transaction Manager: Views](../images/cpq-txn-mgr-views-fields.jpeg)

## Events access

Clicking the Events tab on the view page allows shows the access privileges defined for each event in the Transaction Manager Blueprint.

As with the fields display, these values cannot be modified in the Admin UI. They can only be modified via CSV file import.

![Transaction Manager: Views](../images/cpq-txn-mgr-views-events.jpeg)

## Creating views

To create a new view or modify an existing view, you use CSV and YAML files.

-   The Fields CSV file defines the field access for a persona or set of personas for each stage in the sales process.
-   The Events CSV file defines the event access for a persona or set of personas for each stage in the sales process.
-   The views.yaml file defines the name of the view being added or modified and the location of the two CSV files.

By default, Transaction Manager provides a copy of each of these files for the default view. To create new views, you can use the default view files, modify them, and save them under new file names. Including the new files in the Blueprint.zip file allows you to import the new views into your Transaction Manager Blueprint.

## Fields CSV file

The fields CSV file contains the field access rights to each field in each stage.

-   Transaction level fields
-   Transaction line level fields

For each field, you can define the following access levels:

-   Editable \(Read/Write\)
-   Read Only
-   No Access

In the blueprint.zip file, the file should be located in the following folder hierarchy: `blueprints/default/views`

When you modify a view field file, modified values are entered without the asterisk \(\*\).

Original fields CSV file:

![CSV file](../images/cpq-txn-mgr-views-fields-original.jpeg)

Modified fields CSV file:

![CSV file](../images/cpq-txn-mgr-views-fields-modified.jpeg)

## events CSV file

The events CSV file contains the event access rights to each event in each stage.

-   Transaction level events
-   transaction line level events

For each field, you can define the following access levels:

-   Active
-   No Access

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
-   The location of the field and event CSV files in the Blueprint.zip file

If you have multiple views defined for your Transaction Manager Blueprint, this information will be repeated for each defined view in your Blueprint.

![Yaml file](../images/cpq-txn-mgr-views-yaml.jpeg)

Once all three files are modified, they can be placed in the views folder of the blueprints.zip file and imported into Transaction Manager via the Matrix Loader. Assuming that there are no issues with any of the files, changes to any views will take effect when the Blueprint is deployed.

