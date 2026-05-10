---
title: CAL - Integer Stream action
description: Action that returns an array of integers in the specified range.
locale: en-US
release: australia
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloud Action Library reference, Cloud Action Library, ITOM Cloud Accelerate, IT Operations Management]
---

# CAL - Integer Stream action

Action that returns an array of integers in the specified range.

## Roles and availability

-   **Subscription requirements**

    To use this action in custom flows, you must obtain an Integration Hub Enterprise subscription or an App Engine subscription. For more information, see [Request Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/request-ih-overview.md).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/user-access-flow-designer.md).


## Cloud permission

You don't need any cloud permission to execute this action.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also select data pills using the pill picker.

-   **start**

    Data type: **Integer**

    An integer specifying at which position to start.

-   **end**

    Data type: **Integer**

    An integer specifying at which position to stop. The returned integer stream doesn't include the end integer.

-   **step**

    Data type: **Integer**

    An integer specifying the increment interval for the integer stream.


## Outputs

You can use these outputs as inputs for other actions.

-   **Integer Stream**

    Data type: **Array.Integer**

    An array of integers.


**Parent Topic:**[Cloud Action Library reference](cloud-action-library-reference.md)

