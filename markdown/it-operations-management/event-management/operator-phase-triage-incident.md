---
title: Operator phase 2: Triage an alert
description: After you analyze and acknowledge an alert, you must triage it. The triage phase involves verifying alert correlation and taking an action to help resolve the issue that caused the alert. This topic covers the most common triage task: creating an incident from an alert.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/operator-phase-triage-incident.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Operator responsibilities, Event Management Operator Tutorial, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Operator phase 2: Triage an alert

After you analyze and acknowledge an alert, you must triage it. The triage phase involves verifying alert correlation and taking an action to help resolve the issue that caused the alert. This topic covers the most common triage task: creating an incident from an alert.

## Before you begin

**Note:** The Operator Workspace interface is available only to customers who have upgraded from a release prior to the Utah release. New customers as of the Utah release can use the Service Operations Workspace for ITOM, which offers an enhanced UI for managing alerts.

<table id="table_pp3_vg3_3db"><tbody><tr><td>

Phase 1

</td><td align="justify">

\[Omitted image "progress-complete2.png"\] Alt text: Analyze icon

</td><td>

[Analyze and acknowledge an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-phase-acknowledge-analyze.md)

</td></tr><tr><td>

Phase 2

</td><td align="justify">

\[Omitted image "progress-wip.png"\] Alt text: Triage icon

</td><td>

Triage alerts

</td></tr><tr><td>

Phase 3

</td><td align="justify">

\[Omitted image "progress-not-started.png"\] Alt text: Close alert icon

</td><td>

[Close an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-close-alert.md)

</td></tr></tbody>
</table>Role required: evt\_mgmt\_operator

## Procedure

1.  Before you start to work on the alert, check whether other alerts should be correlated with the one you just reviewed:

    1.  Navigate to **Event Management** &gt; **Service Operations Workspace**.

    2.  Click the same application service tile and review the alerts in the **Alerts** list.

    3.  If multiple alerts are present, open one to determine if it is related to the other alert, or if the underlying issue is the same in both alerts.

        For example, if an alert is associated with a web server and there is already an alert for the database issue, correlate the web server alert as a secondary alert with the database alert as the primary alert.

    4.  Open the secondary alert, click the lookup icon \(\[Omitted image "lookup-icon.png"\] Alt text: Lookup icon\) in the **Parent** field, and then select the primary alert.

        This creates a primary \(parent\) / secondary \(child\) relationship between the two alerts.

        \[Omitted image "operator-alert-parent.png"\] Alt text: Alert

    5.  Repeat this process to correlate as many secondary alerts as necessary.

    6.  Navigate back to the Service Operations Workspace dashboard and verify that the primary alert displays an icon in the **Group** column.

        \[Omitted image "operator-dashbaord-alert-group.png"\] Alt text: Group

        **Note:** Your administrator can set up rules that let the system automatically correlate alerts so that you do not need to do so manually. In that case, a **Feedback** field appears on the Alert form. Select **Yes** if the system correlated the alert correlated correctly, or **No** if not. Currently, the feedback option is available but does not trigger further actions after being logged.

2.  Open the primary alert.

3.  On the Alert form, click **Actions** &gt; **Create Incident**.

    If your organization uses Security Incident Response, the button is **Create Security incident**.

    The Flow Designer opens.

    \[Omitted image "flow-designer-executions-tab.png"\] Alt text: Creating an incident

4.  Click **Refresh**.

    The **Execution Details** page opens.

    \[Omitted image "execution-details-page.png"\] Alt text: Execution Details page

5.  Click **Open Context Record** and then fill in the Incident form.

    \[Omitted image "incident-form.png"\] Alt text: Incident form

<table id="table_z1h_ntr_fdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Caller

</td><td>

Click the lookup icon \(\[Omitted image "lookup-icon.png"\] Alt text: Lookup icon\) and then select your name. The caller is the person who discovered the issue that led to the incident.

</td></tr><tr><td>

Category and Subcategory

</td><td>

Select a category that best describes this alert. In this example, **Database** is the best choice.

</td></tr><tr><td>

Application service

</td><td>

Select the application service to which the CI belongs. In this example, the application service is **Web portal**.

</td></tr><tr><td>

Configuration item

</td><td>

If it is not already populated, select the CI. In this example, the Oracle database \(**PS ORA01**\) is automatically populated into the field.

</td></tr><tr><td>

Impact and Urgency

</td><td>

Select the impact and urgency levels that you think appropriate.

</td></tr><tr><td>

Assignment group

 Assigned to

</td><td>

Click the lookup icons \(\[Omitted image "lookup-icon.png"\] Alt text: Lookup icon\) for both or either of these fields, and then select the group or the individual that can handle the issue.

</td></tr></tbody>
</table>6.  Click **Submit** to create the incident.

    The Alert you are working on reappears. On the Alert form, the incident is populated in the **Task** field. You can also see the incident number in the Task column on the Service Operations Workspace dashboard.

    \[Omitted image "operator-alert-task.png"\] Alt text: Alert


## What to do next

There are other tasks you perform as part of the triage stage:

-   [Run a remediation workflow on an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-run-remdiation.md) if your Event Management administrator already set up a workflow in your ServiceNow instance and your policies allow you to trigger it from the alert.
-   [Launch a web application from an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-launch-web-app.md) to open a website or an event monitoring tool that provides more information about the alert.
-   [Associate a knowledge base article with an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-associate-kb.md) if there is existing information about the alert that might help resolve the underlying issue.
-   [Put an alert into maintenance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-put-alert-into-maintenance.md) to temporarily hide it from the Service Operations Workspace dashboard if the alert does not require action at this time.

If you do not need to perform any other triage actions, proceed to [Phase 3: Close an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-close-alert.md).

-   **[Run a remediation workflow on an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-run-remdiation.md)**  
As an Event Management operator, you can also run a workflow on your ServiceNow instance that helps remediate the alert. For example, you might run a workflow that automatically restarts a server on your network, which might resolve an alert about CPU usage.
-   **[Launch a web application from an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-launch-web-app.md)**  
As an Event Management operator, you can also launch a web application from an alert. The web application might be a console for the event monitoring tool that your organization uses, or any external website that provides additional information you might need about the alert.
-   **[Associate a knowledge base article with an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-associate-kb.md)**  
As an Event Management operator, you can associate a knowledge base \(KB\) article with the alert to capture additional information about the alert. This might include a procedure that someone has to follow to resolve the underlying issue on your network, or a best practice to prevent the issue from reoccurring.
-   **[Put an alert into maintenance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-put-alert-into-maintenance.md)**  
As an Event Management operator, you can put an alert into maintenance if the alert does not require any further action, but you still want to keep the alert active. Putting the alert into maintenance hides it from the Service Operations Workspace dashboard so that other operators do not need to access it, but it does not close the alert.

**Parent Topic:**[What Event Management operators do](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-process.md)

