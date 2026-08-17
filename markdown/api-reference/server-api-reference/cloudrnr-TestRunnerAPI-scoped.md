---
title: Cloud Runner TestRunnerApi – Scoped, Global
description: Manages tests to be executed in a cloud runner for Automated Test Framework \(ATF\). This API is part of the CloudRunnerApi script include.Sets the test runner job to complete status and cancels any generated tests that are running.Provides the status of each test ran for a provided Browser Orchestration Queue \(BOQ\) record.Starts an ATF test or a test suite on the Cloud Runner browser.Cancels the run job according to the given rootTrackerId instead of snboqId. This method is useful when the caller only has the tracker id and no sn\_boq record was ever created.Looks up the run job according to a given rootTrackerId instead of snboqId.Starts the run without waiting for the sn\_boq record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/server-api-reference/cloudrnr-TestRunnerAPI-scoped.html
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Cloud Runner TestRunnerApi – Scoped, Global

Manages tests to be executed in a cloud runner for Automated Test Framework \(ATF\). This API is part of the CloudRunnerApi script include.

You can use this API for the following tasks:

-   Start an ATF test or test suite in the Cloud Runner browser.
-   Check the progress of the test job.
-   Cancel the test job.

In global scope, this API is executed within the sn\_atf\_tg namespace. You must have the [ATF Test Generator and Cloud Runner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/atf-tg-cr-intro.md) \(sn\_atf\_tg\) plugin activated to use this API.

See also:

-   [Cloud Runner TestGenerationApi – Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/cloudrnr-TestGenerationAPI-scoped.md)
-   [Cloud Runner TestUserApi – Scoped, Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/cloudrnr-TestUserAPI-scoped.md)
-   [Cloud Runner Test User REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/cloudrunner-testuser-api.md)

**Parent Topic:**[Server API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/api-server.md)

## TestRunnerApi – cancelJob\(String snboqId\)

Sets the test runner job to complete status and cancels any generated tests that are running.

|Name|Type|Description|
|----|----|-----------|
|snboqId|String|Sys\_id of the Browser Orchestration Queue \(BOQ\) \[sn\_atf\_tg\_sn\_boq\] record associated with the test runner job to cancel.|

|Type|Description|
|----|-----------|
|null|Null if successful, error message otherwise.|

The following example shows how to cancel a test job using snboqId:

```
var testRunnerApi = new sn_atf_tg.TestRunnerApi();

// Cancel job using snboqId
var cancelResult = testRunnerApi.cancelJob('f6e5d4c3b2a1908070605040302010ab', null);

if (cancelResult.status === 'success') {
  gs.info('Test job cancelled successfully');
} else {
  gs.error('Failed to cancel test job: ' + cancelResult.message);
}
```

Output:

```
Test job cancelled successfully
```

## TestRunnerApi – progress\(String snboqId\)

Provides the status of each test ran for a provided Browser Orchestration Queue \(BOQ\) record.

|Name|Type|Description|
|----|----|-----------|
|snboqId|String|Sys\_id of the Browser Orchestration Queue \(BOQ\) \[sn\_atf\_tg\_sn\_boq\] record associated with the test runner job to retrieve.|

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

State of the record.Possible values:

-   `Pending`: The requested test activity has been created and is waiting to be executed.
-   `Processing`: The instance is scanning for records to ensure that the execution trackers are marked for cloud runner before the request is sent to the cloud infrastructure.
-   `Browsers requested`: A request has been sent to the cloud infrastructure to start browsers for test generation or test running.
-   `Running`: Cloud infrastructure browsers find and execute pending tests.
-   `Completed`: The test task is complete.
-   `Failed state`: The test task failed.

Type: String

</td></tr><tr><td>

Error

</td><td>

If unsuccessful, possible error messages:-   No sys\_id passed in – The JSON object provided doesn’t have a BOQ ID entry. Verify that the JSON object is structured as `{snboqId: "<sys_id>"}`.
-   Invalid sys\_id passed in – The ID provided must be for a BOQ record in the Browser Orchestration Queue \[sn\_atf\_tg\_sn\_boq\] table.

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

Sys\_id of the ATF test or test suite to be run in the Cloud Runner browser. Located in one of the following tables:

-   Test \[sys\_atf\_test\]
-   Test Suites \[sys\_atf\_test\_suite\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Returns the sys\_id of the BOQ record in the Browser Orchestration Queue \[sn\_atf\_tg\_sn\_boq\] table.|

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

## TestRunnerApi – cancelJobByTracker\(String rootTrackerId\)

Cancels the run job according to the given rootTrackerId instead of snboqId. This method is useful when the caller only has the tracker id and no sn\_boq record was ever created.

|Name|Type|Description|
|----|----|-----------|
|`rootTrackerId`|String|Sys\_id of the `sys_execution_tracker` for the run you want to cancel.|

|Type|Description|
|----|-----------|
|None|Void. Same cancellation effect as cancelJob\(\).|

The following example cancels the run job for the given rootTrackerID.

```
sn_atf_tg.CloudRunnerAPI.TestRunnerAPI.cancelJobByTracker({
    rootTrackerId: "7a6b5c4d3e2f7a6b5c4d3e2f7a6b5c4d"
});

// No return value; run is marked completed/cancelled.
```

## TestRunnerApi – progressFromTracker\(String rootTrackerId\)

Looks up the run job according to a given rootTrackerId instead of snboqId.

|Name|Type|Description|
|----|----|-----------|
|`rootTrackerId`|String|Sys\_id of the `sys_execution_tracker` for the run you want to look up.|

|Type|Description|
|----|-----------|
|Object|`{ progress: number, state: string }` — same shape as `progress`.|

The following example retrieves the run progress for the given rootTrackerID.

```
var status = sn_atf_tg.CloudRunnerAPI.TestRunnerAPI.progressFromTracker({
    rootTrackerId: "7a6b5c4d3e2f7a6b5c4d3e2f7a6b5c4d"
});
```

Output:

```
{ progress: 40, state: "running" }
```

## TestRunnerApi – startJob\(String testId\)

Starts the run without waiting for the sn\_boq record.

|Name|Type|Description|
|----|----|-----------|
|testId|String|Sys\_id of the Test \[sys\_atf\_test\] or Test Suites \[sys\_atf\_test\_suite\] table record to run.|

|Type|Description|
|----|-----------|
|String|Returns a rootTrackerId, which is the sys\_id of the `sys_execution_tracker` for the run. Can be passed in the progressFromTracker\(\) method.|

The following example starts a suite run without waiting on the browser job record.

```
var rootTrackerId = sn_atf_tg.CloudRunnerAPI.TestRunnerAPI.startJobAsync({
    testId: "a1b2c3d4e5f6a1b2c3d4e5f6a1b2c3d4"
});
```

Output:

```
"7a6b5c4d3e2f7a6b5c4d3e2f7a6b5c4d"  (rootTrackerId)
```

