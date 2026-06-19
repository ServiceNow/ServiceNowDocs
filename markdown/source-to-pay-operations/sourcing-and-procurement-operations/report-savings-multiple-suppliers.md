---
title: Report savings when awarding multiple suppliers
description: When awarding multiple suppliers, enter the spend and savings data for the sourcing event associated with the pipeline project.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/report-savings-multiple-suppliers.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [savings, report savings, enter spend and savings data, awarding suppliers]
breadcrumb: [Using Sourcing Pipeline Management, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Report savings when awarding multiple suppliers

When awarding multiple suppliers, enter the spend and savings data for the sourcing event associated with the pipeline project.

## Before you begin

Role required: sn\_shop.procurement\_specialist

## About this task

The sourcing event that you plan to work on, and all its associated negotiations, sourcing requests, and purchase lines must be in the Requires Decision state. When negotiations are complete for a sourcing event, you can award one or more suppliers. Awarding suppliers creates purchase requisitions for the selected suppliers and items.

## Procedure

1.  Navigate to **Source-to-Pay Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon.\) and do one of the following:

    -   Navigate to **Lists** &gt; **My work** &gt; **Sourcing events**.
    -   Navigate to **Lists** &gt; **All work** &gt; **Sourcing events**.
3.  Open the sourcing event that is in the Requires Decision state.

    \[Omitted image "pipeline-award-multiple.png"\] Alt text: Sourcing event in Requires Decision state.

4.  Select **Award multiple suppliers**.

    The Award suppliers for sourcing event page is displayed.

    \[Omitted image "pipeline-award-suppliers.png"\] Alt text: Review selection option.

5.  Select the supplier for each product you want to purchase.

6.  Select **Review selection**.

    The Review selection dialog box is displayed.

    \[Omitted image "pipeline-review-selection.png"\] Alt text: Review selection page where you select the supplier for each product.

7.  Select **Next**.

8.  Enter the spend and savings data in the **Final spend**, **Annual cost avoidance**, **Lost savings**, and **Other savings** fields.

    \[Omitted image "pipeline-award-supp-financials.png"\] Alt text: Review financials when awarding suppliers to a sourcing event.

    **Note:** The Review financials modal is displayed only if the sourcing event is associated with a pipeline project.

    The **Annual hard savings** field is auto-populated and displays the cumulative savings from all sourcing events associated with the pipeline project. This value is calculated by summing the Negotiated savings from all the selected purchase lines on the Award suppliers page.

    You can edit the **Annual hard savings** field if you’d like. If you edit the **Annual hard savings** field, a warning message appears indicating that the entered value differs from the cumulative negotiated savings on PRLs. This warning is shown only if there are negotiated savings on any PRL.

9.  Select **Submit**.


## Result

The sourcing event is moved to Closed Complete, with the individual negotiations under it moved to Closed Decided or Closed Rejected based on your selection. The awarded sourcing requests are moved to Closed Complete, with purchase requisitions automatically created for the purchase lines. In addition, the spend and savings data is updated in the associated pipeline project.

**Parent Topic:**[Using Sourcing Pipeline Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/use-pipeline-sourcing-mgmt.md)

