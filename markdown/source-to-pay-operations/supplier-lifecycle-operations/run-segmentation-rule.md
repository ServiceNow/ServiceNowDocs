---
title: Run segmentation rule
description: Run a segmentation rule to create and activate KPIs corresponding to the KPI templates and suppliers in that segment. This action also creates new collection tasks and assigns them to suppliers to collect their KPI data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/run-segmentation-rule.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Supplier Relationship and Performance Management, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Run segmentation rule

Run a segmentation rule to create and activate KPIs corresponding to the KPI templates and suppliers in that segment. This action also creates new collection tasks and assigns them to suppliers to collect their KPI data.

## Before you begin

Role required: sn\_kpi.admin or sn\_slm.manager or sn\_slm.admin

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon.\) and navigate to **Lists** &gt; **Performance management** &gt; **Segmentation rules**.

3.  In the Name column, select the link to the segmentation rule.

4.  Select **Execute**.\[Omitted image "run-segmentation-rule.png"\] Alt text: Selected Execute button for running a segmentation rule.


## Result

Running the segmentation rule does the following:

-   Generates KPIs and KPI collection tasks from the KPI templates in the segment if they were never generated before for the newly added suppliers.
-   Sets the KPIs linked to this segment's KPI templates to active and creates new collection tasks for these KPIs.
-   Assigns the new collection tasks to suppliers in this segment.
-   KPI scores will not appear in the performance dashboard until those collection tasks are completed.

**Note:** If the number of suppliers to be processed in the segmentation rule is too large, it may lead to a risk of a timeout.

**Parent Topic:**[Using Supplier Relationship and Performance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/using-supplier-relationship-and-performance-management.md)

**Related topics**  


[Using Supplier Relationship and Performance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/using-supplier-relationship-and-performance-management.md)

[Complete a KPI collection task from the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/complete-kpi-task-spw.md)

[Complete a KPI collection task from the Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/complete-kpi-task-scp.md)

[View KPI data from the List page of the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/view-kpi-data-slo.md)

[Manage supplier KPIs from the supplier record page of the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/kpi-mgmt-tab-supplier.md)

[View supplier performance dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/view-supplier-performance-dashboard.md)

[Create action plan for KPIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/create-action-plan-for-kpis.md)

