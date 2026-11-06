---
title: Use ERP Data action details for flows
description: After you're done creating and managing your model in Zero Copy Connector for ERP, go to Workflow Studio and use the Use ERP Data action to test your model's inputs and outputs. You can then build a flow with the action to incorporate ERP data into the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/erp-integration-framework/erp-canvas-flow-reference-2.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-08-06"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, flow, reference]
breadcrumb: [Troubleshooting, Using, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Use ERP Data action details for flows

After you're done creating and managing your model in Zero Copy Connector for ERP, go to Workflow Studio and use the Use ERP Data action to test your model's inputs and outputs. You can then build a flow with the action to incorporate ERP data into the ServiceNow AI Platform.

For information on using the Use ERP Data action to retrieve ERP data, see [Building flows with the Zero Copy Connector for ERP Use ERP Data action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-canvas-build-flow-operation.md).

## Roles and availability

Available as part of Zero Copy Connector for ERP.

-   **Role requirements**

    Workflow Studio roles are required to run actions in test mode. Having a delegated developer role and the erp\_admin role is not enough to test.

    For example, you may need delegated\_developer, erp\_admin, flow\_designer, flow\_admin, and flow\_operator to test your model's inputs and outputs with the User ERP Data action.

    For more information, see [User access to Workflow Studio flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/user-access-flow-designer.md) and [Delegated development and deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_DelegatedDevelopment.md).


## Inputs

Provide a value for each input that your action requires. To add dynamic values, you can also select data pills using the pill picker.

-   **ModelName**

    Data type: **Dynamic Choice**

    Name of the ERP model that contains the read or update operation. The model must already be created and have the read or update operation defined in Zero Copy Connector for ERP. For more information, see [Exploring Zero Copy Connector for ERP models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/exploring-erp-models.md).

-   **ModelOperation**

    Data type: **Dynamic Choice**

    Whether to **Read** or **Update** the ERP system. The read or update entity must already be defined in Zero Copy Connector for ERP. For more information, see [Adding an entity to a Zero Copy Connector for ERP model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/add-an-entity-to-model.md).

-   **Required Fields**

    Data type: **Dynamic Template**

    Fields that are required for the operation. Fields must already be defined as required input parameters when you manage the model in Zero Copy Connector for ERP. For more information, see [Manage input parameters for a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erpc-manage-model-inputs.md).

-   **Optional Fields**

    Data type: **Dynamic Template**

    Fields that are optional for the operation. Fields must already be defined as optional input parameters when you manage the model. For more information, see [Manage input parameters for a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erpc-manage-model-inputs.md).

-   **System**

    Data type: **Reference**

    Name of the connected ERP system. For more information, see [Working with ERP systems in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-canvas-work-with-systems.md).


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

    Requested data that's returned from the ERP system. For more information, see [Choose output parameters for a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-canvas-manage-outputs.md).


