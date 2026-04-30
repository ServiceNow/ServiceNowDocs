---
title: Compliance score calculation of an entity
description: There are two ways to calculate the compliance score of an entity. The existing method includes only the entity's direct controls, whereas the new logic considers the average of immediate downstream entities along with the average of direct controls of the entity.
locale: en-US
release: yokohama
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Compliance score calculation]
breadcrumb: [Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Compliance score calculation of an entity

There are two ways to calculate the compliance score of an entity. The existing method includes only the entity's direct controls, whereas the new logic considers the average of immediate downstream entities along with the average of direct controls of the entity.

## Compliance score calculation based on direct controls

Calculating the compliance score of an entity is based on the controls that are directly associated with the entity. It is by using a simple formula:

```
Average of all direct controls of an entity
```

![Compliance score calculation based on the direct controls.](../image/compliance-score-rollup-current.png)

## Compliance score calculation rollup - existing logic

The compliance score of ACME US is the average of all its direct controls, which is `(100 + 0) ➗ 2 = 50`. Whereas while calculating the compliance score of ACME Global, the average of its direct controls is only considered, and not the average of controls associated with its downstream entities, which is `(100 + 100) ➗ 2 = 100`.

Although there’s a control associated with the downstream entity \(ACME US\), which is non-compliant, the reflection of its non-compliance status is not reflected in the parent entity \(ACME Global\) and it does not alter the overall compliance score of the parent entity \(ACME Global\).

## Compliance score calculation based on downstream entities and direct controls

Compliance score of an entity can also be calculated based on its downstream entities' compliance scores, which is the average of immediate downstream entities' compliance scores along with its direct controls, by using the formula:

```
Average [Average (downstream entities) + Average (direct controls)]
```

![Compliance score calculation based on downstream entities and direct controls.](../image/compliance-score-rollup-new-logic.png)

## Compliance score calculation rollup - new logic

In this hierarchy, the compliance score of ACME US is 50 and ACME EU is 50. This logic considers the average of the downstream entities that is ACME US and ACME EU while calculating the compliance score of ACME Global, which is `(50 + 50) ➗ 2 = 50%`. Considering the downstream entities and the direct controls of the parent entity, the compliance score is now `(50 + 100) ➗ 2 = 75%`. That is `average of ACME US and ACME EU + average of Control 5 and Control 6`.

