---
title: Perform risk assessment playbook
description: The Perform risk assessment playbook includes activities that enable you to conduct risk assessments for the supplier that you are onboarding.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a supplier, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Perform risk assessment playbook

The Perform risk assessment playbook includes activities that enable you to conduct risk assessments for the supplier that you are onboarding.

The type of flow that is triggered in the Perform risk assessment playbook depends on the plugins that you have installed.

![Perform risk assessment playbook](../image/perform-risk-playbook.png "Perform risk assessment playbook")

<table id="table_ohx_dmp_11c"><thead><tr><th>

Plugins Installed

</th><th>

Playbook flow

</th></tr></thead><tbody><tr><td>

Risk Assessments Integration for Supplier Lifecycle Operations \[com.snc.sn\_supplier\_tprm\]

</td><td>

The Perform risk assessment playbook flow creates risk and tiering assessments to verify the eligibility of the supplier. For more information, see [Risk assessment flow when only Vendor Risk Management is installed](risk-flow-slo-vrm.md).

</td></tr><tr><td>

-   Risk Assessments Integration for Supplier Lifecycle Operations

\[com.snc.sn\_supplier\_tprm\]

-   GRC: Third-party Risk Due Diligence

\[com.sn\_tprm\_onboarding\]


</td><td>

The Perform risk assessment playbook flow create a due diligence request to verify the eligibility of the supplier. For more information, see [Risk assessment flow when Third-party Risk Due Diligence is installed](risk-flow-slo-tprm.md).

</td></tr></tbody>
</table>-   **[Risk assessment flow when only Vendor Risk Management is installed](risk-flow-slo-vrm.md)**  
If you have installed only the Risk Assessments Integration for Supplier Lifecycle Operations \[com.snc.sn\_supplier\_tprm\] plugin, the Perform risk assessment playbook triggers the flow that includes activities to verify the eligibility of the supplier by creating risk assessments.
-   **[Risk assessment flow when Third-party Risk Due Diligence is installed](risk-flow-slo-tprm.md)**  
If you have installed both the Risk Assessments Integration for Supplier Lifecycle Operations \[com.snc.sn\_supplier\_tprm\] and GRC: Third-party Risk Due Diligence \[com.sn\_tprm\_onboarding\] plugins, the Perform risk assessment playbook triggers the flow that includes activities to create a due diligence request, complete Inherent Risk Questionnaire \(IRQ\) assessments, and conduct risk assessments for a third-party and an engagement.

**Parent Topic:**[Create a supplier from the Source-to-Pay Workspace](../task/new-supplier.md)

**Related topics**  


[Use the supplier onboarding playbook to onboard suppliers](use-playbooks-onboard-supp.md#)

[Add a subsidiary for a supplier from the Source-to-Pay Workspace](../task/add-subsidiary.md)

