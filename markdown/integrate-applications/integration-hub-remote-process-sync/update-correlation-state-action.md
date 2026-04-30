---
title: Update Correlation State action
description: Enable or disable synchronization of records by the specified correlation. Set an active correlation to inactive to disable synchronization of records. Set an inactive correlation to active to resume synchronization of records.
locale: en-US
release: zurich
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Actions, Integration Hub Remote Process Sync, Workflow Data Fabric]
---

# Update Correlation State action

Enable or disable synchronization of records by the specified correlation. Set an active correlation to inactive to disable synchronization of records. Set an inactive correlation to active to resume synchronization of records.

## Roles and availability

Available as a ServiceNow Core Remote Process Sync action.

-   **Subscription requirements**

    This action requires an Integration Hub subscription. For more information, see [Request Integration Hub](../../flow-designer/concept/request-ih-overview.md) and [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Workflow Studio flows](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).


## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag pills from the Data panel or select them from the pill picker.

-   **Correlation Detail**

    Data type: **Object**

    Object containing correlation information about a synchronized record. The object identifies the local and remote correlation IDs associated with a local record.

-   **State**

    Data type: **Choice**

    Synchronization state of records. The available options are Active or Inactive. Active records are being synchronized. Inactive records are not synchronized.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Correlation Detail**

    Data type: **Object**

    Object containing correlation information about a record. The object identifies the local and remote correlation IDs associated with a local record.

-   **Status**

    Data type: **Choice**

    Synchronization state of records. The available options are Active or Inactive. Active records are being synchronized. Inactive records are not synchronized.

-   **Error**

    Data type: **String**

    Error returned by the action.


