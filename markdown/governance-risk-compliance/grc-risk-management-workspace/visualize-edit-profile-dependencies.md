---
title: Visualize and edit entity dependencies using the GRC: Workbench
description: The GRC: Workbench gives GRC administrators a graphical interface to create entity dependencies. These relationships enable consistent entity and risk mapping and modeling across the enterprise.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use entity and risk dependencies using the GRC: Workbench, Use, Risk Management, Governance, Risk, and Compliance]
---

# Visualize and edit entity dependencies using the GRC: Workbench

The GRC: Workbench gives GRC administrators a graphical interface to create entity dependencies. These relationships enable consistent entity and risk mapping and modeling across the enterprise.

## Before you begin

Role required: sn\_grc.manager

## Procedure

1.  Navigate to `https://myCompany.service-now.com/$grc_workbench.do`.

2.  Select the **Model Setup** tab at the top, then select the **Dependency** tab below it.

3.  Search for and select an entity from the list on the left.

    Entities are organized hierarchically by entity class, then by entity types.

4.  After selecting an entity from the left, the entity is displayed in the center with its direct upstream and downstream dependencies.

    On the right, eligible entities that can be added as upstream or downstream dependencies are listed.

5.  Perform one of the following actions.

<table id="choicetable_ar5_2j2_pw"><tbody><tr><td id="d147941e100">

**To add an upstream entity dependency**

</td><td>

Drag an eligible upstream entity from the list of eligible entities on the right and drop it on the top half of the entity in the center of the page.

</td></tr><tr><td id="d147941e109">

**To add a downstream entity dependency**

</td><td>

Drag an eligible downstream entity from the list of eligible entities on the right and drop it on the bottom half of the entity in the center of the page.

</td></tr></tbody>
</table>    The entities are removed from the right menu when moved to the center of the page.


**Parent Topic:**[Use entity and risk dependencies using the GRC: Workbench](../concept/grc-workbench.md)

