---
title: Factors affecting compliance score for citations
description: Compliance scores for citations dynamically change based on changes to controls and control objectives.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-11-17"
reading_time_minutes: 3
breadcrumb: [Association of citations to controls, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Factors affecting compliance score for citations

Compliance scores for citations dynamically change based on changes to controls and control objectives.

## Property dependency

-   When the system property, Enable association of Citations to Controls Mapping is Off, compliance scores are calculated using the old formula: Average of child citations + Average of associated control objectives.
-   When the property is ON, compliance scores use the new formula: \(Average of child citations + Average of directly linked controls\) ÷ 2.
-   After enabling the property:
    -   Run the scheduled job Calculate All Citations and Authority Documents Compliance Score to recalculate scores.
    -   Disable the periodic job Compliance Score V2 during recalculation to avoid conflicts.

## Manual actions

When the system property is enabled, the following manual actions affect compliance score for citations:

1.  Adding a control to a citation: Adding a control directly to a citation recalculates the citation’s compliance score using the new formula.

    Example: A citation currently has two controls, and both are compliant, so its compliance score is 100%. When you add a non-compliant control, the new score becomes the average of the two compliant controls and one non-compliant controls: \(100% + 100 + 0%\) ÷ 3 = 33%.

2.  Removing a control from a citation: Removing a control triggers recalculation based on remaining controls.

    Example: A citation has three controls: two compliant and one non-compliant, giving it a compliance score of 66%. If you remove the non-compliant control, the score recalculates to 100% because only the two compliant controls remain.

3.  Adding a citation to a control: Adding a citation to a control updates compliance scores for that citation.

    Example: A citation initially has no controls, so its compliance score is 0%. When you link a compliant control to it, the score updates to 100%.

4.  Remove citation from a control: Removing a citation from a control recalculates compliance scores.

    Example: A citation has two controls, and both are compliant, resulting in a compliance score of 100%. If you remove one of the compliant controls, the score remains 100%, as the remaining control is still compliant, though fewer controls are associated.


## Changes to controls

1.  Control creation due to adding entity or entity types to control objectives: When a new control is created for a control objective that is directly linked to a citation, it is automatically associated with all citations linked to that control objective.

    Example: Adding an entity to a control objective generates new controls. These controls are auto-linked to all citations associated with that control objective, updating their compliance scores.

2.  Control deletion: When a control is deleted from a control objective that is associated to a citation, the compliance score of all the associated citations changes.

    Example: A citation is linked to one control objective that has two controls: one compliant and one non-compliant \(score = 50%\). Deleting the non-compliant control updates the score to 100%.

3.  Control status: Changing a control’s status \(Compliant, Non-Compliant, Not Applicable\) recalculates compliance scores for all associated citations.

    Example: When a citation has only one control with compliant status, the compliance score is 100%. When the status changes to non-compliant, the new score is 0%.

4.  Control weight change: If weighted average is enabled, changing a control’s weight impacts compliance score.

    Example: A compliant control with weight of 100 and a non-compliant control with weight 10 changes the compliance score. So compliance score = \(100 ÷ 110\) × 100 = 91%.

5.  Control active flag change: Activating or deactivating a control recalculates compliance scores for associated citations.

    Example: Deactivating a compliant control reduces the citation’s score because fewer controls remain in calculation.


## Changes to citations

1.  Citation deletion: When a citation is deleted, all the citation-to-control associations are deleted. No recalculation of compliance score for the citation itself, as it’s deleted. Authority document scores may update internally.
2.  Citation associated to a control objective: When a citation is associated to a control objective, all the L1 controls from the control objective are added to the citation and the compliance score is recalculated.

    Example: Linking a citation to a new control objective adds its controls, changing the citation’s compliance score.

3.  Citation disassociated from a control objective: When a citation is disassociated from a control objective, automatically added controls are deleted. The manual controls \(flagged as “outside hierarchy”\) are not deleted. The compliance score is recalculated.

    Example: Removing a control objective association deletes automatically-added controls but keeps manually added controls, updating the citation’s compliance score accordingly.


## Additional notes

-   Manual associations are flagged as Associated Manually = True and are never auto-deleted.
-   When controls go outside hierarchy due to disassociation, the system displays an info message listing those controls for user review.
-   All compliance breakdowns, dashboards, and widgets now source data from the M2M table instead of control objective hierarchy.

