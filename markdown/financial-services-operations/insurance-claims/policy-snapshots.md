---
title: Policy snapshots in Insurance claims
description: Learn how a claim in the Insurance claims application is driven by the policy snapshot throughout its life cycle. The Policy Snapshot table stores a copy of an insurance policy that can be used in a claims case.
locale: en-US
release: yokohama
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Insurance claims, Insurance claims, Claims applications, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Policy snapshots in Insurance claims

Learn how a claim in the Insurance claims application is driven by the policy snapshot throughout its life cycle. The Policy Snapshot table stores a copy of an insurance policy that can be used in a claims case.

When a claim is created, the system by default copies the latest insurance policy, generates the policy snapshot, and attaches it to the claim. This process provides a copy of the latest insurance policy data that the claim can use \(for example, in the claims summary workspace\).

You can also modify the base logic for policy snapshot generation to copy the policy that was active on a specific incident date. For example, if a claim is being created for an incident that occurred four months ago, the policy that was applicable four months ago can be copied and attached as a policy snapshot to the claim.

The PolicySnapshotGenerator script include in your instance contains the code that is responsible for generating a copy of the latest insurance policy. You can use this code as-is if you’re creating a claim that is based on the latest insurance policy, assuming that the latest insurance policy is already present in the Financial Services Operations tables. You should modify this script to retrieve specific policies, integrate with external systems, and so on.

When setting up the Insurance claims application, review the PolicySnapshotGenerator script include to ensure that you’re retrieving the correct policy for your claims.

**Related topics**  


[Insurance Claims Core tables](../../fso-common/reference/insurance-claims-core-tables.md)

[Insurance policies in Insurance claims](insurance-policies.md)

