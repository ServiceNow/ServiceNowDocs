---
title: AWA post work item subflow
description: Configure the base system AWA post work item subflow by defining the input in Workflow Studio.
locale: en-US
release: yokohama
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Management, Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# AWA post work item subflow

Configure the base system AWA post work item subflow by defining the input in Workflow Studio.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the Workflow Studio screen, select **Subflows**.

3.  In the Name column, enter `Template: AWA post work item`.

    This searches for the Template: AWA post work item.

4.  Select **Template: AWA post work item**.

5.  In the subflow header, select the more actions icon \(![More actions icon](../image/awa-more-actions.png)\) and then **Copy subflow.**

6.  On the Create a copy of this subflow dialog, enter a unique and descriptive name for the copied subflow in the **New subflow name** field.

7.  Select **Copy**.

    The new subflow is created and displays as a tab in the subflow designer editor.

8.  You can customize the subflow by doing one of the following:

    -   Integrate with a third-party system by adding an action with a spoke from the Integration Hub \(for more information, see [Spokes](https://www.servicenow.com/docs/access?context=spokes&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)\)
    -   Use a REST action step and call the external endpoint \(for more information, see [REST step](https://www.servicenow.com/docs/access?context=rest-request-action-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)\).
    -   Call a REST message in the subflow itself \(for more information, see [Outbound REST Web Service](https://www.servicenow.com/docs/access?context=c_OutboundRESTWebService&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)\).

**Parent Topic:**[Management](../concept/management.md)

**Related topics**  


[Configure an agent's maximum universal capacity](awa-universal-capacity.md)

[Create or change groups for Advanced Work Assignment queues](awa-groups.md)

