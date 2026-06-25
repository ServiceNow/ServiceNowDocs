---
title: Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Migration of the Agent assist from ITSM Agent Workspace to Service Operations Workspace \(SOW\) include identifying the required tables, eligible form header records for migrations and the migrations process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/agent-assist-migration-itsm-aw-sow.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM

Migration of the Agent assist from ITSM Agent Workspace to Service Operations Workspace \(SOW\) include identifying the required tables, eligible form header records for migrations and the migrations process.

## Tables used for migration

|Table name|Description|
|----------|-----------|
|cxs\_table\_config|Table that contains all the Agent assist configurations in ITSM Agent Workspace and SOW.|
|declarative\_action\_assignment|Table that contains the sys\_id of the cxs\_table\_config record in the component attributes with the cxsTableConfig key name in ITSM Agent Workspace.|
|sys\_ux\_screen|Tables that contains the sys\_id of the cxs\_table\_config record in the **Macroponent Configuration** field of the Agent Assist SNC \(468f70f443b47110cc25ff53e9b8f296\) record. This record is available in the base system.|

## Limitations

When migrating agent assist configurations from ITSM Agent Workspace to SOW, you may encounter any of the following issues:

-   If customer has configured more than one Agent assist configuration on the same table, the most recently updated configuration is migrated.
-   The Agent assist migration from ITSM Agent Workspace overrides any pre-existing changes in SOW.

## Configuring Agent assist in ITSM Agent Workspace and SOW

You can configure Agent assist in ITSM Agent Workspace and SOW using the following tables:

-   For ITSM Agent Workspace, Agent Assist configuration data exist in the following tables where the configuration data is stored:
    -   Agent assist is configured on a particular table using a declarative action with the UI component now-agent-assist.
    -   Configuration is stored in the cxs\_table\_config table.
    -   Declarative action on the table stores the sys\_id of the cxs\_table\_config record in the component attributes with the cxsTableConfig key name.
-   For SOW, Agent assist configuration data exist in the following tables:
    -   The configuration record from cxs\_table\_config is stored in the Agent Assist SNC record from sys\_ux\_screen.
    -   In SOW, a field named Macroponent Configuration contains the mapping of each individual table with its configured sys\_id of cxs\_table\_config record.

## How the migration utility identifies Agent assist for migration

The SOW migration utility identifies the eligible agent assist configuration records for migration from ITSM Agent Workspace to SOW only if the configuration records meet the following conditions:

-   The **Workspace** field is set to **Agent Workspace**.
-   The **ui\_component** field has the value **now-agent-assist**.
-   The **Table** field is set to a value \(table\) for which migration must be done.
-   The **Active** check box is selected.

## How the migration works

The SOW migration utility uses the following sequence to migrate Agent assist from ITSM Agent Workspace to SOW:

1.  Searches the sys\_declarative\_action\_assignment table with the following conditions and only retrieves the record which is recently updated.
    -   The **Workspace** field is set to **Agent Workspace**.
    -   The **ui\_component** field has the value **now-agent-assist**.
    -   The **Table** field is set to a value \(table\) for which migration must be done.
    -   The **Active** check box is selected.
2.  If the sys\_declarative\_action\_assignment record is found with the conditions, then the value in the cxsTableConfig is copied to the Agent assist SNC record from the sys\_ux\_screen against its corresponding table key.

    The following screenshot depicts sys\_id's of all the record types in the **Macroponent Configuration** field of the Agent assist SNC record. \[Omitted image "mu-agent-assist-snc.png"\] Alt text: Agent assist SNC record

    The following screenshot depicts the Agent assist for incident sys\_id record that contains the cxsTableConfig as the component attributes. \[Omitted image "mu-agent-assist-incident.png"\] Alt text: Agent assist incident

3.  If multiple configurations exist for same table, the SOW migration utility migrates the one that was most recently updated.
4.  If an active configuration is not found in the table then the sow configuration remains same and is not updated.

-   **[Perform post-migration tasks for Agent assist configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/verify-migration-status-agent-assist.md)**  
Verify that the Agent assist configurations in Service Operations Workspace \(SOW\) are consistent with the Agent assist configurations in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated Agent assist configuration settings in SOW based on your requirements.

**Parent Topic:**[Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/configurations-and-customizations-from-itsm-aw-sow-itsm.md)

**Related topics**  


[Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

[Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM]()

