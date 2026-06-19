---
title: Request control tailoring
description: Control tailoring requests enable you to modify baseline controls for an authorization package after the Select step without reverting the package to earlier workflow steps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/continuous-risk-monitoring/request-control-tailoring.html
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Implementing controls and assessment objectives in CAM, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Request control tailoring

Control tailoring requests enable you to modify baseline controls for an authorization package after the Select step without reverting the package to earlier workflow steps.

Without control tailoring requests, modifying baseline controls after the Select step requires moving the package back to Select, which resets the control lifecycle for all controls in the package. This requires reimplementing and retesting all controls even when changes affect only a small subset. Control tailoring requests allow incremental modifications by applying only delta changes to the package.

Control tailoring requests let you add new controls or update existing control configurations while maintaining unaffected controls in their current state.

The following control types are supported:

-   Baseline
-   Inherited
-   Hybrid
-   Fully inherited
-   Not applicable
-   Overlay

CAM admins, system owners, ISSOs, and ISSMs can create control tailoring requests for packages in Implement step or later. The request interface displays two panels: Current Records \(left\) showing existing package configuration and Requested Records \(right\) showing proposed modifications. Review current allocations as reference while building requested changes.

## Approval workflow

After you submit a control tailoring request for approval, the system assigns it to the Authorizing Official \(AO\) configured for the authorization package. The AO receives an email notification. The AO reviews only the delta changes in the Requested Changes tab and can approve, request more information, or reassign to a different AO. If more information is needed, the request returns to the submitter for modifications before resubmission.

After approval, changes are applied to the requested controls. Only modified controls transition to new states while unchanged controls retain their current state. All control tailoring activities are recorded in the authorization package work notes.

## Control state transitions

The control tailoring process manages several types of control changes:

When you add a baseline control to the package, the system creates the corresponding control in Draft state. When you change a baseline control from Not Applicable to Applicable, the system creates the control. When you change a baseline control from Applicable to Not Applicable, the system retires the existing control.

When you change a hybrid control to inherited or fully inherited, the system updates the existing control with the new allocation type. When you update the hybrid configuration for an existing hybrid control, the system updates the control requirements to reflect the new configuration.

When an overlay control modification in a control tailoring request is approved, the system applies the overlay's configured behavior and actions to the authorization package.

## Package status during approval

While a control tailoring request is pending approval, the proposed changes don't take effect until the AO approves the request. After approval, the system applies the changes to baseline controls and updates related controls accordingly. Only one control tailoring request in New state is allowed per package at a time.

