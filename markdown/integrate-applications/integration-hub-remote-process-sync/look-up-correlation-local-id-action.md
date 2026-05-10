---
title: Look Up Correlation by Local Correlation ID action
description: Look up an active correlation by a specified local correlation ID. The local correlation ID identifies the correlation on the local instance. Remote Process Sync actions and flows use the returned correlation to synchronize a local record with a record on a remote system.
locale: en-US
release: australia
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Actions, Integration Hub Remote Process Sync, Workflow Data Fabric]
---

# Look Up Correlation by Local Correlation ID action

Look up an active correlation by a specified local correlation ID. The local correlation ID identifies the correlation on the local instance. Remote Process Sync actions and flows use the returned correlation to synchronize a local record with a record on a remote system.

## Roles and availability

Available as a ServiceNow Core Remote Process Sync action.

-   **Subscription requirements**

    This action requires an Integration Hub subscription. For more information, see [Request Integration Hub](../../flow-designer/concept/request-ih-overview.md) and [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Workflow Studio flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/user-access-flow-designer.md).


## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag pills from the Data panel or select them from the pill picker.

-   **Remote System**

    Data type: **Record**

    Reference to the Process Sync Remote System record for the remote instance you are synchronizing processes with. This record identifies the instance that receives outbound synchronization changes or that sent inbound synchronization changes.

-   **Local Correlation ID**

    Data type: **String**

    Globally unique ID of a correlation on the local instance you are synchronizing processes with. This ID uniquely identifies the correlation for inbound transactions.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Correlation Detail**

    Data type: **Object**

    Object containing correlation information about a record. The object identifies the local and remote correlation IDs associated with a local record.

-   **Status**

    Data type: **String**

    Status code returned by the action.


