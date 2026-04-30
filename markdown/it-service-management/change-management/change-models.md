---
title: Change models
description: Change managers can use the Change models feature to conveniently tailor change activities and flows for specific use cases.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Change Management, Change Management, IT Service Management]
---

# Change models

Change managers can use the Change models feature to conveniently tailor change activities and flows for specific use cases.

This feature is an extension to the existing IT Infrastructure Library \(ITIL\) OOB Change types and workflows. You can use it to transit to fit-for-purpose models and ServiceNow® Workflow Studio without compromising on existing capabilities.

Change models enable you to define:

-   Fit-for-purpose state models
-   State transitions
-   State transition conditions

By default, the following models are provided as examples for ITIL mode 1 and mode 2 processes. These models are available with the activation of the Change Management - Change Model Foundation Data \(com.snc.change\_management.change\_model.foundation\) plugin.

-   ITIL mode 1 - This is a traditional and sequential approach to process the Change Requests. This mode goes through a sequential process defined to complete a change successfully.
-   ITIL mode 2 - This is an adaptable approach to expedite the change request. This mode supports the right process for a give change to ensure a Change isn't a blocker to another change.

|Change model|Description|
|------------|-----------|
|Normal|Change model used for ITIL mode 1 Normal changes.|
|Emergency|Change model used for ITIL mode 1 Emergency changes.|
|Standard|Change model used for ITIL mode 1 Standard changes.|
|Change Registration|Change model used to capture change requests in an external system. There are no approvals associated with this model.|
|Cloud Infrastructure|Change model used for change requests that commission and decommission Cloud infrastructure services.|
|Site Reliability Ops|Change model used for site reliability operations.|
|Unauthorized Change|Change model used for change requests that are created from the unauthorized change events.|
|DevOps|Change model used for DevOps change requests. For more information, see [DevOps change models](../../enterprise-dev-ops/concept/devops-change-multimodel.md).|

-   **[Change Models properties](../reference/change-models-properties.md)**  
Configure the Change Models properties to access the Change models capabilities when creating a Change request.
-   **[Create a user criteria record for Change Management](../task/create-user-criteria.md)**  
Create a user criteria record to control user access to widgets.

**Parent Topic:**[Exploring Change Management](exploring-change-management.md)

