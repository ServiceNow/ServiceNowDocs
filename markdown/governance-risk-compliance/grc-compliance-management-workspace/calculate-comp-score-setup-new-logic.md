---
title: Set up the steps required for entity compliance score calculation
description: Enable the system property and run the on-demand job to calculate the compliance score of an entity based on its downstream entities' compliance scores and also its direct controls.
locale: en-US
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Compliance score calculation of an entity, Use, GRC Compliance workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Set up the steps required for entity compliance score calculation

Enable the system property and run the on-demand job to calculate the compliance score of an entity based on its downstream entities' compliance scores and also its direct controls.

## Before you begin

Role required: sn\_compliance.admin, sn\_compliance.manager

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **Properties**.

2.  Select the **Entity hierarchy based scoring** property to set it to **true**.

    By default the property is set to false. When it is false, the compliance score is calculated based on direct controls, which is the average of the controls that are directly associated with the entity. See [Compliance score calculation of an entity](../concept/compliance-score-calculation-pc-ws.md).

    However, if you want to calculate the compliance score of an entity based on its downstream entities and direct controls, then you must set the property to true. There can be a scenario where you might have to update the existing entities' compliance score by this new logic. For this purpose, there is a scheduled job that you must execute manually whenever you want to calculate the compliance score.

3.  To execute the scheduled job, navigate to **All** &gt; **Scheduled Definition** &gt; **Scheduled Jobs**.

4.  Select the **Update compliance scores for hierarchy entities** on-demand job from the list.

    Execute the **Update compliance scores for hierarchy entities** job on demand whenever you are switching the value in the preceding property so that the compliance score of all the entities can be recalculated honoring the property's value.

    Failing to run the on-demand job after changing the value in the property leads to inconsistencies in the calculation of compliance scores of entities.

    **Note:** Whenever you are executing the **Update compliance scores for hierarchy entities** job you must deactivate the **Compliance Score V2** scheduled job until the execution of the **Update compliance scores for hierarchy entities** job is complete. This step is a manual intervention that you must do to streamline the process of compliance score calculation for an entity.

5.  Select **Execute Now** in the Scheduled Script Execution Update compliance scores for hierarchy entities.


