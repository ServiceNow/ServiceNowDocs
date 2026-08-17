---
title: Enable the ServiceNow Otto icon in Care Team Mobile
description: Set up the ServiceNow Otto icon within Care Team Mobile so you can leverage the Request care team assistance agentic workflow in Care Team Mobile.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-now-assist-enable-icon.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow Otto for Care Team Operations, Healthcare and Life Sciences]
---

# Enable the ServiceNow Otto icon in Care Team Mobile

Set up the ServiceNow Otto icon within Care Team Mobile so you can leverage the **Request care team assistance** agentic workflow in Care Team Mobile.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Builder**.

2.  Select the **Care Team Mobile** application scope.

3.  In **Screens**, select **Care Team Launcher**.

4.  In **Quick Action Function Instance**, select **New**.

5.  In **Properties**, enter a name for the icon.

    For example, ServiceNow Otto for Care Team Operations icon.

6.  Enter a display label to identify what this icon displays as for users.

7.  Set **Icon** to **Sparkmoji \[Otto\]**.

8.  Set **Function** to **Agent Chat**.

    Ensure that the Application scope value is **Care Team Mobile**.

9.  Select **Save**.

10. Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistants** &gt; **Manage Assistants**.

11. Select the ServiceNow Otto for Virtual Agent assistant \(default\).

12. In **Display Experiences**, navigate to the **Mobile Apps** tab.

13. In **Chat Launcher Functions**, select **Edit chat experience** and then select **Standard chat**.

14. Select **Apply**.

15. In **Prominent Action Button Override**, select **Edit chat experience** and then select **Standard chat**.

16. Select **Apply**.


## Result

The ServiceNow Otto icon is accessible within Care Team Mobile. Users can select this icon to create support cases using the conversational abilities of Virtual Agent.

