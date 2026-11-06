---
title: Fix split view for chat-opened records
description: Create an AIX URL rewrite rule so that knowledge articles, catalog items, and tickets opened from Moveworks chat display in split view instead of a new tab.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/employee-experience-foundation/rule-split-view.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-06-19"
reading_time_minutes: 1
keywords: [split view, URL rewrite rule, Moveworks, AIX, Employee Center]
breadcrumb: [Chat assistance for catalog and knowledge, Tasks and requests, Working with EmployeeWorks capabilities, ServiceNow EmployeeWorks Web App, EmployeeWorks, Employee Service Management]
---

# Fix split view for chat-opened records

Create an AIX URL rewrite rule so that knowledge articles, catalog items, and tickets opened from Moveworks chat display in split view instead of a new tab.

## Before you begin

The EmployeeWorks Web App is configured with a Moveworks conversational assistant.

Role required: admin

## About this task

When a custom portal configuration is missing an AIX URL rewrite rule, records opened from Moveworks chat open in a new tab instead of the **split view**. Adding the rule maps the portal page URL to the correct AIUX page so records open inline.

## Procedure

1.  In the Moveworks chat, select a knowledge article, catalog item, or ticket link and note the URL passed in the link.

    For example: `/esc?id=kb_article&sys_id=<sys_id_value>`. Note the value of the **id** parameter — this is the portal page identifier you need in the next steps.

2.  Navigate to `sys_aix_url_rewrite_rule_list.do` and select **New**.

3.  Set the rule fields.

    |Field|Value|
    |-----|-----|
    |**Application**|Moveworks App Scope|
    |**Source type**|**Portal Page**|
    |**Portal page**|The **id** parameter value from the portal URL — for example, `kb_article`|
    |**To AIUX Page**|`/knowledge/:sys_id`|
    |**Experience**|EmployeeWorks Web App / EmployeeWorks|
    |**Order**|`100`|

4.  In the **Parameter mapping** section, add a mapping entry.

    |Field|Value|
    |-----|-----|
    |**Key**|The custom **sys\_id** field name from the portal URL — for example, `sys_id`|
    |**Value**|`sys_id`|

5.  Select **Save**.

6.  In the Moveworks chat, select a knowledge article link to verify the record opens in **split view**.

    If the record still opens in a new tab, confirm that the **Portal page** value matches the **id** parameter in the portal URL exactly, and that the correct experience is selected.


## Result

Knowledge Base articles, Service Catalog items, and tickets opened from Moveworks chat display in the **split view** alongside the conversation panel.

