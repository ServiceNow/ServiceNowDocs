---
title: DPR and GRC integration for release compliance
description: The integration between Digital Product Release \(DPR\) and ServiceNow GRC: Policy and Compliance Management connects your release management processes with the enterprise risk and compliance controls. This integration helps you deliver faster, safer, and reliable releases.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Digital Product Release and Integrated Release Management, DPR and GRC integration, Release compliance with GRC compliance framework, Policy and compliance management for DPR releases]
breadcrumb: [Explore, Digital Product Release, IT Service Management]
---

# DPR and GRC integration for release compliance

The integration between Digital Product Release \(DPR\) and ServiceNow® GRC: Policy and Compliance Management connects your release management processes with the enterprise risk and compliance controls. This integration helps you deliver faster, safer, and reliable releases.

Starting with Digital Product Release version 2.3, the DPR integration with GRC: Policy and Compliance Management unifies release management with the organization's risk and compliance operations. This compliance-driven, risk-aware approach automates compliance validation, helping you deliver releases faster and more safely while reducing manual effort.

It enables organizations to:

-   Map Control Objectives and PaCE policies enabled for DPR.
-   Automate compliance checks and risk assessments as part of the release workflow.
-   Manage exceptions and justified deviations from policy in a controlled manner, while maintaining governance and audits.
-   Provide real-time visibility into compliance status, risks, and policy adherence for every release.

    **Note:** Make sure you have the GRC: Policy and Compliance Management \(sn\_compliance\) version 21.1.3 or above installed.


## Digital Product Release and GRC: Policy and Compliance Management integration workflow

The following table shows a simplified, end-to-end workflow for policy compliance validations and exceptions when integrating DPR and GRC.

**Note:** Users must have both `sn_dpr_model.release_user` and `sn_compliance_ws.corporate_compliance_manager` roles to access the **PaCE policies** tab in Control Objective records and the **PaCE results** tab in Control records.

<table id="table_ul4_554_jhc"><thead><tr><th>

In Digital Product Release

</th><th>

In GRC: Policy and Compliance Management

</th></tr></thead><tbody><tr><td>

-

</td><td>

1. In the Compliance Workspace, the compliance manager maps a control objective and policies from the **PaCE policies** tab in the Control Objective record.**Note:** Only the policies that have the exception enabled can be mapped to a control objective.

For more information, see Manage control objectives and policies using the Compliance Workspace.

</td></tr><tr><td>

2. In the Digital Product Release Workspace, the product manager, release admin, or release coordinator maps policies with a phase of a release.

</td><td>

-

</td></tr><tr><td>

3.a. While executing the release, release admin or product manager runs these mapped policies to validate the phase completeness.

</td><td>

-

</td></tr><tr><td>

-

</td><td>

3.b. One or more Controls are created for a combination of release entity and control objective \(CO\).For more information, see Multiple controls for compliance management.

The policy execution status is listed in the **PaCE results** tab in the newly created Control records.

</td></tr><tr><td>

4. If a policy fails, then the release admin or product manager can request an exception providing a reason and business justification. If a previously requested exception has expired, they can request an extension.

</td><td>

-

</td></tr><tr><td>

-

</td><td>

5. Compliance manager or an authorized user from the Policy and Compliance group reviews and approves the policy exception \(or extension\) request.For more information, see Review the policy exception and extension request using the Compliance Workspace.

</td></tr><tr><td>

6. On subsequent execution of the policy, the status of the same failed policy updates to Compliant with exception. The aggregated status in the **Policy status** field on the **Details** tab also updates to **Compliant with exception**.The phase is ready for completion.

</td><td>

-

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Digital Product Release](dpr-exploring-digital-product-release.md)

