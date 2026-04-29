---
title: Delete entity dependencies using the GRC: Workbench
description: When deleting entity dependencies, only the relationship between the entities is deleted. The entities themselves remain unmodified.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use entity and risk dependencies using the GRC: Workbench, Use, Risk Management, Governance, Risk, and Compliance]
---

# Delete entity dependencies using the GRC: Workbench

When deleting entity dependencies, only the relationship between the entities is deleted. The entities themselves remain unmodified.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `https://myCompany.service-now.com/$grc_workbench.do`.

2.  Select the **Model Setup** tab at the top, then select the **Dependency Map** tab below it.

3.  Search for and select the desired entity from the list on the left.

    After selecting an entity from the left, the entity is displayed in the center with its direct upstream and downstream dependencies.

4.  In the center tree, point to the upstream or downstream risk that should be disassociated from the selected center risk.

    As you point to the risk, a delete icon appears, click the delete icon.

5.  Click **Delete** in the confirmation dialog to confirm the deletion of the relationship.

    **Note:** Only the relationship between the entities is deleted. The entities themselves remain unmodified.


**Parent Topic:**[Use entity and risk dependencies using the GRC: Workbench](../concept/grc-workbench.md)

