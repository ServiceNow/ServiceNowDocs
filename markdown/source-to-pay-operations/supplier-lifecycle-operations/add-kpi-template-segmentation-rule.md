---
title: Add KPI templates to a segmentation rule
description: Add KPI templates to a segmentation rule to define the KPIs that are generated for the suppliers in the segment when the rule runs. You must add at least one KPI template before you run the rule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/supplier-lifecycle-operations/add-kpi-template-segmentation-rule.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Supplier Lifecycle Operations, Supplier Relationship, Performance Management, KPI template, segmentation rule, Source-to-Pay Workspace]
breadcrumb: [Create segmentation rule, Configure Supplier Relationship and Performance Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Add KPI templates to a segmentation rule

Add KPI templates to a segmentation rule to define the KPIs that are generated for the suppliers in the segment when the rule runs. You must add at least one KPI template before you run the rule.

## Before you begin

Role required: sn\_slm.manager or sn\_slm.admin

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon.\) and navigate to **Lists** &gt; **Relationship management** &gt; **Segmentation rules**.

3.  In the Name column, select the segmentation rule.

4.  Select the **KPI Template** tab, and then select **Add**.\[Omitted image "add-kpi-template-segmentation-rule.png"\] Alt text: Selected option to create a new template.

5.  On the Add KPI template form, select the check box next to the KPI template and select **Add**.

    The KPI template appears in the **KPI Template** related tab for the segmentation rule.

    **Note:** The weight of the new KPI template doesn't affect the weight of the original KPI template or the weight of the KPIs that were previously created from that template. The new weight applies to KPIs that the rule creates the next time you run it. For more information, see [Run segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/run-segmentation-rule.md).


## Result

KPIs are generated on the next segmentation rule run.

**Parent Topic:**[Create segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/create-segmentation-rule-slo.md)

**Related topics**  


[KPI templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/kpi-templates.md)

[Add suppliers to a segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/add-supplier-segmentation-rule.md)

[Create segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/create-segmentation-rule-slo.md)

