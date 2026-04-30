---
title: Policy invocation API
description: When a PaCE policy is invoked, the calling service passes the relevant object \(tables and document IDs\) that is being validated by providing the documentRecord object. A calling service is a service or product that uses the PaCE API. PaCE determines which policies must be executed by using the mapping table and the documentRecord.
locale: en-US
release: xanadu
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Write and test policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Policy invocation API

When a PaCE policy is invoked, the calling service passes the relevant object \(tables and document IDs\) that is being validated by providing the `documentRecord` object. A calling service is a service or product that uses the PaCE API. PaCE determines which policies must be executed by using the mapping table and the `documentRecord`.

All selected policies are executed concurrently. When all the policies have been executed, a final single decision is returned \(in JSON format\) with information on all executed policies and policy-level decisions. The final decision can be:

-   compliant: Indicates that all the selected policies comply with the requirements and have returned a compliant decision.
-   non\_compliant: Indicates that one or more of the selected policies do not comply with the requirements and have returned a non\_compliant decision.
-   complaint-exception: Indicates that a policy exception has been approved and any policies that are non-compliant are set to the compliant-exception state.
-   other: Indicates decisions that are not complaint, non\_compliant, or complaint-exception.

Policy invocations can be in one of the following states:

-   new
-   in\_progress
-   complete
-   canceled
-   error
-   timeout

