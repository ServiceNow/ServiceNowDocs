---
title: Visualize and edit risk dependencies using the GRC: Workbench
description: The GRC: Workbench gives GRC administrators a graphical interface to create risk dependencies. These relationships enable consistent entity and risk mapping and modeling across the enterprise.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use entity and risk dependencies using the GRC: Workbench, Use, Risk Management, Governance, Risk, and Compliance]
---

# Visualize and edit risk dependencies using the GRC: Workbench

The GRC: Workbench gives GRC administrators a graphical interface to create risk dependencies. These relationships enable consistent entity and risk mapping and modeling across the enterprise.

## Before you begin

Role required: sn\_risk.manager

## Procedure

1.  Navigate to `https://myCompany.service-now.com/$grc_workbench.do`.

2.  Select the **Risk Dependencies** tab at the top, then select the **Relationships** tab below it.

3.  Search for and select a risk from the list on the left.

    Risks are organized hierarchically by entity class, then by entity.

4.  After selecting a risk from the left, the risk is displayed in the center with its direct upstream and downstream dependencies.

    On the right, eligible risks that can be added as upstream or downstream dependencies are listed.

5.  Perform one of the following actions.

<table id="choicetable_ar5_2j2_pw"><tbody><tr><td id="d161002e100">

**To add an upstream risk dependency**

</td><td>

Drag an eligible upstream risk from the list of eligible risks on the right and drop it on the top half of the risk in the center of the page.

</td></tr><tr><td id="d161002e109">

**To add a downstream risk dependency**

</td><td>

Drag an eligible downstream risk from the list of eligible risks on the right and drop it on the bottom half of the risk in the center of the page.

</td></tr></tbody>
</table>
**Parent Topic:**[Use entity and risk dependencies using the GRC: Workbench](../concept/grc-workbench.md)

