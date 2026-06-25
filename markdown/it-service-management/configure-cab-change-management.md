---
title: Configure Change Advisory Board for Simplified Change Management
description: Set up your Change Advisory Board \(CAB\) in the setup wizard to define who reviews and approves significant changes before they are implemented.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configure-cab-change-management.html
release: australia
topic_type: task
last_updated: "2025-05-04"
reading_time_minutes: 3
keywords: [Change Advisory Board, CAB, Change Management, guided setup, CAB configuration, CAB members, CAB schedule, approval policy]
breadcrumb: [Configuring Simplified Change Management, Configuring the fulfiller experience in Simplified IT Service Management, Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configure Change Advisory Board for Simplified Change Management

Set up your Change Advisory Board \(CAB\) in the setup wizard to define who reviews and approves significant changes before they are implemented.

## Before you begin

CAB members &amp; managers you plan to add must already exist in ServiceNow as users or groups.

Role required: sn\_itsm\_chg\_admin.cab\_config

## Procedure

1.  From the header of your ServiceNow instance, navigate to **All** &gt; **Admin Home**.

2.  From the **Manage your products** section, select **View product overview** for IT Service Management.

3.  On the Product Hub page for IT Service Management, from the Configure your product section, select **Configure**.

4.  On the Configuration Console, from the left navigation panel, select **ITSM fulfiller experience &gt; Change Management &gt; Change Advisory Board \(CAB\)**. \[Omitted image "simplified-change-cab.png"\] Alt text: CAB configuration page

5.  In the Who should be on your Change Advisory Board \(CAB\)? section, add members to the CAB in the **CAB members** field.

    Search for and select the users or groups to include as CAB members, such as IT managers, senior system administrators, and application or development leads.

6.  In the Who leads the CAB? section, select a name in the **CAB manager** field.

    The CAB manager sets the agenda, runs the meeting, and makes the final call on approvals. This person has the authority to approve or reject changes.

    The When does your CAB meet? section is pre-configured with a default recurring schedule for CAB meetings.

7.  To update the schedule the recurring schedule for CAB meetings, perform the following steps in the When does your CAB meet? section:

    1.  Select the appropriate time zone from the **Timezone** field.

    2.  Set the meeting start date in the **Date** field.

    3.  Enter the meeting **Start time** and **End time**.

    4.  Set a **Repeat until** date to define when the recurring schedule ends.

    5.  Under **When does this schedule repeat?**, select one of the following recurrence options: **Weekly**, **Monthly**, or **Specific**.

    6.  Enter the interval in the **Repeat every** field.

    -   For Weekly or Specific interval, select the days of the week under **Repeat on** field.
    -   For Monthly interval, select a value in the **Monthly type** field.
    A summary of the configured schedule is displayed. For example: Runs every week on Monday from 09:00:00 to 10:00:00 \(US/Pacific time\) starting 17 March 2026.

    The conditions that determine which change requests are routed to the CAB are pre-configured in the Which changes require CAB review? section.

8.  To update the CAB definition conditions, perform the following steps in the Which changes require CAB review? section.

    1.  For each condition row, select a **Field**, an **Operator**, and a **Value** from the respective dropdowns.

    2.  To add more conditions, select **Add condition set**.

    At least one condition is required before this CAB can go live. Start with conditions based on fields such as **Risk**, **Type**, or **Priority**. Changes matching these criteria are automatically added to the next CAB meeting agenda.

9.  When you have finished configuring, select **Mark as configured** to save your settings and mark this step as complete.

    To revert changes made in the current session before saving, select **Undo**.

    As an alternative to the form-based wizard, you can also complete this configuration through the **Configure with Now Assist** conversational flow, accessible from the banner at the top of the page.


## Result

The CAB is configured with members, a manager, a recurring meeting schedule, and change routing conditions. The CAB Setup step is marked as complete, and your configured groups are available for selection in the per-risk approval policy configuration step.

**Parent Topic:**[Configuring Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-change-management-experience-in-it-service-management.md)

**Related topics**  


[Create a CAB definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/define-your-cab.md)

