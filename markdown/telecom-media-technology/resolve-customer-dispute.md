---
title: Resolve a customer dispute and record the dispute analysis
description: Resolve customer disputes by creating resolution tasks, documenting dispute analysis, and proposing solutions. Complete this stage after investigation and before closure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/resolve-customer-dispute.html
release: australia
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 2
keywords: [resolve, dispute analysis, dispute analysis, customer dispute management]
breadcrumb: [Use Customer DIspute Management, Use, Customer Service Problem Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Resolve a customer dispute and record the dispute analysis

Resolve customer disputes by creating resolution tasks, documenting dispute analysis, and proposing solutions. Complete this stage after investigation and before closure.

## Before you begin

Role required: sn\_telco\_adr\_mgmt.manager

## About this task

This stage in the Customer Dispute Management \(CDM\) playbook focuses on implementing the resolution tasks and documenting the dispute analysis. Both activities must be completed before moving the dispute to closure.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the lists \(\[Omitted image "Lists.png"\] Alt text: Lists Icon.\) icon.

3.  Navigate to **Customer Dispute Management** &gt; **All**.

4.  Open the CDM case record.

5.  To implement the resolution, on the Resolution stage, select **Create tasks** and complete the task fields.

    |Field|Description|
    |-----|-----------|
    |Opened on|Date when the task was created|
    |Priority|Priority level of the resolution task|
    |Assigned to|User responsible for completing the task|
    |State|Current state of the task|
    |Short description|Brief summary of the work to be done|
    |Description|Detailed explanation of the work to be done|

6.  Select **Save**.

    Created tasks appear in a grid showing number, opened date, subject, assigned to, and priority. You can filter, search, and sort this grid.

7.  Mark all resolution tasks complete.

    Open each task, update the state to complete, and save the task.

8.  Select **Continue**.

9.  Select **Add dispute analysis** and complete the dispute analysis fields.

    |Field|Description|
    |-----|-----------|
    |**Category**|General category of the issue.|
    |**Subcategory**|Specific subcategory within the selected category|
    |**Reason**|Dispute reason.|
    |**Products identified**|Product or products associated with the dispute.|
    |**Assignment group**|Group responsible for the affected product line.|

10. Select **Save**.

11. Select **Mark complete**.

    The dispute moves to the Closure stage.

12. Select **Continue**.


## Result

The system sends the customer an email that summarizes the dispute, investigation findings, and proposed resolution. Based on the customer response, you can close the dispute. For more information, see [Close a customer dispute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/close-customer-dispute.md).

**Parent Topic:**[Using Customer Dispute Management case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/use-alternative-dispute-resolution-case.md)

**Related topics**  


[Create a Customer Dispute Management case]()

[Investigate customer disputes]()

[Close a customer dispute]()

[View a Customer Dispute Management case record]()

[Customer Dispute Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/alternative-dispute-resolution.md)

