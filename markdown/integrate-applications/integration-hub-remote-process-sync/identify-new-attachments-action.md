---
title: Identify New Attachments action
description: Identify the attachments already associated with a local record to determine which remote attachments require synchronization. Use the output of this action to request missing attachments from the remote system.
locale: en-US
release: australia
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Actions, Integration Hub Remote Process Sync, Workflow Data Fabric]
---

# Identify New Attachments action

Identify the attachments already associated with a local record to determine which remote attachments require synchronization. Use the output of this action to request missing attachments from the remote system.

## Roles and availability

Available as a ServiceNow Core Remote Process Sync action.

-   **Subscription requirements**

    This action requires an Integration Hub subscription. For more information, see [Request Integration Hub](../../flow-designer/concept/request-ih-overview.md) and [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Workflow Studio flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/user-access-flow-designer.md).


## Retry policy

The Identify New Attachments action uses the RPS Push Attachment Policy to retry failed requests at regular intervals. To view or edit this policy, navigate to the Retry Policies \[sys\_retry\_policy\] table at **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Retry Policies**.

## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Attachments**

    Data type: **Array of Objects**

    Array containing a list of attachment objects to evaluate.

-   **Local Record**

    Data type: **Record**

    Reference to a record on the local instance you are synchronizing with another instance. The data pill contains all the field values for the specified record. For example, a case record on the local instance.

-   **Max Attachment Size \(MB\)**

    Data type: **Integer**

    Integer specifying the maximum uncompressed attachment size that can be included in the list of attachments, in megabytes.

    You can use this field to limit attachment sizes and avoid errors that may result from syncing very large attachments.

    Leave this field blank to use the platform limit for attachment sizes.

-   **Allowed Extensions**

    Data type: **List**

    List containing the attachment extensions that can be included in the list of attachments. Leave this field blank to use the platform restrictions.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Attachments**

    Data type: **Array of Objects**

    Array containing information about the attachments to synchronize.

-   **Count**

    Data type: **Integer**

    Number of attachments identified.


