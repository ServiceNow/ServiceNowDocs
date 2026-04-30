---
title: Cloud Runner TestGenerationApi – Scoped, Global
description: Manages test job generation to be executed in a cloud runner for Automated Test Framework \(ATF\). This API is part of the CloudRunnerApi script include.Sets the test generation job and its associated update set record to complete status. Cancels the root trackers of any generated tests that are running. If any test jobs are in progress on cancellation, this method sets any of the in-progress test records generated to skipped.Provides the status of each generated test for a provided Browser Orchestration Queue \(BOQ\) record.Inserts a record into the Browser Orchestration Queue \(BOQ\) \[sn\_atf\_tg\_sn\_boq\] table to start a test job.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Cloud Runner TestGenerationApi – Scoped, Global

Manages test job generation to be executed in a cloud runner for Automated Test Framework \(ATF\). This API is part of the CloudRunnerApi script include.

You can use this API for the following tasks:

-   Start the test generation job.
-   Check the progress of the test generation job.
-   Cancel the test generation job.

In global scope, this API is executed within the sn\_atf\_tg namespace. You must have the [ATF Test Generator and Cloud Runner](https://www.servicenow.com/docs/access?context=atf-tg-cr-intro&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) \(sn\_atf\_tg\) plugin activated to use this API.

See also:

-   [Cloud Runner TestRunnerApi – Scoped, Global](../../CloudRunnerAPI-TestRunnerAPIScoped/concept/cloudrnr-TestRunnerAPI-scoped.md#)
-   [Cloud Runner TestUserApi – Scoped, Global](../../CloudRunnerAPI-TestUserAPIScoped/concept/cloudrnr-TestUserAPI-scoped.md#)
-   [Cloud Runner Test Generation REST API](../../../../../integrate/inbound-rest/concept/cloudrunner-testgeneration-api.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TestGenerationApi – cancelJob\(String snboqId\)

Sets the test generation job and its associated update set record to complete status. Cancels the root trackers of any generated tests that are running. If any test jobs are in progress on cancellation, this method sets any of the in-progress test records generated to skipped.

|Name|Type|Description|
|----|----|-----------|
|snboqId|String|Required. The sys\_id of the BOQ record in the Browser Orchestration Queue \[sn\_atf\_tg\_sn\_boq\] table.|

|Type|Description|
|----|-----------|
|null|Null if successful, error message otherwise.|

The following example shows how to start generating tests for the incident table and cancel the test generation. In the global scope, use the sn\_atf\_tg namespace.

```
var insertedSnboqId = CloudRunnerAPI.TestGenerationAPI.startJob({
  tableEncodedQuery: "nameISincident",
  catalogEncodedQuery: "sysIdISEMPTY",
  maxTestCount: 10
});

CloudRunnerAPI.TestGenerationAPI.cancelJob({snboqId: insertedSnboqId});
```

## TestGenerationApi – progress\(String snboqId\)

Provides the status of each generated test for a provided Browser Orchestration Queue \(BOQ\) record.

|Name|Type|Description|
|----|----|-----------|
|snboqId|String|Required. The sys\_id of the BOQ record in the Browser Orchestration Queue \[sn\_atf\_tg\_sn\_boq\] table.|

<table id="table_fpx_lv4_g1c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information about the test job. You can find advanced test details in the Generated Tests \[sn\_atf\_tg\_generated\_test\] table.```
{
  "testsFailed": Number,
  "testsInProgress": Number,
  "testsPending": Number,
  "testsSkipped": Number,
  "testsSucceeded": Number
}
```

</td></tr><tr><td>

testsFailed

</td><td>

The number of failed tests generated. The failure reasons are listed in the Generated Tests \[sn\_atf\_tg\_generated\_test\] table.Data type: Number

</td></tr><tr><td>

testsInProgress

</td><td>

The number of use cases being created.Data type: Number

</td></tr><tr><td>

testsPending

</td><td>

The number of use cases remaining to be generated.Data type: Number

</td></tr><tr><td>

testsSkipped

</td><td>

The number of tests skipped due to job cancellation.Data type: Number

</td></tr><tr><td>

testsSucceeded

</td><td>

The number of successfully generated tests.Data type: Number

</td></tr></tbody>
</table>The following example shows how to start generating tests for the incident table, get the progress, and cancel the test generation. In the global scope, use the sn\_atf\_tg namespace.

```
var snboqId = CloudRunnerAPI.TestGenerationAPI.startJob({
  "tableEncodedQuery": "nameISincident",
  "catalogEncodedQuery": "sysIdISEMPTY",
  "maxTestCount": 10
});

gs.info(JSON.stringify(CloudRunnerAPI.TestGenerationAPI.progress({snboqId: snboqId})));

CloudRunnerAPI.TestGenerationAPI.cancelJob({"snboqId": snboqId});
```

Output:

```
{
  "testsSucceeded": 4,
  "testsFailed": 2,
  "testsPending": 2,
  "testsInProgress": 8,
  "testsSkipped": 0
}
```

## TestGenerationApi – startJob\(String tableEncodedQuery, String userEncodedQuery, String catalogEncodedQuery, Number maxTestCount, Number maxTestCountPerTable, Number maxTestCountPerItem, String email, Boolean separateUpdateSetPerScope, String scopeForGeneratingTests, String suiteName\)

Inserts a record into the Browser Orchestration Queue \(BOQ\) \[sn\_atf\_tg\_sn\_boq\] table to start a test job.

<table id="table_epx_lv4_g1c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

catalogEncodedQuery

</td><td>

String

</td><td>

Optional. Encoded query specifying the catalog items \(CIs\) on which to generate tests.Default: All CIs \(empty string\)

</td></tr><tr><td>

email

</td><td>

String

</td><td>

Optional. Email address to send a notification to when the test generation is complete.Default: No email \(empty string\)

</td></tr><tr><td>

maxTestCount

</td><td>

Number

</td><td>

Optional. Maximum number of tests to generate.Possible values: 1-9999

Default: 9999 \(maximum value\)

</td></tr><tr><td>

maxTestCountPerItem

</td><td>

Number

</td><td>

Optional. Maximum number of tests to generate per CI.Possible values: 1-10

Default: 10 \(maximum value\)

</td></tr><tr><td>

maxTestCountPerTable

</td><td>

Number

</td><td>

Optional. Maximum number of tests to generate per table.Possible values: 1-10

Default: 10 \(maximum value\)

</td></tr><tr id="store-2024-05"><td>

scopeForGeneratingTests

</td><td>

String

</td><td>

Required when **separateUpdateSetPerScope** is set to false. Sys\_id of the scope in which to place all generated tests.Default: No sys\_id \(empty string\)

</td></tr><tr><td>

separateUpdateSetPerScope

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether to separate generated tests into respective suites, update sets, and scopes, or to place tests into one suite, update set, and scope.Valid values:

-   true: Tests are placed into their respective suite and update set according to the scope of each table or catalog item.
-   false: All generated tests are placed in the same suite, update set, and scope. If false, **scopeForGeneratingTests** is required in the request.

Default: true

</td></tr><tr><td>

testSuite

</td><td>

String

</td><td>

Optional. Name of the test suite to create using test generation.Data type: String

Default: ATF Generated Suite - &lt;time\_stamp&gt;

</td></tr><tr><td>

tableEncodedQuery

</td><td>

String

</td><td>

Optional. Encoded query specifying the tables on which to generate tests. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).Default: All tables \(empty string\)

</td></tr><tr><td>

userEncodedQuery

</td><td>

String

</td><td>

Optional. Encoded query specifying the users on which to generate tests.Default: All users \(empty string\)

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|The sys\_id of the BOQ record in the Browser Orchestration Queue \[sn\_atf\_tg\_sn\_boq\] table.|

The following example shows how to start generating tests for the incident table. In the global scope, use the sn\_atf\_tg namespace.

```
var insertedSnboqId = CloudRunnerAPI.TestGenerationAPI.startJob({
  tableEncodedQuery: "nameISincident",
  catalogEncodedQuery: "sysIdISEMPTY",
  suiteName: "Suite123",
  maxTestCount: 10
});

gs.info(insertedSnboqId);
```

Output:

```
<sys_id of inserted BOQ record>
```

