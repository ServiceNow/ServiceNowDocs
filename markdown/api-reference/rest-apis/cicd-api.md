---
title: Continuous Integration/Continuous Delivery \(CICD\) API
description: The CICD API provides endpoints that enable integration with common DevOps tools for building pipelines. These tools include Jenkins, Azure Pipelines, GitLab, GitHub Actions, Atlassian Bamboo/Pipelines, and more.Returns the results of a batch install based on a specified result identifier.Returns the current progress and status of the CI/CD instance scan function associated with a passed-in progress ID. Call this method after calling one of the other instance scan CI/CD endpoints such as /sn\_cicd/instance\_scan/full\_scan or /sn\_cicd/instance\_scan/point\_scan.Returns the current progress and status of the Continuous Integration and Continuous Delivery \(CICD\) function associated with a specified progress ID.Returns the results of a test suite run based on a specified results identifier.Installs two or more packages in a single specified batch.Rolls back all of the packages associated with a specific batch installation to their previous versions.Installs the specified application from the application repository onto the instance making the endpoint call.Publishes the specified application and all of its artifacts to the application repository.Initiates a rollback of a specified application to a specified version.Runs all active checks present in your instance.Executes all applicable checks against a specified record.Runs a scan using a suite and target \(scoped apps or update sets\) that have already run previously.Runs all active checks inside a suite against a list of scoped apps.Runs all active checks inside a suite against a list of update sets.Activates the specified plugin.Rolls back the specified plugin to the previous installed version. If no prior version has been installed, returns an error.Starts applying changes from a remote source control to a specified local application or application-customization.Starts applying a previously generated "stash" of changes from a remote source control to a specified local application or application-customization.Imports an application using the specified repository URL and branch name.Starts a specified automated test suite. The test suite runs on the instance from which the endpoint was called.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 86
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Continuous Integration/Continuous Delivery \(CICD\) API

The CICD API provides endpoints that enable integration with common DevOps tools for building pipelines. These tools include Jenkins, Azure Pipelines, GitLab, GitHub Actions, Atlassian Bamboo/Pipelines, and more.

It provides integrators with the ability to build CICD pipelines for ServiceNow AI Platform applications driven by pull/merge request workflows typical in source-driven development. It leverages the Source Control, Application Repository, and Automated Test Framework features.

The CI/CD API provides the following product and feature areas:

-   Source control

    Apply remote changes for an application linked to a remote Git repository through the Source Control feature in Studio, on a specific instance.

    Imports an application using the specified repository URL and branch name.

-   Application repository: Available for scoped applications, global application, application customizations for scoped applications on the ServiceNow Store, and through plugins.
    -   Publish an application from an instance to the connected application repository.
    -   Install an application onto an instance from the connected application repository.
    -   Rollback an application that was installed through rollback context.
-   Batch
    -   Define a JSON manifest file to batch install multiple applications together.
    -   Rollback the entire batch install through rollback context.
    -   Returns the results of a batch install based on a specified result identifier.
-   Plugins
    -   Activate a plugin.
    -   Rollback a plugin through rollback context.
-   Automated Test Framework \(ATF\)
    -   Start an ATF test suite.
    -   Obtain the pass/fail result of an ATF test suite.
-   Instance scan
    -   Start an instance scan \(full, point scan on table, point scan on record, scoped application, update set, combination of these items.\)
    -   Obtain the pass/fail result of an instance scan run.
-   Progress

    Obtain the percentage completion on an instance for processes initiated by other endpoint calls. You can use this feature to poll until progress completion before proceeding with the next step.


This API uses an asynchronous response model. When you call an endpoint, such as to run a test suite /sn\_cicd/testsuite/run, the endpoint kicks off the associated function, such as starting the execution of the test suite. The endpoint then returns a response message that contains the execution status of the requested function, typically `Pending`, along with a unique identifier and link. Use this information to obtain additional information about the progress, source, results, and/or findings of the request. Depending on the function request, you can use one of the following means to obtain additional information about a request:

-   Call the /sn\_cicd/progress/\{progress\_id\} endpoint using the **links.progress.id** parameter returned by the initiating endpoint.
-   Call the /sn\_cicd/testsuite/results/\{result\_id\} endpoint using the **links.result.id** parameter returned by the initiating endpoint.
-   Call the /sn\_cicd/instance\_scan/result/\{progress\_id\} endpoint using the **links.progress.id** parameter returned by the initiating endpoint.
-   Call the /sn\_cicd/sc/apply\_stash/\{stash\_id\} endpoint using the **links.stash.id** parameter returned by the/sn\_cicd/progress/\{progress\_id\} endpoint.
-   Link out to the **links.&lt;progress/result/source/findings&gt;.url** parameter returned by the initiating endpoint.

**Note:** To install an application from a repository, the application must first be published to the repository using the /sn\_cicd/app\_repo/publish endpoint. Once published, any instance connected to that repository can then install and rollback the application. If the application is not first published, the installation request fails.

The sn\_cicd.sys\_ci\_automation or admin role is required to use this API.

Beginning in Tokyo, the CICD API endpoints that need to obtain the **instance wide lock / mutex** to perform their requested operation will use a queue, rather than rejecting requests while the **instance wide lock / mutex** is occupied. Multiple CICD pipelines simultaneously make requests without detecting the rejection and retrying, and instead, can simply monitor the progress as they would for successful requests previously. This behavior is on by default.

The current queue can be inspected by a user with the admin role by navigating to the **System Diagnostic** **-&gt;Application Operation Queue**. From here the queue can be paused and resumed by the admin to allow for other manual operations that may require the **instance wide lock / mutex**.

**Note:** When paused, any in progress operation will run to completion but no new operation will be started. The API will continue to accept and queue new requests. A pending operation can also be cancelled before it begins running by updating the listed execution tracker to a cancelled state. If for whatever reason, an operation cannot proceed after the time out specified in com.glide.update\_operation.job\_cancel\_timeout\_minutes \(default: 48 hours\), it will be cancelled.

When an upgrade is scheduled, the queue will go into an upgrade paused state two hours prior to the upgrade unless overridden by the property com.glide.update\_operation.queue\_upgrade\_window. This allows for any in progress operation to complete before the upgrade commences.

**Note:** The queue automatically resumes when the upgrade is completed.

For additional information on CICD, see:

