---
title: Migrate the UI component from ITSM Agent Workspace to Service Operations Workspace for field decorators actions
description: Configure the UI component to migrate field decorators actions from ITSM Agent Workspace to Service Operations Workspace.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration, Service Operations Workspace for ITSM, IT Service Management]
---

# Migrate the UI component from ITSM Agent Workspace to Service Operations Workspace for field decorators actions

Configure the UI component to migrate field decorators actions from ITSM Agent Workspace to Service Operations Workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **Field Decorators**.

2.  Filter the records based for **Implemented As** is set as **UI component**.

3.  View the log in the failed record in the migration process and find the **sys\_Id** of the record from the list of **Related List Actions**.

4.  Select the failed record with the corresponding sys\_id.

5.  Right-click on the header, and select **Insert and Stay**.

6.  Clear the **Workspace** and **View** fields.

7.  Select the **Experience Restricted** check box.

8.  Update the value in the **Implemented as** field as `UXF Client Action`.

9.  In the **Action configuration** related list, select **Edit**, and then select **SOW Actions** from **Collection** to **Action configurations** list.

10. Select **Save** to save the **Action configurations** related list.

    **Note:** Adding MRA or Interceptor to the field isn’t a valid scenario. If there is still a customization, you must verify add-on event mapping in the base system. In the base system, the add-on event mappings for field declarative action are unavailable.

11. Select **Update**.

    The migration utility supports MRA and interceptor declarative actions of UI Component type only.

12. For MRA, create an action payload as specified below, update the values in action attributes with component attributes of ITSM Agent Workspace declarative action.

    If no value is filled in the ITSM Agent Workspace declarative action record, then fill the value with \{\{ key \}\}. For example, if the component attributes table is empty then in the payload the value should \{\{table\}\}.

    ```
    { 
    
    "label": "label", 
    
                    "extensionPoint": "extensionPoint", 
    
                    "userGivenTable": "userGivenTable", 
    
                    "hideSelectAll": "hideSelectAll", 
    
                    "parentRecordSysId": "parentRecordSysId", 
    
                    "table": "table", 
    
                    "referencedFieldName": "referencedFieldName", 
    
                    "type": "type", 
    
                    "parentFieldName": "parentFieldName", 
    
                    "columns": "columns", 
    
                    "view": "view", 
    
                    "relatedListName": "relatedListName" 
    
            } 
    ```

13. For Interceptor, create an action payload as specified below in the sys\_declarative\_action\_payload\_definition table.

    ```
    { 
    
        "table": "target", 
    
                    "sysId": "-1", 
    
                    "parentTable": "{{parentTable}}", 
    
                    "parentSysId": "{{parentRecordSysId}}", 
    
                    "referencedFieldName": "", 
    
                    "pageTitle": "Create " + tableLabel, 
    
                    "pageSubTitle": "Choose one of the following " + tableLabel + " types", 
    
                    "useDomain": false 
    
    } 
    ```

14. Add an add-on event mapping to the migrated declarative action.

    Find the matching declarative action in SOW and add all the add-on event mapping to the migrated declarative action. Use the following steps to find the equivalent declarative action in SOW.

    1.  Navigate to **All** &gt; **sys\_ux\_addon\_event\_mapping.list**

    2.  Filter the table and using the migrated `tablename` and **Target Payload Mapping** contains `mra` or `interceptor route`.

    3.  If the record is found, return the declarative action sys\_id.

        Iterate through all add-on event mapping of the found DA and add them to the migrated DA.

    4.  If the record isn’t found with the table, remove the table filter and search for targetPayload contains route=mra or interceptor.

        For **List** and **Field** decorator, you must add the mra and interceptor add-on event mappings manually. For more information, see [Create a UX add-on event mapping](https://www.servicenow.com/docs/access?context=create-a-ux-add-on-event-mapping&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

    **Note:**

    The Change\_request interceptor record in ITSM Agent Workspace exists in SOW.

    Migrating workspace space record type selector for the interceptor type of declarative action are:

    -   ITSM Agent Workspace table: aw\_record\_type\_selector
    -   SOW table: sn\_sow\_interceptor\_record\_type\_selector
    For a change\_request table that has a value as standard, Active is set as False when migrating the records from ITSM Agent Workspace to SOW.


**Parent Topic:**[Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/field-declarative-actions-aw-sow.md)

