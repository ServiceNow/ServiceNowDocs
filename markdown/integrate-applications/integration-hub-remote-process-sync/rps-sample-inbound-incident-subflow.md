---
title: Remote Process Sync Inbound Flow Template - Basic
description: A sample Remote Process Sync subflow to process incoming payloads received from a remote instance. This subflow creates a correlation between a remote record and a local incident record. Copy this subflow and edit the actions that refer to the Incident table.
locale: en-US
release: zurich
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Sample subflows, Integration Hub Remote Process Sync, Workflow Data Fabric]
---

# Remote Process Sync Inbound Flow Template - Basic

A sample Remote Process Sync subflow to process incoming payloads received from a remote instance. This subflow creates a correlation between a remote record and a local incident record. Copy this subflow and edit the actions that refer to the Incident table.

## Roles and availability

Available as a Global Remote Process Sync subflow.

-   **Subscription requirements**

    This action requires an Integration Hub subscription. For more information, see [Request Integration Hub](../../flow-designer/concept/request-ih-overview.md) and [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Workflow Studio flows](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).


## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag pills from the Data panel or select them from the pill picker.

-   **Wait for Completion**

    Data type: **True/False**

    Option to require the parent flow to wait for the subflow to complete. If enabled, the parent flow cannot proceed to the next action until the subflow completes.

-   **Remote System**

    Data type: **Record**

    Reference to the Process Sync Remote System record for the remote instance you are synchronizing processes with. This record identifies the instance that receives outbound synchronization changes or that sent inbound synchronization changes.

-   **Remote Correlation ID**

    Data type: **String**

    Globally unique ID of a correlation on a remote instance you are synchronizing processes with. This ID uniquely identifies the correlation for outbound transactions.

-   **Local Correlation ID**

    Data type: **String**

    Globally unique ID of a correlation on the local instance you are synchronizing processes with. This ID uniquely identifies the correlation for inbound transactions.

-   **Process Event**

    Data type: **String**

    Name of the process event to run. The name is the same on each instance that participates in process synchronization. For example, case-to-incident.

-   **Payload**

    Data type: **String**

    JSON string containing changes generated on a remote instance. For example, a list of field changes for a case record from a remote instance. The system transforms this JSON string to an object on the local instance.

-   **CRUD Operation**

    Data type: **Choice**

    Database operation that triggered the process event. The available options are Create, Update, or Delete.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Error Message**

    Data type: **String**

    Error returned by the action.

-   **Status**

    Data type: **Choice**

    Synchronization state of records. The available options are Active or Inactive. Active records are being synchronized. Inactive records are not synchronized.


