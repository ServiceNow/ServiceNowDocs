---
title: Delete risk dependencies using the GRC: Workbench
description: When deleting risk dependencies, only the relationship between the risks is deleted. The risks themselves remain unmodified.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use entity and risk dependencies using the GRC: Workbench, Use, Risk Management, Governance, Risk, and Compliance]
---

# Delete risk dependencies using the GRC: Workbench

When deleting risk dependencies, only the relationship between the risks is deleted. The risks themselves remain unmodified.

## Before you begin

Role required: sn\_risk.manager

## Procedure

1.  Navigate to `https://myCompany.service-now.com/$grc_workbench.do`.

2.  Select the **Risk Dependencies** tab at the top, then select the **Relationships** tab below it.

3.  Search for and select a risk from the list on the left.

    Risks are organized hierarchically by entity class, then by entity.

4.  In the center tree, point to the upstream or downstream risk that should be disassociated from the selected center risk.

    As you point to the risk, a delete icon appears, click the delete icon.

5.  Click **Delete** in the confirmation dialog to confirm the deletion of the relationship.

    **Note:** Only the relationship between the risks is deleted. The risks themselves remain unmodified.


**Parent Topic:**[Use entity and risk dependencies using the GRC: Workbench](../concept/grc-workbench.md)

