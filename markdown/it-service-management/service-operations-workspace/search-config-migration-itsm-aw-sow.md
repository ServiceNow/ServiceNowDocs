---
title: Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: Migration of the search configuration from ITSM Agent Workspace to Service Operations Workspace \(SOW\) include identifying the eligible form header records and the migration process.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Migration of search configurations from ITSM Agent Workspace to Service Operations Workspace for ITSM

Migration of the search configuration from ITSM Agent Workspace to Service Operations Workspace \(SOW\) include identifying the eligible form header records and the migration process.

## How the migration utility identifies search configuration for migration

The migration utility in SOW identifies the eligible set of search configuration records to be migrated based on the following sequence:

1.  Filters the application search sources records \(sys\_search\_source\) that are mapped to ITSM Agent Workspace master config record using the m2m\_search\_context\_config\_search\_source table.
2.  Checks the application search sources that are mapped to SOW context config record.
3.  Searches each filtered record that are mapped to ITSM Agent Workspace master config record and checks if that record is not mapped to SOW context config record to identify the search sources which are unique to ITSM Agent Workspace only and not mapped to SOW context config record.
4.  For all those unique search records that are mapped to ITSM Agent Workspace, the SOW migration utility creates similar mapping to SOW context config record at m2m\_search\_context\_config\_search\_source table.
5.  If common search sources mapped between ITSM Agent Workspace and SOW are found and the order of the mapping is differed in SOW from ITSM Agent Workspace, the SOW migration utility updates the order from ITSM Agent Workspace mapping to SOW mapping.
6.  Migrates the values of ITSM Agent Workspace search view config record to SOW search view config record.
7.  When both the search view config and the search sources are mapped to SOW from ITSM Agent Workspace, the SOW migration utility updates the **globalSearchDataConfigIdSOW** page property to reflect SOW context config record available in the base system.

## How the migration works

The SOW migration utility uses the following sequence to migrate the search configuration records from ITSM Agent Workspace to SOW:

1.  Searches the reference record for Global Search Data Config and Global Search View Config using the sys\_aw\_master\_config table in ITSM Agent Workspace.
2.  Determines the Search engine type in the Global Search Data Config record. If the search engine is zing then migration proceeds. Else, the migration process stops.
3.  Using the Global Search Data Config record, a query is run on the Application Search Sources \(m2m\_search\_context\_config\_search\_source\) table to retrieve all the search sources.
4.  Using the SOW search context config available in the base system, a query is executed on the Application Search Sources \(m2m\_search\_context\_config\_search\_source\) table to retrieve all the search sources.

    The SOW search context config exists as a record in the sys\_search\_context\_config table and sys\_id can be found at SOW page property called **globalSearchDataConfigId**.

5.  Compares between the search sources by executing a query on the Application Search Sources \(m2m\_search\_context\_config\_search\_source\) table using Global Search Data Config record \(ITSM Agent Workspace search sources\) and SOW search context config record \(SOW search sources\), to find unique search sources mapped to ITSM Agent Workspace but not SOW.
6.  If the order value of a SOW search source is different than the order value of the ITSM Agent Workspace search source at the Application Search Sources table, the SOW migration utility updates the SOW search source with the same order value as in mapped in ITSM Agent Workspace.
7.  Creates record in the Application Search Sources \(m2m\_search\_context\_config\_search\_source\) table with SOW context config record that is available in the base system and searches the unique sources that are found by comparing the ITSM Agent Workspace search sources and SOW search sources.
8.  Opens the Global Search View Config reference record that is retrieved using the sys\_aw\_master\_config table in ITSM Agent Workspace and copy all the values to SOW view config record \(SOW page property with name global\_search\_configurations\). The SOW view config record is available in the base system.
9.  Updates the SOW page property **globalSearchDataConfigId** to have OOB SOW context config record.

-   **[Perform post-migration tasks for search configurations](../task/verify-migration-status-search-config.md)**  
Verify that the search configurations in Service Operations Workspace \(SOW\) are consistent with the search configurations in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated search configurations settings in SOW based on your requirements.

**Parent Topic:**[Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM](../concept/configurations-and-customizations-from-itsm-aw-sow-itsm.md)

**Related topics**  


[Migration of UI actions and layouts from ITSM Agent Workspace to Service Operations Workspace for ITSM](ui-actions-layouts-migration-itsm-aw-sow.md)

[Ribbons migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](ribbons-migration-itsm-aw-sow.md)

[Migration of view rules from ITSM Agent Workspace to Service Operations Workspace for ITSM](view-rules-migration-itsm-aw-sow.md)

[New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](new-record-menu-items-migration-itsm-aw-sow.md)

[Migration of highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM](highlighted-fields-lists-forms-migration-itsm-aw-sow.md)

[List actions migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-actions-migration-itsm-aw-sow.md)

[List categories and modules migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](list-categories-modules-migration-itsm-aw-sow.md)

[Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM](form-headers-migration-itsm-aw-sow.md)

[Migration of Agent assist from ITSM Agent Workspace to Service Operations Workspace for ITSM](agent-assist-migration-itsm-aw-sow.md)

[Migration of Related list declarative actions from ITSM Agent Workspace to Service Operations Workspace for ITSM](related-list-declarative-actions-aw-sow.md)

[Migration of field decorators from ITSM Agent Workspace to Service Operations Workspace for ITSM](field-declarative-actions-aw-sow.md)

