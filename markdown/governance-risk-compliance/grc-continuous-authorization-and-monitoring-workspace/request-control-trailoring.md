---
title: Request control trailoring
description: Control tailoring requests enable you to modify the baseline controls for an authorization package after the Select step without reverting the package or disrupting ongoing assessments. You can add new controls, change control applicability status, or update hybrid and inherited control configurations while maintaining the current workflow step and preserving unaffected controls.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2026-01-26"
reading_time_minutes: 2
breadcrumb: [View package details in CAM Workspace, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Request control trailoring

Control tailoring requests enable you to modify the baseline controls for an authorization package after the Select step without reverting the package or disrupting ongoing assessments. You can add new controls, change control applicability status, or update hybrid and inherited control configurations while maintaining the current workflow step and preserving unaffected controls.

When you need to modify baseline controls after moving beyond the Select step in the Risk Management Framework \(RMF\) process, you create a control tailoring request instead of reverting the package to Select. The request captures your proposed changes and routes them to the Authorizing Official \(AO\) for review and approval.

After you submit a control tailoring request, the system generates an approval task and assigns it to the AO or AO Delegate configured for the authorization package. The AO reviews the proposed changes and either approves or rejects the request. Upon approval, the system triggers an item generation job that applies the changes to the baseline controls and updates related controls accordingly.

## Control state transitions

The control tailoring process manages several types of baseline control changes:

When you add a new baseline control to the package, the system creates the corresponding control in Draft state. When you change a baseline control from Not Applicable to Applicable, the system creates the control. When you change a baseline control from Applicable to Not Applicable, the system retires the existing control and sets its active flag to false. Retired controls do not appear in the default control list views.

When you change a hybrid control to inherited or fully inherited, the system retires the hybrid control configuration and creates or updates the control with the new allocation type. When you update the hybrid configuration for an existing hybrid control, the system updates the control requirements to reflect the new configuration.

## Package status during approval

While a control tailoring request is pending approval, the authorization package displays an indicator showing that baseline changes are under review. You can continue working on other package activities, but the proposed baseline changes do not take effect until the AO approves the request. After approval, the item generation job processes the changes asynchronously, and the package status updates to reflect that the control tailoring request has been approved.

-   **[Create a control tailoring request](../task/create-a-control-tailoring-request.md)**  
Create a control tailoring request to modify baseline controls for an authorization package after the Select step without reverting the package or disrupting ongoing assessments.

**Parent Topic:**[View package details in CAM Workspace](../task/auth-package-overview-ws.md)

