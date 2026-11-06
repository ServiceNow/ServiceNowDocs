---
title: Send communication updates
description: Update users on the latest communication on an incident through selected communication channels.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-communications-management/send-comm-updates.html
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Managing incident communications, Incident Communications Management, IT Service Management]
---

# Send communication updates

Update users on the latest communication on an incident through selected communication channels.

## Before you begin

-   To send communication through SMS, the Notify plugin \(com.snc.notify\) must be active.
-   At least one communication channel of the communication task must be set to SMS or email.

Role required: itil \(assigned to the incident communication task\), ia\_admin, mim\_manager, or admin

## Procedure

1.  Navigate to **Incident Communications Management** &gt; **All**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/service-operations-workspace/redirect-ui16-module-links-sow.md).

2.  Open an incident communication plan record.

3.  From the Incident Communication Tasks related list, open the incident communication task for which you want to send updates.

4.  In the related links, select **Send Updates**.

5.  Fill in the required information.

    To send an SMS communication, in the **From** list, select the number from which to send the communication. The list contains phone numbers derived from the selected **Provider selector** column, which references the Provider selector table \[notify\_group\_selector\]. The **From** list displays phone numbers of all the groups associated with the Provider selector only when the following conditions are met:

    -   The **Manual selector** check box in the Provider selector form is selected.
    -   The value of the **Source table** field in the Provider selector is either empty or the same table that you have selected.
6.  Select **Compose**.


**Parent Topic:**[Managing incident communications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/working-with-inci-comm-mgmt.md)

