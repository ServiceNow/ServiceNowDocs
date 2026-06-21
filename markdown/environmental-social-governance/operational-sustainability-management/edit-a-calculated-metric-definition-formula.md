---
title: Edit a calculated metric definition formula
description: Edit a formula in a calculated metric definition to update the calculation logic or apply changes to historical data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/operational-sustainability-management/edit-a-calculated-metric-definition-formula.html
release: australia
product: Operational Sustainability Management
classification: operational-sustainability-management
topic_type: task
last_updated: "2026-06-21"
reading_time_minutes: 1
breadcrumb: [Formula building in a calculated metric definition, Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Edit a calculated metric definition formula

Edit a formula in a calculated metric definition to update the calculation logic or apply changes to historical data.

## Before you begin

Roles required: sn\_esg.metric\_manager, or sn\_esg.program\_manager

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace**.

2.  Select **List** &gt; **Metrics** &gt; **Calculated metric definitions**.

3.  Open a calculated metric definition record.

4.  Select **Formula builder** from the left panel.

5.  Select **Edit**.

6.  Make the required changes to the formula in the text field.

7.  Select **Save formula**.

    The **Apply changes and save** dialog opens. The changes are applied to future data by default.

8.  If you want to apply the changes to historical data, do the following.

    1.  Select the **Apply to historical data as well** check box.

    2.  In the **Apply changes from** field, select a period.

        All data records from the selected period onward are reset to Pending and recalculated using the updated formula.

9.  Enter any relevant notes in the **Type your comments here** field.

10. Select **Save**.


## Result

The formula is saved as a new version. The new version is listed in the **Versions** related list on the calculated metric definition.

**Parent Topic:**[Formula building in a calculated metric definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/operational-sustainability-management/formula-building-at-metric-definition-and-entity-level.md)

