---
title: Get Attachment Metadata for Local Record action
description: Get the list of attachments associated with a specified local record. Use the output of this action to synchronize the attachments of a local record with the attachments of a remote record.
locale: en-US
release: yokohama
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Remote Process Sync actions, Integration Hub Remote Process Sync, Data and Automation]
---

# Get Attachment Metadata for Local Record action

Get the list of attachments associated with a specified local record. Use the output of this action to synchronize the attachments of a local record with the attachments of a remote record.

## Roles and availability

Available as a ServiceNow Core Remote Process Sync action.

-   **Subscription requirements**

    This action requires an Integration Hub subscription. For more information, see [Request Integration Hub](../../flow-designer/concept/request-ih-overview.md) and [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Workflow Studio flows](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).


## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag pills from the Data panel or select them from the pill picker.

-   **Local Record**

    Data type: **Record**

    Reference to a record on the local instance you are synchronizing with another instance. The data pill contains all the field values for the specified record. For example, a case record on the local instance.

-   **Strategy**

    Data type: **Choice**

    Level of attachment detail to gather. The available options are All or Deltas. Use the All option to gather all synchronized attachments. Use the Deltas option to gather only attachments that have changed since the last synchronization.

-   **Remote System**

    Data type: **Record**

    Reference to the Process Sync Remote System record for the remote instance you are synchronizing processes with. This record identifies the instance that receives outbound synchronization changes or that sent inbound synchronization changes.

-   **Correlation Detail**

    Data type: **Object**

    Object containing correlation information about a synchronized record. The object identifies the local and remote correlation IDs associated with a local record.

-   **Attachments**

    Data type: **Array of Objects**

    Array containing a list of attachment objects to evaluate.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

Attachments: Data type: **Array of Objects**

Array containing information about the attachments to synchronize.

