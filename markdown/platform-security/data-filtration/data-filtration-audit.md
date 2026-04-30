---
title: Data filtration debugging
description: Use the session log to see how data filtration affects your records and debug user access issues.
locale: en-US
release: xanadu
product: Data Filtration
classification: data-filtration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data filtration, Access Management]
---

# Data filtration debugging

Use the session log to see how data filtration affects your records and debug user access issues.

## Before you begin

Role required: admin

Output information appears in the session logs when users access records. You can use this logging information along with impersonation to learn why users see or do not see records. You can then use that information to adjust your data filtration rules and ensure that users only see what you intend.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Debugging** &gt; **Debug All Security**.

    The **Script Debugger** opens in a new browser tab or window.

    ![Session log window](../image/session-log-window.png)

2.  In the **Script Debugger** window, select the **Session Log** tab.

3.  In another browser tab or window, impersonate a user to troubleshoot that user's access.

    **Note:** Impersonation allows an admin to see an instance with another users settings and access. For details on impersonation, see [Impersonate a user](https://www.servicenow.com/docs/access?context=c_ImpersonateAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

4.  While impersonating a user, access a list or record where you see unexpected behavior.

    This behavior may be a record the user sees, but should not see, or a list of records that are not appearing as expected for a user.

    After accessing records with the impersonated user, you should begin to see output in the session debugger.

5.  Look for data filtration information in the session debugger.

    ![Failed logging information created by a data filter](../image/df-log-fail.png)

    This example shows two log messages where a data filter denied access to records. The log entries appear as red text, and include why the data filter denied access, as well as the sys\_id of the data filter. You can click on this sys\_id to open the data filtration record.

    ![Passed logging information created by a data filter](../image/df-log-pass.png)

    This example shows a log message where a data filter allowed access to a record. These log entries appear as green text. As with the first message, you can click this sys\_id to open the data filtration record.

6.  Use this information to make any adjustments to your data filtration rules.

    Repeat these steps to refine your rules and give users the access they need.


