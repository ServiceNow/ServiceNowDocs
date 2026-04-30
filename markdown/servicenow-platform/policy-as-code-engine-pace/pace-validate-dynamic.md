---
title: Map PaCE policies using Dynamic Mapping
description: Use Dynamic Mapping to map multiple PaCE policies against specified conditions.
locale: en-US
release: xanadu
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [PaCE mapping, Manage PaCE policies, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Map PaCE policies using Dynamic Mapping

Use Dynamic Mapping to map multiple PaCE policies against specified conditions.

## Before you begin

If you don’t have a condition created, do the following steps.

1.  Navigate to **Mappings** &gt; **Conditions**.
2.  Select **New**.
3.  Fill in the **Short description** and **Table** field, then add the conditions of the deployables you want to map.
4.  Select **Run** to preview the existing deployables that will be mapped in the condition.

    **Note:** The results are capped at 10,000 records.

5.  Select **Save**or **Continue to mapping** to navigate to the Dynamic Mapping page.

    **Note:** When you select **Continue to mapping**, the condition is pre-selected based on the condition you created, additionally you can edit or delete the condition by selecting the short description.


Role required: sn\_pace.mapping\_admin

## Procedure

1.  Navigate to **Mappings** &gt; **Dynamic Mappings**.

2.  Select **Add**.

3.  Select a document type in the **Document Type** field, then a condition in the **Condition** field.

4.  Select a policy in the **Policy** field or you can select the Search icon ![Search icon.](../image/pace-search-icon.jpg) to view and select multiple policies, then select **Map**.

5.  When you're finished, select **Done**.


## Result

The map will show up in the Dynamic Mappings list. You can delete a map on the list by selecting the box next to the Input, then select **Delete**.

