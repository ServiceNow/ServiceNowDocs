---
title: Associate multiple fields to a blueprint
description: You can associate any number of fields to a blueprint by using the Blueprint Import function in the Matrix Loader.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-11-19"
reading_time_minutes: 1
breadcrumb: [Set up blueprints, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Associate multiple fields to a blueprint

You can associate any number of fields to a blueprint by using the Blueprint Import function in the Matrix Loader.

## Before you begin

Role required: Admin

## Procedure

1.  Create or edit a blueprint.yaml file and define the blueprint variable name and name in the following format \(removing the angle brackets around the variable names\).

    ```
    blueprints:
    -variableName: <variableNameOfBlueprint>
    	relatedFields:
    	-<fieldVariableName1>
    	-<fieldVariableName2>
    	-<fieldVariableName3>
    	-<etc...>
    name: <Name of Blueprint>
    ```

2.  Add the variable names of the desired fields.

3.  Import the YAML file into the Matrix Loader.

    Choose Blueprint as the upload type.

    **Note:** Any existing fields or configurable products in the blueprint will be disassociated from it unless they are also defined in the YAML file.


**Related topics**  


[Enable Markdown in text fields](enable-markdown-in-text-fields.md)

