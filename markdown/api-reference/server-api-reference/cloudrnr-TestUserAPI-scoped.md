---
title: Cloud Runner TestUserApi – Scoped, Global
description: Manages test user jobs to be executed in a cloud runner for Automated Test Framework \(ATF\). This API is part of the CloudRunnerApi script include.Sets the test user job status in the Browser Orchestration Queue \[sn\_atf\_tg\_sn\_boq\] table to complete.Checks whether a provided user is a valid cloud user.Provides the status of each user test for a provided Browser Orchestration Queue \(BOQ\) record.Starts an end-to-end test user job on cloud runner. If the user is able to log in correctly with the admin role, then the cloud user property is set as this user for future test runs and test generations on the cloud runner infrastructure.Starts an end to end test user job on cloud runner.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Cloud Runner TestUserApi – Scoped, Global

Manages test user jobs to be executed in a cloud runner for Automated Test Framework \(ATF\). This API is part of the CloudRunnerApi script include.

You can use this API for the following tasks:

-   Start the user test job.
-   Set the cloud user.
-   Check if the user specified is valid.
-   Check the progress of the user test job.
-   Cancel the test job.

In global scope, this API is executed within the sn\_atf\_tg namespace. You must have the [ATF Test Generator and Cloud Runner](https://www.servicenow.com/docs/access?context=atf-tg-cr-intro&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) \(sn\_atf\_tg\) plugin activated to use this API.

See also:

-   [Cloud Runner TestGenerationApi – Scoped, Global](../../CloudRunnerAPI-TestGenerationAPIScoped/concept/cloudrnr-TestGenerationAPI-scoped.md#)
-   [Cloud Runner TestRunnerApi – Scoped, Global](../../CloudRunnerAPI-TestRunnerAPIScoped/concept/cloudrnr-TestRunnerAPI-scoped.md#)
-   [Cloud Runner Test Runner REST API](../../../../../integrate/inbound-rest/concept/cloudrunner-testrunner-api.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TestUserApi – cancelJob\(String snboqId\)

Sets the test user job status in the Browser Orchestration Queue \[sn\_atf\_tg\_sn\_boq\] table to complete.

|Name|Type|Description|
|----|----|-----------|
|snboqId|String|Required. The sys\_id of the BOQ record in the Browser Orchestration Queue \[sn\_atf\_tg\_sn\_boq\] table.|

<table id="table_fpx_lv4_g1c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

null

</td><td>

Null if successful, error message otherwise.

</td></tr><tr><td>

Error

</td><td>

If unsuccessful, possible error messages:-   No BOQ ID passed in – The JSON object provided doesn’t have a BOQ ID entry. Verify that the JSON object is structured as `{snboqId: "<sys_id>"}`.
-   Invalid BOQ sys\_id passed in – The ID provided must be for a BOQ record in the Browser Orchestration Queue \[sn\_atf\_tg\_sn\_boq\] table.

</td></tr></tbody>
</table>The following example shows how to start a test user for the admin user, get the progress, and cancel the test user. After confirming the locked out user as a valid cloud user, the code sets the cloud user as an ITIL administrator. In the global scope, use the sn\_atf\_tg namespace.

```
var snboqId = CloudRunnerAPI.TestUserAPI.startJob({username: "abel.tuter"});

gs.info(JSON.stringify(CloudRunnerAPI.TestUserAPI.progress({snboqId: snboqId})));

CloudRunnerAPI.TestUserAPI.cancelJob({snboqId: snboqId});

gs.info(CloudRunnerAPI.TestUserAPI.isValidCloudUser({username: <name of the user who has been locked out>}));

CloudRunnerAPI.TestUserAPI.selectCloudUser({username: "itil_admin"});
```

Output:

```
{progress: 64, state: running}
User is missing the following criteria: 
	User is locked out
False
```

## TestUserApi – isValidCloudUser\(String username\)

Checks whether a provided user is a valid cloud user.

|Name|Type|Description|
|----|----|-----------|
|username|Object|Required. User ID of a valid user listed in the Users \[sys\_user\] table. This value is provided as a string in a JSON object. For example, `{username: "abel.tuter"}`.|

<table id="table_fpx_lv4_g1c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user provided is a valid cloud user.

 Valid values:

-   true: The user provided is a valid cloud user.
-   false: The user provided is invalid for one or more of the following reasons:
    -   The user wasn’t found.
    -   The user is inactive.
    -   The user is locked out.
    -   The user needs a password reset.
    -   The user doesn’t have an admin role.
    -   The user has read-only access.
    -   The user has web services only access.

</td></tr></tbody>
</table>The following example shows how to start a test user for the admin user, get the progress, and cancel the test user. After confirming the locked out user as a valid cloud user, the code sets the cloud user as an ITIL administrator. In the global scope, use the sn\_atf\_tg namespace.

```
var snboqId = CloudRunnerAPI.TestUserAPI.startJob({username: "abel.tuter"});

gs.info(JSON.stringify(CloudRunnerAPI.TestUserAPI.progress({snboqId: snboqId})));

CloudRunnerAPI.TestUserAPI.cancelJob({snboqId: snboqId});

gs.info(CloudRunnerAPI.TestUserAPI.isValidCloudUser({username: <name of the user who has been locked out>}));

CloudRunnerAPI.TestUserAPI.selectCloudUser({username: "itil_admin"});
```

Output:

```
{progress: 64, state: running}
User is missing the following criteria: 
	User is locked out
False
```

## TestUserApi – progress\(String snboqId\)

Provides the status of each user test for a provided Browser Orchestration Queue \(BOQ\) record.

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
</table>The following example shows how to start a test user for the admin user, get the progress, and cancel the test user. After confirming the locked out user as a valid cloud user, the code sets the cloud user as an ITIL administrator. In the global scope, use the sn\_atf\_tg namespace.

```
var snboqId = CloudRunnerAPI.TestUserAPI.startJob({username: "abel.tuter"});

gs.info(JSON.stringify(CloudRunnerAPI.TestUserAPI.progress({snboqId: snboqId})));

CloudRunnerAPI.TestUserAPI.cancelJob({snboqId: snboqId});

gs.info(CloudRunnerAPI.TestUserAPI.isValidCloudUser({username: <name of the user who has been locked out>}));

CloudRunnerAPI.TestUserAPI.selectCloudUser({username: "itil_admin"});
```

Output:

```
{progress: 64, state: running}
User is missing the following criteria: 
	User is locked out
False
```

## TestUserApi – selectCloudUser\(String username\)

Starts an end-to-end test user job on cloud runner. If the user is able to log in correctly with the admin role, then the cloud user property is set as this user for future test runs and test generations on the cloud runner infrastructure.

|Name|Type|Description|
|----|----|-----------|
|username|Object|Required. User ID of a valid user listed in the Users \[sys\_user\] table. This value is provided as a string in a JSON object. For example, `{username: "abel.tuter"}`.|

<table id="table_fpx_lv4_g1c" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Null

</td><td>

Null if successful. Error message otherwise.`Unable to set cloud user as cloud user not valid` – This error indicates that the user provided is invalid for one or more of the following reasons:

-   The user wasn’t found.
-   The user is inactive.
-   The user is locked out.
-   The user needs a password reset.
-   The user doesn’t have an admin role.
-   The user has read-only access.
-   The user has web services only access.

</td></tr></tbody>
</table>The following example shows how to start a test user for the admin user, get the progress, and cancel the test user. After confirming the locked out user as a valid cloud user, the code sets the cloud user as an ITIL administrator. In the global scope, use the sn\_atf\_tg namespace.

```
var snboqId = CloudRunnerAPI.TestUserAPI.startJob({username: "abel.tuter"});

gs.info(JSON.stringify(CloudRunnerAPI.TestUserAPI.progress({snboqId: snboqId})));

CloudRunnerAPI.TestUserAPI.cancelJob({snboqId: snboqId});

gs.info(CloudRunnerAPI.TestUserAPI.isValidCloudUser({username: <name of the user who has been locked out>}));

CloudRunnerAPI.TestUserAPI.selectCloudUser({username: "itil_admin"});
```

Output:

```
{progress: 64, state: running}
User is missing the following criteria: 
	User is locked out
False
```

## TestUserApi – startJob\(String username\)

Starts an end to end test user job on cloud runner.

|Name|Type|Description|
|----|----|-----------|
|username|String|Required. User name of sys\_user to test the end to end infrastructure of cloud runner.|

|Type|Description|
|----|-----------|
|String|The sys\_id of the BOQ record in the Browser Orchestration Queue \[sn\_atf\_tg\_sn\_boq\] table.|

The following example shows how to start a test user for the admin user, get the progress, and cancel the test user. After confirming the locked out user as a valid cloud user, the code sets the cloud user as an ITIL administrator. In the global scope, use the sn\_atf\_tg namespace.

```
var snboqId = CloudRunnerAPI.TestUserAPI.startJob({username: "abel.tuter"});

gs.info(JSON.stringify(CloudRunnerAPI.TestUserAPI.progress({snboqId: snboqId})));

CloudRunnerAPI.TestUserAPI.cancelJob({snboqId: snboqId});

gs.info(CloudRunnerAPI.TestUserAPI.isValidCloudUser({username: <name of the user who has been locked out>}));

CloudRunnerAPI.TestUserAPI.selectCloudUser({username: "itil_admin"});
```

Output:

```
{progress: 64, state: running}
User is missing the following criteria: 
	User is locked out
False
```

