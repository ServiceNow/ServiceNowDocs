---
title: Edit a calculated metric definition formula
description: Edit a formula in a calculated metric definition to update the calculation logic or apply changes to historical data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/environmental-social-governance/edit-a-calculated-metric-definition-formula.html
release: australia
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 1
breadcrumb: [Formula building in a calculated metric definition, Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Edit a calculated metric definition formula

Edit a formula in a calculated metric definition to update the calculation logic or apply changes to historical data.

## Before you begin

Roles required: sn\_esg.metric\_manager, or sn\_esg.program\_manager

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace**.

2.  Select the List icon \(\[Omitted image "icon-lists.png"\] Alt text:\).

3.  In the **Lists** tab, select**Metrics** &gt; **Calculated metric definitions**.

4.  Open a calculated metric definition record.

5.  Select **Formula** &gt; **Formula builder** from the navigation panel.

6.  Select **Edit**.

7.  Make the required changes to the formula in the text field.

8.  Select **Save formula**.

9.  In the **Apply changes and save** dialog box, apply the changes to historical data as well as future data.

    1.  Select the **Apply to historical data as well** check box.

    2.  In the **Apply changes from** field, select a time period from the drop-down list.

        All data records from the selected period onward will be reset to Pending and recalculated using the updated formula.

10. Enter any relevant notes in the **Type your comments here** field.

11. Select **Save**.


## Result

The formula is saved as a new version. The new version is listed in the **Versions** related list on the calculated metric definition.

**Parent Topic:**[Formula building in a calculated metric definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/environmental-social-governance/formula-building-at-metric-definition-and-entity-level.md)

