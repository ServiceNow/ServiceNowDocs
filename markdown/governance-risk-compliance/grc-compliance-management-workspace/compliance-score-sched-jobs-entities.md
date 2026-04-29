---
title: Determining the logic in calculating compliance score
description: Determining the calculation of an entity's compliance score, either by its direct controls or based on its downstream entities and direct controls, is based on the Entity hierarchy based scoring property.
locale: en-US
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Compliance score calculation of an entity, Use, GRC Compliance workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Determining the logic in calculating compliance score

Determining the calculation of an entity's compliance score, either by its direct controls or based on its downstream entities and direct controls, is based on the **Entity hierarchy based scoring** property.

## Calculating entity score based on the property

The **Compliance Score V2** scheduled job runs at a periodical interval of every two minutes. When the compliance status of a control changes, the job picks up the record in its next scheduled run to process its compliance in an order. Thereafter, an entry is created in the compliance score table \[sn\_compliance\_compliance\_score\].

The point at which the compliance status of a control changes and the calculation of the score at the entity level gets impacted is a trigger point.

## Compliance score update scenarios for an entity based on the average of direct controls and average of downstream entities

Trigger points at which the compliance score of an entity is impacted and the entity record is added to the compliance score table:

1.  If one of the downstream entity is deleted, then the entity's compliance score is recalculated. If the **Entity hierarchy based scoring** property is true, then the parent entity's compliance score is calculated based on the average of its downstream entities and also the average of its direct controls. On the other hand, if the property is false, then the compliance score is calculated based on the average of its direct controls only.
2.  When an upstream entity is deleted in the hierarchy.
3.  When a downstream entity or an upstream entity is added in the hierarchy.
4.  When a downstream entity or an upstream entity is updated in the hierarchy.
5.  When an entity becomes active.
6.  When an entity is inactivated.
7.  When a control is added to an entity or deleted from an entity.
8.  When the control's status changes.

The **Compliance Score V2** scheduled job picks up the records from the compliance score table to calculate the score. Based on the **Entity hierarchy based scoring** property value, the logic in calculating the entity's compliance score is determined. For more information, see [Properties installed with GRC: Policy and Compliance Management](../../grc-policy-and-compliance/reference/r_InstallWPolAndCompl.md#).

