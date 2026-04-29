---
title: Request control tailoring
description: Control tailoring requests enable you to modify baseline controls for an authorization package after the Select step without reverting the package to earlier workflow steps.
locale: en-US
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

You can add new controls, change control applicability status, or update hybrid and inherited control configurations while maintaining unaffected controls in their current state.

Previously, modifying baseline controls after the Select step required moving the package back to Select, which reset the control lifecycle for all controls in the package. This meant re-implementing and re-testing all controls even when changes affected only a small subset. Control tailoring requests allow incremental modifications by applying only delta changes to the package.

CAM admins, System owners, ISSOs, and ISSMs can create control tailoring requests for packages in Implement step or later. The request interface displays two panels: Current Records \(left\) showing existing package configuration and Requested Records \(right\) showing proposed modifications. Users review current allocations as reference while building requested changes.

## Approval workflow

After you request approval for a control tailoring request, the system assigns it to the Authorizing Official \(AO\) configured for the authorization package and sends an email notification. The AO reviews only the delta changes in the Requested Changes tab and can approve, request more information, or reassign to a different AO. If more information is needed, the request returns to the submitter for modifications before resubmission.

On approval, changes are applied to baseline controls. Only modified controls transition to new states while unchanged controls retain their current state. All control tailoring activities are recorded in the authorization package work notes.

## Control state transitions

The control tailoring process manages several types of baseline control changes:

When you add a new baseline control to the package, the system creates the corresponding control in Draft state. When you change a baseline control from Not Applicable to Applicable, the system creates the control. When you change a baseline control from Applicable to Not Applicable, the system retires the existing control.

When you change a hybrid control to inherited or fully inherited, the system updates the existing control with the new allocation type. When you update the hybrid configuration for an existing hybrid control, the system updates the control requirements to reflect the new configuration.

## Package status during approval

While a control tailoring request is pending approval, the proposed baseline changes do not take effect until the AO approves the request. Only one new control tailoring request is allowed per package at a time.

