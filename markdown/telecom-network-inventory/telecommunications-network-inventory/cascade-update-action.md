---
title: Cascade Update function
description: The Cascade Update function enables you to update a configuration item \(CI\) attribute in the Telecommunications Network Inventory application and cascade the change in all related CIs. You can use this function to automatically cascade the field values in related CIs when you use Workflow Studio.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Telecommunications Network Inventory function catalog, Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# Cascade Update function

The Cascade Update function enables you to update a configuration item \(CI\) attribute in the Telecommunications Network Inventory application and cascade the change in all related CIs. You can use this function to automatically cascade the field values in related CIs when you use Workflow Studio.

You can use the Cascade Update function to update any field in the inventory record and cascade the changes all the way down to the hierarchy mentioned in the inventory record.

If there’s a conflict, such as any discrepancies found in the related CIs, this function returns an error. For example, let's say that you pass the change request and CI but the CI isn’t added to the affected CI list of the change request. Instead, it returns a sort error with the conflict information in execution.

**Note:** This function doesn’t work on **Life Cycle Stage** and **Life Cycle Status** fields.

You can use this function as a Workflow Studio action in the Telecommunications Network Inventory workflow.

## Roles and availability

Users with the admin role can add an action to a flow and define the configuration details of the flow. This function is available as a Workflow Studio action in the Telecommunications Network Inventory application so that you can perform inventory-related data operations.

## Input fields

The following table lists the input fields in the Cascade Update function and their descriptions.

|Field Name|Description|Data Type|Mandatory?|
|----------|-----------|---------|----------|
|Change Request|Change request that is related to the affected CI list.|Reference.Change Request|No|
|CI|CI where you want to update the field.|Reference.Configuration Item|No|
|Field|Attribute in the CI that you want to cascade.|String|No|

To learn more about the variable data types, see [Flow Designer input and output data variables](https://www.servicenow.com/docs/access?context=action-inputs-outputs&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

## Output

Use this function to update the CI attribute in all related CIs.

## Cascade rule for all common attributes of CI

The following table lists the information about the cascade rules for the different types of CIs.

|CI|Cascade Rule|Example|
|---|------------|-------|
|Telco Equipment|Attributes that are updated for the related equipment holder \(slot\), interface card, telco equipment holder \(subslot\), and network interface records.|The Type field that is updated in the equipment record cascades all the way down to the hierarchy mentioned in the inventory record.|
|Telco Equipment Holder|Attributes that are updated for the related interface card, telco equipment holder \(subslot\), and network interface records.|The Type field that is updated in the equipment record cascades all the way down to the hierarchy mentioned.|
|Interface Card|Attributes that are updated for the related telco equipment holder \(subslot\) and network interface records.|The Type field that is updated in the equipment record cascades all the way down to the hierarchy mentioned.|
|Network Interface|Attributes that are updated for the related network interface record.|The Port Bandwidth field that is updated in the equipment record cascades all the way down to the hierarchy mentioned in the inventory record.|
|Physical Connection|Attributes are updated for the related physical connection record.|The Bandwidth field that is updated in the equipment record cascades all the way down to the hierarchy mentioned in the inventory record.|
|Logical Connection|Attributes that are updated for all the next element CI records, which are defined in the connection element that reference the logical connection record.|The Bandwidth field that is updated in the equipment record cascades all the way down to the hierarchy mentioned in the inventory record.|

**Parent Topic:**[Telecommunications Network Inventory function catalog](tni-flow-action.md)

**Related topics**  


[Allocate Free Number function](allocate-free-number-action.md)

[Create CI From Template function](add-card-action.md)

[Create and Assign Range/Single Number function](create-assign-range-single-number-function.md)

[Create Logical Interface function](create-logical-interface-action.md)

[Create Logical Connection function](create-logical-connection-action.md)

[Create Physical Connection function](create-physical-connection-action.md)

[Create IP subnetwork function](create_ip_subnetwork.md)

[CIDR to IP range function](cidr_to_ip_range.md)

[Get Interface Summary function](get-interface-summary-action.md)

[Lookup Next Hub function](lookup-next-hub-action.md)

[Path Search function](path-compute-action.md)

