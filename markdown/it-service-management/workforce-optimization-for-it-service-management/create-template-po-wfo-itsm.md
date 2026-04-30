---
title: Create Process Mining templates
description: Create templates on tables for which you want to create the process mining projects.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up the integration of Process Mining with Workforce Optimization for ITSM, Integrating Process Mining with Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Create Process Mining templates

Create templates on tables for which you want to create the process mining projects.

## Before you begin

Role required: admin

**Note:** You can only create templates for tables where Sys Audit \(sys\_audit\) is enabled. For more information on Sys Audit, see [Sys Audit and Audit Relationship Change tables](https://www.servicenow.com/docs/access?context=c_UnderstandingTheSysAuditTable&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) and [Enable auditing for a table](https://www.servicenow.com/docs/access?context=t_EnableAuditingForATable&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Templates** &gt; **All Templates**.

2.  Create a default process mining template.

    **Note:** The Process Mining template for the Incident table is available by default.

    1.  Select **New**.

        The **Project Definition** screen appears.

    2.  In the **Name** field, enter a name for the process mining template.

    3.  In the **Template type** field, select **Default**.

    4.  Right-click the form header and select **Save**.

3.  Create table configuration for the process mining template.

    1.  In the Table Configuration related list, select **New**.

    2.  In the **Name** field, enter a name for the table configuration.

    3.  In the Table menu, select the table, for example, Incident, for which you want to mine the data.

    4.  Select **Submit**.

4.  Create an activity definition.

    1.  Select the table configuration that you’ve created.

    2.  In the Activity Definitions related list, select **New**.

        You must add at least one activity to create the process project.

    3.  In the **Field** field, select the field for which you want to create the activity definition.

    4.  Select **Submit**.

5.  Select **Submit**.

    Repeat these steps and create a template for each table for which you want to mine the data.


**Parent Topic:**[Setting up the integration of Process Mining with Workforce Optimization for ITSM](../concept/setting-up-process-optimization-wfo-itsm.md)

**Related topics**  


[Create a Process Mining project for a KPI group](create-project-po-wfo-itsm.md)

