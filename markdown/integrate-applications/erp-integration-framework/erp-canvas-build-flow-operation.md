---
title: Building flows to read or update the ERP system
description: After you configure an operation in Zero Copy Connector for ERP \(Enterprise Resource Planning\), you can build a flow in Workflow Studio to specify details for querying the ERP system. For example, build a flow that filters by Order ID.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [erp, integration, canvas, data hub, zero, copy, connector, sap, build, flow]
breadcrumb: [Building with ERP data, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Building flows to read or update the ERP system

After you configure an operation in Zero Copy Connector for ERP \(Enterprise Resource Planning\), you can build a flow in Workflow Studio to specify details for querying the ERP system. For example, build a flow that filters by Order ID.

## Actions in Workflow Studio for calling the ERP system

The Use ERP Data action is automatically available in Workflow Studio after installing Zero Copy Connector for ERP.

The Use ERP Data action enables you to use ERP data outside of Zero Copy Connector for ERP for other processes. For example, you could create a task or an incident based on ERP data using the Use ERP Data action.

After you're done creating and managing your model in Zero Copy Connector for ERP, go to Workflow Studio and use the Use ERP Data action to test your model's inputs and outputs.

When you test the action, you must specify the model you're using, which fields to read or update, and the ERP system. For more information on the action, see [Use ERP Data action details for flows](../reference/erp-canvas-flow-reference-2.md).

## Using parameters to filter data requests

After you successfully test the Use ERP Data action, build a flow that uses that action to retrieve or update the specified data in the ERP system.

When you add the Use ERP Data action to a flow, you can specify any **Mandatory Field\(s\)** and **Optional Field\(s\)** defined as inputs when you managed the model. Required and optional fields must already be configured as required and optional input parameters.

If you select a field that was defined as a parameter for the system query, you can then enter a value to filter on. For example, if you build a flow using the Use ERP Data action and specify the SAP Stock Movement model, you can select **iseg\_fiscal\_year** as a required field. Then, enter a year to filter the data returned, for example `2023`.

## Process for building flows to retrieve ERP data

If you want to use ERP data for processes or tasks outside of Zero Copy Connector for ERP, use the following workflow:

1.  In Workflow Studio, test the **Use ERP Data** action by selecting the model in the **System** field of the Test Action modal and then specifying the inputs.
    -   For more information on testing actions, see Test an action.
    -   For more details on inputs for the action, see [Use ERP Data action details for flows](../reference/erp-canvas-flow-reference-2.md).
2.  After the test runs, view the action execution details. For more information, see Flow execution details.
3.  The returned data from testing the action appears in the **Response** field of the output data.
    -   For more information on outputs for the action, see [Use ERP Data action details for flows](../reference/erp-canvas-flow-reference-2.md).
    -   For details on incorporating returned ERP data, see [Specifying where ERP system data is saved](erpc-call-response-data.md).
4.  Build a flow that runs the Use ERP Data action.

    The **Use ERP Data** action returns ERP data in an output data pill called **Response**. The **Response** pill is available when you build a flow in Workflow Studio with the **Use ERP Data** action. The **Response** data pill is available in the following places of the action:

    -   The **Outputs** tab
    -   The **Output** section in the **Data** pane
    You can then add the **Response** data pill or any of the child **record** data pills to a flow to parse the returned JSON.

    For more information, see Building flows.


**Note:** Zero Copy Connector for ERP appears as **ERP Integration** when you work with it in Workflow Studio.

**Parent Topic:**[Building with ERP data](erp-canvas-building-with-erp-data.md)

