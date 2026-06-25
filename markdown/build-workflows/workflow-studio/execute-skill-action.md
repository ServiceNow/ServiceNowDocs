---
title: Execute Skill action
description: Run a published Now Assist skill and use the skill outputs in a flow or subflow.For existing actions and subflows, copy the short description from the product documentation, or insert a content reference to it. For new actions and subflows, create reusable content and insert a content reference to the short description.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/execute-skill-action.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Actions, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Execute Skill action

Run a published Now Assist skill and use the skill outputs in a flow or subflow.

## Roles and availability

Available as a Now Assist Skill Kit action.

-   **Subscription requirements**

    This action requires activiating the Now Assist Skill Kit plugin from the Now Assist panel. For more information, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Workflow Studio flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/user-access-flow-designer.md).


## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag pills from the Data panel or select them from the pill picker.

-   **Workflow**

    Data type: **Dynamic Choice**

    The Workflow deployment setting that the Now Assist skill uses. For more information on skill deployment settings, see .

-   **Product**

    Data type: **Dynamic Choice**

    The Product deployment setting that the Now Assist skill uses. For more information on skill deployment settings, see .

-   **Feature**

    Data type: **Dynamic Choice**

    The Feature deployment setting that the Now Assist skill uses. For more information on skill deployment settings, see .

-   **Skill Config**

    Data type: **Dynamic Choice**

    The name of the Now Assist skill that you want the action to run. For more information on skill configurations, see .

-   **Skill Inputs**

    Data type: **Dynamic Inputs**

    The list of inputs that the Now Assist skill uses. For more information on skill inputs, see .


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Output**

    Data type: **Dynamic Object**

    The response provided by the Now Assist skill as a JSON-formatted object.


**Parent Topic:**[Workflow Studio actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-actions.md)

