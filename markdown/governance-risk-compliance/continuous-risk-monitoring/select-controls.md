---
title: RMF step 2 - Select controls for an authorization package
description: When the impact levels for the package have been approved, it is time to select baseline controls.
locale: en-US
release: xanadu
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-07-29"
reading_time_minutes: 3
breadcrumb: [Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# RMF step 2 - Select controls for an authorization package

When the impact levels for the package have been approved, it is time to select baseline controls.

## Before you begin

Role required: To write to the sn\_im\_cont\_baseline\_control\_objective table: sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.info\_system\_sec\_officer, sn\_irm\_cont\_auth.admin

To access **Mark as not Applicable**: sn\_irm\_cont\_auth.info\_system\_sec\_officer, sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.admin.

## GRC Continuous Authorization and Monitoring

GRC: Continuous Authorization and Monitoring quick start tests require activating the Continuous Authorization and Monitoring plugin \(com.sn\_compliance\) and loading the demo data.

<table id="atf-tests-cam"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

GRC: System Owner create and validate responsibilities and roles for an AB and AP

</td><td>

System Owner creates and validates responsibilities and roles for an Authorization Boundary and Authorization Package.Information Owners and System User are pre-populated when selecting the Authorization Boundary.

</td><td>

Quebec \(compatible with Paris and Orlando\)

</td></tr><tr><td>

GRC: System Owner validate App Modules visibility

</td><td>

Verifies that the system owner persona is able to view the Continuous Authorization &amp; Monitoring application menu and the following modules under that menu:-   All Authorization Boundaries
-   All Authorization Packages
-   Information Type Library
-   Control Overlays
-   Control Objectives
-   Controls
-   All Engagements

</td><td>

Quebec \(compatible with Paris and Orlando\)

</td></tr><tr><td>

GRC: System Owner Request First approval &amp; My approvals module

</td><td>

System Owner requests an approval.

</td><td>

Quebec \(compatible with Paris and Orlando\)

</td></tr><tr><td>

SO: Create and validate responsibilities and roles for an AB and AP

</td><td>

Verifies if a system owner can create an Authorization Boundary by completing the fields on the Authorization Boundary form. Also verify if the same SO can create an Authorization Package from the form view.

</td><td>

Quebec \(compatible with Paris and Orlando\)

</td></tr></tbody>
</table>To learn more about Continuous Authorization and Monitoring, see [Continuous Authorization and Monitoring](../reference/grc-cam-landing-page.md).

## About this task

When approval was received on the Authorization Package form, a **Control overlays** field and a series of **Controls** related lists appeared on the form.

## Procedure

1.  Select the **Baseline Controls** related list.

    The list shows the baseline controls for the calculated impact level of the package. The number of controls to be implemented \(as defined by NIST\) depends on the Impact level \(High, Moderate, and Low\).

2.  You can perform the following actions on the list of controls.

<table id="table_d4j_jry_2nb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add controls to the list

</td><td>

Select **Add**, select the controls you want to add, and then select **Create Baseline Controls**.**Note:** When adding control objectives, you cannot select multiple control objectives with the same reference ID to add to the baseline controls. You cannot add a control objective if its reference ID already exists in the baseline controls list.

</td></tr><tr><td>

Add controls using a control overlay

</td><td>

Select a control overlay from the **Control overlays** field. **Note:** Privacy overlays and other types of control overlays might be mandated by government agencies, but you can create them to add a specified number of controls to your list.

</td></tr><tr><td>

Identify certain controls as being non-applicable

</td><td>

Select the controls, select **Select**, enter a justification, and then select **Confirm**.

 The controls you marked this way are removed from the **Baseline Controls** list to the **Not Applicable Controls** related list.

 **Note:**

-   You cannot move control objectives with the same reference ID from the baseline controls list to the not applicable controls.
-   You cannot move control objectives with the same reference ID from baseline controls to not applicable controls, or from not applicable controls to baseline controls.
-   When you select two control objectives with the same reference ID from the Not Applicable Controls list, the Return to Baseline Control action is disabled.


</td></tr><tr><td>

Inherit controls from common controls

</td><td>

You can create common controls to which other, subordinate controls can be assigned so they can inherit risk guidance from them. For example, if you have a control that handles an entire facility, you can identify related controls that will inherit protection and compliance from the common control.

 To create a common control, select the control, select **Create Common Control**, select **OK** to confirm. For information on allowing a control to inherit from a common control, see [Inherit from a common control](create-common-control.md).

</td></tr></tbody>
</table>3.  Select **Request Approval**.

    An approval request is sent to the authorizing official, who will access My Approvals from the navigation pane and review the information in the package. When approval is received, the package transitions to the **Implement** state.

    To send the package back to the Categorize state, select **Back to previous step**. All baseline controls are removed and the package must receive approval to advance again to the Select state.


