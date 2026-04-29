---
title: Migrate the client action from ITSM Agent Workspace to Service Operations Workspace
description: Configure the client actions to migrate related list declarative actions from ITSM Agent Workspace to Service Operations Workspace.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Migrate the client action from ITSM Agent Workspace to Service Operations Workspace

Configure the client actions to migrate related list declarative actions from ITSM Agent Workspace to Service Operations Workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **Related List actions**.

2.  Filter the records based for **Implemented As** is set as **Client action**.

3.  View the log in the failed record in the migration process and find the **sys\_Id** of the record from the list of **Related List Actions**.

4.  Select the failed record with the corresponding sys\_id.

5.  Right-click on the header, and select **Insert and Stay**.

6.  Clear the **Workspace** and **View** fields.

7.  Select the **Experience Restricted** check box.

8.  Update the value in the **Implemented as** field as `UXF Client Action`.

9.  In the **Action configuration** related list, select **Edit**, and then select **SOW Actions** from **Collection** to **Action configurations** list.

10. Select **Save** to save the **Action configurations** related list.

11. Select **Update**.

12. If specify client action key is **ITEM\_SELECTED** or **PREVIEW\_RECORD**, create CREATE\_NEW\_RECORD key with the payload mentioned below in the code block in the sys\_declarative\_action\_payload\_definition table.

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

13. Modify the client action created for **ITEM\_SELECTED** and **PREVIEW\_RECORD** declarative actions records.

    When you modify the specific client action, then payload Map in action Attributes should be transformed based on the payload.

    The following tables are used in the migration process:

    -   sys\_ux\_m2m\_action\_assignment\_action\_config
    -   sys\_declarative\_action\_payload\_definition
    **Note:** The **ITEM\_SELECTED** and **PREVIEW\_RECORD** actions function in the ITSM Agent Workspace but not in SOW. Therefore, a new action payload named "CREATE\_NEW\_RECORD" Is introduced in SOW. While there could be other action payloads that might not function properly, the base system client actions for List continue to work effectively in SOW post-migration.


**Parent Topic:**[Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/related-list-declarative-actions-aw-sow.md)

