---
title: Approve or reject requests in Approval Hub
description: As an approver, review master data and journal entry requests in Approval Hub and approve or reject them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-approve-request.html
release: australia
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 2
keywords: [app, engine, erp, sap, rapid, deployment, pack, approval, hub]
breadcrumb: [Use, App Engine for ERP rapid deployment packs, Building low-code applications, Developing your application, Building applications]
---

# Approve or reject requests in Approval Hub

As an approver, review master data and journal entry requests in Approval Hub and approve or reject them.

## Before you begin

Role required: An MDM Orchestrator approval role. \(For more information, see [Roles used in App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-components-installed.md).\)

## About this task

Approval Hub is the unified interface where approvers review and decide on pending requests across all rapid deployment packs. For more information, see [Approval Hub rapid deployment pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-approval-hub.md).

## Procedure

1.  Navigate to **All** &gt; **My Approvals Hub** &gt; **My Approvals**.

    The **MDM Dashboard** is displayed by default. Select **ERP Dashboard** or **JE Dashboard** \(Journal Entry Dashboard\) at any time. For details about the information on the dashboards, see [App Engine for ERP Approval Hub dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-approval-hub-dashboards.md).

2.  Adjust the time frame \(default is **Last Month**\), by selecting the picker and choosing an option, such as last 7 days or all time.

    \[Omitted image "aes-erp-rdp-approve-hub1.png"\] Alt text: Approval hub with mdm dashboard displayed.

3.  View information about MDM, ERP, and journal entry approvals.

4.  Select the ERP requests, MDM requests, or JE requests icon.

    \[Omitted image "aes-erp-rdp-approve-hub2.png"\] Alt text: ERP requests, MDM requests, and JE requests icons.

    Individual requests are displayed as tiles.

5.  Filter the tiles as needed.

    For example, filter the MDM requests to show only update requests or filter the journel entry requests to show only expense requests.

6.  If you're ready to make a decision, select **Accept** or **Reject** on a request tile.

    \[Omitted image "aes-erp-rdp-approve-hub3.png"\] Alt text: Tiles filtered to show only MDM create requests and accept/reject buttons highlighted.

    If you reject a request, you must enter a reason.

7.  For more information, select a tile.

    \[Omitted image "aes-erp-rdp-approve-hub4.png"\] Alt text: A single request record showing options and fields.

    The request record contains the requestor details, the enrichment data, the governance review and compliance checks, and an activity timeline of all changes and approvals at each stage.

8.  To gather more content before acting, select the virtual agent icon to use the conversational agent.

    Ask questions using natural language about all, some, or one request. For example, ask which requests are pending, which have waited longest, or which are critical today. Approve and reject controls are available within the conversation.

    \[Omitted image "aes-erp-rdp-approve-hub5.png"\] Alt text: Virtual agent chat conversation about obtaining a list of the most urgent requests.

9.  Review the activity timeline.

    Examine the history to see the changes made during enrichment \(old value and new value\), the governance comments, and the timestamps for each stage.

10. Accept or reject the request.

    -   **Accept**

        The record is created or updated in the ERP system.

    -   **Reject**

        Provide a reason for rejection, such as missing documentation, a duplicate record, or incorrect information. The requestor receives a notification and can correct and resubmit the request.


## Result

After final approval, MDM Orchestrator hands the record off to your ERP integration layer, for example Integration Hub spokes or Zero Copy Connector for ERP, for creation in the target ERP system.

**Parent Topic:**[Using App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-use.md)

