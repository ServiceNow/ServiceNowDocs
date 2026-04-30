---
title: PaCE API invocation parameters
description: This table describes the properties that can be configured when the PaCE API is invoked. These properties can be set whenever the API is invoked or when you test a policy in the Test Playground.
locale: en-US
release: yokohama
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Write and test policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# PaCE API invocation parameters

This table describes the properties that can be configured when the PaCE API is invoked. These properties can be set whenever the API is invoked or when you test a policy in the Test Playground.

<table id="table_jbc_rp5_jrb"><thead><tr><th>

Property name

</th><th>

Required

</th><th>

Default value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

service

</td><td>

yes

</td><td>

 

</td><td>

The calling service that is invoking the API.

</td></tr><tr><td>

category

</td><td>

no

</td><td>

 

</td><td>

The category type.

</td></tr><tr><td>

type

</td><td>

no

</td><td>

standard

</td><td>

Can be standard or test.

</td></tr><tr><td>

documentIds

</td><td>

yes \(array of table, sysID\)

</td><td>

 

</td><td>

The documentIds is an array of the table and sysID \(of the deployable\).

</td></tr><tr><td colspan="4">

**Note:** The properties shown in the preceding table cannot be configured in the Test Playground. They can only be used when the PaCE API is invoked.

</td></tr><tr><td>

data

</td><td>

yes

</td><td>

 

</td><td>

The policy-specific data that includes all possible caller inputs.

</td></tr><tr><td>

executionTag

</td><td>

no

</td><td>

 

</td><td>

Can be used to tag one or more policy executions records resulting from this invocation. It can be used to retrieve execution details of the policy based on the executionTag.

</td></tr><tr><td>

verboseResponse

</td><td>

no

</td><td>

false

</td><td>

Default value is **false**. If set to **true**, additional debug information \(in this case the ids of the mapped policies\) is returned. A sample invocation response with options.verboseResponse:true is shown here:

```
// Sample execution response
{
  "rootExecutionId": "50202b3ec37b101017e06c576e40dd81",
  "mappedPolicies": [
    {
      "policyId": "3d1de0a8c363101017e06c576e40dde4",
      "policyName": "Production Database Policy",
      "shortDescription": "Policy to check database passwords",
      "versonId": "4ed08520c3a3101017e06c576e40ddcb",
      "versonTyep": "4f2cb75473331010ce6c39282bf6a753",
      "versionState": "published",
      "versionApproval": "approved"
    },
    {
      "policyId": "addd2ca8c363101017e06c576e40dd12",
      "policyName": "API Policy",
      "shortDescription": "Policy to check API policies",
      "versonId": "a6418920c3a3101017e06c576e40dd57",
      "versonTyep": "4f2cb75473331010ce6c39282bf6a753",
      "versionState": "published",
      "versionApproval": "approved"
    }
  ],
  "logs": []
}
```

If `options.verboseResponse:false`, the mapped policies are not included in the response.

</td></tr><tr><td>

failFast

</td><td>

no

</td><td>

false

</td><td>

The default value is **false**. If this property is set to **true**, the first failed policy stops the execution of all the mapped policies.

</td></tr><tr><td>

logLevel

</td><td>

no

</td><td>

info

</td><td>

This parameter can be used to specify how the log messages should be displayed.-   info
-   debug
-   warn
-   error

</td></tr><tr><td>

timeout

</td><td>

no

</td><td>

3600

</td><td>

The timeout period in seconds. The default value is 3600.

</td></tr><tr><td>

waitForResult

</td><td>

no

</td><td>

3600

</td><td>

The waitForResult period in seconds. **Note:** This parameter is available only in the Test Playground.

</td></tr></tbody>
</table>