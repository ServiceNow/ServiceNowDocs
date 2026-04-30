---
title: Use ERP Data action details for flows
description: After you're done creating and managing your model in Zero Copy Connector for ERP, go to Workflow Studio and use the Use ERP Data action to test your model's inputs and outputs. You can then build a flow with the action to incorporate ERP \(Enterprise Resource Planning\) data into the ServiceNow AI Platform.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, flow, reference]
breadcrumb: [Reference, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Use ERP Data action details for flows

After you're done creating and managing your model in Zero Copy Connector for ERP, go to Workflow Studio and use the Use ERP Data action to test your model's inputs and outputs. You can then build a flow with the action to incorporate ERP \(Enterprise Resource Planning\) data into the ServiceNow AI Platform.

For information on using the Use ERP Data action to retrieve ERP data, see [Building flows to read or update the ERP system](../concept/erp-canvas-build-flow-operation.md).

## Roles and availability

Available as part of Zero Copy Connector for ERP.

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Workflow Studio flows](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).


## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also select data pills using the pill picker.

-   **ModelName**

    Data type: **Dynamic Choice**

    Name of the ERP model that contains the read or update operation. The model must already be created, and have the read or update operation defined in Zero Copy Connector for ERP. For more information, see [Managing how models read and update the ERP system](../concept/erpc-managing-models-read.md).

-   **ModelOperation**

    Data type: **Dynamic Choice**

    Whether to **Read** or **Update** the ERP system. The read or update entity must already be defined in Zero Copy Connector for ERP. For more information, see [Add an entity to a model](../concept/add-an-entity-to-model.md).

-   **Required Fields**

    Data type: **Dynamic Template**

    Fields that are required for the operation. Fields must already be defined as required input parameters when you manage the model in Zero Copy Connector for ERP. For more information, see [Manage input parameters for a Zero Copy Connector for ERP model operation](../task/erpc-manage-model-inputs.md).

-   **Optional Fields**

    Data type: **Dynamic Template**

    Fields that are optional for the operation. Fields must already be defined as optional input parameters when you managed the model. For more information, see [Manage input parameters for a Zero Copy Connector for ERP model operation](../task/erpc-manage-model-inputs.md).

-   **System**

    Data type: **Reference**

    Name of the connected ERP system. For more information, see [Working with ERP systems in Zero Copy Connector for ERP](../concept/erp-canvas-work-with-systems.md).


## Outputs

You can use these outputs as inputs for other items.

-   **Action status**

    Data type: **Object**

    Data pill that contains the current runtime details about the action. The **Action Status** object consists of a code and a message.

-   **Don't Treat As Error**

    Data type: **True/False**

    Option to report the Action Status as an error or a success when returned to a flow.

-   **Error Message**

    Data type: **String**

    String data pill containing the error message produced by the action, step, or system operation.

-   **Response**

    Data type: **Dynamic Object**

    Requested data that's returned from the ERP system. For more information, see [Choose output parameters for a model](../task/erp-canvas-manage-outputs.md).


**Parent Topic:**[Zero Copy Connector for ERP reference](erp-integration-reference.md)

