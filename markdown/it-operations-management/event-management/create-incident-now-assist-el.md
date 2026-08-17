---
title: Create an incident from an alert with ServiceNow Otto in Express List
description: Create an incident with a human-readable, AI-generated description from the Express List pane by using AI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/create-incident-now-assist-el.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [generative AI for IT Operations Management, generative AI for ITOM, create an incident, alert, Express List, Now Assist]
breadcrumb: [Promote alerts in Express List, Express List in SOW for ITOM, Event Management, ITOM AIOps, IT Operations Management]
---

# Create an incident from an alert with ServiceNow Otto in Express List

Create an incident with a human-readable, AI-generated description from the Express List pane by using AI.

## Before you begin

**Note:** Currently, ServiceNow Otto for ITOM only supports tag-based, CMDB, Log Analytics, Mixed, Automated, and Network Traffic-based alert groups. For all other alert group types, it only analyzes the parent alert.

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon \[Omitted image "express-list1.png"\].

3.  Create an incident from a selected alert.

    1.  In the Express List pane, select the alert.

        **Note:** To display the individual alerts inside a group, select the chevron icon \(\[Omitted image "icon-chevron.png"\] Alt text: Chevron icon.\) at the beginning of the alert group row.

    2.  Select the **Alert actions** drop-down list.

        \[Omitted image "alert-actions-tool-tip.png"\] Alt text: Alert actions drop down arrow

    3.  Under **Response actions**, select **Create Incident with ServiceNow Otto**.

    An incident with a human-readable, AI-generated description is created from the selected alert and a confirmation message is displayed.


