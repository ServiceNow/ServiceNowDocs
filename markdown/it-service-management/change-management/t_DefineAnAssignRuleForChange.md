---
title: Create a change request assignment rule
description: Define assignment rules to assign change requests automatically to the appropriate group or individual.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/t\_DefineAnAssignRuleForChange.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Create a change request assignment rule

Define assignment rules to assign change requests automatically to the appropriate group or individual.

## Before you begin

Role required: admin

## About this task

You can define an assignment rule either for the change request or for the change tasks that are generated for change requests. In the following example, you create an assignment rule to assign change requests for configuration items in the database class to the **Database** group.

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Assignment**, and then select **New**.

2.  In the **Name** field, enter `Database Change`.

3.  In the Applies To form section, select the table **Change Request \[change\_request\]** and add the condition \[**Configuration Item.Class**\] \[**is**\] \[**Database**\].

4.  In the Assign To section, select the group **Database**.

5.  Select **Submit**.


## What to do next

To test the assignment rule, navigate to **Change** &gt; **Create New** and enter a Normal change. Complete the form, selecting **bond\_trade\_ny**, or another CI in the database class, in the **Configuration Item** field.

Save the change and verify that it's automatically assigned to the **Database** group.

**Parent Topic:**[Configuring Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/configure-change-management.md)

