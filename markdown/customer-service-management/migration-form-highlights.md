---
title: Highlights
description: Learn how CSM Agent Workspace highlights function with CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/migration-form-highlights.html
release: australia
topic_type: concept
last_updated: "2026-10-25"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Highlights

Learn how CSM Agent Workspace highlights function with CSM Configurable Workspace.

Highlights provide background color that visually expresses the status of a highlighted value. The status you choose determines the color highlight.

Highlighted values are the color-coded status badges that agents see on record lists and case headers, such as a red badge on high-priority cases. If you don't migrate them, those visual cues don't appear in CSM Configurable Workspace.

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_highlighted\_value|sys\_highlighted\_value sys\_ux\_highlighted\_value\_config sys\_ux\_m2m\_highlighted\_value\_config|

To migrate your highlights, add an extra step in the custom highlighted values to CSM Configurable Workspace.

An additional highlighted value configuration is provided out of box, CSM/FSM Configurable Workspace Highlighted Value Config.

This configuration record is created automatically when you activate CSM Configurable Workspace, but it doesn't include your existing CSM Agent Workspace highlighted value records. You must link them manually.

-   Legacy highlighted values in form headers work without modification, but may affect the functionality of CSM Configurable Workspace.
-   Highlighted values must be added to a highlighted value configuration to appear in CSM Configurable Workspace.

For more information, see [Set up a highlighted value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/config-csm-config-ws-highlight-value.md).

## Link highlighted values to CSM Configurable Workspace

Role required: admin

Before you begin, navigate to **All** &gt; **Workspace Experience** &gt; **Administration** &gt; **Highlighted Values** to view your existing highlighted value records, and identify the table that each one applies to, such as sn\_customerservice\_case.

1.  Switch to the CSM and FSM Configurable Workspace Foundation scope.
2.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Highlighted Value Configurations**.
3.  Open the **CSM/FSM Configurable Workspace Highlighted Values Config** record.
4.  In the **Highlighted Values** related list, select **Edit**.
5.  Add a filter condition for the table, such as `Table starts with sn_customerservice_case`, and select **Run filter**.
6.  Select the highlighted values that you want to include and move them to the **Highlighted Values List**.
7.  Select **Save**.
8.  Repeat these steps for each additional table whose highlighted values you need to migrate.

