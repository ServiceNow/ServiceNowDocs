---
title: Associate multiple incidents with a major incident
description: You can associate one or more incidents with a major incident using the Actions menu.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working on major incident management, Managing major incidents, Incident Management, IT Service Management]
---

# Associate multiple incidents with a major incident

You can associate one or more incidents with a major incident using the Actions menu.

## Before you begin

Role required: itil, sn\_incident\_write, or admin

## About this task

When a major incident occurs, there are usually multiple incidents created for the same issue and there might be multiple major incident candidates created for a single issue. All the incidents for a single issue can be associated with the appropriate major incident.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Select the incidents that need to be associated with a major incident.

3.  On the Actions menu, click **Link to Major Incident**.

    ![Associate multiple incidents with a major incident](../image/link-inci-to-major-inci.png)

4.  In the Choose a Major Incident dialog box, select the major incident with which you want to associate the incidents.

5.  Click **OK**.

    The incidents are added as a child to the major incident.


**Parent Topic:**[Working on major incident management](../concept/work-on-mim.md)

