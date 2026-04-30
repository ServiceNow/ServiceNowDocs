---
title: Managing Commercial Lines Claims
description: Learn which roles use the Commercial Lines Claims application to create, investigate, and manage an insurance claim from the first notice of loss \(FNOL\) to the claim closure.
locale: en-US
release: xanadu
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Commercial Lines Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Managing Commercial Lines Claims

Learn which roles use the Commercial Lines Claims application to create, investigate, and manage an insurance claim from the first notice of loss \(FNOL\) to the claim closure.

With the Commercial Lines Claims application, FNOL representatives can submit the claim requests, while processors and adjusters can work on the cases for the following commercial policy case types.

## Commercial case types

The following are commercial case types available.

-   Commercial auto policy
-   You can also create case types for commercial lines claims by extending a case type from the commercial claim base case.

## Workspace

Processors, adjusters, and other roles use Workspace to work on all aspects of insurance claim cases. With Workspace, users with these roles can do the following tasks:

-   Monitor the workload and performance
-   Focus on high-priority items
-   Easily navigate across tasks

For more information, see [Workspaces](../../fso-common/concept/fso-workspace.md).

The following table shows which Workspace users can use the Commercial Lines Claims application.

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

</td></tr><tr><td colspan="2">

First notice of loss representative workspace

</td></tr><tr><td>

First notice of loss representative

</td><td>

Creates claim cases on behalf of customers, and uploads relevant documents.

</td></tr><tr><td colspan="2">

Processor workspace

</td></tr><tr><td>

Claims processor

</td><td>

Works on claim cases and tasks to resolve cases that are managed by them.

</td></tr><tr><td colspan="2">

SIU workspace

</td></tr><tr><td>

Special Investigation Unit \(SIU\) agent

</td><td>

Works on potential fraud claim investigation tasks.

</td></tr><tr><td colspan="2">

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

