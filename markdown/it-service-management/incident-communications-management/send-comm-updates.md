---
title: Send communication updates
description: Update users on the latest communication on an incident through selected communication channels.
locale: en-US
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing Incident Communications, Incident Communications Management, IT Service Management]
---

# Send communication updates

Update users on the latest communication on an incident through selected communication channels.

## Before you begin

-   Role required: itil \(itil user is assigned to incident communication task\) or ia\_admin or mim\_manager or admin.
-   Activate the Notify plugin \(com.snc.notify\) if you want to send communication through SMS.
-   Set atleast one communication channel of a communication task as SMS or email.

## Procedure

1.  Navigate to **Incident Communications Management** &gt; **All**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

2.  Open an incident communication plan record.

3.  From the Incident Communication Tasks related list, open the incident communication task for which you want to send updates.

4.  In the related links, click **Send Updates**.

5.  Fill in the required information and click **Compose**.

    For sending an SMS communication, in the **From** list, select a number from which you want to send the communication. It contains a list of phone numbers derived from the selected **Provider selector** column which is a reference to the Provider selector table \[notify\_group\_selector\]. The **From** list displays phone numbers of all the groups associated with the Provider selector only when the following conditions are met:

    -   The **Manual selector** check box in the Provider selector form is selected.
    -   The value of the **Source table** field in the Provider selector is either empty or the same table that you have selected.
6.  Click **Compose**.


**Parent Topic:**[Managing Incident Communications](../concept/working-with-inci-comm-mgmt.md)

