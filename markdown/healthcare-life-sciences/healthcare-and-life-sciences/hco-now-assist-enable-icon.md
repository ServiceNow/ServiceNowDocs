---
title: Enable the Now Assist icon in Care Team Mobile
description: Set up the Now Assist icon within Care Team Mobile so you can leverage the Request care team assistance agentic workflow in Care Team Mobile.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/healthcare-life-sciences/healthcare-and-life-sciences/hco-now-assist-enable-icon.html
release: zurich
product: Healthcare and Life Sciences
classification: healthcare-and-life-sciences
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for Healthcare Operations, Healthcare and Life Sciences]
---

# Enable the Now Assist icon in Care Team Mobile

Set up the Now Assist icon within Care Team Mobile so you can leverage the **Request care team assistance** agentic workflow in Care Team Mobile.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile Builder**.

2.  Select the **Care Team Mobile** application scope.

3.  In **Screens**, select **Care Team Launcher**.

4.  In **Quick Action Function Instance**, select **New**.

5.  In **Properties**, enter a name for the icon.

    For example, Now Assist for Care Team icon.

6.  Enter a display label to identify what this icon displays as for users.

7.  Set **Icon** to **spark-solid \(AIS\)**.

8.  Set **Function** to **Agent Chat**.

    Ensure that the Application scope value is **Care Team Mobile**.

9.  Select **Save**.

10. Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistants** &gt; **Manage Assistants**.

11. Select the Now Assist in Virtual Agent assistant \(default\).

12. In **Display Experiences**, navigate to the **Mobile Apps** tab.

13. In **Chat Launcher Functions**, select **Edit chat experience** and then select **Standard chat**.

14. Select **Apply**.

15. In **Prominent Action Button Override**, select **Edit chat experience** and then select **Standard chat**.

16. Select **Apply**.


## Result

The Now Assist icon is accessible within Care Team Mobile. Users can select this icon to create support cases using the conversational abilities of Virtual Agent.

