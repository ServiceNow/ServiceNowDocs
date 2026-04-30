---
title: Execute policies
description: Execute a policy to determine if the policy is compliant or non-compliant. Executions can be run as part of your policy evaluation process, or in real time when mapped to an object \(table or document ID\).I presume we should also mention invoking with the API? Do we want to tell the user how to do that exactly?
locale: en-US
release: xanadu
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Execute policies

Execute a policy to determine if the policy is compliant or non-compliant. Executions can be run as part of your policy evaluation process, or in real time when mapped to an object \(table or document ID\).

Before you publish a policy version, you can run a test evaluation of the version to determine if it is compliant, non-compliant, compliant-exception, or other. Evaluating a policy enables you to test repeatedly and apply any required changes to the policy version, before moving it to a production environment. For further information about testing your policy version, see [Use the Test Playground for PaCE policies](pace-use-test-playground.md).

When the version is ready to be moved into the production environment, make sure that all policy mappings are in place and verified. When the policy is invoked by the relevant object, its execution output is stored for review. For further information, see [Review executed policy activity](../task/pace-review-executed-policies.md).

