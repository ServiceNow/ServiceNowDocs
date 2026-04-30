---
title: Identify New Attachments action
description: Identify the attachments a local record already has to determine which remote attachments need synchronization. Use the output of this action to request missing attachments from a remote system.
locale: en-US
release: xanadu
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Remote Process Sync actions, Integration Hub Remote Process Sync, Creating integrations with applications]
---

# Identify New Attachments action

Identify the attachments a local record already has to determine which remote attachments need synchronization. Use the output of this action to request missing attachments from a remote system.

## Roles and availability

Available as a ServiceNow Core Remote Process Sync action.

-   **Subscription requirements**

    This action requires an Integration Hub subscription. For more information, see [Request Integration Hub](../../flow-designer/concept/request-ih-overview.md) and [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

-   **Role requirements**

    This action requires roles granted by delegated development or assigned to the user. For more information, see [User access to Workflow Studio flows](https://www.servicenow.com/docs/access?context=user-access-flow-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).


## Inputs

Provide a value for each input that your action needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Attachments**

    Data type: **Array of Objects**

    Array containing a list of attachment objects to evaluate.

-   **Local Record**

    Data type: **Record**

    Reference to a record on the local instance you are synchronizing with another instance. The data pill contains all the field values for the specified record. For example, a case record on the local instance.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **Attachments**

    Data type: **Array of Objects**

    Array containing information about the attachments to synchronize.

-   **Count**

    Data type: **Integer**

    Number of attachments identified.


