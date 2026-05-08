---
title: Cloud Runner TestRunnerApi – Scoped, Global
description: Manages tests to be executed in a cloud runner for Automated Test Framework \(ATF\). This API is part of the CloudRunnerApi script include.Sets the test runner job to complete status and cancels the root trackers of any generated tests that are running.Provides the status of each test ran for a provided Browser Orchestration Queue \(BOQ\) record.Starts an ATF test or a test suite on the Cloud Runner browser.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Cloud Runner TestRunnerApi – Scoped, Global

Manages tests to be executed in a cloud runner for Automated Test Framework \(ATF\). This API is part of the CloudRunnerApi script include.

You can use this API for the following tasks:

-   Start an ATF test or test suite in the Cloud Runner browser.
-   Check the progress of the test job.
-   Cancel the test job.

In global scope, this API is executed within the sn\_atf\_tg namespace. You must have the ATF Test Generator and Cloud Runner \(sn\_atf\_tg\) plugin activated to use this API.

See also:

-   [Cloud Runner TestGenerationApi – Scoped, Global](../../CloudRunnerAPI-TestGenerationAPIScoped/concept/cloudrnr-TestGenerationAPI-scoped.md#)
-   [Cloud Runner TestUserApi – Scoped, Global](../../CloudRunnerAPI-TestUserAPIScoped/concept/cloudrnr-TestUserAPI-scoped.md#)
-   [Cloud Runner Test User REST API](../../../../../integrate/inbound-rest/concept/cloudrunner-testuser-api.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TestRunnerApi – cancelJob\(String snboqId\)

Sets the test runner job to complete status and cancels the root trackers of any generated tests that are running.

|Name|Type|Description|
|----|----|-----------|
|snboqId|String|Required. The sys\_id of the BOQ record in the Browser Orchestration Queue \[sn\_atf\_tg\_sn\_boq\] table.|

|Type|Description|
|----|-----------|
|null|Null if successful, error message otherwise.|

The following example shows how to start a test run an ATF test, display the progress, and stop the test run. In the global scope, use the sn\_atf\_tg namespace.

```
var snboqId = CloudRunnerAPI.TestRunnerAPI.startJob({
	"testId": "<sys_id>"
});

gs.info(JSON.stringify(CloudRunnerAPI.TestRunnerAPI.progress({"snboqId": snboqId})));

CloudRunnerAPI.TestRunnerAPI.cancelJob({"snboqId": snboqId});
```

Output:

```
{progress: 64, state: running}
```

## TestRunnerApi – progress\(String snboqId\)

Provides the status of each test ran for a provided Browser Orchestration Queue \(BOQ\) record.

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

JSON object indicating test progress.```
{
  "progress": Number,
  "state": "String"
}
```

</td></tr><tr><td>

Object.progress

</td><td>

Indicates test progress percentage complete.Type: Number

</td></tr><tr><td>

Object.state

</td><td>

State of the BOQ record.Possible values:

-   Pending – The requested test activity has been created and is waiting to be executed.
-   Processing – The instance is scanning for records to ensure that the execution trackers are marked for cloud runner before the request is sent to the cloud infrastructure.
-   Browsers requested – A request has been sent to the cloud infrastructure to start browsers for test generation or test running.
-   Running – Cloud infrastructure browsers find and execute pending tests.
-   Completed – The test task is complete.
-   Failed state – The test task failed.

Type: String

</td></tr><tr><td>

Error

</td><td>

If unsuccessful, possible error messages:-   No BOQ ID passed in – The JSON object provided doesn’t have a BOQ ID entry. Verify that the JSON object is structured as `{snboqId: "<sys_id>"}`.
-   Invalid BOQ sys\_id passed in – The ID provided must be for a BOQ record in the Browser Orchestration Queue \[sn\_atf\_tg\_sn\_boq\] table.

</td></tr></tbody>
</table>The following example shows how to start a test run an ATF test, display the progress, and stop the test run. In the global scope, use the sn\_atf\_tg namespace.

```
var snboqId = CloudRunnerAPI.TestRunnerAPI.startJob({
	"testId": "<sys_id>"
});

gs.info(JSON.stringify(CloudRunnerAPI.TestRunnerAPI.progress({"snboqId": snboqId})));

CloudRunnerAPI.TestRunnerAPI.cancelJob({"snboqId": snboqId});
```

Output:

```
{progress: 64, state: running}
```

## TestRunnerApi – startJob\(String testId\)

Starts an ATF test or a test suite on the Cloud Runner browser.

<table id="table_epx_lv4_g1c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

testId

</td><td>

String

</td><td>

Required. The sys\_id of the ATF test or test suite to be run in the Cloud Runner browser. Located in one of the following tables:-   Test \[sys\_atf\_test\]
-   Test Suites \[sys\_atf\_test\_suite\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|The sys\_id of the BOQ record in the Browser Orchestration Queue \[sn\_atf\_tg\_sn\_boq\] table.|

The following example shows how to start a test run an ATF test, display the progress, and stop the test run. In the global scope, use the sn\_atf\_tg namespace.

```
var snboqId = CloudRunnerAPI.TestRunnerAPI.startJob({
	"testId": "<sys_id>"
});

gs.info(JSON.stringify(CloudRunnerAPI.TestRunnerAPI.progress({"snboqId": snboqId})));

CloudRunnerAPI.TestRunnerAPI.cancelJob({"snboqId": snboqId});
```

Output:

```
{progress: 64, state: running}
```

