---
title: Create a contract type
description: As a contract configurator, create a contract type for defining different types of contract requests and associate it to a contract model.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Contract type]
breadcrumb: [Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
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
    ![Contract type form](../image/cmpro-contract-type-form.png "Contract template form")

3.  In the **Name** field, enter a unique name for the contract type.

4.  The **Description** field, enter a description for the contract type.

5.  Select **Active** to enable this contract type.

    Only active contract types are available for use in document templates, contract repository, and contract requests.

6.  Add contract model.

    1.  In the Contract Model embedded list, double-click **Insert a new row**.

    2.  Select Lookup using list icon\(![Lookup using list icon](../image/lsd-cont-rec-search.png)\).

        List of contract models is displayed.

    3.  Select the contract model that has not be mapped before to another contract type or create new one.

    **Note:** Map only one contract model to a contract type. An error will be displayed when try to save the contract type record after adding more than one contract model.

7.  Save the contract type.

    -   To save a new contract type, select **Submit**.
    -   To save the changes to an existing contract type, select **Update**.

## Result

The contract type is now available for selection in relevant configurations and when creating new contract requests.

