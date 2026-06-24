---
title: Create a system properties module
description: You can add a module in the application navigator to access the list of system properties. This module makes it easy to add properties to the System Properties table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/t\_CreatingAPropertiesModule.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Basic system configuration, Get started, Administer]
---

# Create a system properties module

You can add a module in the application navigator to access the list of system properties. This module makes it easy to add properties to the System Properties table.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Application Menus**.

2.  Search for the application you want to add the properties table to, for example **System Properties**.

    Select an application that is restricted to the admin role so that non-admin users cannot access it.

3.  From the Modules related list, click **New**.

4.  Complete the form fields.

    |Field|Description|
    |-----|-----------|
    |Title|Module name. For example, **All Properties**.|
    |Application Menu|Specifies the name of the application menu the module appears under. This field should automatically be populated with the name of the application you accessed the Modules related list from.|
    |Link type|Specifies the type of link this modules opens. For a list of system properties, select **List of Records**.|
    |Table|Specifies the table used by the module. Select **System Properties \[sys\_properties\]**.|

5.  Click **Submit**.

6.  Verify that the module was created. For example, navigate to **System Properties** &gt; **All Properties**.


## What to do next

If you want to include additional parameters for the list of system properties module, see [Create a module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/automated-test-framework-atf/test-steps-app-navigator-category.md).

**Parent Topic:**[Basic system configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/p_CoreConfigurationOverview.md)

