---
title: Risk Management Framework \(RMF\) step 3 - Implement controls
description: After you have selected controls for implementation and performed any of the possible actions on them, you can implement the controls.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/continuous-risk-monitoring/implement-controls.html
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-08-20"
reading_time_minutes: 1
breadcrumb: [Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Risk Management Framework \(RMF\) step 3 - Implement controls

After you have selected controls for implementation and performed any of the possible actions on them, you can implement the controls.

## Before you begin

Role required: sn\_irm\_cont\_auth.information\_type, sn\_irm\_cont\_auth.information\_owner, or sn\_irm\_cont\_auth.admin

## About this task

When approval was received on the Authorization Package form, a **Percentage of controls implemented** field and a **Controls** related list appeared on the form.

The **Controls** related list contains all of the controls created from the control objectives within the selected authorization boundary.

## Procedure

1.  From the list of controls, select the control number \(with a CTRL prefix\) to open the control.

    \[Omitted image "control-implement.png"\] Alt text: Control

2.  The implementation process performed by your system owner and other technical or security personnel employs the control management workflow inherent in the base GRC system.

    For details, see the following:

    -   [Manage controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/policy-and-compliance-management/c_GRCControls.md)
    -   [Manage control attestations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/policy-and-compliance-management/c_Attestations.md)
    -   [Manage control indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/policy-and-compliance-management/manage-indicators-policy-comp.md)
3.  The **Percentage of controls implemented** field keeps track of your progress while you implement the controls.

4.  After you have completed the implementation process for all controls, select **Assess** to transition the package to the **Assess** state.

    To send the package back to the **Select** state, select **Back to previous step**. All active controls will be retired and the package must get approval to advance again to the **Implement** state.


