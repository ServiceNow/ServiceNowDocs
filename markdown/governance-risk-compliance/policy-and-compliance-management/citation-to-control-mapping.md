---
title: Association of citations to controls
description: A direct citation-to-control mapping feature that improves compliance score accuracy and provides flexibility to manage associations between controls and citations without relying on control objectives.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-11-17"
reading_time_minutes: 2
breadcrumb: [Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Association of citations to controls

A direct citation-to-control mapping feature that improves compliance score accuracy and provides flexibility to manage associations between controls and citations without relying on control objectives.

In many compliance frameworks, a single control objective may be referenced by multiple citations across different standards, regulations, or policy requirements. Without proper association management, organizations risk duplicating controls, misinterpreting coverage, or inaccurately reporting compliance. The association of citations to controls feature addresses this challenge by enabling users to associate controls with citations directly. When this feature is enabled, compliance scores update dynamically based on the status of directly associated active controls.

## Direct citation-to-control mapping for accurate compliance scoring

The new Citation to Control Mapping feature remedies this by introducing an association table called sn\_compliance\_mtm\_citation\_control, which allows direct mapping between citations and controls. This enhancement enables users to manually associate or disassociate controls with citations, ensuring flexibility and accuracy. It also improves compliance score calculations by basing them on controls rather than indirect relationships through control objectives.

To enable this feature, a property named Association of Citations to Controls Mapping is added. This property is disabled by default. To enable this feature, see [Enable associations of citation to controls mapping](../task/enable-citation-to-control-mapping.md).

## New compliance score formula

When this feature is enabled, the compliance score formula changes to:

```
Citation compliance score = Average(Child Citations) + Average(Directly Linked Controls)
```

This shift ensures that the compliance scores reflect only the relevant controls associated with each citation. For more information on compliance score calculations, see [Compliance score calculation for a citation](compliance-score-calculation-for-a-citation.md).

## UI changes to Citation page

When the Enable association of Citations to Controls Mapping property is set to Yes, the following changes appear in the Citation page:

-   You will see a related list of controls that are currently associated with that citation.
-   When you click Add to associate more controls, the system does not show all the available controls. Instead, it applies hierarchy-based eligibility rules.
-   The Add list displays the following eligible controls:
    -   All controls from control objectives directly associated with the citation.
    -   Controls from child control objectives of those directly associated control objectives \(traverse downward in the hierarchy\).
    -   Controls from grandchild control objectives, until the last level.
    -   All the independent controls \(those without any control objective\) are always eligible for association.
-   When you add controls to the citation, the compliance score will change based on the compliance or non-compliance state of the controls.

    **Note:** Controls must be active for them to be included in the compliance score calculations.


## UI changes to Control page

When the Enable association of Citations to Controls Mapping property is set to Yes, the following changes appear in the Control page:

-   You will see a related list of citations that are currently associated with that control.
-   When you click Add to associate more citations, the system does not show all citations in the instance. Instead, it applies hierarchy-based eligibility rules.
-   The Add list displays the following citations:
    -   All citations directly associated with the control objective linked to the control.
    -   Citations associated with parent control objectives \(traverse upward in the hierarchy\).
    -   Citations associated with child control objectives \(traverse downward in the hierarchy\).
    -   If the control is independent \(not linked to any control objective\), all citations are available for association.

