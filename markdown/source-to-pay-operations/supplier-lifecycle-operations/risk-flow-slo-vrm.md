---
title: Risk assessment flow when only Vendor Risk Management is installed
description: If you have installed only the Risk Assessments Integration for Supplier Lifecycle Operations \[com.snc.sn\_supplier\_tprm\] plugin, the Perform risk assessment playbook triggers the flow that includes activities to verify the eligibility of the supplier by creating risk assessments.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use the risk assessment playbook, Create a supplier, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Risk assessment flow when only Vendor Risk Management is installed

If you have installed only the Risk Assessments Integration for Supplier Lifecycle Operations \[com.snc.sn\_supplier\_tprm\] plugin, the Perform risk assessment playbook triggers the flow that includes activities to verify the eligibility of the supplier by creating risk assessments.

The Risk Assessments Integration for Supplier Lifecycle Operations \[com.snc.sn\_supplier\_tprm\] plugin automatically installs the Vendor Risk Management \[sn\_vdr\_risk\_asmt\] plugin.

![Risk assessment flow when only VRM is installed.](../image/risk-flow-slo-vrm.png "Risk assessment flow when only VRM is installed")

In this flow, the following occurs:

1.  The supplier manager receives a supplier onboarding request.
2.  The supplier manager uses the onboarding playbook, which provides a streamlined and guided process to onboard suppliers. For more information, see [Use the supplier onboarding playbook to onboard suppliers](use-playbooks-onboard-supp.md#).
3.  During the onboarding process, the playbook automatically creates the risk and tiering assessments. The assessment records are listed in the **Risk Assessments** and **Tiering Assessments** tabs.
4.  The supplier manager assigns the risk and tiering assessments to the third-party risk assessor.
5.  The TPR assessor assigns the assessments to the supplier contact.
6.  The supplier contact logs in to the Supplier Collaboration Portal and completes the risk and tiering assessments. For more information, see [Complete a risk assessment from the Supplier Collaboration Portal](../task/complete-risk-assessments.md).
7.  After the risk assessment has been completed, the supplier manager evaluates the risk information in combination with any other data and determines whether to continue or cancel the onboarding process.

    After the assessments are completed, you can continue with completing the activities in the Activation stage.


-   **[Playbook stages and activities when only Vendor Risk Management is installed](risk-flow-vrm-stages.md)**  
The following table lists the Perform risk assessment playbook stages and activities when only Vendor Risk Management \(VRM\) is installed.

**Parent Topic:**[Perform risk assessment playbook](perform-risk-playbook.md)

**Related topics**  


[Playbook stages and activities when only Vendor Risk Management is installed](risk-flow-vrm-stages.md)

