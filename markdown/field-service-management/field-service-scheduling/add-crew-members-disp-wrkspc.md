---
title: Add Field Service crew members in Dispatcher Workspace
description: Add agents to the Field Service crew as needed in Dispatcher Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/field-service-management/field-service-scheduling/add-crew-members-disp-wrkspc.html
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Crew operations, Using Dispatcher Workspace, Assigning WOTs from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Add Field Service crew members in Dispatcher Workspace

Add agents to the Field Service crew as needed in Dispatcher Workspace.

## Before you begin

Role required: wm\_dispatcher and wm\_crew\_moderator

## About this task

You can add crew members on the run for undersized crew tasks, such as agent is unavailable for a long time or available members are less than the mentioned crew requirement.

## Procedure

1.  Navigate to **All** &gt; **Field Service Management** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Click **Dispatcher Workspace**.

3.  In the tasks panel, select **Undersized Crew Tasks** from the list.

4.  Select the work order task to which you want to assign the agent.

5.  Search for a field service agent whom you want to add to the crew.

    For more information, see [Identify crews and agents for crew tasks on Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/field-service-scheduling/sort-crews-for-wot.md).

6.  In the agent card, click the More actions icon \(\[Omitted image "more\_actions.png"\] Alt text: More actions icon\) and select **Add to crew**.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Member|Auto-populated name of the agent.|
    |Crew|Name of the Field Service crew to which you want to add a crew member.|
    |Effective from|Start date from when the member is available to work on the task.|
    |Effective to|End date until when the member is available to work on the task.|

8.  Click **Save**.

9.  Repeat steps 3 through 6 to add more members to the crew.


## Result

The members are added to the crew.