-   [Continuous Integration and Continuous Delivery \(CICD\) Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/cicd-spoke.md)
-   [https://plugins.jenkins.io/servicenow-cicd/](https://plugins.jenkins.io/servicenow-cicd/)
-   [https://marketplace.visualstudio.com/items?itemName=ServiceNow.vss-services-servicenow-cicd](https://marketplace.visualstudio.com/items?itemName=ServiceNow.vss-services-servicenow-cicd)
-   [https://github.com/marketplace?type=actions&amp;query=servicenow](https://github.com/marketplace?type=actions&query=servicenow)
-   [https://hub.docker.com/r/servicenowdevx/sncicd-gitlab-docker](https://hub.docker.com/r/servicenowdevx/sncicd-gitlab-docker)

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CI/CD - GET /sn\_cicd/app/batch/results/\{result\_id\}

Returns the results of a batch install based on a specified result identifier.

Call this method after calling the /sn\_cicd/app/batch/install endpoint to obtain the results of the batch install. Use the value returned in the **links.results.id** parameter of the return results of /sn\_cicd/app/batch/install endpoint as the **result\_id** for this endpoint. You can also call the /api/sn\_cicd/progress/\{progress\_id\} endpoint to obtain information on the progress of the installation if it has not yet completed.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/app/batch/results/{result_id}`

Default URL: `/api/sn_cicd/app/batch/results/{result_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

result\_id

</td><td>

Sys\_id of the batch installation for which to return results information. This value is returned in the **links.results.id** parameter of the /sn\_cicd/app/batch/install endpoint.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|404|Not found. The requested item wasn’t found.|
|405|Invalid method. The functionality is inactive.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-error"><td>

error

</td><td>

Error message with details about the error.Data type: String

</td></tr><tr><td>

batch\_items

</td><td>

JSON array, where each object provides details of a package installation.Data type: Array

 ```
"batch_items" [{
  "customization_version": "String",
  "id": "String",
  "install_date": "String",
  "name": "String",
  "notes": "String",
  "state": "String",
  "status_message": "String",
  "type": "String",
  "url": "String",
  "version": "String" 
}]
```

</td></tr><tr><td>

batch\_items.customization\_version

</td><td>

Only applicable when the **batch\_items.type** parameter is set to application or plugin and the **requested\_customization\_version** parameter is passed in the batch install request. Version of the store application or scoped ServiceNow plugin customization package to install, such as 1.0.2 or 2.3.Data type: String

</td></tr><tr><td>

batch\_items.id

</td><td>

Sys\_id of the application or identifier of the plugin to install. Same as the **packages.id** parameter in the initiating /sn\_cicd/app/batch/install endpoint call.Data type: String

</td></tr><tr><td>

batch\_items.install\_date

</td><td>

Date and time that the package was installed. Empty if the request is still in progress.Data type: String

</td></tr><tr><td>

batch\_items.name

</td><td>

Name of the package.Data type: String

</td></tr><tr><td>

batch\_items.notes

</td><td>

User specified notes about the package. Same as the **packages.notes** parameter in the initiating /sn\_cicd/app/batch/install endpoint call. Data type: String

</td></tr><tr><td>

batch\_items.state

</td><td>

Current state of the associated package installation.Possible values:

-   Failed
-   In progress
-   Installed
-   Invalid
-   Ready
-   Rolled Back

 Data type: String

</td></tr><tr><td>

batch\_items.status\_message

</td><td>

Describes any errors that occurred during the installation of the package and/or customizations.Data type: String

</td></tr><tr><td>

batch\_items.type

</td><td>

Type of application. Same as the **packages.type** parameter in the initiating /sn\_cicd/app/batch/install endpoint call.Valid values:

-   application
-   plugin

 Data type: String

</td></tr><tr><td>

batch\_items.url

</td><td>

URL of the associated package installation record on your ServiceNow instance.Data type: String

</td></tr><tr><td>

batch\_items.version

</td><td>

Version of the package to install, such as 1.0.2 or 2.3. Same as the **packages.requested\_version** parameter in the initiating /sn\_cicd/app/batch/install endpoint call.Data type: String

</td></tr><tr><td>

batch\_plan

</td><td>

Describes the installation batch plan.Data type: Object

 ```
"batch_plan": {
  "id": "String",
  "name": "String",
  "notes": "String",
  "state": "String",
  "url": "String"
}
```

</td></tr><tr><td>

batch\_plan.id

</td><td>

Sys\_id of the return results information. Same value as what was passed in the **result\_id** request parameter.Data type: String

</td></tr><tr><td>

batch\_plan.name

</td><td>

User specified descriptive name for this batch request. Same as the **name** parameter in the initiating /sn\_cicd/app/batch/install endpoint call.Data type: String

</td></tr><tr><td>

batch\_plan.notes

</td><td>

Notes that were passed in when the batch install was invoked. Same as the **notes** parameter in the initiating /sn\_cicd/app/batch/install endpoint call.Data type: String

</td></tr><tr><td>

batch\_plan.state

</td><td>

Current state of the overall batch installation.Possible values:

-   Failed
-   In progress
-   Installed
-   Invalid
-   Partial Install
-   Ready
-   Rolled Back

 Data type: String

</td></tr><tr><td>

batch\_plan.url

</td><td>

URL of the batch installation plan record on your ServiceNow instance.Data type: String

</td></tr></tbody>
</table>### cURL request

This example checks the status of a batch installation plan called Release 2.0 IT Operations.

```
curl 'instance.servicenow.com/api/sn_cicd/app/batch/results/df24b1e9db2d0110b5e3f6c5ae97c561 \
--request GET \
--header 'Accept: application/json' \
--user 'username':'password' 
```

```
{
"result": {
  "batch_plan": {
    "name":“Release 2.0 IT Operations”,
    "id": "df24b1e9db2d0110b5e3f6c5ae97c561",
    "url": "https://instance.service-now.com/sys_batch_install_plan.do?sys_id=df24b1e9db2d0110b5e3f6c5ae97c561",
    "state": "Installed",
    "notes": "User specified notes for batch install plan",
  }
  "batch_items": [
    {
      "name": "com.sn_cicd_spoke",
      "type": "Application",
      "version": "7.0.0",
      "state": "Installed",
      "install_date": "2020-08-31 15:30:01",
      "id": "c159b1e9db1c0010b5e3f6c5ae961903",
      "url":"https://instance.service-now.com/sys_batch_install_item.do?sys_id=c159b1e9db1c0010b5e3f6c5ae961903",
      "notes" : ""
    },
    {
      "name": "Customization for CSM App1",
      "type": "Application",
      "version": "1.0.0",
      "state": "Installed",
      "install_date": "2020-08-31 15:32:01",
      "id": "e824b1e9db2d1001b5e3f6c5ae97d628",
      "url": "https://instance.service-now.com/sys_batch_install_item.do?sys_id=e824b1e9db2d1001b5e3f6c5ae97d628",
      "notes": "Customized headers.",
      "customization_version": "2.1.1”,
      "status_message": ""

    }]
  }
}

```

## CI/CD - GET /sn\_cicd/instance\_scan/result/\{progress\_id\}

Returns the current progress and status of the CI/CD instance scan function associated with a passed-in progress ID. Call this method after calling one of the other instance scan CI/CD endpoints such as /sn\_cicd/instance\_scan/full\_scan or /sn\_cicd/instance\_scan/point\_scan.

**Note:** This endpoint is part of the CICD Instance Scan Execution Service API and is used under the `sn_cicd` namespace.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/instance_scan/result/{progress_id}`

Default URL: `/api/sn_cicd/instance_scan/result/{progress_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_request_parameters"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td>

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

progress\_id

</td><td>

Unique identifier of the function for which to return progress information. This value is returned in the **links.progress.id** parameter of the endpoint that initiated the action, such as /sn\_cicd/instance\_scan/full\_scan or /sn\_cicd/instance\_scan/point\_scan.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Request body

The API accepts these JSON or XML elements in the request body.

|Element|Description|
|-------|-----------|
|None| |

### Response body

The API returns these JSON or XML elements in the response body.

<table id="table_mc1_pr1_tx"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error">

Error message with details about the error.Data type: String

</td></tr><tr><td>

links

</td><td id="entry-link">

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr><td>

links.findings

</td><td>

Object that contains information about the instance scan findings.

</td></tr><tr><td>

links.findings.label

</td><td>

Additional information about the instance scan findings.

</td></tr><tr><td>

links.findings.url

</td><td>

URL to use to retrieve a list of records that violated the checks.

</td></tr><tr><td>

links.progress

</td><td id="entry-links_progress">

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr><td>

links.progress.id

</td><td>

Unique identifier of the progress detail.

</td></tr><tr><td>

links.progress.url

</td><td id="entry-progress_url">

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr><td>

links.results

</td><td id="entry-links_results">

ID and URL of the execution results.Data type: Object

```
"results": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr><td>

links.results.id

</td><td id="entry-links_results_id">

Sys\_id of the instance scan results record.

</td></tr><tr><td>

links.results.url

</td><td id="entry-links_results_url">

URL to use to obtain the results of the instance scan.

</td></tr><tr><td>

status

</td><td id="entry-status">

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr><td>

status\_detail

</td><td id="entry-status_detail">

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr><td>

status\_label

</td><td id="entry-status_label">

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr><td>

status\_message

</td><td id="entry-healthscan_status_message">

Additional information about why the operation failed. Returns an empty string if the operation is successful.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl 'instance.service-now.com/api/sn_cicd/instance_scan/result/a74c70a11b7800103d374087bc4bcb28' \
--request GET \
--header 'Accept: application/json' \
--user 'username':'password'
```

```
{
    "result": {
        "links": {
            "findings": {
                "url": "https://instance.service-now.com/api/now/table/scan_finding?sysparm_query%3Dresult%3D6f4cf8651b7800103d374087bc4bcb41%5EORDERBYsys_id",
                "label": "First 10,000 findings"
            },
            "progress": {
                "id": "a74c70a11b7800103d374087bc4bcb28",
                "url": "https://instance.service-now.com/api/sn_cicd/progress/a74c70a11b7800103d374087bc4bcb28"
            },
            "results": {
                "id": "a74c70a11b7800103d374087bc4bcb28",
                "url": "https://instance.service-now.com/api/sn_cicd/instance_scan/result/a74c70a11b7800103d374087bc4bcb28"
            }
        },
        "status": "2",
        "status_label": "Successful",
        "status_message": "",
        "status_detail": "",
        "error": ""
    }
}
```

## CI/CD - GET /sn\_cicd/progress/\{progress\_id\}

Returns the current progress and status of the Continuous Integration and Continuous Delivery \(CICD\) function associated with a specified progress ID.

Call this method after calling one of the asynchronous CICD endpoints such as /sn\_cicd/app\_repo/publish, /sn\_cicd/app\_repo/install, /sn\_cicd/testsuite/run, or /sn\_cicd/sc/apply\_stash.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/progress/{progress_id}`

Default URL: `/api/sn_cicd/progress/{progress_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

progress\_id

</td><td>

Unique identifier of the function for which to return progress information. This value is returned in the **links.progress.id** parameter of the endpoint that initiated the action, such as /sn\_cicd/app\_repo/publish, /sn\_cicd/app\_repo/install, /sn\_cicd/testsuite/run, or /sn\_cicd/sc/apply\_stash.

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|404|Not found. The requested item wasn’t found.|
|405|Invalid method. The functionality is inactive.|
|409|Conflict. The requested item isn’t unique.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-error"><td>

error

</td><td>

Error message with details about the error.Data type: String

</td></tr><tr id="row-link"><td>

links

</td><td>

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr id="row-links_progress"><td>

links.progress

</td><td>

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_progress_id"><td>

links.progress.id

</td><td>

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr id="row-links_progress_url"><td>

links.progress.url

</td><td>

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr id="row-links_results"><td>

links.results

</td><td>

ID and URL of the execution results.Data type: Object

```
"results": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_results_id"><td>

links.results.id

</td><td>

Sys\_id of the results information. Use this value when calling the associated results endpoint.Data type: String

</td></tr><tr id="row-links_results_url"><td>

links.results.url

</td><td>

URL to use to obtain the results of the endpoint execution.Data type: String

</td></tr><tr id="row-links_source"><td>

links.source

</td><td>

Sys\_id and URL information about the source record in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: Object

```
"source": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_source_id"><td>

links.source.id

</td><td>

Unique identifier of the source record.Table: Execution Tracker \[sys\_execution\_tracker\] table

Data type: String

</td></tr><tr id="row-links_source_url"><td>

links.source.url

</td><td>

URL to use to obtain the source information in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr><td>

links.stash

</td><td>

If a was created during an [apply\_changes](cicd-api.md#) operation, this object contains information about the stash. This object is not returned if a stash wasn’t created. Data type: Object

 ```
"stash": { 
 "id": "String",
 "url": "String"
} 
```

</td></tr><tr><td>

links.stash.id

</td><td>

Unique identifier of the created stash. Use this value when calling the [CI/CD - POST /sn\_cicd/sc/apply\_stash/\{stash\_id\}](cicd-api.md#) endpoint to apply the stash.Data type: String

</td></tr><tr><td>

links.stash.url

</td><td>

URL of the associated stash. Data type: String

</td></tr><tr id="row-percent_complete"><td>

percent\_complete

</td><td>

Percentage of the request that is complete.Data type: Number

</td></tr><tr id="row-status"><td>

status

</td><td>

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr id="row-status_detail"><td>

status\_detail

</td><td>

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr id="row-status_label"><td>

status\_label

</td><td>

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr id="row-status_message"><td>

status\_message

</td><td>

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### Obtain the progress of a test suite run

```
curl 'instance.servicenow.com/api/sn_cicd/progress/a4fae8911bdc00103d374087bc4bcbbd' \
--request GET \
--header 'Accept: application/json' \
--user 'username':'password'
```

Progress of the apply changes call.

```
{
    "result": {
        "links": {
            "progress": {
                "id": "a4fae8911bdc00103d374087bc4bcbbd",
                "url": "https://instance.servicenow.com/api/sn_cicd/progress/a4fae8911bdc00103d374087bc4bcbbd"
            },
            "source": {
                "id": "59c4c4d11b5c00103d374087bc4bcb26",
                "url": "https://instance.servicenow.com/api/now/table/sys_app/59c4c4d11b5c00103d374087bc4bcb26"
            }
        },
        "status": "2",
        "status_label": "Successful",
        "status_message": "This operation succeeded",
        "status_detail": "Successfully applied commit 1f14e11a7dedcbfa194beb5875fcdaa15ed8accb from source control",
        "error": "",
        "percent_complete": 100
    }
}
```

### Obtain the progress of an apply changes call. In this case, there were unsaved/uncommitted changes on the instance in Studio, so a stash was created to hold the unsaved changes

```
curl 'instance.servicenow.com/api/sn_cicd/progress/a4fae8911bdc00103d374087bc4bcbbd' \
--request GET \
--header 'Accept: application/json' \
--user 'username':'password'
```

Progress providing information on the created stash.

```
{
"result": {
   "links": {
      "progress": {
         "id": "5b12eca4e0429110f8771827f8fd36a4",
         "url": "https://instance.servicenow.com/api/sn_cicd/progress/5b12eca4e0429110f8771827f8fd36a4"
       },
       "stash": {
         "id": "fc2224e4e0429110f8771827f8fd3634",
         "url": "https://instance.servicenow.com/api/sn_cicd/sc/apply_stash/fc2224e4e0429110f8771827f8fd3634"
}
    },
    "status": "2",
    "status_label": "Successful",
    "status_message": "This operation succeeded",
    "status_detail": "Successfully applied commit fa5626f6f1f7fef677c16b4a0dd8b22ba8a6e311 from source control",
    "error": "",
    "percent_complete": 100
  }
}
```

### cURL request

```
curl 'instance.servicenow.com/api/sn_cicd/progress/5b12eca4e0429110f8771827f8fd36a4' \
--request GET \
--header 'Accept: application/json' \
--user 'username':'password'
```

Progress of a test suite run \(/sn\_cicd/testsuite/run\).

```
{
"result": {
   "links": {
      "progress": {
         "id": "e891389d1b1040103d374087bc4bcb75",
         "url": "https://instance.servicenow.com/api/sn_cicd/progress/e891389d1b1040103d374087bc4bcb75"
       },
       "results": {
         "id": "2891389d1b1040103d374087bc4bcb09",
         "url": "https://instance.servicenow.com/api/sn_cicd/testsuite/results/2891389d1b1040103d374087bc4bcb09"
       }
    },
    "status": "2",
    "status_label": "Successful",
    "status_message": "Suite passed",
    "status_detail": "Suite passed",
    "error": "",
    "percent_complete": 100
  }
}
```

## CI/CD - GET /sn\_cicd/testsuite/results/\{result\_id\}

Returns the results of a test suite run based on a specified results identifier.

Call this endpoint after calling /sn\_cicd/progress/\{progress\_id\} to obtain the result of the executed test suite.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/testsuite/results/{result_id}`

Default URL: `/api/sn_cicd/testsuite/results/{result_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

result\_id

</td><td>

Unique identifier of the test suite results to retrieve. The corresponding /sn\_cicd/progress/\{progress\_id\} endpoint call returns this information.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|404|Not found. The requested item wasn’t found.|
|405|Invalid method. The functionality is inactive.|
|409|Conflict. The requested item isn’t unique.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

child\_suite\_results

</td><td>

Results of nested test suites. The format of this content is the same as the parent test.

</td></tr><tr id="row-error"><td>

error

</td><td id="entry-error">

Error message.Data type: String

</td></tr><tr id="row-link"><td>

links

</td><td id="entry-link">

Object that contains all links and sys\_ids associated with the response.Data type: Object

</td></tr><tr id="row-links_results"><td>

links.results

</td><td id="entry-links_results">

Object that contains the results information.Data type: Object

</td></tr><tr id="row-links_results_id"><td>

links.results.id

</td><td id="entry-links_results_id">

Unique identifier of the results information. Use this value when calling the endpoint /sn\_cicd/testsuite/results/\{result\_id\}.Data type: String

</td></tr><tr id="row-links_results_url"><td>

links.results.url

</td><td id="entry-links_results_url">

URL to use to obtain the results of the endpoint execution, such as results.Data type: String

</td></tr><tr id="row-percent_complete"><td>

percent\_complete

</td><td id="entry-percent_complete">

Percentage of the request that is complete.

</td></tr><tr><td>

rolledup\_test\_error\_count

</td><td>

Number of tests with errors.Data type: Number

</td></tr><tr><td>

rolledup\_test\_failure\_count

</td><td>

Number of tests that failed.Data type: Number

</td></tr><tr><td>

rolledup\_test\_skip\_count

</td><td>

Number of tests that were skipped.Data type: Number

</td></tr><tr><td>

rolledup\_test\_success\_count

</td><td>

Number of tests that ran successfully.Data type: Number

</td></tr><tr id="row-status"><td>

status

</td><td id="entry-status">

Numeric execution state. Used with **status\_label**, such as 0: Pending.Values:

-   0 \(Pending\)
-   1 \(Running\)
-   2 \(Successful\)
-   3 \(Failed\)
-   4 \(Canceled\)

 Data type: String

</td></tr><tr id="row-status_detail"><td>

status\_detail

</td><td id="entry-status_detail">

Additional information about the current state.Data type: String

</td></tr><tr id="row-status_label"><td>

status\_label

</td><td id="entry-status_label">

Execution state description. Used with **status**, such as 0: Pending.Values:

-   Pending
-   Running
-   Successful
-   Failed
-   Canceled

 Data type: String

</td></tr><tr id="row-status_message"><td>

status\_message

</td><td id="entry-status_message">

Description of the current state.Data type: String

</td></tr><tr><td>

test\_suite\_duration

</td><td>

Amount of time that it took to execute the test suite.Unit: Seconds

 Data type: String

</td></tr><tr><td>

test\_suite\_name

</td><td>

Name of the test suite.Data type: String

</td></tr><tr><td>

test\_suite\_status

</td><td>

State of the test suite.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl 'instance.servicenow.com/api/sn_cicd/testsuite/results/2891389d1b1040103d374087bc4bcb09' \
--request GET \
--header 'Accept: application/json' \
--user 'username':'password'
```

```
{
"result": {
   "links": {
       "results": {
           "id": "2891389d1b1040103d374087bc4bcb09",
           "url": "https://instance.servicenow.com/sys_atf_test_suite_result.do?sys_id=2891389d1b1040103d374087bc4bcb09"
       }
   },
   "status": "2",
   "status_label": "Successful",
   "status_message": "",
   "status_detail": "",
   "error": "",
   "test_suite_status": "success",
   "test_suite_duration": "1 Second",
   "rolledup_test_success_count": 1,
   "rolledup_test_failure_count": 0,
   "rolledup_test_error_count": 0,
   "rolledup_test_skip_count": 0,
   "test_suite_name": "Quick Test",
   "child_suite_results": []
 }
}
```

## CI/CD - POST /sn\_cicd/app/batch/install

Installs two or more packages in a single specified batch.

A batch can contain any combination of the following types:

-   Application:
    -   Scoped applications in the ServiceNow Store that are not owned by your company
    -   Scoped or global applications in the application repository that are owned by your company
    -   Your application customizations for Store applications in the application repository
-   ServiceNow plugin:

    Application customizations for scoped applications that were packaged in a plugin and were published to the application repository.


**Note:** This endpoint uses an asynchronous response model. When you call an endpoint, it kicks off the associated function, such as starting the execution of the batch install plan. The endpoint then returns a response message that contains the execution status of the requested function, typically Pending, along with a unique identifier and link. Use this information to obtain additional information about the progress or results of the request.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/app/batch/install`

Default URL: `/api/sn_cicd/app/batch/install`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

Required. User specified descriptive name for this batch request. Data type: String

</td></tr><tr><td>

notes

</td><td>

User specified additional notes about the batch install plan.Data type: String

 Default: Null

</td></tr><tr><td>

packages

</td><td>

Required. JSON array, where each object specifies details of a package to install.Data type: Array

 ```
"packages": [{
  "id": "String",
  "load_demo_data": Boolean,
  "notes": "String",
  "requested_customization_version": "String",
  "requested_version": "String",
  "type": "String" 
}]
```

</td></tr><tr><td>

packages.id

</td><td>

Required. Sys\_id of the application or identifier of the plugin to install.Data type: String

</td></tr><tr><td>

packages.load\_demo\_data

</td><td>

Flag that indicates whether demo data is loaded when installing the package.Valid values:

-   true: Demo data should be loaded.
-   false: Demo data should not be loaded.

 Data type: Boolean

 Default: false

</td></tr><tr><td>

packages.notes

</td><td>

User specified notes about the package.Data type: String

 Default: Null

</td></tr><tr><td>

packages.requested\_customization\_version

</td><td>

Version of the application customization to the store application or to the scoped ServiceNow plugin to install, such as 1.0.2 or 2.3. Data type: String

 Default: None. If this parameter is not set, then the system does not look for customizations for the application.

</td></tr><tr><td>

packages.requested\_version

</td><td>

Required if **packages.type** is set to application; ignored if set to plugin. Version of the package to install, such as 1.0.2 or 2.3.Data type: String

</td></tr><tr><td>

packages.type

</td><td>

Required. Type of package.Valid values:

-   application
-   plugin

 Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|405|Invalid method. The functionality is disabled.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-error"><td>

error

</td><td>

Error message with details about the error.Data type: String

</td></tr><tr id="row-link"><td>

links

</td><td>

All links and sys\_ids associated with the response.Data type: Object

 ```
"links": {
  "progress": {Object},
  "results": {Object},
  "rollback": {Object}
}
```

</td></tr><tr id="row-links_progress"><td>

links.progress

</td><td>

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_progress_id"><td>

links.progress.id

</td><td>

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr id="row-links_progress_url"><td>

links.progress.url

</td><td>

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr><td>

links.results

</td><td>

Describes the results link information.Data type: Object

 ```
"results": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr><td>

links.results.id

</td><td>

Sys\_id of the results of the batch endpoint call. Use this value when calling the endpoint specified in **links.results.url** to query the batch install results.Data type: String

</td></tr><tr><td>

links.results.url

</td><td>

URL to use to retrieve the results of the batch install.Data type: String

</td></tr><tr><td>

links.rollback

</td><td>

Describes the batch install rollback information.Data type: Object

 ```
"rollback": {
  "id": "String"
}
```

</td></tr><tr><td>

links.rollback.id

</td><td>

Sys\_id of the rollback details for the installed packages. Use this parameter to rollback the installation of the specified packages to their previous versions using the /sn\_cicd/app/batch/rollback/\{rollback\_id\} endpoint.**Note:** The rollback capability is only available after the installation is complete.

 Data type: String

</td></tr><tr id="row-percent_complete"><td>

percent\_complete

</td><td>

Percentage of the request that is complete.Data type: Number

</td></tr><tr id="row-status"><td>

status

</td><td>

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr id="row-status_detail"><td>

status\_detail

</td><td>

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr id="row-status_label"><td>

status\_label

</td><td>

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr id="row-status_message"><td>

status\_message

</td><td>

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### cURL request

This example initiates a batch installation called Release 2.2 Deployment that contains three packages \(one of each type\) to install.

```
curl 'instance.servicenow.com/api/sn_cicd/app/batch/install \
--request POST \
--header 'Accept: application/json' \
--user 'username':'password' \
--data { "name": "Release 2.2 Deployment",
 "packages": [
   {
     "id": "syd_id_abcefghi",
     "type": "application",
     "load_demo_data": false,
     "requested_version": "1.0.2",
     "notes": "User specific text to describe this application install"
   },
   { 
     "id": "syd_id_defabcde",
     "type": "application",
     "requested_version": "1.0.0",
     "requested_customization_version": "2.0.7",
     "notes": "Customization for CSM App1"
   },
   {
     "id": "com.glide.some.plugin",
     "type": "plugin",
     "load_demo_data": true,
     "notes": "Plugin related notes"
   }]
 }
```

```
{
"result": {
   "links": {
     "progress": {
       "id": "c159b1e9db1c0010b5e3f6c5ae961903",
       "url": "https://instance.servicenow.com/api/sn_cicd/progress/c159b1e9db1c0010b5e3f6c5ae961903"
     },
     "results": {
       "id": "df24b1e9db2d0110b5e3f6c5ae97c561",
       "url": "https://instance.servicenow.com/api/sn_cicd/app/batch/results/df24b1e9db2d0110b5e3f6c5ae97c561"
     },
     "rollback":{
       "id": "a329f82e871da64c724ba21c82a764f2"
     },
   },
   "status": "0",
   "status_label": "Pending",
   "status_message": "",
   "status_detail": "",
   "error": "",
   "percent_complete": 0
  }
}
```

## CI/CD - POST /sn\_cicd/app/batch/rollback/\{rollback\_id\}

Rolls back all of the packages associated with a specific batch installation to their previous versions.

This endpoint works in conjunction with the /sn\_cicd/app/batch/install endpoint. The **rollback\_id** is provided in the return results of this endpoint. When this endpoint is called, it rolls back all packages specified in the associated install; you cannot rollback individual packages. If there is no previous version, the endpoint uninstalls the associated package.

**Note:** This endpoint uses an asynchronous response model. When you call an endpoint, it kicks off the associated function, such as starting the execution of the batch install plan. The endpoint then returns a response message that contains the execution status of the requested function, typically Pending, along with a unique identifier and link. Use this information to obtain additional information about the progress or results of the request.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/app/batch/rollback/{rollback_id}`

Default URL: `/api/sn_cicd/app/batch/rollback/{rollback_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

rollback\_id

</td><td>

Sys\_id of the batch installation plan for which to rollback the installed packages to their previous versions. This value is returned in the **links.rollback.id** parameter of the /sn\_cicd/app/batch/install endpoint.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|404|Not found. The requested item wasn’t found.|
|405|Invalid method. The functionality is inactive.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-error"><td>

error

</td><td>

Error message with details about the error.Data type: String

</td></tr><tr id="row-link"><td>

links

</td><td>

All links and sys\_ids associated with the response.Data type: Object

 ```
"links": {
  "progress": {Object}
}
```

</td></tr><tr id="row-links_progress"><td>

links.progress

</td><td>

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_progress_id"><td>

links.progress.id

</td><td>

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr id="row-links_progress_url"><td>

links.progress.url

</td><td>

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr id="row-percent_complete"><td>

percent\_complete

</td><td>

Percentage of the request that is complete.Data type: Number

</td></tr><tr id="row-status"><td>

status

</td><td>

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr id="row-status_detail"><td>

status\_detail

</td><td>

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr id="row-status_label"><td>

status\_label

</td><td>

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr id="row-status_message"><td>

status\_message

</td><td>

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### cURL request

This example rolls back all the packages within the specified installation batch plan to their previous version.

```
curl 'instance.servicenow.com/api/sn_cicd/app/batch/rollback/a329f82e871da64c724ba21c82a764f2 \
--request POST \
--header 'Accept: application/json' \
--user 'username':'password'
```

```
{
"result": {
   "links": {
     "progress": {
       "id": "c159b1e9db1c0010b5e3f6c5ae961903",
       "url": "https://instance.servicenow.com/api/sn_cicd/progress/c159b1e9db1c0010b5e3f6c5ae961903"
     },
   "status": "0",
   "status_label": "Pending",
   "status_message": "",
   "status_detail": "",
   "error": "",
   "percent_complete": 0
  }
}
```

## CI/CD - POST /sn\_cicd/app\_repo/install

Installs the specified application from the application repository onto the instance making the endpoint call.

Using this endpoint you are able to install both unaltered and customized ServiceNow base system and ServiceNow Store applications, customized ServiceNow plugins, and your own ServiceNow applications.

The following outlines the parameters that you need to pass to implement specific use cases. All parameters that are not specified are not passed in and use the associated defaults.

-   To only install the base application and not the corresponding application customizations.
    -   sys\_id: Sys\_id of the base application that has been customized.
    -   base\_app\_version: Version of the base application to install.
-   To install a specified version of application customizations and automatically install the recommended base application version. The recommended base application version is the version of the base application that was installed on the instance at the time that the customizations were last published. Every version of application customizations has a corresponding recommended base application version.
    -   sys\_id: Sys\_id of the application that has been customized.
    -   auto\_upgrade\_base\_app: true
    -   version: Version of the application customizations to install.
-   To install the latest version of the application customizations and its corresponding recommended base application version.
    -   sys\_id: Sys\_id of the application that has been customized.
    -   auto\_upgrade\_base\_app: true
-   To install the latest version of the application customizations, but not upgrade the base application to the application customizations recommended base application version.
    -   sys\_id: Sys\_id of the application that has been customized.
    -   auto\_upgrade\_base\_app: false
-   To install application customizations along with the scoped ServiceNow plugin of the current release.
    -   scope: Scope of the plugin that has been customized OR
    -   sys\_id: Sys\_id of the application that has been customized. This is not the ID of the plugin.
    -   version: Version of the application customizations to install.
-   To install application customizations for an already installed and activated scoped plugin.
    -   sys\_id: Sys\_id of the application that has been customized. This is not the ID of the plugin.
    -   auto\_upgrade\_base\_app: false
    -   version: Version of the application customizations to install.

Since base plugins can have only one version per family release, the **auto\_upgrade\_base\_app** and **base\_app\_version** parameters don't apply to application customization installs for plugins. To activate a plugin for the first time on an instance, use the /sn\_cicd/plugin/\{plugin\_id\}/activate endpoint instead.

**Note:** This endpoint uses an asynchronous response model. When you call an endpoint, it kicks off the associated function, such as starting the execution of the batch install plan. The endpoint then returns a response message that contains the execution status of the requested function, typically Pending, along with a unique identifier and link. Use this information to obtain additional information about the progress or results of the request.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/app_repo/install`

Default URL: `/api/sn_cicd/app_repo/install`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

auto\_upgrade\_base\_app

</td><td>

Only applicable if you intend to install application customizations and the base application was built on a version that is later than the currently installed version. Flag that indicates whether the associated base application should be automatically upgraded to a later version.

Valid values:

-   true: Automatically upgrade the associated base application.
-   false: Leave the base application as the version currently installed on the instance.

Data type: Boolean

Default: false

</td></tr><tr><td>

base\_app\_version

</td><td>

Version of the base application to install. A base application is any third-party application that is available in theServiceNow Store. If the application has no application customizations, or if the application has application customizations and you are only updating the base application, then enter the updated version of the application in this parameter. If you are updating application customizations, don't pass this parameter, but rather pass the **version** parameter.

Data type: String

Default: Null

</td></tr><tr><td>

scope

</td><td>

Required if **sys\_id** is not specified. Scope name of the application, such as `x_aah_custom_app`.Data type: String

Table: In the scope field in the Custom Application \[sys\_app\] table or Store Application \[sys\_store\_app\] table.

</td></tr><tr><td>

sys\_id

</td><td>

Required if **scope** is not specified. Sys\_id of the application to install.Data type: String

Table: In the Sys ID field in the Custom Application \[sys\_app\] table or Store Application \[sys\_store\_app\] table.

</td></tr><tr><td>

version

</td><td>

Version of the application to install.Data type: String

Default: If the **base\_app\_version** parameter is empty and the **auto\_upgrade\_base\_app** parameter is set to true, installs the latest application customizations and its recommended base application version \(as long as it doesn't downgrade the base application.\)

If the **auto\_upgrade\_base\_app** parameter is false, installs the application customizations, but the base application is not upgraded.

If the **base\_app\_version** parameter is defined, only installs the base application.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|404|Not found. The requested item wasn’t found.|
|405|Invalid method. The functionality is inactive.|
|409|Conflict. The requested item isn’t unique.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-error"><td>

error

</td><td>

Error message with details about the error.Data type: String

</td></tr><tr id="row-link"><td>

links

</td><td>

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr id="row-links_progress"><td>

links.progress

</td><td>

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_progress_id"><td>

links.progress.id

</td><td>

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr id="row-links_progress_url"><td>

links.progress.url

</td><td>

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr id="row-percent_complete"><td>

percent\_complete

</td><td>

Percentage of the request that is complete.Data type: Number

</td></tr><tr><td>

rollback\_version

</td><td>

If available, the previously installed version. If not available, null.Data type: String

</td></tr><tr id="row-status"><td>

status

</td><td>

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr id="row-status_detail"><td>

status\_detail

</td><td>

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr id="row-status_label"><td>

status\_label

</td><td>

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr id="row-status_message"><td>

status\_message

</td><td>

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl 'instance.servicenow.com/api/sn_cicd/app_repo/install?sys_id=2d146921dbd80010caf55268dc9619d8' \
--request POST \
--header 'Accept: application/json' \
--user 'username':'password'
```

```
{
"result": {
   "links": {
     "progress": {
        "id": "c159b1e9db1c0010b5e3f6c5ae961903",
        "url": "https://instance.servicenow.com/api/sn_cicd/progress/c159b1e9db1c0010b5e3f6c5ae961903"
      }
   },
   "status": "0",
   "status_label": "Pending",
   "status_message": "",
   "status_detail": "",
   "error": "",
   "percent_complete": 0,
   "rollback_version": "1.1.0"
  }
}
```

## CI/CD - POST /sn\_cicd/app\_repo/publish

Publishes the specified application and all of its artifacts to the application repository.

**Note:** If there are uncommitted changes to tracked files when you call this endpoint, it returns a 400 Bad Request status code. You can either commit the changes manually in Studio or call the [CI/CD - POST /sn\_cicd/sc/apply\_changes](cicd-api.md#) endpoint to stash the changes. Changes that aren’t tracked in the Customer Updates \[sys\_update\_xml\] table are committed automatically after publishing to the application repository. For information about the layout of the changes in the Customer Updates table and a description of the changes that aren’t represented in this table, see [Customer Updates table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_CustomerUpdatesTable.md).

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/app_repo/publish`

Default URL: `/api/sn_cicd/app_repo/publish`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dev\_notes

</td><td>

Developer notes to store with the application.Data type: String

</td></tr><tr><td>

scope

</td><td>

Required if **sys\_id** isn’t specified. The scope of the application.Data type: String

Table: In the scope field of the Custom Application \[sys\_app\] table.

</td></tr><tr><td>

sys\_id

</td><td>

Required if **scope** isn’t specified. The sys\_id of the application to store in the repository.Data type: String

Table: In the Sys ID field of the Custom Application \[sys\_app\] table.

</td></tr><tr><td>

version

</td><td>

Version under which to store the application.If the version number is passed, the publish process uses that version and updates the local application version if different. If the version number isn’t passed, the publish process uses the current version of the local application and fails if that version exists in the application repository.

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Request failed. Possible issues:

-   The application version isn’t correct or is a downgrade.
-   The application is connected to source control and contains uncommitted changes that must be resolved.

Consult the returned error message for additional information.

</td></tr><tr id="row-401-status-code"><td>

401

</td><td>

The user credentials are incorrect.

</td></tr><tr id="row-403-status-code"><td>

403

</td><td>

Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.

</td></tr><tr id="row-404-status-code"><td>

404

</td><td>

Not found. The requested item wasn’t found.

</td></tr><tr id="row-405-status-code"><td>

405

</td><td>

Invalid method. The functionality is inactive.

</td></tr><tr id="row-409-status-code"><td>

409

</td><td>

Conflict. The requested item isn’t unique.

</td></tr><tr id="row-500-status-code"><td>

500

</td><td>

Internal server error. An unexpected error occurred while processing the request.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-error"><td>

error

</td><td>

Error message with details about the error.Data type: String

</td></tr><tr id="row-link"><td>

links

</td><td>

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr id="row-links_progress"><td>

links.progress

</td><td>

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_progress_id"><td>

links.progress.id

</td><td>

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr id="row-links_progress_url"><td>

links.progress.url

</td><td>

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr id="row-percent_complete"><td>

percent\_complete

</td><td>

Percentage of the request that is complete.Data type: Number

</td></tr><tr id="row-status"><td>

status

</td><td>

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr id="row-status_detail"><td>

status\_detail

</td><td>

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr id="row-status_label"><td>

status\_label

</td><td>

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr id="row-status_message"><td>

status\_message

</td><td>

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>The following example shows how to publish the application with the specified sys\_id and all of its artifacts to the application repository.

```
curl 'instance.servicenow.com/api/sn_cicd/app_repo/publish?sys_id=4dd9686d1b9800103d374087bc4bcb3d' \
--request POST \
--header 'Accept: application/json' \
--user 'username':'password'
```

```
{
"result": {
   "links": {
       "progress": {
           "id": "d174f8e11bd800103d374087bc4bcbd9",
           "url": "https://instance.service-now.com/api/sn_cicd/progress/d174f8e11bd800103d374087bc4bcbd9"
        }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": "",
    "percent_complete": 0
  }
}
```

## CI/CD - POST /sn\_cicd/app\_repo/rollback

Initiates a rollback of a specified application to a specified version.

**Note:** The rollback functionality is only available after the installation is complete.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/app_repo/rollback`

Default URL: `/api/sn_cicd/app_repo/rollback`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

scope

</td><td>

Required if **sys\_id** is not specified. The scope name of the application to rollback.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Required if **scope** is not specified. The sys\_id of the application to rollback.Data type: String

</td></tr><tr><td>

version

</td><td>

Required. Version of the application that is expected after the rollback operation. If the request is to rollback an App Customization install, then set this field to the version of the base application that the system is expected to have after the rollback operation.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|405|Invalid method. The functionality is inactive.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-error"><td>

error

</td><td>

Error message with details about the error.Data type: String

</td></tr><tr id="row-link"><td>

links

</td><td>

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr id="row-links_progress"><td>

links.progress

</td><td>

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_progress_id"><td>

links.progress.id

</td><td>

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr id="row-links_progress_url"><td>

links.progress.url

</td><td>

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr id="row-percent_complete"><td>

percent\_complete

</td><td>

Percentage of the request that is complete.Data type: Number

</td></tr><tr id="row-status"><td>

status

</td><td>

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr id="row-status_detail"><td>

status\_detail

</td><td>

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr id="row-status_label"><td>

status\_label

</td><td>

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr id="row-status_message"><td>

status\_message

</td><td>

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl 'instance.servicenow.com/api/sn_cicd/app_repo/rollback?sys_id=2d146921dbd80010caf55268dc9619d8&version=1.1.0' \
--request POST \
--header 'Accept: application/json' \
--user 'username':'password'
```

```
{
"result": {
   "links": {
      "progress": {
          "id": "f7ddb1eddb1c0010b5e3f6c5ae9619c1",
          "url": "https://instance.service-now.com/api/sn_cicd/progress/f7ddb1eddb1c0010b5e3f6c5ae9619c1"
       }
   },
   "status": "0",
   "status_label": "Pending",
   "status_message": "",
   "status_detail": "",
   "error": "",
   "percent_complete": 0
  }
}
```

## CI/CD - POST /sn\_cicd/instance\_scan/full\_scan

Runs all active checks present in your instance.

You can run checks that are provided with Instance Scan or you can create your own checks. For more information, see [Instance Scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hs-landing-page.md).

**Note:** This endpoint is part of the CICD Instance Scan Execution Service API and is used under the `sn_cicd` namespace.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/instance_scan/full_scan`

Default URL: `/api/sn_cicd/instance_scan/full_scan`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_request_parameters"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td>

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Request body

The API accepts these JSON or XML elements in the request body.

|Element|Description|
|-------|-----------|
|None| |

### Response body

The API returns these JSON or XML elements in the response body.

<table id="table_mc1_pr1_tx"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error">

Error message with details about the error.Data type: String

</td></tr><tr><td>

links

</td><td id="entry-link">

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr><td>

links.progress

</td><td id="entry-links_progress">

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr><td>

links.progress.id

</td><td>

Unique identifier of the progress detail. Use this value when calling the endpoint /sn\_cicd/instance\_scan/result/\{progress\_id\}.

</td></tr><tr><td>

links.progress.url

</td><td id="entry-progress_url">

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr><td>

status

</td><td id="entry-status">

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr><td>

status\_detail

</td><td id="entry-status_detail">

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr><td>

status\_label

</td><td id="entry-status_label">

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr><td>

status\_message

</td><td id="entry-healthscan_status_message">

Additional information about why the operation failed. Returns an empty string if the operation is successful.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl 'instance.service-now.com/api/sn_cicd/instance_scan/full_scan' \
--request POST \
--header 'Accept: application/json' \
--user 'username':'password'
```

```
{
"result": {
   "links": {
       "progress": {
           "id": "a4fae8911bdc00103d374087bc4bcbbd",
           "url": "https://instance.service-now/api/sn_cicd/progress/a4fae8911bdc00103d374087bc4bcbbd"
        }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": ""
  }
}
```

## CI/CD - POST /sn\_cicd/instance\_scan/point\_scan

Executes all applicable checks against a specified record.

For example, if you execute a point scan against a Catalog Item, only the checks applicable to the Catalog Item table run, and only the specified record is scanned.

You can run checks that are provided with Instance Scan or you can create your own checks. For more information, see [Instance Scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hs-landing-page.md).

**Note:** This endpoint is part of the CICD Instance Scan Execution Service API and is used under the `sn_cicd` namespace.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/instance_scan/point_scan`

Default URL: `/api/sn_cicd/instance_scan/point_scan`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_request_parameters"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td>

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

target\_table

</td><td>

Required. Name of the table in which the record to scan resides, such as "Incident."Data type: String

</td></tr><tr><td>

target\_sys\_id

</td><td>

Required. The sys\_id of the record within the specified table to scan.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Invalid or empty query parameters.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Request body

The API accepts these JSON or XML elements in the request body.

|Element|Description|
|-------|-----------|
|None| |

### Response body

The API returns these JSON or XML elements in the response body.

<table id="table_mc1_pr1_tx"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error">

Error message with details about the error.Data type: String

</td></tr><tr><td>

links

</td><td id="entry-link">

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr><td>

links.progress

</td><td id="entry-links_progress">

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr><td>

links.progress.id

</td><td>

Unique identifier of the progress detail. Use this value when calling the endpoint /sn\_cicd/instance\_scan/result/\{progress\_id\}.

</td></tr><tr><td>

links.progress.url

</td><td id="entry-progress_url">

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr><td>

status

</td><td id="entry-status">

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr><td>

status\_detail

</td><td id="entry-status_detail">

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr><td>

status\_label

</td><td id="entry-status_label">

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr><td>

status\_message

</td><td id="entry-healthscan_status_message">

Additional information about why the operation failed. Returns an empty string if the operation is successful.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl 'instance.service-now.com/api/sn_cicd/instance_scan/point_scan?target_table=incident&target_sys_id=2d146921dbd80010caf55268dc9619d8' \
--request POST \
--header 'Accept: application/json' \
--user 'username':'password'
```

```
{
"result": {
   "links": {
       "progress": {
           "id": "a4fae8911bdc00103d374087bc4bcbbd",
           "url": "https://instance.service-now/api/sn_cicd/progress/a4fae8911bdc00103d374087bc4bcbbd"
        }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": ""
  }
}
```

## CI/CD - POST /sn\_cicd/instance\_scan/suite\_scan/combo/\{combo\_sys\_id\}

Runs a scan using a suite and target \(scoped apps or update sets\) that have already run previously.

Before calling this endpoint, you must call the /sn\_cicd/instance\_scan/suite\_scan/\{suite\_sys\_id\}/scoped\_apps or /sn\_cicd/instance\_scan/suite\_scan/\{suite\_sys\_id\}/update\_sets endpoints, or [execute a suite scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hc-execute-suite-scan.md) in the UI.

**Note:** This endpoint is part of the CICD Instance Scan Execution Service API and is used under the `sn_cicd` namespace.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/instance_scan/suite_scan/combo/{combo_sys_id}`

Default URL: `/api/sn_cicd/instance_scan/suite_scan/combo/{combo_sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

combo\_sys\_id

</td><td>

Sys\_id of the scan to run. The scan must be an existing scan that you want to re-run.Data type: String

Table: Combo \[scan\_combo\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error">

Error message with details about the error.Data type: String

</td></tr><tr><td>

links

</td><td id="entry-link">

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr><td>

links.progress

</td><td id="entry-links_progress">

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr><td>

links.progress.id

</td><td>

Unique identifier of the progress detail. Use this value when calling the endpoint /sn\_cicd/instance\_scan/result/\{progress\_id\}.Data type: String

</td></tr><tr><td>

links.progress.url

</td><td id="entry-progress_url">

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr><td>

status

</td><td id="entry-status">

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr><td>

status\_detail

</td><td id="entry-status_detail">

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr><td>

status\_label

</td><td id="entry-status_label">

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr><td>

status\_message

</td><td id="entry-healthscan_status_message">

Additional information about why the operation failed. Returns an empty string if the operation is successful.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_cicd/instance_scan/suite_scan/combo/245d29cc1bd32010178aed72604bcb4b" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body - success.

```
{
  "result": {
    "links": {
      "progress": {
        "id": "c08be5c71b1b2010178aed72604bcb6e",
        "url": "https://instance.servicenow.com/api/sn_cicd/progress/c08be5c71b1b2010178aed72604bcb6e"
      }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": ""
  }
}
```

## CI/CD - POST /sn\_cicd/instance\_scan/suite\_scan/\{suite\_sys\_id\}/scoped\_apps

Runs all active checks inside a suite against a list of scoped apps.

**Note:** This endpoint is part of the CICD Instance Scan Execution Service API and is used under the `sn_cicd` namespace.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/instance_scan/suite_scan/{suite_sys_id}/scoped_apps`

Default URL: `/api/sn_cicd/instance_scan/suite_scan/{suite_sys_id}/scoped_apps`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

suite\_sys\_id

</td><td>

Sys\_id of the [suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hc-suites-mgmt.md) to run.Data type: String

Table: Suite \[scan\_check\_suite\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

app\_scope\_sys\_ids

</td><td>

Required. A list of sys\_ids of the scoped applications to scan. Can't be an empty array. Data type: Array

```
app_scope_sys_ids: ["String", "String", "String"]
```

Table: Application \[sys\_scope\]

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error">

Error message with details about the error.Data type: String

</td></tr><tr><td>

links

</td><td id="entry-link">

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr><td>

links.progress

</td><td id="entry-links_progress">

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr><td>

links.progress.id

</td><td>

Unique identifier of the progress detail. Use this value when calling the endpoint /sn\_cicd/instance\_scan/result/\{progress\_id\}.Data type: String

</td></tr><tr><td>

links.progress.url

</td><td id="entry-progress_url">

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr><td>

status

</td><td id="entry-status">

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr><td>

status\_detail

</td><td id="entry-status_detail">

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr><td>

status\_label

</td><td id="entry-status_label">

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr><td>

status\_message

</td><td id="entry-healthscan_status_message">

Additional information about why the operation failed. Returns an empty string if the operation is successful.Data type: String

</td></tr></tbody>
</table>### cURL request

This example runs all active checks inside a suite against one scoped application.

```
curl "https://instance.servicenow.com/api/sn_cicd/instance_scan/suite_scan/833655cc1b94101046e87733cd4bcb4e/scoped_apps" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{app_scope_sys_ids: [\"078e8020950f12a215a92e8ad9b346e0\"]}" \
--user 'username':'password'
```

Response body - success.

```
{
  "result": {
    "links": {
      "progress": {
        "id": "147fc14b1b572010178aed72604bcbca",
        "url": "https://instance.servicenow.com/api/sn_cicd/progress/147fc14b1b572010178aed72604bcbca"
      }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": ""
  }
}
```

## CI/CD - POST /sn\_cicd/instance\_scan/suite\_scan/\{suite\_sys\_id\}/update\_sets

Runs all active checks inside a suite against a list of update sets.

**Note:** This endpoint is part of the CICD Instance Scan Execution Service API and is used under the `sn_cicd` namespace.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/instance_scan/suite_scan/{suite_sys_id}/update_sets`

Default URL: `/api/sn_cicd/instance_scan/suite_scan/{suite_sys_id}/update_sets`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

suite\_sys\_id

</td><td>

Sys\_id of the [suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/instance-scan/hc-suites-mgmt.md) to run.Data type: String

Table: Suite \[scan\_check\_suite\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

update\_set\_sys\_ids

</td><td>

Required. List of sys\_ids of the update sets to scan. Can't be an empty array. Data type: Array

```
update_set_sys_ids: ["String", "String", "String"]
```

Table: Update Set \[sys\_update\_set\]

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_dm1_1pk_fpb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td id="entry-error">

Error message with details about the error.Data type: String

</td></tr><tr><td>

links

</td><td id="entry-link">

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr><td>

links.progress

</td><td id="entry-links_progress">

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr><td>

links.progress.id

</td><td>

Unique identifier of the progress detail. Use this value when calling the endpoint /sn\_cicd/instance\_scan/result/\{progress\_id\}.Data type: String

</td></tr><tr><td>

links.progress.url

</td><td id="entry-progress_url">

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr><td>

status

</td><td id="entry-status">

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr><td>

status\_detail

</td><td id="entry-status_detail">

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr><td>

status\_label

</td><td id="entry-status_label">

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr><td>

status\_message

</td><td id="entry-healthscan_status_message">

Additional information about why the operation failed. Returns an empty string if the operation is successful.Data type: String

</td></tr></tbody>
</table>### cURL request

This example runs all active checks inside a suite against one update set.

```
curl "https://instance.servicenow.com/api/sn_cicd/instance_scan/suite_scan/833655cc1b94101046e87733cd4bcb4e/update_sets" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{update_set_sys_ids: [\"7abef63c1b572010178aed72604bcbfd\"]}" \
--user 'username':'password'
```

Response body - success.

```
{
  "result": {
    "links": {
      "progress": {
        "id": "d27511031b972010178aed72604bcb72",
        "url": "https://instance.servicenow.com/api/sn_cicd/progress/d27511031b972010178aed72604bcb72"
      }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": ""
  }
}
```

## CI/CD - POST /sn\_cicd/plugin/\{plugin\_id\}/activate

Activates the specified plugin.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/plugin/{plugin_id}/activate`

Default URL: `/api/sn_cicd/plugin/{plugin_id}/activate`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr id="row-plugin_id"><td>

plugin\_id

</td><td id="entry-plugin_id">

Unique identifier of the plugin. You can locate this identifier on the Plugins page within the card of the desired plugin; identified with the name "ID".Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|404|Not found. The requested item wasn’t found.|
|405|Invalid method. The functionality is inactive.|
|409|Conflict. The requested item isn’t unique.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-error"><td>

error

</td><td>

Error message with details about the error.Data type: String

</td></tr><tr id="row-link"><td>

links

</td><td>

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr id="row-links_progress"><td>

links.progress

</td><td>

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_progress_id"><td>

links.progress.id

</td><td>

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr id="row-links_progress_url"><td>

links.progress.url

</td><td>

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr id="row-links_results"><td>

links.results

</td><td>

ID and URL of the execution results.Data type: Object

```
"results": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_results_id"><td>

links.results.id

</td><td>

Sys\_id of the results information. Use this value when calling the associated results endpoint.Data type: String

</td></tr><tr id="row-links_results_url"><td>

links.results.url

</td><td>

URL to use to obtain the results of the endpoint execution.Data type: String

</td></tr><tr id="row-percent_complete"><td>

percent\_complete

</td><td>

Percentage of the request that is complete.Data type: Number

</td></tr><tr id="row-status"><td>

status

</td><td>

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr id="row-status_detail"><td>

status\_detail

</td><td>

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr id="row-status_label"><td>

status\_label

</td><td>

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr id="row-status_message"><td>

status\_message

</td><td>

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl 'instance.servicenow.com/api/sn_cicd/plugin/com.glide.web_service_aggregate/activate' \
--request POST \
--header 'Accept: application/json' \
--user 'username':'password'
```

```
{
"result": {
   "links": {
      "progress": {
          "id": "5b3f052ddb580010caf55268dc961963",
          "url": "https://instance.service-now.com/api/sn_cicd/progress/5b3f052ddb580010caf55268dc961963"
       }
   },
   "status": "0",
   "status_label": "Pending",
   "status_message": "",
   "status_detail": "",
   "error": "",
   "percent_complete": 0
  }
}
```

## CI/CD - POST /sn\_cicd/plugin/\{plugin\_id\}/rollback

Rolls back the specified plugin to the previous installed version. If no prior version has been installed, returns an error.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}plugin/{plugin_id}/rollback`

Default URL: `/api/sn_cicd/plugin/{plugin_id}/rollback`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr id="row-plugin_id"><td>

plugin\_id

</td><td id="entry-plugin_id">

Unique identifier of the plugin. You can locate this identifier on the Plugins page within the card of the desired plugin; identified with the name "ID".Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|404|Not found. The requested item wasn’t found.|
|405|Invalid method. The functionality is inactive.|
|409|Conflict. The requested item isn’t unique.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-error"><td>

error

</td><td>

Error message with details about the error.Data type: String

</td></tr><tr id="row-link"><td>

links

</td><td>

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr id="row-links_progress"><td>

links.progress

</td><td>

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_progress_id"><td>

links.progress.id

</td><td>

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr id="row-links_progress_url"><td>

links.progress.url

</td><td>

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr id="row-percent_complete"><td>

percent\_complete

</td><td>

Percentage of the request that is complete.Data type: Number

</td></tr><tr id="row-status"><td>

status

</td><td>

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr id="row-status_detail"><td>

status\_detail

</td><td>

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr id="row-status_label"><td>

status\_label

</td><td>

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr id="row-status_message"><td>

status\_message

</td><td>

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl 'instance.servicenow.com/api/sn_cicd/plugin/com.glide.web_service_aggregate/rollback' \
--request POST \
--header 'Accept: application/json' \
--user 'username':'password'
```

```
{
"result": {
   "links": {
      "progress": {
         "id": "6185dd61db980010caf55268dc961916",
          "url": "https://instance.service-now.com/api/sn_cicd/progress/6185dd61db980010caf55268dc961916"
        }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": "",
    "percent_complete": 0
  }
}
```

## CI/CD - POST /sn\_cicd/sc/apply\_changes

Starts applying changes from a remote source control to a specified local application or application-customization.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/sc/apply_changes`

Default URL: `/api/sn_cicd/sc/apply_changes`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

auto\_upgrade\_base\_app

</td><td>

Only applicable when changes are applied for app-customization and the latest commit on the Git repository is built on a version that is later than that of the base application that is currently installed on the local instance. Flag that indicates whether the system should auto upgrade the base application to a later version. Data type: Boolean

 Default: true

</td></tr><tr><td>

branch\_name

</td><td>

Name of the branch in the source control system from which to acquire the application.Data type: String

 Default: Default branch specified on the source control system.

</td></tr><tr><td>

scope

</td><td>

Required if **sys\_id** is not specified. The scope name of the application for which to apply the changes, such as x\_aah\_custom\_app. You can locate this value in the **scope** field in the Custom Application \[sys\_app\] table or Store Application \[sys\_store\_app\] table for the app-customization.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Required if **scope** is not specified. The sys\_id of the application for which to apply the changes. You can locate this value in the **Sys ID** field in the Custom Application \[sys\_app\] table or Store Application \[sys\_store\_app\] table for the app-customization.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|404|Not found. The requested item wasn’t found.|
|405|Invalid method. The functionality is inactive.|
|409|Conflict. The requested item isn’t unique.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-error"><td>

error

</td><td>

Error message with details about the error.Data type: String

</td></tr><tr id="row-link"><td>

links

</td><td>

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr id="row-links_progress"><td>

links.progress

</td><td>

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_progress_id"><td>

links.progress.id

</td><td>

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr id="row-links_progress_url"><td>

links.progress.url

</td><td>

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr id="row-percent_complete"><td>

percent\_complete

</td><td>

Percentage of the request that is complete.Data type: Number

</td></tr><tr id="row-status"><td>

status

</td><td>

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr id="row-status_detail"><td>

status\_detail

</td><td>

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr id="row-status_label"><td>

status\_label

</td><td>

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr id="row-status_message"><td>

status\_message

</td><td>

Additional information about why the operation failed. Returns an empty string if the operation is successful.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl 'https://instance.servicenow.com/api/sn_cicd/sc/apply_changes?app_sys_id=043db024db737300a9a754e4dc961915' \
--request POST \
--header 'Accept: application/json' \
--user 'username':'password'
```

```
{
"result": {
   "links": {
       "progress": {
           "id": "a4fae8911bdc00103d374087bc4bcbbd",
           "url": "https://instance.service-now/api/sn_cicd/progress/a4fae8911bdc00103d374087bc4bcbbd"
        }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": "",
    "percent_complete": 0
  }
}
```

## CI/CD - POST /sn\_cicd/sc/apply\_stash/\{stash\_id\}

Starts applying a previously generated "stash" of changes from a remote source control to a specified local application or application-customization.

This endpoint works in conjunction with the [POST/api/sn\_cicd/sc/apply\_changes](cicd-api.md#) and [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#) endpoints. When the POST /api/sn\_cicd/sc/apply\_changes endpoint is called, any unsaved or uncommitted changes in App Engine Studio on the associated instance are saved into the database as a [stash](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/stash-changes.md).

The way to determine whether a stash was created when the changes were initially applied is to call the GET /sn\_cicd/progress/\{progress\_id\} endpoint. If a stash was created, the sys\_id \(**stash\_id**\) and URL of the stash are returned. To apply the stashed changes to the associated application, call this apply\_stash endpoint using the **stash\_id** returned by the progress endpoint.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/sc/apply_stash/{stash_id}`

Default URL: `/api/sn_cicd/sc/apply_stash/{stash_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

stash\_id

</td><td>

Unique identifier of the stash to apply. This value is returned in the **links.stash.id** parameter in the corresponding [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#) endpoint call.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|404|Not found. The requested item wasn’t found.|
|405|Invalid method. The functionality is inactive.|
|409|Conflict. The requested item isn’t unique.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-error"><td>

error

</td><td>

Error message with details about the error.Data type: String

</td></tr><tr id="row-link"><td>

links

</td><td>

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr id="row-links_progress"><td>

links.progress

</td><td>

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_progress_id"><td>

links.progress.id

</td><td>

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr id="row-links_progress_url"><td>

links.progress.url

</td><td>

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr id="row-percent_complete"><td>

percent\_complete

</td><td>

Percentage of the request that is complete.Data type: Number

</td></tr><tr id="row-status"><td>

status

</td><td>

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr id="row-status_detail"><td>

status\_detail

</td><td>

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr id="row-status_label"><td>

status\_label

</td><td>

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr id="row-status_message"><td>

status\_message

</td><td>

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call the apply\_stash endpoint for **stash\_id** fc2224e4e0429110f8771827f8fd3634.

```
curl "https://instance.servicenow.com/api/sn_cicd/sc/apply_stash/fc2224e4e0429110f8771827f8fd3634"\
--request POST \
--header "Accept:application/json" \
--header "Content_Type:application/json" \
--user 'username':'password'

```

The stash is pending, so not yet applied.

```
{
  "result": {
    "links": {
      "progress": {
        "id": "6b04ec28e0429110f8771827f8fd36a4",
        "url": "https://instance.servicenow.com/api/sn_cicd/progress/6b04ec28e0429110f8771827f8fd36a4"
      }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": "",
    "percent_complete": 0
  }
}
```

## CI/CD - POST /sn\_cicd/sc/import

Imports an application using the specified repository URL and branch name.

Use this endpoint to import an application from source control in the calling instance so you can then use Continuous Integration and Continuous Delivery \(CICD\) endpoints, such as [/sn\_cicd/sc/apply\_changes](cicd-api.md#), to deploy the application to upper environments.

**Note:** Before using this endpoint, a Git repository that has been setup by another instance using **Link to source control** must be available.

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/sc/import`

Default URL: `/api/sn_cicd/sc/import`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

auto\_upgrade\_base\_app

</td><td>

Only applicable when the application being imported is an app-customization and the latest commit on the Git repository is built on a version that is later than that of the base application that is currently installed on the local instance. Flag that indicates whether the system should auto-upgrade the base application to a later version.

 Valid values:

-   true: Auto-upgrade the base application.
-   false: Do not auto-upgrade the base application.

 Data type: Boolean

 Default: True

</td></tr><tr><td>

branch\_name

</td><td>

Required. Name of the branch in the source control system to import the application from.Data type: String

</td></tr><tr><td>

credential\_sys\_id

</td><td>

Sys\_id of the credentials that have access to the Git repository.Data type: String

 Default: Sys\_id set in the system properties glide.source\_control.default\_basic\_auth\_credential\_sys\_id or glide.source\_control.default\_ssh\_private\_key\_credential\_sys\_id, depending on whether the **repo\_url** parameter is an https or ssh repository. By default, this property is empty.

</td></tr><tr><td>

mid\_server\_sys\_id

</td><td>

Sys\_id of the MID server to use for source control operations for this application.Data type: String

 Default: Empty string/NULL

</td></tr><tr><td>

repo\_url

</td><td>

Required. URL of the Git repository to import the application from.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|404|Not found. The requested item wasn’t found.|
|405|Invalid method. The functionality is inactive.|
|409|Conflict. The requested item isn’t unique.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-error"><td>

error

</td><td>

Error message with details about the error.Data type: String

</td></tr><tr id="row-link"><td>

links

</td><td>

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr id="row-links_progress"><td>

links.progress

</td><td>

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_progress_id"><td>

links.progress.id

</td><td>

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr id="row-links_progress_url"><td>

links.progress.url

</td><td>

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr id="row-percent_complete"><td>

percent\_complete

</td><td>

Percentage of the request that is complete.Data type: Number

</td></tr><tr id="row-status"><td>

status

</td><td>

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr id="row-status_detail"><td>

status\_detail

</td><td>

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr id="row-status_label"><td>

status\_label

</td><td>

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr id="row-status_message"><td>

status\_message

</td><td>

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to import the application located at `https://code.devsnc.com/some-user/ncRegrApp1.git` in the `main_branch`.

```
curl "https://instance.servicenow.com/api/sn_cicd/sc/import?repo_url=https%3A%2F%2Fcode.devsnc.com%2Fsome-user%2FncRegrApp1.git&branch_name=main_branch&credential_sys_id=af9b6d6180feb010f8779c30d4dd6b6b" \
--request POST \
--header "Accept:application/json" \
--user 'admin':'admin'
```

Returns the progress of the import.

```
{
  "result": {
    "links": {
      "progress": {
        "id": "a18c06ea64f23010f87769cd983d4574",
        "url": "https://instance.servicenow.com/api/sn_cicd/progress/a18c06ea64f23010f87769cd983d4574"
      }
    },
    "status": "0",
    "status_label": "Pending",
    "status_message": "",
    "status_detail": "",
    "error": "",
    "percent_complete": 0
  }
}
```

## CI/CD - POST /sn\_cicd/testsuite/run

Starts a specified automated test suite. The test suite runs on the instance from which the endpoint was called.

**Note:** If the suite you are running contains UI tests, you must have either a scheduled Client Test Runner open, or be able to configure headless Test Runner execution. To learn more, see [Headless browser for Automated Test Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-headless-browser.md).

### URL format

Versioned URL: `/api/sn_cicd/{api_version}/testsuite/run`

Default URL: `/api/sn_cicd/testsuite/run`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

browser\_name

</td><td>

Name of the browser to use to run the client test. This value must match what is specified in the scheduled client test runner. For additional information on scheduled client test runners, see [Scheduled Client Test Runners](https://developer.servicenow.com/app.do#!/training/article/app_store_learnv2_atf_rome_using_the_automated_test_framework/app_store_learnv2_atf_rome_scheduled_client_test_runners?v=utah).Data type: String

 Valid values: \(must be all lower-case\)

 -   any
-   chrome
-   firefox
-   edge
-   ie
-   safari

 Default: any

</td></tr><tr><td>

browser\_version

</td><td>

Starting value of the version of the browser specified in **browser\_name** to use to run the test. For example, if you enter "9", that would enable all 9.x.x.x versions. This value must match what is specified in the scheduled client test runner.Data type: String

</td></tr><tr><td>

is\_performance\_run

</td><td>

Optional. Flag that indicates whether to execute the test suite as a performance test \(Performance Run\).

Valid values:

-   true: Runs the test suite as a performance test.
-   false: Runs the test suite with the default behavior of a standard, functional test of the instance.

Default: false

</td></tr><tr><td>

os\_name

</td><td>

Name of the operating system under which to run the test suite. This value must match what is specified in the scheduled client test runner.Data type: String

</td></tr><tr><td>

os\_version

</td><td>

Starting value of the version of the operating system under which to run the test suite. For example, if you enter "8", that would enable all 8.x.x.x versions. This value must match what is specified in the scheduled client test runner.Data type: String

</td></tr><tr><td>

run\_in\_cloud

</td><td>

Optional. Flag that indicates whether to execute the test suite in Cloud Runner or manually.Valid values:

-   true: Runs the test suite using the Cloud Runner.
-   false: Runs the test suite using the manual test runner.

Default: false

</td></tr><tr><td>

test\_suite\_sys\_id

</td><td>

Required if **test\_suite\_name** is not specified. The sys\_id of the test suite to run.Data type: String

Table: Test \[sys\_atf\_test\_suite\]

</td></tr><tr><td>

test\_suite\_name

</td><td>

Required if **test\_suite\_sys\_id** is not specified. The name of the test suite to run.Data type: String

Table:Test \[sys\_atf\_test\_suite\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|The user credentials are incorrect.|
|403|Forbidden. The user isn’t an admin or doesn’t have the sn\_cicd.sys\_ci\_automation role.|
|404|Not found. The requested item wasn’t found.|
|405|Invalid method. The functionality is inactive.|
|409|Conflict. The requested item isn’t unique.|
|500|Internal server error. An unexpected error occurred while processing the request.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-error"><td>

error

</td><td>

Error message with details about the error.Data type: String

</td></tr><tr id="row-link"><td>

links

</td><td>

Information about any links and sys\_ids associated with the update set.Data type: Object

```
"links": {
  "progress": {Object}
}
```

</td></tr><tr id="row-links_progress"><td>

links.progress

</td><td>

Progress information about the operation performed on the update set.Data type: Object

```
"progress": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_progress_id"><td>

links.progress.id

</td><td>

Sys\_id containing progress details for the operation. You can use this value when calling the endpoint [CI/CD - GET /sn\_cicd/progress/\{progress\_id\}](cicd-api.md#).Data type: String

</td></tr><tr id="row-links_progress_url"><td>

links.progress.url

</td><td>

URL to use to retrieve the progress details about the operation performed on the update set.Data type: String

</td></tr><tr id="row-links_results"><td>

links.results

</td><td>

ID and URL of the execution results.Data type: Object

```
"results": {
  "id": "String",
  "url": "String"
}
```

</td></tr><tr id="row-links_results_id"><td>

links.results.id

</td><td>

Sys\_id of the results information. Use this value when calling the associated results endpoint.Data type: String

</td></tr><tr id="row-links_results_url"><td>

links.results.url

</td><td>

URL to use to obtain the results of the endpoint execution.Data type: String

</td></tr><tr id="row-percent_complete"><td>

percent\_complete

</td><td>

Percentage of the request that is complete.Data type: Number

</td></tr><tr id="row-status"><td>

status

</td><td>

Number representing the execution state of the action performed on the update set. Corresponds with the **status\_label** descriptor.Possible values:

-   0: Pending
-   1: Running
-   2: Successful
-   3: Failed
-   4: Canceled

Data type: String

</td></tr><tr id="row-status_detail"><td>

status\_detail

</td><td>

Detailed message about the execution status, if available. Corresponds to the detailed\_message field in the Execution Tracker \[sys\_execution\_tracker\] table.Data type: String

</td></tr><tr id="row-status_label"><td>

status\_label

</td><td>

Execution status of the update set action. Corresponds with the **status** number.Possible values:

-   Canceled
-   Failed
-   Pending
-   Running
-   Successful

Data type: String

</td></tr><tr id="row-status_message"><td>

status\_message

</td><td>

Additional description of the action's current state, if available.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl 'https://instance.servicenow.com/api/sn_cicd/testsuite/run?test_suite_sys_id=632e43900b20220050192f15d6673a7e' \
--request POST \
--header 'Accept: application/json' \
--user 'username':'password'
```

```
{
"result": {
   "links": {
       "progress": {
           "id": "0578a8d91bdc00103d374087bc4bcbcc",
           "url": "https://instance.service-now.com/api/sn_cicd/progress/0578a8d91bdc00103d374087bc4bcbcc"
        }
   },
   "status": "0",
   "status_label": "Pending",
   "status_message": "",
   "status_detail": "",
   "error": "",
   "percent_complete": 0
  }
}
```

Failure response:

```
{
"result": {
    "status": "3",
    "status_label": "Failed",
    "status_message": "",
    "status_detail": "",
    "error": "Scheduled test/suite execution is disabled. Change the value of property 'sn_atf.schedule.enabled' to true to enable it"
  }
}
```

