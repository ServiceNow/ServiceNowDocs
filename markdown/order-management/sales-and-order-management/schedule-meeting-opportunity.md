---
title: Schedule a meeting from an opportunity
description: Schedule a client meeting directly from an opportunity record to associate it with the opportunity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/schedule-meeting-opportunity.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 1
breadcrumb: [Opportunity Management, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Schedule a meeting from an opportunity

Schedule a client meeting directly from an opportunity record to associate it with the opportunity.

## Before you begin

-   The Meetings plugin \(sn\_meeting\_mgmt\) must be installed. This plugin is installed automatically as a dependency of the Opportunity Management data model plugin.
-   The opportunity must be in a non-closed state.

Role required: sn\_meeting\_mgmt.meeting\_creator

## About this task

When you schedule a meeting from an opportunity, the system automatically associates the meeting with that opportunity. The meeting then appears in the opportunity **Meetings** tab.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** \[Omitted image "list-outline-24.svg"\] Alt text: view.

2.  In the **Opportunity - All** list, open the opportunity record.

3.  In the opportunity header, select **Create** &gt; **Meeting**.

    The **Meeting** option is only visible when you have permission to create meetings. It is hidden when the opportunity is in a closed state.

4.  Complete the meeting form.

    **Note:**

    The meeting is automatically associated with the opportunity, no manual linking is required.

5.  Select **Save**.


## Result

The meeting is created and linked to the opportunity. It appears in the **Meetings** tab of the opportunity record.

## What to do next

To view all meetings for the opportunity, select the **Meetings** tab.

**Note:** The **Meetings** tab displays both meetings linked directly to the opportunity and meetings linked to the opportunity's touchpoints.

**Parent Topic:**[Using Opportunity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/opportunity-mgmt-using.md)

