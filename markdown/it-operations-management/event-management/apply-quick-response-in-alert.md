---
title: Apply a quick response in an alert
description: In an alert, use the Quick Response feature to apply remediation to the alert or to launch a web application.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [View alert information, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Apply a quick response in an alert

In an alert, use the `Quick Response` feature to apply remediation to the alert or to launch a web application.

## Before you begin

Role required: evt\_mgmt\_operator, evt\_mgmt\_admin

## About this task

**Quick Response** is a feature that enables you to perform a quick action on the selected alert. The action is to apply remediation or to launch an application. If you have upgraded from Istanbul or earlier, this feature is a combination of the **Remediation** and **Launch an application** features.

If you select a remediation link when invoking a Quick Response, a workflow is executed according to the criteria specified in the alert management rule. Click a launch application link to launch the web application that was configured in the alert management rule. For further information, see [Migrate an alert action rule to an alert management rule](t_EMCreateAlertRule.md).

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Alerts**.

2.  In the Alerts list, right-click the required alert and select **Quick Response**.

    ![Event Management response](../image/Slimmed_Down_Image_Roy.png)

3.  In the Quick Response page, click the required link to perform the required action.

    If the link that you require is not available, perform one of these actions.

<table id="choicetable_ehj_lwd_lz"><tbody><tr><td id="d652798e125">

**For Remediation, define a remediation task using an Alert rule based on the selected alert**

</td><td>

1.  Navigate to **Alert Rules**.
2.  Select the required alert management rule to edit.
3.  Click **Remediation**.
4.  Click **Enable Remediation**.
5.  In the **Execution** field, select either Automatic or Manual.
6.  In the **Orchestration** workflow field, specify the remediation workflow.
    -   For **Orchestration**, in the workflow settings, select **Remediation Task \[em\_remediation\_task\]** in the **Table** field.
    -   After you finish configuring the orchestration workflow, publish it.
7.  Click **Update**.
 For further information, see [Migrate an alert action rule to an alert management rule](t_EMCreateAlertRule.md).

</td></tr><tr><td id="d652798e204">

**For Launch Application, create a web application link using an Alert rule based on the selected alert**

</td><td>

1.  Navigate to **Alert Rules**.
2.  Select the required alert management rule to edit.
3.  Click **Launcher**.
4.  Click **Enable**.
5.  In the **Display Name** field, specify a name for the link.
6.  In the **URL** field, compose the URL using data from the alert in the format: `${source}.com:${port}/${cmdb_ci.name}`
7.  Click **Update**.
 For further information, see [Migrate an alert action rule to an alert management rule](t_EMCreateAlertRule.md).

</td></tr></tbody>
</table>
## What to do next

To create a remediation task or web application link, see [Migrate an alert action rule to an alert management rule](t_EMCreateAlertRule.md).

**Parent Topic:**[View alert information](t_EMViewAlert.md)

**Related topics**  


[Launch web application from alert](t_EMLaunchAnApplication.md)

