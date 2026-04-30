---
title: Create a contract type
description: As a contract configurator, create a contract type for defining different types of contract requests and associate it to a contract model.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Create a contract type

As a contract configurator, create a contract type for defining different types of contract requests and associate it to a contract model.

## Before you begin

Ensure that the application is in Global scope.

Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contracts Administration** &gt; **Contract Types**.

2.  Create or modify a contract type.

    -   To create a contract type, select **New**.
    -   To modify an existing contract type, open the contract type from the list.
3.  In the **Name** field, enter a unique name for the contract type.

4.  The **Description** field, enter a description for the contract type.

5.  Select **Active** to enable this contract type.

    Only active contract types are available for use in document templates, contract repository, and contract requests.

6.  Add contract model.

    1.  In the Contract Model embedded list, double-click **Insert a new row**.

    2.  Select Lookup using list icon\(![Lookup using list icon](../image/lsd-cont-rec-search.png)\).

        List of contract models is displayed.

    3.  Select the contract model from the list or create new one.

    **Note:** Map only one contract model to a contract type. An error will be displayed when try to save the contract type record after adding more than one contract model.

7.  Save the contract type.

    -   To save a new contract type, select **Submit**.
    -   To save the changes to an existing contract type, select **Update**.

