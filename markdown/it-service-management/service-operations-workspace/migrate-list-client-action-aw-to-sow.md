---
title: Migrate the client action from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Configure the client actions to migrate list actions from ITSM Agent Workspace to Service Operations Workspace for ITSM.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Migrate the client action from ITSM Agent Workspace to Service Operations Workspace for ITSM

Configure the client actions to migrate list actions from ITSM Agent Workspace to Service Operations Workspace for ITSM.

## Before you begin

When performing the migration, you must have selected the **List actions** option for ITSM Agent Workspace features. For example, the **List actions** option for List. For information about the migration process, see [Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](migrate-itsm-agent-workspace-to-sow.md).

Role required: admin

## About this task

At the end of the migration process, a confirmation message specifies if the migration is successful or not. You can review the migration information and perform the post-migration steps to confirm successful migration of your configuration or customization.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **List actions**.

2.  Filter the records based for **Implemented As** is set as **Client action**.

3.  View the log in the failed record in the migration process and find the **sys\_Id** of the record from the List Actions list.

4.  Select the failed record with the corresponding sys\_id.

5.  Select and hold \(or right-click\) on the header, and select **Insert and Stay**.

6.  Clear the **Workspace** and **View** fields.

7.  Select the **Experience Restricted** check box.

8.  Update the value in the **Implemented as** field as `UXF Client Action`.

9.  In the Action configuration related list, select **Edit**, and then select **SOW Actions** from the Collection list to the Action configurations list.

10. Save the Action configurations list by selecting **Save**.

11. Select **Update**.

12. If the client action key is **ITEM\_SELECTED** or **PREVIEW\_RECORD**, create a CREATE\_NEW\_RECORD key with the code block payload for the Action Payload Definition \[sys\_declarative\_action\_payload\_definition\] table.

    This step is performed only once.

    ```
    { 
                "route": "record", 
                "fields": { 
                    "table": "{{table}}", 
                    "sysId": "-1" 
                }, 
                "params": { 
                    "query": "{{query}}", 
                    "parentTable": "{{parentTable}}", 
                    "parentRecordSysId": "{{parentRecordSysId}}" 
                }, 
                "parent_table": "{{parentTable}}", 
                "additional_data": { 
                    "query": "{{query}}" 
                } 
            } 
    ```

13. Modify the client action created for **ITEM\_SELECTED** and **PREVIEW\_RECORD** list records.

    When you modify the client action, the payload map in action attributes should be transformed based on the payload.

    The following tables are used in the migration process:

    -   M2m Action Assig Ux Action Config \[sys\_ux\_m2m\_action\_assignment\_action\_config\]
    -   Action Payload Definition \[sys\_declarative\_action\_payload\_definition\]
    **Note:** The **ITEM\_SELECTED** and **PREVIEW\_RECORD** actions function in the ITSM Agent Workspace but not in SOW. Therefore, an action payload named CREATE\_NEW\_RECORD Is introduced in SOW. While there could be other action payloads that might not function properly, the base system client actions for the list continue to work effectively in SOW post-migration.


**Parent Topic:**[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/list-actions-migration-itsm-aw-sow.md)

