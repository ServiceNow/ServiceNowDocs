---
title: How to write and test custom PaCE policies
description: This section provides guidelines on how to write and test PaCE policies.
locale: en-US
release: zurich
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [DevOps Config custom policies, How to write DevOps Config policies, How to create DevOps Config policies, How to test DevOps Config policies, Creating DevOps Config policies, Writing DevOps Config policies, DevOps Config policy]
breadcrumb: [Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# How to write and test custom PaCE policies

This section provides guidelines on how to write and test PaCE policies.

You can write PaCE policies using JavaScript and create the policy record within your instance application scope. PaCE policies can be executed within the scope in which they are created and all functions available in this scope are available to the policy.

When a policy is invoked, a default set of parameters is passed and these parameters can be used in the policy logic as required. A decision indicating whether the policy is compliant, non-compliant, or compliant-exception and additional information is returned using the decision object.

