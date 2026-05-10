---
title: Configure the health screening form
description: Provide additional information on contacts or consumers to health screeners by adding fields to the health screening form.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating with Safe Workplace applications, Integrate, Customer Service Management]
---

# Configure the health screening form

Provide additional information on contacts or consumers to health screeners by adding fields to the health screening form.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Record Producers**.

    1.  In the Record Producers list, search for `Screen a person` in the **Name** column.

    2.  In the Variables related list, click **New**.

    3.  Create a variable.

        For more information about the different types of variables and how to configure them, see [Creating variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/r_CreatingVariablesForFieldTypes.md).

    4.  Click **Submit**.

    5.  In the Catalog Client Scripts related list, open **Show additional CSM fields**.

    6.  Add the variable to the client script as a consumer or contact field.

        For more information on client scripts, see [Client scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/client-scripts.md).

2.  Navigate to **Activity Subscriptions** &gt; **Script Includes**.

    1.  Add the variables to the **HealthScreeningUtil** script include.

        For more information on script includes, see [Script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_ScriptIncludes.md).


