---
title: Define a question choice for a variable
description: Define a question choice for a variable with service catalog.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a service catalog variable, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Define a question choice for a variable

Define a question choice for a variable with service catalog.

## Before you begin

Role required: admin

## About this task

Some variable types present the user with a list of choices. For example, a multiple choice variable that asks how much memory you want in a computer requires you to define the available choices, such as 1 GB and 2 GB.

## Procedure

1.  Open the variable definition.

2.  In the **Question Choices** related list, click **New**.

3.  Enter the question choice details in **Question Choice** form and click **Submit** to save the record.

    -   **Price** and **Recurring price**: variables can affect the item [price](../concept/c_ServiceCatalogVariablePricing.md#) and recurring price \(if used\).
    -   **Order**: the number defining the order in which the price appears when displayed.
    -   **Question**: the actual question being asked for that variable.
    -   **Text**: the choice presented to the user.
    -   **Value**: the value stored in the database.
    -   **Inactive**: Option to make a question choice inactive.
4.  Repeat the steps for each available choice to define the full set of choices for that variable.

    **Note:** When you modify variable choices that are attached to a catalog item, the existing requested items \(RITMs\) are also affected. For example, if you add a variable choice for the catalog item, the value of that choice is also considered in the existing RITMs. If you delete a variable choice that is selected for a RITM, the value of that choice still persists in the RITM.


**Parent Topic:**[Create a service catalog variable](t_CreateAVariableForACatalogItem.md)

**Related topics**  


[Define help information for a service catalog variable](t_DefineHelpInformation.md)

[Service Catalog variable attributes](../reference/variable-attributes.md)

