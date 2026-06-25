---
title: Add KPI templates to a segmentation rule
description: You can add new KPI templates to a segmentation rule if the existing templates used for suppliers don’t meet your needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/add-kpi-template-segmentation-rule.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create segmentation rule, Configure Supplier Relationship and Performance Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Add KPI templates to a segmentation rule

You can add new KPI templates to a segmentation rule if the existing templates used for suppliers don’t meet your needs.

## Before you begin

Role required: sn\_slm.manager or sn\_slm.admin

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon.\) and navigate to **Lists** &gt; **Performance management** &gt; **Segmentation rules**.

3.  In the Name column, select the link to the segmentation rule.

4.  Select the **KPI Template** tab and select **Add**.\[Omitted image "add-kpi-template-segmentation-rule.png"\] Alt text: Selectd option to create a new template.

5.  On the Add KPI template form, select the check box next to the KPI template and select **Add**.

    The newly added supplier is shown in the **KPI Template** related tab for the segmentation rule.

    **Note:** The weight of the new KPI template doesn’t affect the original KPI template weight or the weight of the KPI that was previously created from this template. However, this change will affect any newly created KPIs that are part of this segmentation rule after you run it by selecting Execute. For more information, see [Run segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/run-segmentation-rule.md).


## Result

KPIs are generated on the next segmentation rule run.

**Parent Topic:**[Create segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/create-segmentation-rule-slo.md)

**Related topics**  


[KPI templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/kpi-templates.md)

[Add suppliers to a segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/add-supplier-segmentation-rule.md)

[Create segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/create-segmentation-rule-slo.md)

