---
title: Create a transaction view
description: Create or modify a ServiceNow Quote Experience view by editing the fields CSV, events CSV, and views YAML files and importing them through the blueprint ZIP in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-configure-view.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Views, Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a transaction view

Create or modify a ServiceNow Quote Experience view by editing the fields CSV, events CSV, and views YAML files and importing them through the blueprint ZIP in ServiceNow CPQ.

## Before you begin

The personas to associate with the view must exist. For more information, see [Create a transaction persona](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-persona.md).

Access to the Matrix Loader for blueprint import is required.

Role required: admin

## About this task

View field and event access values cannot be modified in the ServiceNow Quote Experience administration interface. All changes are made by editing the CSV and YAML files in the blueprint ZIP and importing the updated file. ServiceNow Quote Experience provides a default view file set as a starting point for new views.

## Procedure

1.  Obtain a copy of the default view files from the `blueprints/default/views` folder of your existing blueprint ZIP.

2.  Edit the fields CSV file to set the access level for each field at each stage.

    Enter modified values without an asterisk \(\*\). Leave unmodified values with their asterisk. Access level values are Editable, Read Only, and No Access.

3.  Edit the events CSV file to set the access level for each event at each stage.

    Access level values for events are Active and No Access. Enter modified values without an asterisk.

4.  Edit the views YAML file to define the view name, variable name, the variable names of the personas assigned to the view, and the locations of the fields and events CSV files.

5.  Place the updated files in the `blueprints/default/views` folder of the blueprint ZIP file.

6.  Import the updated blueprint ZIP file using the Matrix Loader.

7.  Deploy the blueprint to apply the view changes.

    The updated view takes effect when the blueprint deployment completes.


