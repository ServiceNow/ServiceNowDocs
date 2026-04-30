---
title: Create new PaCE policy versions
description: You can create new versions for any of your existing policies.
locale: en-US
release: zurich
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage PaCE policy versions, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Create new PaCE policy versions

You can create new versions for any of your existing policies.

After you have created a policy, a draft policy version is automatically created. This policy version contains the actual policy script, and may also contain mapping inputs and caller input definitions.

You can create a policy version from scratch, using low-code, or copy an existing policy version and use that as the basis for a new version. The version can include input definitions for mapping or caller variables. These parameters are used with the logic of the policy to determine whether the policy is in compliance.

For example, for a travel expense policy you can create several policy versions. Each version can include different mapping inputs, for example, limiting the different types of expenses. In one version, the breakfast expense limit could be $25, and the dinner expense limit could be $50. Each time the policy \(and the relevant Current version\) is invoked, the various expenses are validated by the policy to ensure they are in compliance.

