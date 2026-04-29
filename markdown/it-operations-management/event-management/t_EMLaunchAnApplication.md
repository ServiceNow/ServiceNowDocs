---
title: Launch web application from alert
description: You can launch a web application from an alert that matches the conditions set in an alert action rule.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Launch web application from alert

You can launch a web application from an alert that matches the conditions set in an alert action rule.

## Before you begin

Create an alert action rule that is configured to prepare a URL when the conditions that you stipulate are met. For example, based on the results when the alert parameters are resolved, this feature can open a Knowledge Base article or construct a URL.

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

Right-click an alert in All Alerts or the Alert list in the Event Management Dashboard \(for instances upgraded from a release before Orlando\), and choose **Quick Response**. Click the required link to launch the web application that was configured in the alert action rule. For further information, see [Migrate an alert action rule to an alert management rule](t_EMCreateAlertRule.md).

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Alerts**.

2.  Right-click the required alert and select **Quick Response**.

    A window appears with a list of available web applications that were configured in the alert action rule and the filter that matches the alert. To see the target URL, point to the cursor over the application name.

    **Note:** If one or more of the alert action rule parameters cannot be resolved, the related application name appears in black. When the alert parameters are resolved, then the application name becomes a link.

3.  Click the name of an application to open the URL in another tab or window in your browser.


## Example

A common use case is launch in context to the source management system.

Other examples include to search in knowledge bases, not only within ServiceNow, but externally as well. Any URL-based action can utilize the alert parameters and the URLs can refer to wikis, messaging services, REST APIs, and so on.

**Parent Topic:**[Using Event Management](../concept/user-guide.md)

**Related topics**  


[Migrate an alert action rule to an alert management rule](t_EMCreateAlertRule.md)

[Apply a quick response in an alert](apply-quick-response-in-alert.md)

