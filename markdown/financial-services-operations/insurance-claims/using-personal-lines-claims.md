---
title: Managing Personal Lines Claims
description: Learn which roles use the Personal Lines Claims application to create, investigate, and manage an insurance claim from the first notice of loss \(FNOL\) to the claim closure.
locale: en-US
release: xanadu
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Personal Lines Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Managing Personal Lines Claims

Learn which roles use the Personal Lines Claims application to create, investigate, and manage an insurance claim from the first notice of loss \(FNOL\) to the claim closure.

With the Personal Lines Claims application, FNOL representatives can submit claim requests, while processors and adjusters can work on the cases for the following personal policy case types.

## Personal case types

The following are personal case types available.

-   Personal auto policy
-   You can also create case types for personal lines claims by extending a case type from the personal claim base case.

## Workspace

Processors, adjusters, and other roles use Workspace to work on all aspects of insurance claim cases. With Workspace, users with these roles can do the following tasks:

-   Monitor the workload and performance
-   Focus on high-priority items
-   Easily navigate across tasks

For more information, see [Workspaces](../../fso-common/concept/fso-workspace.md).

The following table shows which Workspace users can use the Personal Lines Claims application.

<table id="table_qy1_452_wrb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Claims admin

</td><td>

Configures Workspace per the business requirements. For more information, see [Configure CSM Configurable Workspace](../../fso-common/task/configure-csm-workspace-fso-apps.md).

</td></tr><tr><td>

Claims manager

</td><td>

Approves reserve and payment requests, and views the analytics and Process Mining dashboards.

</td></tr><tr><td colspan="2" align="center">

First notice of loss representative workspace

</td></tr><tr><td>

First notice of loss representative

</td><td>

Creates claim cases on behalf of customers, and uploads relevant documents.

</td></tr><tr><td colspan="2" align="center">

Processor workspace

</td></tr><tr><td>

Claims processor

</td><td>

Works on claim cases and tasks to resolve cases that are managed by them.

</td></tr><tr><td colspan="2" align="center">

SIU workspace

</td></tr><tr><td>

Special Investigation Unit \(SIU\) agent

</td><td>

Works on potential fraud claim investigation tasks.

</td></tr><tr><td colspan="2" align="center">

Adjuster workspace

</td></tr><tr><td>

Adjuster

</td><td>

Evaluates a claim by reviewing the claim documents, coverages, reserves, and payments.

</td></tr></tbody>
</table>## Claim participants

You can add any person or company as a participant for a claim. The participant can be an entity in the policy or a third-party.

The insurance processor adds participants to a claim during the First Notice of Loss activity, and can assign them a role \(such as reporter or witness\).

FSO insurance applications store claim contact information in the following Insurance Claims Core tables:

-   The Claim Participant table \[sn\_ins\_claim\_profile\] stores details about all participants involved in the claims process.
-   The Participant Role table \[sn\_ins\_claim\_participant\] stores information on the participant's role in the claim \(such as if they are the injured or insured\).

For more information, see [Insurance Claims Core tables](../../fso-common/reference/insurance-claims-core-tables.md).

