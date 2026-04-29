---
title: Create Correlation action
description: Create a correlation between a record on the local instance and a record on a remote instance. A correlation identifies a remote system and a local record to synchronize. Each instance maintains a copy of the correlation, which contains a set of shared correlation identifiers. Remote Process Sync actions and flows use the correlation identifiers to synchronize records.
locale: en-US
release: australia
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Actions, Integration Hub Remote Process Sync, Workflow Data Fabric]
---

# Create Correlation action

Create a correlation between a record on the local instance and a record on a remote instance. A correlation identifies a remote system and a local record to synchronize. Each instance maintains a copy of the correlation, which contains a set of shared correlation identifiers. Remote Process Sync actions and flows use the correlation identifiers to synchronize records.

## Roles and availability

Available as a ServiceNow Core Remote Process Sync action.

-   **Subscription requirements**

    This action requires an Integration Hub subscription. For more information, see [Request Integration Hub](../../flow-designer/concept/request-ih-overview.md) and [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Workflow Studio flows](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=australia&pubname=australia-build-workflows&ft:locale=en-US).


## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Remote Correlation ID**

    Data type: **String**

    Globally unique ID of a correlation on a remote instance you are synchronizing processes with. This ID uniquely identifies the correlation for outbound transactions.

-   **Local Correlation ID**

    Data type: **String**

    Globally unique ID of a correlation on the local instance you are synchronizing processes with. This ID uniquely identifies the correlation for inbound transactions.

-   **Remote System**

    Data type: **Record**

    Reference to the Process Sync Remote System record for the remote instance you are synchronizing processes with. This record identifies the instance that receives outbound synchronization changes or that sent inbound synchronization changes.

-   **Local Record**

    Data type: **Record**

    Reference to a record on the local instance you are synchronizing with another instance. The data pill contains all the field values for the specified record. For example, a case record on the local instance.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Correlation Detail**

    Data type: **Object**

    Object containing correlation information about a record. The object identifies the local and remote correlation IDs associated with a local record.

-   **Status**

    Data type: **String**

    Status code returned by the action.

-   **Error**

    Data type: **String**

    Error returned by the action.


