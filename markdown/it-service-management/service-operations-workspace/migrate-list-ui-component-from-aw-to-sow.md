---
title: Migrate the UI component from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Configure the UI component to migrate list actions from ITSM Agent Workspace to Service Operations Workspace \(SOW\) for ITSM.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Migrate the UI component from ITSM Agent Workspace to Service Operations Workspace for ITSM

Configure the UI component to migrate list actions from ITSM Agent Workspace to Service Operations Workspace \(SOW\) for ITSM.

## Before you begin

When performing the migration, you must have selected the **List actions** option for ITSM Agent Workspace features. For example, the **List actions** option for List. For information about the migration process, see [Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](migrate-itsm-agent-workspace-to-sow.md).

Role required: admin

## About this task

At the end of the migration process, a confirmation message specifies if the migration is successful or not. You can review the migration information and perform the post-migration steps to confirm successful migration of your configuration or customization.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **List actions**.

2.  Filter the records based for **Implemented As** is set as **UI component**.

3.  View the log in the failed record in the migration process and find the **sys\_Id** of the record from the List Actions list.

4.  Select the failed record with the corresponding sys\_id.

5.  Select and hold \(or right-click\) on the header, and select **Insert and Stay**.

6.  Clear the **Workspace** and **View** fields.

7.  Select the **Experience Restricted** check box.

8.  Update the value in the **Implemented as** field as `UXF Client Action`.

9.  In the Action configuration related list, select **Edit**, and then select **SOW Actions** from the **Collection** list to the Action configurations list.

10. Save the **Action configurations** list by selecting **Save**.

    **Note:**

    Adding Multiple Record Associator \(MRA\) or Interceptor to the list isn’t a valid scenario. If you’re migrating a customization with the MRA or Interceptor, you must verify the add-on event mapping for the base system records. In the base system, add-on event mappings for list declarative actions aren’t specified.

11. Select **Update**.

    The migration utility supports MRA and interceptor declarative actions of UI component type only.

12. For MRA, create an action payload as mentioned in the code block, update the values in action attributes with component attributes of the ITSM Agent Workspace declarative action.

    If no value is filled in the ITSM Agent Workspace declarative action record, then fill the value with \{\{ key \}\}. For example, if the component attributes table is empty then in the payload the value should be \{\{table\}\}.

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

13. For Interceptor, create an action payload as mentioned in the code block in the Action Payload Definition \[sys\_declarative\_action\_payload\_definition\] table.

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

        Iterate through all add-on event mappings of for the filtered declarative actions and add them to the migrated declarative actions.

    4.  If the record isn’t found with the table, remove the table filter and search for `targetPayload contains route=mra or interceptor`.

        For **List** and **Field** decorator, you must add the MRA and interceptor add-on event mappings manually. For more information, see [Create a UX add-on event mapping](https://www.servicenow.com/docs/access?context=create-a-ux-add-on-event-mapping&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

    **Note:**

    The Change Request \[change\_request\] interceptor record in ITSM Agent Workspace exists in SOW.

    Migrating workspace space record type selectors for the interceptor type of declarative action are:

    -   ITSM Agent Workspace table: Workspace Record Types Selector \[aw\_record\_type\_selector\]
    -   SOW table: Record Type Selector \[sn\_sow\_interceptor\_record\_type\_selector\]
    For a Change Request \[change\_request\] table that has a value as standard, Active is set as False when migrating the records from ITSM Agent Workspace to SOW.


**Parent Topic:**[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/list-actions-migration-itsm-aw-sow.md)

