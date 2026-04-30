---
title: Create or update a treemap category
description: You can modify the predefined categories for the security incident treemaps or create categories as needed.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security incident treemaps, Security Incident Response Overview dashboard, Visual representation of Security Incident Response reporting, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create or update a treemap category

You can modify the predefined categories for the security incident treemaps or create categories as needed.

## Before you begin

Role required: sn\_si.admin

The treemaps use performance analytics as the data source. The Performance Analytics module requires a separate plugin.

## About this task

In the base system, treemap categories such as Incident Risk, Denial of Service, and Incident Severity are included. You can modify these categories or define more categories as needed.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Administration**, and open the treemap definition you want to configure categories for:

    -   **Service Criticality Reporting Definition**
    -   **Real-time Definition**
2.  Change the treemap definition name.

    In the base system, the default name for the service impact treemap definition is **Security Incident**. The default name for the real-time treemap definition is **Security Incident - Real time**.

3.  Unless you are using a custom-built treemap, do not change the **PA Indicator Group** value.

4.  To deactivate the treemap definition, clear the **Active** check box.

    If, for example, you deactivate the Denial of Service category from the system impact dashboard, that treemap category is not available.

5.  In the **Treemap Categories** related list, select a category to modify or click **New** to create a new category.

6.  Fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|The name that is displayed for the category in the **Categories** list above the treemap.|
    |Order|The order that the category appears in the **Categories** list above the treemap.|
    |Treemap|The name of the treemap that uses this category.|
    |Color|The color displayed for this category in the treemap.|
    |Active|Select to activate this category.|
    |Description|A description of the category.|
    |Visible by all roles|Select to make this category visible to all users regardless of their role.|
    |Roles|If you did not select the **Visible by all roles** check box, select the roles able to view this category.|

7.  Click **Submit** or **Update**.


**Parent Topic:**[Security incident treemaps](../concept/c_ConfigureTreemaps.md)

