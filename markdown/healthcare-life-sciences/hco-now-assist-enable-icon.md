---
title: Enable the Now Assist icon in Care Team Mobile
description: Set up the Now Assist icon within Care Team Mobile so you can leverage the Request care team assistance agentic workflow in Care Team Mobile.
locale: en-US
release: zurich
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

6.  Set **Icon** to **spark-solid \(AIS\)**.

7.  Set **Function** to **Agent Chat**.

    Ensure that the Application scope value is **Now Mobile**.

8.  Select **Save**.

9.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistants** &gt; **Manage Assistants**.

10. Select the Now Assist in Virtual Agent assistant.

11. In **Display Experiences**, navigate to the **Mobile Apps** tab.

12. In **Chat Launcher Functions**, select **Edit chat experience** and then select **Standard chat**.

13. Select **Apply**.

14. In **Prominent Action Button Override**, select **Edit chat experience** and then select **Standard chat**.

15. Select **Apply**.


## Result

The Now Assist icon is accessible within Care Team Mobile. Users can select this icon to create support cases using the conversational abilities of Virtual Agent.

