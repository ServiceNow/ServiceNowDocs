---
title: Transform Payload from Inbound Sample action
description: Transform a Remote Process Sync payload from a JSON string to a complex object. Generate the object structure from a sample of the inbound payload.
locale: en-US
release: australia
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Actions, Integration Hub Remote Process Sync, Workflow Data Fabric]
---

# Transform Payload from Inbound Sample action

Transform a Remote Process Sync payload from a JSON string to a complex object. Generate the object structure from a sample of the inbound payload.

## Roles and availability

Available as a ServiceNow Core Remote Process Sync action.

-   **Subscription requirements**

    This action requires an Integration Hub subscription. For more information, see [Request Integration Hub](../../flow-designer/concept/request-ih-overview.md) and [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see User access to Workflow Studio flows.


## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag pills from the Data panel or select them from the pill picker.

-   **Payload**

    Data type: **String**

    JSON string containing changes generated on a remote instance. For example, a list of field changes for a case record from a remote instance. The system transforms this JSON string to an object on the local instance.

-   **Sample Payload**

    Data type: **String**

    Portion of a JSON payload you want to use to generate an object structure. Select the elements of the JSON structure you want to map to elements of an object structure.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Capture Metadata**

    Data type: **Object**

    Object containing information about the capture definition that created the payload.

-   **Changed Fields**

    Data type: **Dynamic Object**

    Object containing information about the field value changes. The system uses these changes to synchronize correlation and local records.

-   **Attachment Metadata**

    Data type: **Array of Object**

    Array containing information about the attachments to synchronize.

-   **Error Message**

    Data type: **String**

    Error returned by the action.


