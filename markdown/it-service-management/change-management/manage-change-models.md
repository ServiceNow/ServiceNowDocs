---
title: Change model management
description: Change models help streamline change requests by tailoring a fit-for-purpose process to support specific, common change use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/change-management/manage-change-models.html
release: zurich
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-04-09"
reading_time_minutes: 3
breadcrumb: [Explore, Change Management, IT Service Management]
---

# Change model management

Change models help streamline change requests by tailoring a fit-for-purpose process to support specific, common change use cases.

Change models define the process for managing specific change use cases. A model-based approach simplifies change implementation and improves change governance. Change models help record only the data needed for the specific change use case more efficiently and then use this data for risk evaluation and change approval decisions.

Change models are defined using several elements such as change states, change state transitions, approval policies, and change templates. These elements are managed as individual records and can be reused across different models. For more information, see .

By default, the following models are provided as examples for ITIL mode 1 and mode 2 processes.

-   ITIL mode 1- This is a traditional and sequential approach to process the Change Requests. This mode goes through a sequential process defined to complete a change successfully.
-   ITIL mode 2- This is an adaptable approach to expedite the change request. This mode supports the right process for a given change to verify that it isn't a blocker for another change being processed.

Change models have been categorized based on IT Infrastructure Library \(ITIL\) Change types and federated change types. The following types of change models are based on the ITIL change types:

-   Normal: Used for ITIL mode 1 Normal changes.
-   Standard: Used for ITIL mode 1 Standard changes where some of the change states and approvals are pre-approved by default.
-   Emergency: Used for ITIL mode 1 Emergency changes that need quicker resolution.

The following change models are based on the federated change types that combines multiple states tailored to the purpose and management of specific change use cases:

-   DevOps: Change model used for DevOps change requests. For more information, see [DevOps change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/devops-change-multimodel.md).
-   Cloud Infrastructure: Used for change requests that commission and decommission Cloud infrastructure services.
-   Unauthorized: Used for change requests that are created from the unauthorized change events.
-   App: Change model used for application based change requests that skip the assessment state.
-   Low Risk: Change model used for low risk based changes.
-   Patching: Change model used for low risk defect and patching related changes.

Change models can be tailored to address specific use cases and role-based access is configured to maintain compliance and mitigate risks. Change models can be made available while creating new change requests and standard information for specific fields can be configured to be displayed when a new change request is created using the model.

Define fields that are displayed for change requests created using the change model. For more information, see [Create a Change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/create-a-change-model.md).

Change models can be configured so that each change can go through a series of states based on the use case. For example, a normal change would go through all major assessment and approval states, while an emergency change would skip some states for emergency handling and quicker resolution.

Configure change model states and transition processes for the newly created change models. For more information, see .

After creating a change model, you can create a change template for the model to pre-populate data and make the change creation process faster and more consistent. You can configure parent and child categories for templates and manage their proposal, creation and approval process. For more information, see .

-   **[Change Models properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/change-models-properties.md)**  
Configure the Change Models properties to access the Change models capabilities when creating a Change request.
-   **[Create a user criteria record for Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/create-user-criteria.md)**  
Create a user criteria record to control user access to widgets.

**Parent Topic:**[Exploring Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/change-management/exploring-change-management.md)

