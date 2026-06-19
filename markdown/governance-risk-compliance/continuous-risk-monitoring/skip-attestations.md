---
title: Skip Attestations
description: Skip Attestations lets you bypass the attestation stage for all controls in a package. When enabled \(before implementation\), controls move directly from Draft to Review, attestation-related UI elements are hidden, and Review/Monitor actions replace attestation workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/continuous-risk-monitoring/skip-attestations.html
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: concept
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [CAM workflow configuration, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Skip Attestations

Skip Attestations lets you bypass the attestation stage for all controls in a package. When enabled \(before implementation\), controls move directly from Draft to Review, attestation-related UI elements are hidden, and Review/Monitor actions replace attestation workflows.

To skip the attestation stage for all controls in a package, select **Skip attestations** in the package configuration form.

\[Omitted image "skip-attestations.png"\] Alt text: Package configuration form with the Skip attestations option selected

This option is editable when the package is in the Prepare, Categorize, or Select step. After controls are created in the Implement step, the configuration becomes read-only.

When enabled, the following changes apply to all controls generated from this package: The **Attest** button isn't available in any view: form view, list view, related list view, hierarchical grid view, and classic view.

-   Controls move directly from Draft to Review instead of passing through the attestation stage.
-   The **Review** button is available in the controls list view in the CAM workspace. The **Review** button appears only when Skip attestations is enabled for the package and at least one control is in Draft state. When selected, the system reads each control's package configuration and moves only eligible controls to Review; controls from packages where Skip attestations is not enabled are skipped.
-   The **Monitor** button is available in the controls list view and related list view in the CAM workspace. The **Monitor** button appears only when at least one control is in Review state.
-   The following attestation-related UI elements are hidden on control and control requirement records:
    -   Attestations related list on the control record
    -   Attestation widgets on the control overview page
    -   Attestations related list on the control requirement record
    -   Attestation section in the control requirement details view

This configuration applies only to controls generated from packages where Skip attestations is enabled. Controls from other packages, including other CAM packages where this option is not selected, continue to follow the standard attestation workflow and are not affected by this setting. Standard compliance controls on instances without CAM are also unaffected.

## Edit control status

When attestation is skipped for a package, you can directly edit the status of a control or control requirement. The available status values are Compliant, Non-Compliant, and Not Applicable.

The following role-based rules determine who can edit the status and when:

-   Control Owner or System Owner can edit the status when the control is in Draft state.
-   ISSO, ISSM, and CAM Admin can edit the status when the control is in Review state.

An implementation statement is required before changing the status of a control or control requirement. The status change is blocked if no implementation statement is present.

The following validation rules apply when setting a status to Compliant:

-   A control cannot be set to Compliant if one or more of its control requirements is Non-Compliant.
-   A control or control requirement cannot be set to Compliant if an open issue is associated with it.

The following parent-child syncing rules apply when status changes:

-   When a control requirement is set to Non-Compliant, the parent control's status is automatically updated to Non-Compliant.
-   When a control is set to Compliant, control requirements with an empty status are automatically updated to Compliant.

