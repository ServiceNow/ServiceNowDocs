---
title: Managing Individual Life Claims
description: Learn which roles use the Individual Life Claims application to create, investigate, and manage an insurance claim from the first notice of loss \(FNOL\) to the claim closure.
locale: en-US
release: yokohama
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Individual Life Claims, Claims applications, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Managing Individual Life Claims

Learn which roles use the Individual Life Claims application to create, investigate, and manage an insurance claim from the first notice of loss \(FNOL\) to the claim closure.

The Individual Life Claims application includes a death benefit claim workflow that enables your adjusters to work on multiple policy claims from a single case. FNOL representatives can submit claim requests, while adjusters can work on the cases for the individual life claims.

## Workspace

Use Workspace to work on all aspects of an individual life claim case. Users with these roles can do the following tasks:

-   Monitor the workload and performance
-   Focus on high-priority items
-   Navigate across tasks
-   Manage multiple policies in a claim

For more information, see [Workspaces](../../fso-common/concept/fso-workspace.md).

The following table shows which workspace users can use the Individual Life Claims application in.

<table id="table_qkp_c3q_4bc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Claims admin

</td><td>

Configures workspace according to the business requirements.

 For more information, see [Configure Individual Life Claims](../task/configure-individual-life-claims.md) and [Configure CSM Configurable Workspace](../../fso-common/task/configure-csm-workspace-fso-apps.md).

</td></tr><tr><td>

Claims manager

</td><td>

Approves the reserve and payment requests, and views the analytics dashboards. Can also access the claim workspace tab in a case and the FNOL playbook.

</td></tr><tr><td>

FNOL representative

</td><td>

Creates the claim cases on behalf of customers, and uploads the relevant documents in the FNOL playbook.

</td></tr><tr><td>

Adjuster

</td><td>

Evaluates a claim by reviewing the claim documents, coverages, reserves, and payments in the case's claim workspace tab. Can also access the FNOL playbook.

</td></tr><tr><td>

Claims viewer

</td><td>

Views the claim details, deceased details, and beneficiary details.

</td></tr></tbody>
</table>## Claim participants

You can add any person or company as a participant for a claim. The participant can be an entity in the policy or a third-party.

The insurance processor adds participants to a claim during the First Notice of Loss activity, and can assign them a role \(such as reporter or witness\).

FSO insurance applications store claim contact information in the following Insurance Claims Core tables:

-   The Claim Participant table \[sn\_ins\_claim\_profile\] stores details about all participants involved in the claims process.
-   The Participant Role table \[sn\_ins\_claim\_participant\] stores information on the participant's role in the claim \(such as if they are the injured or insured\).

For more information, see [Insurance Claims Core tables](../../fso-common/reference/insurance-claims-core-tables.md).

