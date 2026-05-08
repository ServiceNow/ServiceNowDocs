---
title: DevOps API
description: The DevOps API provides endpoints that enable the interaction with external DevOps tools.Returns the schema object for a specified code resource: commit, repository, or branch.Returns the current status of the specified onboarding event which is processed or being processed asynchronously by the DevOps service.Checks if the orchestration task is under change control.Retrieves change request details for a specified orchestration pipeline execution.Returns the schema object for a specified orchestration resource.Verifies that the information being passed is valid for the creation of an orchestration task and is valid for association to a previously created step.Returns the schema object for a specific plan: app, version, or work item.Enables orchestration tools to register artifacts into a ServiceNow instance.Creates an onboarding app event that is asynchronously processed by the DevOps service.Creates an onboarding tool event that is asynchronously processed by the DevOps service.Registers a callback with a ServiceNow instance for an orchestration task under change control, which can be called once a decision has been made on the change request.Verifies that the information being passed is valid for the creation of an orchestration task and is valid for association to a previously created step. If both are valid, it creates the orchestration task and makes the association.Enables orchestration tools to create new artifact packages that contain specified artifact versions.Posts the passed in payload to the Inbound Event \[sn\_devops\_inbound\] table for processing by a custom DevOps subflow.Posts the passed in payload from GitHub, Jira, or Bitbucket to the Events \[sn\_devops\_event\] table for processing by a pre-built subflow.Updates the change control information for the specified orchestration task.Updates fields in a specified change request.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 98
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# DevOps API

The DevOps API provides endpoints that enable the interaction with external DevOps tools.

This REST API enables integrators to:

-   Retrieve the available DevOps tools associated with an instance.
-   Retrieve the schema object for a code resource, plan, or orchestration resource.
-   Check if an orchestration task is under change control and check its change control status.
-   Create callbacks to associate with task executions under change control.
-   Send various event payloads, which are transformed into normalized objects and stored as code, orchestration, and plan objects.
-   Search a commit, branch, or repository using encoded queries and specific search/sort criteria.
-   Register artifact versions and packages along with their associated pipeline execution and commits.
-   Create and manage onboarding application and tool events.

For additional information, see DevOps Config.

Starting with v2, this API supports token-based authentication. Tokens can be acquired by clicking the **Copy token** button on the tool record, located in the Tool \[sn\_devops\_tool\] table. The token can then be used in an authorization header in the format `Authorization: sn_devops.DevOpsToken <tool_sys_id>:<tool_token>`.

**Note:** If Basic Auth details \(user name and password\) are provided in addition to an authorization header with token, Basic Auth takes precedence.

If the **devops.system** user is not available in your instance, use the **Switch to this user after token based authentication is successful** property. This property enables setting any user that has the sn\_devops.integration role, which is needed to complete the token authentication. For information, see DevOps Change Velocity properties.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## DevOps - GET /devops/code/schema

Returns the schema object for a specified code resource: commit, repository, or branch.

Once you have the required schema object, use it to create the request body for your corresponding POST call; POST /code/commit, POST /code/repository, or POST /code/branch.

**Note:** This endpoint only returns the request body elements that are required.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/code/schema`

Default URL: `/api/sn_devops/devops/code/schema`

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

resource

</td><td>

Required. Type of resource schema to return.Valid values \(not case-sensitive\):

-   branch
-   commit
-   repository

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|401|Invalid or missing authentication.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

branch

</td><td>

Description of the branch in which the code commit was made. Data type: Object

```
"branch": {
  "name": "String",
  "path": "String"
}
```

</td></tr><tr><td>

branch.name

</td><td>

Name of the branch in which the code commit was made. Data type: String

</td></tr><tr><td>

branch.path

</td><td>

Relative path of the branch. Data type: String

</td></tr><tr><td>

commits

</td><td>

Description of the commits.Data type: Array of Objects

```
"commits": [
  {
    "committedDate": "String",
    "committer": {Object},
    "details": [Array],
    "id": "String",
    "url": "String"      
  }
]
```

</td></tr><tr><td>

commits.committedDate

</td><td>

Date/time on which the code was committed in source DevOps tool. Data type: String

Format: ISO 8601 with time zone offset

For example: 1970-01-01T08:15:30-05:00

</td></tr><tr><td>

commits.committer

</td><td>

Description of the person/entity that requested the commit. Data type: Object

```
"committer": {
  "email": "String"
}
```

</td></tr><tr><td>

commits.committer.email

</td><td>

Email address of the person that requested the commit. Data type: String

</td></tr><tr><td>

commits.details

</td><td>

Details of the commit. **Note:** Including details in a commit is not mandatory. This endpoint returns an empty array for details if they are not included in the commit.

Data type: Array of Objects

```
"details": [
  {
    "action": "String",
    "additions": Number,
    "changes": Number,
    "deletions": Number,
    "file": "String",
    "totalChanges": Number
  }
]
```

</td></tr><tr><td>

commits.details.action

</td><td>

Action that was performed on the file. Data type: String

</td></tr><tr><td>

commits.details.additions

</td><td>

Total number of additions in the file. Data type: Number

</td></tr><tr><td>

commits.details.changes

</td><td>

Total number of changes that were made. Data type: Number

</td></tr><tr><td>

commits.details.deletions

</td><td>

Total number of deletions in the file. Data type: Number

</td></tr><tr><td>

commits.details.file

</td><td>

Path of the file that was modified relative to the branch. Data type: String

</td></tr><tr><td>

commits.details.totalChanges

</td><td>

Total number of additions and deletions. Data type: Number

</td></tr><tr><td>

commits.id

</td><td>

Source platform identifier or the commit SHA.Data type: String

</td></tr><tr><td>

commits.url

</td><td>

URL of the commit, such as "https://github.com/mycompany/mobileplatform/commit/3fa85f6457174562b3fc2c963f66afa6".Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the branch or repository, such as "Master" or "Platform-Mobile".Data type: String

</td></tr><tr><td>

path

</td><td>

Relative path of the branch. Data type: String

</td></tr><tr><td>

repository

</td><td>

Description of the repository in which the commit was made. Data type: Object

```
"repository": {
  "name": "String",
  "url": "String"
}
```

</td></tr><tr><td>

repository.name

</td><td>

Name of the repository. Data type: String

</td></tr><tr><td>

repository.url

</td><td>

URL of the repository in the source DevOps tool. Data type: String

</td></tr><tr><td>

url

</td><td>

URL of the repository, such as "https://github.com/mycompany/mobileplatform".Data type: String

</td></tr></tbody>
</table>### Sample cURL request for resource=branch

```
curl "https://instance.servicenow.com/api/sn_devops/v1/devops/code/schema?resource=branch" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
   "result": {
      "name": "Master",
      "path": "refs/heads/master",
      "repository": {
         "name": "Platform-Mobile",
         "url": "https://github.com/mycompany/mobileplatform"
      }
   }
}
```

### Sample cURL request for resource=commit

```
curl "https://instance.servicenow.com/api/sn_devops/v1/devops/code/schema?resource=commit" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
   "result": {
      "repository": {
         "name": "Platform-Mobile",
         "url": "https://github.com/mycompany/mobileplatform"
      },
      "branch": {
         "name": "refs/heads/master"
      },
      "commits": [
         {
            "committer": {
               "email": "name@email.com"
            },
            "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
            "url": "https://github.com/mycompany/mobileplatform/commit/3fa85f6457174562b3fc2c963f66afa6",
            "committedDate": "2022-01-01T08:15:30-05:00",
            "details": [
               {
                  "action": "edit",
                  "changes": "",
                  "file": "/azure-pipelines.yml",
                  "additions": 1,
                  "deletions": 0,
                  "totalChanges": 1
               }
            ]
         }
      ]
   }
}
```

### Sample cURL request for resource=repository

```
curl "https://instance.servicenow.com/api/sn_devops/v1/devops/code/schema?resource=repository" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
    "result": {
        "name": "Platform-Mobile",
        "url": "https://github.com/mycompany/mobileplatform"
    }
}
```

## DevOps - GET /devops/onboarding/status

Returns the current status of the specified onboarding event which is processed or being processed asynchronously by the DevOps service.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/onboarding/status`

Default URL: `/api/sn_devops/devops/onboarding/status`

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

id

</td><td>

Unique identifier of the onboarding event whose status to return. This value is provided in the return results of the endpoint that invoked the event request, such as /devops/onboarding/app or /devops/onboarding/tool.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|202|Pending - The onboarding request has been created and the DevOps service is processing the request.|
|207|Partial Success - The onboarding request has been created and the DevOps service will process the request.|
|400|Failed - The onboarding event failed.|
|404|Failed - The endpoint failed to find any request matching the specified event ID.|

### Response body parameters

<table id="table_rrm_t1n_h4b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Results of the onboarding request.Data type: Object

```
"result": {
  "code": "String",
  "importRequestsSysIds": "[Array],
  "messageDetails": {Object],
  "onboardingRequestID": "String",
  "status": "String"
}
```

</td></tr><tr><td>

result.code

</td><td>

HTTP status code.Data type: String

</td></tr><tr><td>

result.importRequestsSysIds

</td><td>

List of import requests that have been created as a part on the onboarding request.Data type: Array of Strings

</td></tr><tr><td>

result.messageDetails

</td><td>

Details about the onboarding event progress.Data type: Object

```
"messageDetails": {
  "apps": [Array],
  "pipelines": [Array],
  "plans": [Array],
  "repositories": [Array],
  "status": "String",
  "toolResponse": [Array]
}
```

</td></tr><tr><td>

result.messageDetails.apps

</td><td>

Defines the apps to create within the associated ServiceNow instance.Data type: Array of Objects

```
"apps": [{
  "appId": "String",
  "message": "String",
  "name": "String",
  "status": "String",
}]
```

</td></tr><tr><td>

result.messageDetails.apps.appId

</td><td>

Sys\_id of the application that was generated when the application was onboarded.Data type: String

Table: Apps \[sn\_devops\_app\]

</td></tr><tr><td>

result.messageDetails.apps.message

</td><td>

Message that describes the status of the application onboarding.Data type: String

</td></tr><tr><td>

result.messageDetails.apps.name

</td><td>

Name of the application being onboarded.Data type: String

</td></tr><tr><td>

result.messageDetails.apps.status

</td><td>

Current status of the application onboarding.Possible values:

-   Failed
-   Partial Success
-   Success

Data type: String

</td></tr><tr><td>

result.messageDetails.pipelines

</td><td>

List of pipelines associated with the onboarding event and their corresponding details.Data type: Array of Objects

```
"pipelines": [{
  "changeStepAssociation": [Array],
  "errors": "String",
  "message": "String",
  "name": "String",
  "status": "String",
}]
```

</td></tr><tr><td>

result.messageDetails.pipelines.changeStepAssociation

</td><td>

Array of objects that describe any change steps that are associated with the onboarding.Data type: Array of Objects

```
"changeStepAssociation": [{
  "changeStepName": "String",
  "status": "String",
  "summary": "String",
}]
```

</td></tr><tr><td>

result.messageDetails.pipelines.changeStepAssociation.changeStepName

</td><td>

Name of the change step.Data type: String

</td></tr><tr><td>

result.messageDetails.pipelines.changeStepAssociation.status

</td><td>

Status of change step association to the pipeline.Possible values:

-   Failed
-   Success

Data type: String

</td></tr><tr><td>

result.messageDetails.pipelines.changeStepAssociation.summary

</td><td>

Summary of the status of the change step association.Data type: String

</td></tr><tr><td>

result.messageDetails.pipelines.errors

</td><td>

List of errors detected when associating the pipeline.Data type: Array

</td></tr><tr><td>

result.messageDetails.pipelines.message

</td><td>

Message that describes the status of the pipeline association.Data type: String

</td></tr><tr><td>

result.messageDetails.pipelines.name

</td><td>

Name of the pipeline.Data type: String

</td></tr><tr><td>

result.messageDetails.pipelines.status

</td><td>

Status of the pipeline association.Data type: String

</td></tr><tr><td>

result.messageDetails.plans

</td><td>

List of plans associated with the onboarding event and their corresponding details.Data type: Array of Objects

```
"plans": [{
  "errors": "String",
  "message": "String",
  "name": "String",
  "status": "String",
}]
```

</td></tr><tr><td>

result.messageDetails.plans.errors

</td><td>

List of errors detected when associating the plan.Data type: Array

</td></tr><tr><td>

result.messageDetails.plans.message

</td><td>

Message that describes the status of the pipeline association.Data type: String

</td></tr><tr><td>

result.messageDetails.plans.name

</td><td>

Name of the plan.Data type: String

</td></tr><tr><td>

result.messageDetails.plans.status

</td><td>

Status of the plan association.Data type: String

</td></tr><tr><td>

result.messageDetails.repositories

</td><td>

List of repositories associated with the onboarding event and their corresponding details.Data type: Array of Objects

```
"repositories": [{
  "configureStatus": {Object}, 
  "name": "String",
  "status": "String",
}]
```

</td></tr><tr><td>

result.messageDetails.repositories.configureStatus

</td><td>

Details of the webhook configuration status for the repository.Data type: Object

```
"configureStatus": {
  "message": "String",
  "status": "String",
}
```

</td></tr><tr><td>

result.messageDetails.repositories.configureStatus.message

</td><td>

Message that describes the current webhook configuration status.Data type: String

</td></tr><tr><td>

result.messageDetails.repositories.configureStatus.status

</td><td>

Status of the webhook configuration.Data type: String

</td></tr><tr><td>

result.messageDetails.repositories.message

</td><td>

Message that describes the current repository association status.Data type: String

</td></tr><tr><td>

result.messageDetails.repositories.name

</td><td>

Name of the repository.Data type: String

</td></tr><tr><td>

result.messageDetails.repositories.status

</td><td>

Status of the repository association.Data type: String

</td></tr><tr><td>

result.messageDetails.status

</td><td>

Status of the onboarding request. Possible values:

-   Failed
-   Partial Success
-   Success

Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse

</td><td>

List of tools to onboard within the associated ServiceNow instance.Data type: Array of Objects

```
"toolResponse": [{
  "configureStatus": {Object},
  "connectStatus": {Object},
  "createStatus": {Object},
  "discoveryStatus": {Object},
  "name": "String",
  "status": "String",
  "type": "String"
}]
```

</td></tr><tr><td>

result.messageDetails.toolResponse.configureStatus

</td><td>

Configuration status of the tool. In case of success, it returns the **status** and **message**. In case of error, it returns the **status** and **error**.Data type: Object

```
"configureStatus": {
  "error": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

result.messageDetails.toolResponse.configureStatus.error

</td><td>

Errors detected during tool configuration.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.configureStatus.message

</td><td>

Message that describes the successful status of the tool configuration.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.configureStatus.status

</td><td>

Status of the tool configuration.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.connectStatus

</td><td>

Connection status of the tool. In case of success, it returns the **status** and **message**. In case of error, it returns the **status** and **error**.Data type: Object

```
"connectStatus": {
  "error": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

result.messageDetails.toolResponse.connectStatus.error

</td><td>

Errors detected during tool connection.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.connectStatus.message

</td><td>

Message that describes the successful status of the tool connection.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.connectStatus.status

</td><td>

Status of the tool connection.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.createStatus

</td><td>

Creation status of the tool. In case of success, it returns the **status** and **message**. In case of error, it returns the **status** and **error**.Data type: Object

```
"createStatus": {
  "error": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

result.messageDetails.toolResponse.createStatus.error

</td><td>

Errors detected during tool creation.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.createStatus.message

</td><td>

Message that describes the successful status of the tool creation.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.createStatus.status

</td><td>

Status of the tool creation.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.discoveryStatus

</td><td>

Discovery status of the tool. In case of success, it returns the **status** and **message**. In case of error, it returns the **status** and **error**.Data type: Object

```
"discoveryStatus": {
  "error": "String",
  "imports: [Array],
  "message": "String",
  "status": "String"
}
```

</td></tr><tr><td>

result.messageDetails.toolResponse.discoveryStatus.error

</td><td>

Errors detected during tool discovery.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.discoveryStatus.imports

</td><td>

List of entities that were discovered.Data type: Array of Objects

```
"imports": [{
  "details": "String",
  "id": "String",
  "status": "String"
}]
```

</td></tr><tr><td>

result.messageDetails.toolResponse.discoveryStatus.imports.details

</td><td>

Details that describe the import performed.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.discoveryStatus.imports.id

</td><td>

Sys\_id of the import request.Data type: String

Table: sn\_devops\_m2m\_inbound\_event\_import\_request

</td></tr><tr><td>

result.messageDetails.toolResponse.discoveryStatus.imports.status

</td><td>

Status of the import.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.discoveryStatus.message

</td><td>

Message that describes the status of the tool discovery.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.discoveryStatus.status

</td><td>

Status of the tool discovery.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.name

</td><td>

Name of the tool being onboarded.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.status

</td><td>

Status of the tool onboarding.Data type: String

</td></tr><tr><td>

result.messageDetails.toolResponse.type

</td><td>

Type of tool, such as Jira or Jenkins. Data type: String

</td></tr><tr><td>

result.onboardingRequestID

</td><td>

Unique identifier of the onboarding request. Use this value when calling the /devops/onboarding/status endpoint to obtain the status of the associated tool onboarding process.Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status of the onboarding request.Possible values:

-   Failed
-   Partial Success
-   Success

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows the status request of a tool onboarding.

```
curl -X GET "https://servicenow-instance/api/sn_devops/v1/devops/onboarding/status?id=IBE0001603" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
```

```
{
    "result": {
        "code": "207",
        "onboardingRequestID": "IBE0001603",
        "status": "partial-success",
        "messageDetails": {
            "status": "Partial Success",
            "toolResponse": [
                {
                    "name": "Primary Azure",
                    "type": "Azure DevOps",
                    "status": "Partial Success",
                    "createStatus": {
                        "status": "Success",
                        "message": "Created successfully"
                    },
                    "connectStatus": {
                        "status": "Failed",
                        "error": "Method failed: (/testFirst/_apis/work/boards) with code: 401 - Invalid username/password combo"
                    }
                },
                {
                    "name": "Primary Jenkins",
                    "type": "Jenkins",
                    "status": "Success",
                    "createStatus": {
                        "status": "Success",
                        "message": "Created successfully"
                    },
                    "connectStatus": {
                        "status": "Success",
                        "message": "Connected successfully"
                    },
                    "discoveryStatus": {
                        "status": "Success",
                        "message": "Discovered successfully",
                        "imports": [
                            {
                                "status": "completed",
                                "id": "2a4d216bdb2d2450fe4fd6a75e9619c3",
                                "details": "Discovered 1 new job(s) and 3 new pipeline(s)\n"
                            }
                        ]
                    }
                },
                {
                    "name": "Primary GitHub",
                    "type": "GitHub",
                    "status": "Success",
                    "createStatus": {
                        "status": "Success",
                        "message": "Created successfully"
                    },
                    "connectStatus": {
                        "status": "Success",
                        "message": "Connected successfully"
                    },
                    "discoveryStatus": {
                        "status": "Success",
                        "message": "Discovered successfully",
                        "imports": [
                            {
                                "status": "completed",
                                "id": "7f4d616bdb2d2450fe4fd6a75e9619c2",
                                "details": "Discovered 5 new repositories. "
                            }
                        ]
                    }
                },
                {
                    "name": "Primary Bitbucket",
                    "type": "BitBucket",
                    "status": "Success",
                    "createStatus": {
                        "status": "Success",
                        "message": "Created successfully"
                    },
                    "connectStatus": {
                        "status": "Success",
                        "message": "Connected successfully"
                    },
                    "discoveryStatus": {
                        "status": "Success",
                        "message": "Discovered successfully",
                        "imports": [
                            {
                                "status": "completed",
                                "id": "815da16bdb2d2450fe4fd6a75e9619d0",
                                "details": "Discovered 11 new repositories. "
                            }
                        ]
                    }
                },
                {
                    "name": "Primary Gitlab",
                    "type": "GitLab",
                    "status": "Partial Success",
                    "createStatus": {
                        "status": "Success",
                        "message": "Created successfully"
                    },
                    "connectStatus": {
                        "status": "Failed",
                        "error": "The current operation ended in state: ERROR"
                    }
                }
            ],
            "importRequestsSysIds": [
                "2a4d216bdb2d2450fe4fd6a75e9619c3",
                "7f4d616bdb2d2450fe4fd6a75e9619c2",
                "815da16bdb2d2450fe4fd6a75e9619d0"
            ]
        }
    }
}
```

### cURL request

The following example shows the status request of an application onboarding.

```
curl -X POST "https://servicenow-instance/api/sn_devops/v1/devops/onboarding/status?onboardingRequestID=IBE0001604" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
```

```
{
    "result": {
        "code": "207",
        "onboardingRequestID": "IBE0001604",
        "status": "partial-success",
        "messageDetails": {
            "status": "Partial Success",
            "apps": [
                {
                    "name": "Bike Rentals Service",
                    "status": "Success",
                    "appId": "c7fd696bdb2d2450fe4fd6a75e961993",
                    "message": "App by name 'Bike Rentals Service' has been successfully created"
                }
            ],
            "pipelines": [
                {
                    "name": "Bike Rentals",
                    "status": "Success",
                    "message": "Successfully associated with app 'Bike Rentals Service'",
                    "changeStepAssociation": [
                        {
                            "status": "Success",
                            "changeStepName": "Prod",
                            "summary": "Change step with name 'Prod' has been created"
                        }
                    ]
                }
            ],
            "repositories": [
                {
                    "name": "nowdevops01/BikeRentals",
                    "status": "Partial Success",
                    "message": "Successfully associated with app 'Bike Rentals Service'",
                    "configureStatus": {
                        "status": "Failed",
                        "message": "Webhook configuration failed due to empty credentials for repository by name nowdevops01/BikeRentals in tool Primary GitHub"
                    }
                }
            ],
            "plans": [
                {
                    "status": "Failed",
                    "name": "testFirst",
                    "errors": [
                        "Plan by name 'testFirst' does not exist in tool Primary Azure"
                    ]
                }
            ]
        }
    }
}
```

## DevOps - GET /devops/orchestration/changeControl

Checks if the orchestration task is under change control.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/orchestration/changeControl`

Default URL: `/api/sn_devops/devops/orchestration/changeControl`

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

orchestrationTaskName

</td><td>

Name of the orchestration task to check.Data type: String

</td></tr><tr><td>

testConnection

</td><td>

Flag that indicates whether to test the end-to-end connection between the instance and the DevOps tool.Valid values:

-   true: Test the end-to-end connection.
-   false: Do'ot test the end-to-end connection.

Data type: Boolean

Default: false

</td></tr><tr><td>

toolId

</td><td>

Required. Sys\_id of the orchestration tool.Data type: String

Table: Orchestration Tool \[sn\_devops\_orchestration\_tool\]

</td></tr><tr><td>

toolType

</td><td>

Type of tool.Valid values: jenkins

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

</th></tr></thead><tbody><tr id="accept-row-RESTAPI"><td>

Accept

</td><td>

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Authorization

</td><td>

Starting with v2, this API supports token-based authentication. Tokens can be acquired by clicking the **Copy token** button on the tool record, located in the Tool \[sn\_devops\_tool\] table. The token can then be used in an authorization header in the format `Authorization: sn_devops.DevOpsToken <tool_sys_id>:<tool_token>`.

**Note:** If Basic Auth details \(user name and password\) are provided in addition to an authorization header with token, Basic Auth takes precedence.

If the **devops.system** user is not available in your instance, use the **Switch to this user after token based authentication is successful** property. This property enables setting any user that has the sn\_devops.integration role, which is needed to complete the token authentication. For information, see DevOps Change Velocity properties.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Invalid or missing authentication.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changeControl

</td><td>

Flag that indicates whether the orchestration task is under change control.Possible values:

-   true: Under change control.
-   false: Not under change control.

Data type: Boolean

</td></tr></tbody>
</table>### Under change control and using API v2

```
curl -X GET "https://instance.servicenow.com/api/sn_devops/v2/devops/orchestration/changeControl?toolId=1c219f7e8708f1508ca933383cbb3543&orchestrationTaskName=Platform-Analytics-UAT-Deployment&orchestrationTaskURL=https%253A%252F%252Fjenkins.mycompany.com%253A8080%252Fjob%252FMobile-Platform-deploy%252F&toolType=jenkins" 
-H "accept: application/json"\
-H "Authorization: sn_devops.DevOpsToken 1c219f7e8708f1508ca933383cbb3543:FtN13dfDuahYEtdfDvhHorh0QPp9na3u"
```

Response body.

```
{
"result": {
  "changeControl": true,
  "status": "Success" 
  } 
}
```

### Not under change control and using API v1

```
curl -X GET "https://instance.servicenow.com/api/sn_devops/v1/devops/orchestration/changeControl?toolId=f0ca45679323008b52f3b457415ae6&orchestrationTaskName=Platform-Analytics-UAT-Deployment&orchestrationTaskURL=https%253A%252F%252Fjenkins.mycompany.com%253A8080%252Fjob%252FMobile-Platform-deploy%252F&toolType=jenkins" 
-H "accept: application/json"\
-u "username":"password"
```

Response body.

```
{
    "result": {
        "changeControl": false
    }
}
```

## DevOps - GET /devops/orchestration/changeInfo

Retrieves change request details for a specified orchestration pipeline execution.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/orchestration/changeInfo`

Default URL: `/api/sn_devops/devops/orchestration/changeInfo`

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

branchName

</td><td>

Name of the branch associated with the orchestration task.**Note:** You should provide this parameter when referencing multi-branch pipelines or the response may include incorrect change details.

Data type: String

</td></tr><tr><td>

buildNumber

</td><td>

Required. Pipeline build number within the orchestration tool.Data type: String

</td></tr><tr><td>

pipelineName

</td><td>

Optional for Jenkins Freestyle or Maven projects, required for all others. Orchestration pipeline name.Data type: String

</td></tr><tr><td>

projectName

</td><td>

Required for Jenkins Freestyle or Maven projects, optional for all others. Orchestration tool project name.Data type: String

</td></tr><tr><td>

stageName

</td><td>

Optional for Jenkins Freestyle or Maven projects, required for all others. Orchestration stage name.Data type: String

Maximum length: 160

</td></tr><tr><td>

toolId

</td><td>

Required. Sys\_id of the orchestration tool.Data type: String

Table: Orchestration Tool \[sn\_devops\_orchestration\_tool\]

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

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Authorization

</td><td>

Starting with v2, this API supports token-based authentication. Tokens can be acquired by clicking the **Copy token** button on the tool record, located in the Tool \[sn\_devops\_tool\] table. The token can then be used in an authorization header in the format `Authorization: sn_devops.DevOpsToken <tool_sys_id>:<tool_token>`.

**Note:** If Basic Auth details \(user name and password\) are provided in addition to an authorization header with token, Basic Auth takes precedence.

If the **devops.system** user is not available in your instance, use the **Switch to this user after token based authentication is successful** property. This property enables setting any user that has the sn\_devops.integration role, which is needed to complete the token authentication. For information, see DevOps Change Velocity properties.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changeFound

</td><td>

Flag that indicates whether the change request was located.Possible values:

-   true: Change request was found.
-   false: Change request wasn't found.

Data type: Boolean

</td></tr><tr><td>

number

</td><td>

Change request number.Data type: String

</td></tr><tr><td>

phase

</td><td>

Current phase.Data type: String

</td></tr><tr><td>

phase\_state

</td><td>

State of the current phase.Data type: String

</td></tr><tr><td>

priority

</td><td>

Priority of the change request. Priority is based on the impact and urgency of the request. It identifies how quickly the service desk should address the request.Possible values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low

Data type: String

</td></tr><tr><td>

risk

</td><td>

Level of risk for the change.Possible values:

-   Low
-   High
-   Moderate

Data type: String

</td></tr><tr><td>

state

</td><td>

State of the change request.Possible values:

-   Assess
-   Authorize
-   Canceled
-   Closed
-   Implement
-   New
-   Review
-   Scheduled

Data type: String

Default: New

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the change request.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of change request.Possible values:

-   Emergency
-   Normal
-   Standard

Data type: String

</td></tr><tr><td>

url

</td><td>

URL of the change request within the associated ServiceNow instance.Data type: String

</td></tr><tr><td>

changeAssignmentGroup

</td><td>

Assignment group of the change request.Data type: String

</td></tr><tr><td>

changeApprovers

</td><td>

List of approvers with whom the change is pending for approval.Data type: String

</td></tr><tr><td>

plannedStartDate

</td><td>

Planned start date and time of the change. Data type: String

</td></tr><tr><td>

plannedEndDate

</td><td>

Planned end date and time of the change.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl -X GET "https://instance.servicenow.com/api/sn_devops/v1/devops/orchestration/changeInfo?toolId=1487f457db642810765555535e9619d3&pipelineName=Automation/apps HR/family release&stageName=deployfamilyrelease&buildNumber=1639"  
-H "accept: application/json"\ 
-u "username":"password"
```

```
{  
  "result": {  
    "changeFound": true,  
    "sys_id": "ee89341bdb642810765555535e96196e",  
    "number": "CHG0030001",  
    "type": "normal",  
    "state": "0",  
    "phase": "requested",  
    "phase_state": "open",  
    "priority": "4",  
    "risk": "4",  
    "url": "https://instance.servicenow.com/change_request.do?sys_id=ee89341bdb642810765555535e96196e",  
    "changeAssignmentGroup": "Change Management", 
    "changeApprovers": "Ron Kettering, Christen Mitchell, Howard Johnson, Luke Wilson", 
    "plannedStartDate": "2023-02-05 08:00:00", 
    "plannedEndDate": "2024-02-05 08:00:00" 
  }  
}
```

## DevOps - GET /devops/orchestration/schema

Returns the schema object for a specified orchestration resource.

Once you have the required schema object, use it to create the request body for your corresponding POST call; /orchestration/orchestrationTask or /orchestration/taskExecution.

**Note:** This endpoint only returns the request body elements that are required.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/orchestration/schema`

Default URL: `/api/sn_devops/devops/orchestration/schema`

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

resource

</td><td>

Type of resource schema to return.Valid values \(not case-sensitive\):

-   build\_details
-   callback
-   orchestration\_task
-   task\_execution

 Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|401|Invalid or missing authentication.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

callbackURL

</td><td>

URL of the callback.Data type: String

</td></tr><tr><td>

endDateTime

</td><td>

Date/time that the task execution ended. Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the orchestration task.Data type: String

</td></tr><tr><td>

number

</td><td>

Task execution number. Same as an incident number. Data type: String

</td></tr><tr><td>

orchestrationTaskDetails

</td><td>

Description of the orchestration task. Data type: Object

 ```
"orchestrationTaskDetails": {
  "message": "String",
  "name": "String",
  "triggerType": "String",
  "url": "String"
}
```

</td></tr><tr><td>

orchestrationTaskDetails.message

</td><td>

Free-form text message. Data type: String

</td></tr><tr><td>

orchestrationTaskDetails.name

</td><td>

Name of the orchestration task. Data type: String

</td></tr><tr><td>

orchestrationTaskDetails.triggerType

</td><td>

The way the orchestration task was started. Data type: String

</td></tr><tr><td>

orchestrationTaskDetails.url

</td><td>

URL of the associated orchestration tool's orchestration task. Data type: String

</td></tr><tr><td>

orchestrationTaskURL

</td><td>

URL of the orchestration task. Data type: String

</td></tr><tr><td>

result

</td><td>

Execution result of the task execution. Valid values:

-   Failed
-   Success

 Data type: String

</td></tr><tr><td>

startDateTime

</td><td>

Date/time that the task execution started. Data type: String

</td></tr><tr><td>

taskExecutionURL

</td><td>

URL of the task to execute.Data type: String

</td></tr><tr><td>

triggerType

</td><td>

The way the orchestration task was started. Valid values:

 -   scm: Git/scm tool code commit triggered the job.
-   upstream: Upstream job triggered this job.
-   user: User manually started the job.

 Data type: String

</td></tr><tr><td>

url

</td><td>

URL of the associated orchestration tool's orchestration task. Data type: String

</td></tr></tbody>
</table>### Sample cURL request with resource=task\_execution

```
curl -X GET \
'https://instance.servicenow.com/api/sn_devops/v1/devops/orchestration/schema?resource=task_execution' \
-H 'Accept: application/json'\
-u 'username':'password'
```

```
{
"result": {
  "number": 40,
  "url": "https://jenkins.mycompany.com:8080/job/Mobile-Platform-CI/40/",
  "startDateTime": "1970-01-01T08:15:30-05:00",
  "endDateTime": "1970-01-01T08:25:30-05:00",
  "triggerType": "upstream",
  "result": "Success",
  "orchestrationTaskDetails": {
    "name": "Mobile-Platform-CI",
    "url": "https://jenkins.mycompany.com:8080/job/Mobile-Platform-CI/"
    }
  }
}
```

### Sample cURL request with resource=orchestration\_task

```
curl -X GET \ 
'https://instance.servicenow.com/api/sn_devops/v1/devops/orchestration/schema?resource=orchestration_task' \
-H 'Accept: application/json'\
-u 'username':'password' 

```

```
{ 
"result": { 
  "name": "Mobile-Platform-CI", 
  "url": "https://jenkins.mycompnay.com:8080/job/Mobile-Platform-CI/" 
  } 
} 
```

### Sample cURL request with resource=callback

```
curl -X GET \
'https://instance.servicenow.com/api/sn_devops/v1/devops/orchestration/schema?resource=task_execution' \
-H 'Accept: application/json' \
-u 'username':'password'

```

```
{ 
  "result": { 
    "callbackURL": "http://127.0.0.1:8090/jenkins/sn-devops/9b0feb79-f0b9-4661-83ef-2861b8924784", 
    "orchestrationTaskURL": "http://127.0.0.1:8090/jenkins/job/felipe-downstream/", 
    "orchestrationTaskDetails": { 
      "message": "Started by upstream project \"felipe-upstream\" build number 27", 
      "triggerType": "upstream" 
    } 
  } 
} 
```

## DevOps - GET /devops/orchestration/stepMapping

Verifies that the information being passed is valid for the creation of an orchestration task and is valid for association to a previously created step.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/orchestration/stepMapping`

Default URL: `/api/sn_devops/devops/orchestration/stepMapping`

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

</th></tr></thead><tbody><tr id="row-stepMap-branchName"><td>

branchName

</td><td>

Name of the branch associated with the orchestration task. Data type: String

</td></tr><tr id="row-stepMap-isMultiBranch"><td>

isMultiBranch

</td><td>

If the orchestration tool is Jenkins, flag that indicates whether the project is of type Multibranch. Valid values:

-   true: Project is of type Multibranch.
-   false: Project is not of type Multibranch.

Data type: Boolean

Default: false

</td></tr><tr id="row-stepMap-parentStageName"><td>

parentStageName

</td><td>

If the orchestration task is a child nested inside a parent orchestration task, the name of the parent orchestration task. Data type: String

</td></tr><tr id="row-stepMap-parentStageURL"><td>

parentStageURL

</td><td>

If the orchestration task is a child nested inside a parent orchestration task, the URL of the parent orchestration task. Data type: String

</td></tr><tr><td>

orchestrationTaskName

</td><td>

Required. Name of the orchestration task.Data type: String

</td></tr><tr><td>

orchestrationTaskURL

</td><td>

Required. URL of the orchestration task.**Note:** Must be percent \(%\) encoded, such as https%3A%2F%2Fjenkins.mycompany.com%3A8080%2Fjob%2FMobile-Platform-deploy%2F.

Data type: String

</td></tr><tr><td>

testConnection

</td><td>

Flag that indicates whether to test the end-to-end connection between the instance and the DevOps tool. Valid values:

-   true: Test the end-to-end connection.
-   false: Do not test the end-to-end connection.

 Data type: Boolean

 Default: false

</td></tr><tr id="row-stepMap-toolId"><td>

toolId

</td><td>

Required. Sys\_id of the orchestration tool. Located in the Orchestration Tool \[sn\_devops\_orchestration\_tool\] table. Data type: String

</td></tr><tr id="row-stepMap-toolType"><td>

toolType

</td><td>

Required. Type of tool. Valid values: jenkins

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="table_xb5_513_bmb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Flag that indicates whether the verification was successful.Valid values:

-   true: Verification was successful.
-   false: Verification wasn't successful.

Data type: Boolean

</td></tr><tr><td>

stepValid

</td><td>

Flag that indicates whether the information sent is valid.Valid values:

-   true: Information sent is valid.
-   false: Information sent isn't valid.

Data type: Boolean

</td></tr></tbody>
</table>### Sample cURL request

```
curl -X GET "https://instance.servicenow.com/api/sn_devops/v1/devops/orchestration/stepMapping?toolId=f0ca45679323008b52f3b457415ae6&orchestrationTaskName=Platform-Analytics-UAT-Deployment&orchestrationTaskURL=https%253A%252F%252Fjenkins.mycompany.com%253A8080%252Fjob%252FMobile-Platform-deploy%252F&toolType=jenkins "
 -H "Accept: application/json" \
 -u "username":"password"

```

Results if information is valid.

```
{
  "result": {
    "stepValid": true,
    "status": "Success"
  }
}
```

### Sample cURL request

```
curl -X GET "https://instance.servicenow.com/api/sn_devops/v1/devops/orchestration/stepMapping?toolId=f0ca45679323008b52f3b457415ae6&orchestrationTaskName=Platform-Analytics-UAT-Deployment&orchestrationTaskURL=https%253A%252F%252Fjenkins.mycompany.com%253A8080%252Fjob%252FMobile-Platform-deploy%252F&toolType=jenkins "
 -H "Accept: application/json" \
 -u "username":"password"

```

Results if information is invalid.

```
{
"result": {
  "stepValid": false,
  "status": "Success"
}

```

## DevOps - GET /devops/plan/schema

Returns the schema object for a specific plan: app, version, or work item.

Once you have the required schema object, use it to create the request body for your corresponding POST call; POST /plan/app, POST /plan/version, or POST /plan/workitem.

**Note:** This endpoint only returns the request body elements that are required.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/plan/schema`

Default URL: `/api/sn_devops/devops/plan/schema`

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

resource

</td><td>

Type of resource schema to return.Valid values \(not case-sensitive\):

 -   app
-   version
-   work\_item

 Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Invalid or missing authentication.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

app

</td><td>

Description of the application to associate with the version. Data type: Object

 ```
"app": {
  "createdDateTime": "String",
  "id": "String",
  "shortDescription": "String",
  "team": {Object},
  "url": "String"
}
```

</td></tr><tr><td>

app.createdDateTime

</td><td>

Date/time the application was created in the source DevOps tool. Data type: String

</td></tr><tr><td>

app.id

</td><td>

Unique identifier of the application. Generated by the source planning tool. Data type: String

</td></tr><tr><td>

app.shortDescription

</td><td>

Brief description of the associated application. Data type: String

</td></tr><tr><td>

app.team

</td><td>

Description of the team associated with the application. Data type: Object

 ```
"team": {
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

app.team.id

</td><td>

Unique identifier of the team associated with the application. Generated by the source planning tool. Data type: String

</td></tr><tr><td>

app.team.name

</td><td>

Name of the team associated with the application. Data type: String

</td></tr><tr><td>

app.url

</td><td>

URL of the application on the source planning tool site. Data type: String

</td></tr><tr><td>

assignedTo

</td><td>

Description of the person to which the work item is assigned. Data type: Object

 ```
"assignedTo": {
  "email": "String",
  "id": "String",
  "name": "String",
  "userName": "String"
}
```

</td></tr><tr><td>

assignedTo.email

</td><td>

Email address of the person assigned to the work item. Data type: String

</td></tr><tr><td>

assignedTo.id

</td><td>

Unique identifier of the person assigned to the work item. Data type: String

</td></tr><tr><td>

assignedTo.name

</td><td>

Name of the person assigned to the work item. Data type: String

</td></tr><tr><td>

assignedTo.userName

</td><td>

User name of the person assigned to the work item. Data type: String

</td></tr><tr><td>

createDateTime

</td><td>

Date and time that the application, version, or work item record was created.Data type: String

</td></tr><tr><td>

id

</td><td>

Unique identifier of the application, version, or work item. Generated by the source planning tool.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the application.Data type: String

</td></tr><tr><td>

path

</td><td>

Relative path to the application.Data type: String

</td></tr><tr><td>

shortDescription

</td><td>

Brief description of the application, version, or work item.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the work item. Generated by the source planning tool. Data type: String

</td></tr><tr><td>

team

</td><td>

Description of the team associated with the application. Data type: Object

 ```
"team": {
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

team.id

</td><td>

Unique identifier of the team associated with the application. Generated by the source planning tool. Data type: String

</td></tr><tr><td>

team.name

</td><td>

Name of the team associated with the application. Data type: String

</td></tr><tr><td>

type

</td><td>

Type of work item. Generated by the planning tool.Data type: String

</td></tr><tr><td>

url

</td><td>

URL to use to access the application, version, or work item.Data type: String

</td></tr><tr><td>

version

</td><td>

Array that describes the version.Data type: Object

 ```
"version": {
  "app": {Object},
  "createdDateTime": "String",
  "id": "String",
  "shortDescription": "String",
  "url": "String"
}
```

</td></tr><tr><td>

version.app

</td><td>

Description of the application to associate with the version. Data type: Object

 ```
"app": {
  "createdDateTime": "String",
  "id": "String",
  "shortDescription": "String",
  "team": {Object},
  "url": "String"
}
```

</td></tr><tr><td>

version.app.createdDateTime

</td><td>

Date/time that the version was created on the source DevOps tool. Data type: String

</td></tr><tr><td>

version.app.id

</td><td>

Unique identifier of the application. Generated by the source planning tool. Data type: String

</td></tr><tr><td>

version.app.shortDescription

</td><td>

Brief description of the associated application. Data type: String

</td></tr><tr><td>

version.app.team

</td><td>

Description of the team associated with the application. Data type: Object

 ```
"team": {
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

version.app.team.id

</td><td>

Unique identifier of the team associated with the application. Generated by the source planning tool. Data type: String

</td></tr><tr><td>

version.app.team.name

</td><td>

Name of the team associated with the application. Data type: String

</td></tr><tr><td>

version.app.url

</td><td>

URL of the application on the source planning tool site. Data type: String

</td></tr><tr><td>

version.createdDateTime

</td><td>

Date/time that the version was created on the source DevOps tool. Data type: String

</td></tr><tr><td>

version.id

</td><td>

Unique identifier of the version. Generated by the source planning tool. Data type: String

</td></tr><tr><td>

version.shortDescription

</td><td>

Brief description of the associated version. Data type: String

</td></tr><tr><td>

version.url

</td><td>

URL of the version on the source planning tool site. Data type: String

</td></tr></tbody>
</table>### Sample cURL request for resource=app

```
curl "https://instance.servicenow.com/api/sn_devops/v1/devops/plan/schema?resource=app" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": {
    "id": "PRODUCT1234",
    "shortDescription": "Mobile UI",
    "createdDateTime": "1970-01-01T08:15:30-05:00",
    "team": {
      "name": "Mobile UI",
      "id": "f0ca45679323008b52f3b457415ae6"
    },
    "url": "https://jira.com/mycompany/browse/PRODUCT-125"
  }
}
```

### Sample cURL request for resource=version

```
curl "https://instance.servicenow.com/api/sn_devops/v1/devops/plan/schema?resource=version" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": {
    "id": "REL1234",
    "shortDescription": "APIs Release",
    "createdDateTime": "1970-01-01T08:15:30-05:00",
    "app": {
      "id": "PRODUCT1234",
      "shortDescription": "Mobile UI",
      "createdDateTime": "1970-01-01T08:15:30-05:00",
      "team": {
        "name": "Mobile UI",
        "id": "f0ca45679323008b52f3b457415ae6"
      },
      "url": "https://jira.com/mycompany/browse/PRODUCT-125"
    },
    "url": "https://jira.com/mycompany/browse/REL-125"
  }
}
```

### Sample cURL request for resource=work\_item

```
curl "https://instance.servicenow.com/api/sn_devops/v1/devops/plan/schema?resource=work_item" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": {
    "id": "STR1234",
    "type": "Story",
    "shortDescription": "Planning API Spec",
    "state": "In-progress",
    "createdDateTime": "1970-01-01T08:15:30-05:00",
    "assignedTo": {
      "name": "Leo Neo",
      "userName": "lenn",
      "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "email": "lenn@smithworksinc.com"
    },
    "version": {
      "id": "REL1234",
      "shortDescription": "APIs Release",
      "createdDateTime": "1970-01-01T08:15:30-05:00",
      "app": {
        "id": "PRODUCT1234",
        "shortDescription": "Mobile UI",
        "createdDateTime": "1970-01-01T08:15:30-05:00",
        "team": {
          "name": "Mobile UI",
          "id": "f0ca45679323008b52f3b457415ae6"
        },
        "url": "https://jira.com/mycompany/browse/PRODUCT-125"
        },
        "url": "https://jira.com/mycompany/browse/REL-125"
    },
    "app": {
      "id": "PRODUCT1234",
      "shortDescription": "Mobile UI",
      "createdDateTime": "1970-01-01T08:15:30-05:00",
      "team": {
        "name": "Mobile UI",
        "id": "f0ca45679323008b52f3b457415ae6"
      },
      "url": "https://jira.com/mycompany/browse/PRODUCT-125"
    },
    "url": "https://jira.com/mycompany/browse/HALOKEY-25"
  }
}
```

## DevOps - POST /devops/artifact/registration

Enables orchestration tools to register artifacts into a ServiceNow instance.

This endpoint creates new artifacts and artifact versions, and associates them to commits. The following describes the endpoint process flow:

-   If the **toolId** is passed in the request, the endpoint validates that the tool exists within the instance. It also checks if the artifact repository specified in **artifacts.repositoryName** exists, and if not, creates it under the associated artifact tool.
-   If the **toolId** is not passed in the request, a repository is created but it is not linked to any artifact tool.
-   It then checks if the artifact specified in **artifacts.name** already exists, and if not, creates it under the associated repository.
-   If the **artifact.version** is passed in the request:
    -   If it does not exist, a new artifact version record is created in the associated Artifact Version \[sn\_devops\_artifact\_version\] table.
    -   The endpoint then looks for associated task executions based on the provided build details \(**pipelineName** or **projectName**, **taskExecutionNumber**, **branchName**, and **stageName**\) and the **orchestrationToolId** parameter.
    -   If a task execution is found, and its post-processing is complete, the artifact version is linked to the task execution and stored in the Artifact to TaskExecution \[sn\_devops\_m2m\_artifact\_execution\] table. Commits linked to these task executions are also associated to the artifact version and stored in the Artifact Version to Commit \[sn\_devops\_m2m\_artifact\_version\_commit\] table. Any commits that are linked to previous task executions that did not create an artifact, are also associated with the artifact version.
    -   If a task execution is found, and its post-processing is not complete, then the request is persisted in the Artifact Staged Request \[sn\_devops\_artifact\_staging\] table. The staged request contains a reference to the task execution.
    -   If a task execution is not found, the request is persisted in the staging table. The staged request contains the build details.
-   If the **artifact.version** is not passed in, then depending on the tool configuration, the artifact version is either retrieved by calling the /devops/tool/artifact endpoint if your artifact tool supports webhooks or through a custom subflow that retrieves the artifact version from the artifact tool.

For additional information on artifacts, see Using DevOps change acceleration for releases.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/artifact/registration`

Default URL: `/api/sn_devops/devops/artifact/registration`

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

orchestrationToolId

</td><td>

Required. Sys\_id of the orchestration tool associated with the artifact. The endpoint uses this information to locate task execution information.Data type: String

Table: Orchestration Tool \[sn\_devops\_orchestration\_tool\]

</td></tr><tr><td>

toolId

</td><td>

Sys\_id of the artifact tool associated with the artifact.Data type: String

Table: Artifact Tool \[sn\_devops\_artifact\_tool\]

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

artifacts

</td><td>

At least one entry required. Array of objects in which each object uniquely identifies an artifact version to register.Data type: Array of Objects

```
"artifacts": [
  {
    "name": "String",
    "repositoryName": "String",
    "semanticVersion": "String",
    "version": "String"
  }
]
```

</td></tr><tr><td>

artifacts.name

</td><td>

Required. Artifact file name.Data type: String

Maximum length: 160 characters

</td></tr><tr><td>

artifacts.repositoryName

</td><td>

Required. Artifact repository name.If the specified repository record does not exist, it is created.

Data type: String

Maximum length: 160 characters

</td></tr><tr><td>

artifacts.semanticVersion

</td><td>

Semantic version of the artifact. Data type: String

Format: MAJOR.MINOR.PATCH

Examples of possible values:

-   2.0.0
-   2.0.0-rc.2
-   2.0.0-rc.1
-   1.0.0-beta

Maximum length: 160 characters

Default: Null

</td></tr><tr><td>

artifacts.version

</td><td>

Required if **toolId** is not passed. Artifact version.Data type: String

Format: MAJOR.MINOR

Maximum length: 160 characters

Default: Null

</td></tr><tr><td>

branchName

</td><td>

Required if it is a multi-branch project. Name of the branch in the repository where the artifact is stored. Data type: String

Maximum length: 160

Default: Null

</td></tr><tr><td>

pipelineName

</td><td>

Required if **projectName** is not passed. Pipeline name.Data type: String

Maximum length: 160

Default: Null

</td></tr><tr><td>

projectName

</td><td>

Required if **pipelineName** is not passed. Free-form project name.Data type: String

Maximum length: 160

Default: Null

</td></tr><tr><td>

stageName

</td><td>

Required if **pipelineName** is passed. Stage name. Data type: String

Maximum length: 160

Default: Null

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Authorization

</td><td>

Starting with v2, this API supports token-based authentication. Tokens can be acquired by clicking the **Copy token** button on the tool record, located in the Tool \[sn\_devops\_tool\] table. The token can then be used in an authorization header in the format `Authorization: sn_devops.DevOpsToken <tool_sys_id>:<tool_token>`.

**Note:** If Basic Auth details \(user name and password\) are provided in addition to an authorization header with token, Basic Auth takes precedence.

If the **devops.system** user is not available in your instance, use the **Switch to this user after token based authentication is successful** property. This property enables setting any user that has the sn\_devops.integration role, which is needed to complete the token authentication. For information, see DevOps Change Velocity properties.

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
|200|Success. Success with response body.|
|201|Created. Success with response body.|
|400|Bad Request. The request URI does not match the APIs in the system, or the operation failed for unknown reasons. Invalid headers can also cause this error.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

response

</td><td>

Results of the artifact registration request.Data type: Object

```
"response": {
  "artifact": {Object},
  "artifact_register_requests": {Object},
  "artifact_repository": {Object},
  "artifact_version": {Object}
}
```

</td></tr><tr><td>

response.artifact

</td><td>

Results for each processed artifact.Data type: Object

```
"artifact": {
  "create": [Array],
  "found": [Array],
  "update": [Array]
}
```

</td></tr><tr><td>

response.artifact.create

</td><td>

If the request created artifact records, the list of sys\_ids of the created records.Data type: Array of Objects

```
"create": [
  {
    "id": "String"
  }
]
```

Table: Artifacts \[sn\_devops\_artifact\]

</td></tr><tr><td>

response.artifact.create.id

</td><td>

Sys\_id of the artifact record created by the request.Data type: String

</td></tr><tr><td>

response.artifact.found

</td><td>

If an artifact already exists in the Artifacts table, the list of sys\_ids of the existing artifact records.**Note:** No modifications are made to existing packages.

Data type: Array of Objects

```
"found": [
  {
    "id": "String"
  }
]
```

</td></tr><tr><td>

response.artifact.found.id

</td><td>

Sys\_id of the existing artifact record.Data type: String

</td></tr><tr><td>

response.artifact.update

</td><td>

Currently unused

</td></tr><tr><td>

response.artifact.update.id

</td><td>

Currently unused

</td></tr><tr><td>

response.artifact\_register\_requests

</td><td>

Results for any artifacts register requests that have not completed processing and have been stored in the Artifact Staged Request table.Data type: Object

```
"artifact_register_requests": {
  "create": [Array],
  "found": [Array],
  "update": [Array]
}
```

</td></tr><tr><td>

response.artifact\_register\_requests.create

</td><td>

If the request created artifact staging records, the list of sys\_ids of the created records.Data type: Array of Objects

```
"create": [
  {
    "id": "String"
  }
]
```

</td></tr><tr><td>

response.artifact\_register\_requests.create.id

</td><td>

Sys\_id of the artifact staging record created by the request.Data type: String

</td></tr><tr><td>

response.artifact\_register\_requests.found

</td><td>

If artifacts already have associated artifact staging records, the list of sys\_ids of the existing artifact staging records.**Note:** No modifications are made to existing packages.

Data type: Array of Objects

```
"found": [
  {
    "id": "String"
  }
]
```

</td></tr><tr><td>

response.artifact\_register\_requests.found.id

</td><td>

Sys\_id of an existing artifact staging record.Data type: String

</td></tr><tr><td>

response.artifact\_register\_requests.update

</td><td>

Currently unused

</td></tr><tr><td>

response.artifact\_register\_requests.update.id

</td><td>

Currently unused

</td></tr><tr><td>

response.artifact\_repository

</td><td>

Results for any artifact repository records that were manipulated during the processing of the request.Data type: Object

```
"artifact_repository": {
  "create": [Array],
  "found": [Array],
  "update": [Array]
}
```

</td></tr><tr><td>

response.artifact\_repository.create

</td><td>

If artifact repositories were created by the request, the list of sys\_ids of the created records.Data type: Array of Objects

```
"create": [
  {
    "id": "String"
  }
]
```

</td></tr><tr><td>

response.artifact\_repository.create.id

</td><td>

Sys\_id of the artifact repository record created by the request.Data type: String

</td></tr><tr><td>

response.artifact\_repository.found

</td><td>

If artifact repository records used in the register request already exist, the list of sys\_ids of the existing records.**Note:** No modifications are made to existing packages.

Data type: Array of Objects

```
"found": [
  {
    "id": "String"
  }
]
```

</td></tr><tr><td>

response.artifact\_repository.found.id

</td><td>

Sys\_id of an existing artifact repository record used by the request.Data type: String

</td></tr><tr><td>

response.artifact\_repository.update

</td><td>

If the endpoint updates the track flag on a repository to true \(from false\), the list of sys\_ids of the repository records that were modified.Data type: Array of Objects

```
"update": [
  {
    "id": "String"
  }
]
```

</td></tr><tr><td>

response.artifact\_repository.update.id

</td><td>

Sys\_id of the repository record whose track flag was modified.Data type: String

</td></tr><tr><td>

response.artifact\_version

</td><td>

Results for any artifact version records that were manipulated during the processing of the request.Data type: Object

```
"artifact_version": {
  "create": [Array],
  "found": [Array],
  "update": [Array]
}
```

</td></tr><tr><td>

response.artifact\_version.create

</td><td>

Results for any artifact version records that were created during the processing of the request.Data type: Array of Objects

```
"create": [
  {
    "id": "String"
  }
]
```

</td></tr><tr><td>

response.artifact\_version.create.id

</td><td>

Sys\_id of the artifact version record created by the request.Data type: String

</td></tr><tr><td>

response.artifact\_version.found

</td><td>

If artifact version records used in the register request already exist, the list of sys\_ids of the existing records.Data type: Array of Objects

```
"found": [
  {
    "id": "String"
  }
]
```

</td></tr><tr><td>

response.artifact\_version.found.id

</td><td>

Sys\_id of the existing artifact version record used by the request.Data type: String

</td></tr><tr><td>

response.artifact\_version.update

</td><td>

Currently unused

</td></tr><tr><td>

response.artifact\_version.update.id

</td><td>

Currently unused

</td></tr><tr><td>

status

</td><td>

Status of the registration request.Possible values:

-   Success: Response body contains return results.
-   Error: Response body contains list of all errors.

Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl -X POST \
'https://instance.servicenow.com/api/sn_devops/devops/artifact/registration?toolId=391b4ff6dba24010bc8cdd384b96198f&orchestrationToolId=99d70b36dba24010bc8cdd384b961985' \
-H 'Accept: application/json' \
-H 'Content-Type: application/json' \
-u 'username':'password' \
-d ' {"artifacts": [\
 {\
 "name": "sa-web.jar",\
 "version": "3.1",\
 "semanticVersion": "3.1.0",\
 "repositoryName": "services-1031"\
 },\
 {\
 "name": "sa-frontend.jar",\
 "version": "3.2",\
 "semanticVersion": "3.2.0",\
 "repositoryName": "services-1031"\
 }\
 ],\
 "pipelineName": "spring-boot-app",\
 "taskExecutionNumber": "160",\
 "stageName": "Build",\
 "branchName": "primary"\
}]'
```

```
{
"result": {
  "status": "Success",
  "response": {
    "artifact_repository": {
      "create": [
        {
          "id": "2e50ba8bdbaa4010bc8cdd384b961988"
        }
      ],
      "update": [],
      "found": [
        {
          "id": "2e50ba8bdbaa4010bc8cdd384b961988"
        }
      ]
    },
    "artifact": {
      "create": [
        {
          "id": "6a50f603dbea4010bc8cdd384b96193d"
        },
        {
          "id": "2e50f603dbea4010bc8cdd384b96193f"
        }
      ],
      "update": [],
      "found": []
    },
    "artifact_version": {
      "create": [
        {
          "id": "a650f603dbea4010bc8cdd384b96193e"
        },
        {
          "id": "6250f603dbea4010bc8cdd384b961940"
        }
      ],
      "update": [],
      "found": []
    },
    "artifact_register_requests": {
      "create": [
        {
          "id": "6250f603dbea4010bc8cdd384b96193f"
        },
        {
          "id": "6650f603dbea4010bc8cdd384b961940"
        }
      ],
      "update": [],
      "found": []
    }
  }
 }
}
```

## DevOps - POST /devops/onboarding/app

Creates an onboarding app event that is asynchronously processed by the DevOps service.

This endpoint can perform the following actions:

-   Create applications.
-   Associate DevOps objects such as, plan, repository, and pipeline, to an application.
-   Create a change step record and associate a change approval process to a pipeline.

All of these actions are tool and capability specific. The following table outlines the actions available for each supported tool.

![Application onboarding matrix](../image/devops-onboarding_app-matrix.png)

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/onboarding/app`

Default URL: `/api/sn_devops/devops/onboarding/app`

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

apps

</td><td>

Array of objects that define the apps to create within the associated ServiceNow instance.Data type: Array

 ```
"apps": [{
  "bussinessApp": "String",
  "name": "String"
}]
```

</td></tr><tr><td>

apps.bussinessApp

</td><td>

Name of the cmdb\_ci\_business\_app to which map the application. This ties the DevOps application to the specified CMDB application.Data type: String

</td></tr><tr><td>

apps.name

</td><td>

Required. User friendly name of the application to create to create. An app is a DevOps product container object that ties plans, repositories, and pipelines together. Data type: String

</td></tr><tr><td>

credentials

</td><td>

Required. Credentials to use for the webhook creation. The created webhook is used by the tool to send notifications.Data type: Object

 ```
"credentials": {
  "name": "String",
  "password": "String"
}
```

</td></tr><tr><td>

credentials.name

</td><td>

Required. ServiceNow user ID of the user making the endpoint request. This user must have the devops.integration.user role. Starting with version 1.34.1, this user must have the sn\_devops.admin role.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

credentials.password

</td><td>

Required. Password of the user specified in the **credenitals.name** parameter.Data type: String

</td></tr><tr><td>

pipelines

</td><td>

List of pipelines to associate with applications. Data type: Array of Objects

```
"pipelines": [{
  "app": "String",
  "name": "String",
  "tool": "String"
}]
```

</td></tr><tr><td>

pipelines.app

</td><td>

Required if a **pipelines** object is specified. Name of the application to associate with the plan specified in the **pipelines.name** parameter. The application must have already been created or be specified in the **apps** object of this request. Data type: String

</td></tr><tr><td>

pipelines.changeSteps

</td><td>

Change steps to create for the pipeline specified in the **pipelines.name** field. Data type: Array of Objects

```
"changeSteps": [{
  "changeApprovalGroup": "String",
  "changeControlledBranches": "String",
  "changeType": "String",
  "name": "String",
  "type": "String"
}]
```

</td></tr><tr><td>

pipelines.changeSteps.changeApprovalGroup

</td><td>

Required if a **changeSteps** object is specified. Name of the change approval group to associate with the pipeline. This group must already exist on the ServiceNow instance. Data type: String

Table: Group \[sys\_user\_group\]

</td></tr><tr><td>

pipelines.changeSteps.changeControlledBranches

</td><td>

Comma-separated list of code branches that are under change control. This only applies for multi branch support. Data type: String

Default: \* \(all branches\)

</td></tr><tr><td>

pipelines.changeSteps.changeType

</td><td>

Required if a **changeSteps** object is specified. Type of change request to create.Data type: String

Table: In the Type field of the Change Request \[change\_request\] table.

</td></tr><tr><td>

pipelines.changeSteps.name

</td><td>

Required if a **changeSteps** object is specified. Name of the step to create. The step name must match the name of the corresponding step in the orchestration tool’s pipeline. Data type: String

</td></tr><tr><td>

pipelines.changeSteps.type

</td><td>

Required if a **changeSteps** object is specified. Type of step to create.Data type: String

Table: In the Type field of the Steps \[sn\_devops\_step\] table.

</td></tr><tr><td>

pipelines.name

</td><td>

Required if a **pipelines** object is specified. Name of the pipeline to associate with the application specified in **pipelines.app** parameter. This pipeline must already be discovered on the ServiceNow instance. Data type: String

</td></tr><tr><td>

pipelines.project

</td><td>

Required if a `pipelines` object is specified and the pipelines.tool supports projects entity \(for example, the ADO tool\). Project to associate with the pipeline to create a unique pipeline/tool identifier. Parameter value must derive from a project in the Project \[sn\_devops\_project\] table.Data type: String

</td></tr><tr><td>

pipelines.tool

</td><td>

Required if a **pipelines** object is specified. Tool to associate with the pipeline to create a unique pipeline/tool identifier. Data type: String

</td></tr><tr><td>

plans

</td><td>

List of plans to associate with an application. Data type: Array of Objects

```
"plans": [{
  "app": "String",
  "name": "String",
  "tool": "String"
}]
```

</td></tr><tr><td>

plans.apps

</td><td>

Required if a **plans** object is specified. Names of applications to associate with the plan specified in the **plans.name** parameter. These applications must have already been created or be specified in the **apps** object of this request. Data type: Array of Strings

</td></tr><tr><td>

plans.name

</td><td>

Required if a **plans** object is specified. Name of the plan to associate with the application specified in **plans.app** parameter. This plan must already be discovered on the ServiceNow instance. Data type: String

</td></tr><tr><td>

plans.project

</td><td>

Required if a `plans` object is specified and the plans.tool supports projects entity \(for example, the ADO tool\). Tool to associate with the pipeline to create a unique plans/tool identifier. Parameter value must derive from a project in the Project \[sn\_devops\_project\] table.Data type: String

</td></tr><tr><td>

plans.tool

</td><td>

Required if a **plans** object is specified. Tool to associate with the plan to create a unique plan/tool identifier. Data type: String

</td></tr><tr><td>

repositories

</td><td>

List of repositories associated with an application. If the repositories object contains an app parameter, then it maps the repository to the application. Data type: Array of Objects

```
"repositories": [{
  "app": "String",
  "name": "String",
  "tool": "String"
}]
```

</td></tr><tr><td>

repositories.app

</td><td>

Required if a **repositories** object is specified. Name of the application to associate with this repository. The application must have already been created or be specified in the **apps** object of this request. Data type: String

</td></tr><tr><td>

repositories.name

</td><td>

Required if a **repositories** object is specified. Name of the repository to associate with the application specified in **repositories.app** parameter. This repository must already be discovered on the ServiceNow instance. Data type: String

</td></tr><tr><td>

repositories.project

</td><td>

Required if a `repositories` object is specified and the **repositories.tool** supports a projects entity \(for example, the ADO tool\). Tool to associate with the repositories to create a unique repository/tool identifier. Parameter value must derive from a project in the Project \[sn\_devops\_project\] table.Data type: String

</td></tr><tr><td>

repositories.tool

</td><td>

Required if a **repositories** object is specified. User friendly tool name to associate with the repository to create a unique repository/tool identifier. The tool must already be created on the ServiceNow instance. Data type: String

</td></tr><tr><td>

artifactRepositories.app

</td><td>

Required if the `artifactRepositories` object is specified. Name of the application to associate with this artifactRepositories. The application must have already been created or be specified in the `apps` object of this request.Data type: String

</td></tr><tr><td>

artifactRepositories.name

</td><td>

Required if the `artifactRepositories` object is specified. Name of the artifactRepositories to associate with the application specified in **artifactRepositories**.app parameter. This artifactRepositories must already be discovered on the ServiceNow instance.Data type: String

</td></tr><tr><td>

artifactRepositories.tool

</td><td>

Required if the `artifactRepositories` object is specified. User friendly tool name to associate with the artifactRepositories to create a unique artifactRepositories /tool identifier. The tool must already be created on the ServiceNow instance.Data type: String

</td></tr><tr><td>

artifactRepositories.project

</td><td>

Required if the `artifactRepositories` object is specified and the **repositories.tool** supports projects entity \(for example, the ADO tool\). Tool to associate with the **artifactRepositories** to create a unique pipeline/tool identifier. Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|202|Onboarding request was successfully created.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Results of the onboarding request.Data type: Object

```
"result": {
  "code": "String",
  "details": "String",
  "errors": {Object],
  "onboardingRequestID": "String",
  "status": "String"
}
```

</td></tr><tr><td>

result.code

</td><td>

HTTP status code.Data type: String

</td></tr><tr><td>

result.details

</td><td>

Details about the onboarding request.Data type: String

</td></tr><tr><td>

result.errors

</td><td>

Description of any error that occurred.Data type: Object

</td></tr><tr><td>

result.error.message

</td><td>

Error message.Data type: String

</td></tr><tr><td>

result.onboardingRequestID

</td><td>

Unique identifier of the onboarding request. Use this value when calling the /devops/onboarding/status endpoint to obtain the status of the associated onboarding process.Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status of the onboarding request, either Success or Failed.Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates the application Bike Rental Service and associates it with the Jenkins pipeline Bike Rentals, the GitHub repository nowDevops01/CorpSite, and the Azure plan testPlan\_Bike\_Rental.

```
curl -X POST "https://servicenow-instance/api/sn_devops/v1/devops/onboarding/app" \ 
-H "Accept: application/json" \ 
-H "Content-Type: application/json" \ 
-u "username":"password" \ 
-d "{ 
  "apps": [ 
    { 
      "name": "Bike Rental Service" 
    } 
  ] 
  "pipelines": [ 
    { 
      "tool": "Primary Jenkins", 
      "name": "Bike Rentals", 
      "app": "Bike Rental Service", 
      "changeSteps": [ 
        { 
          "name": "Prod", 
          "type": "deploy", 
          "changeApprovalGroup": "Change Management", 
          "changeType": "normal" 
        } 
      ] 
    } 
  ], 
  "repositories": [ 
    { 
      "tool": "Primary GitHub", 
      "name": "nowDevops01/CorpSite", 
      "app": "Bike Rental Service" 
    } 
  ] 
  "plans": [ 
    { 
      "tool": "Primary Azure", 
      "name": "testPlan_Bike_Rental", 
"project": "DemoProjecttt", 
      "apps": [ 
        "Bike Rental Service" 
      ] 
    } 
  ] 
"artifactRepositories": [ 
{ 
"tool": "AdoTool", 
"name": "empb5-sonar", 
"apps": [ 
"appXXXXtz" 
] 
} 
] 
 
  "credentials" : { 
    "name": "devops_user", 
    "password": "devops_password" 
  }  
} 
```

Output:

```
{ 
  "result":{ 
    "status": "Success", 
    "details": "Onboarding request has been created. Please use the /status api and the onboarding request number to get the status of the request", 
    "onboardingRequestID": "IBE0001045", 
    "code": "202" 
  } 
} 
```

## DevOps - POST /devops/onboarding/tool

Creates an onboarding tool event that is asynchronously processed by the DevOps service.

Depending on the type of tool for which the request is posted, the endpoint performs the following actions:

-   Creates the tool within the associated ServiceNow instance
-   Connects to the tool
-   Tries to configure the tool \(only if the connection is successful\)
-   Discovers the tool \(only if the connection is successful\)

All of these actions are tool specific and are executed based on the integration capabilities for the specified tool.

![Tool onboarding matrix](../image/devops-tool_onboarding-matrix.png)

The return results for this endpoint only indicate whether the request was posted, it does not indicate whether the associated tools were created. The actual tool creation is processed asynchronously. To obtain the status of the tool creation and all other actions, you must call the [/devops/onboarding/status](devops-api.md#) endpoint and pass in the **onboardingRequestID** parameter that is returned by this endpoint.

Before you are able to access this endpoint, your admin must have configured the DevOps connection and credential alias \(CreateDevOpsTool\) to setup tools in the instance. For details, see Install DevOps Change Velocity. In addition, the calling entity must have the devops.integration.user role.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/onboarding/tool`

Default URL: `/api/sn_devops/devops/onboarding/tool`

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

credentials

</td><td>

Required. Credentials to use for the webhook creation. The tool uses the created webhook to send notifications.Data type: Object

 ```
"credentials": {
  "name": "String",
  "password": "String"
}
```

</td></tr><tr><td>

credentials.name

</td><td>

Required. ServiceNow identifier of the user making the endpoint request. This user must have the devops.integration.user role. Starting with version 1.34.1, this user must have the sn\_devops.admin role.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

credentials.password

</td><td>

Required. Password of the user specified in the **credenitals.name** parameter.Data type: String

</td></tr><tr><td>

tools

</td><td>

Required. Tools to create within the associated ServiceNow instance. You can create one or more tools in a single request.Data type: Array of Objects

```
"tools": [{
  "name": "String",
  "password": "String",
  "type": "String",
  "useMidServer": Boolean,
  "username": "String",
  "url": "String"
}]
```

</td></tr><tr><td>

tools.name

</td><td>

Required. User friendly name or label of the tool to create. This name is used to identify the tool in the DevOps service.Data type: String

</td></tr><tr><td>

tools.password

</td><td>

Required except for Agile tool. Password to use to access the tool. Supported authentications are basic and token; OAuth is not supported.Data type: String

</td></tr><tr><td>

tools.type

</td><td>

Required. Type of tool to create, such as GitHub or BitBucket. The specified value must be one of the Tool labels in the Tool Integrations \[sn\_devops\_tool\_integration\] table. Data type: String

</td></tr><tr><td>

tools.useMidServer

</td><td>

Flag that indicates whether the tool connects through a MID Server.Valid values:

-   true: Connects through a MID Server.
-   false: Does not connect through a MID Server.

Data type: Boolean

</td></tr><tr><td>

tools.username

</td><td>

Required except for Agile tool. User name to use to access the tool through this endpoint.Data type: String

</td></tr><tr><td>

tools.url

</td><td>

Required except for Agile tool. URL of the tool to create. The DevOps service uses this URL to integrate with the tool. If using the 'Azure DevOps' tool, **tools.url** can contain either the ADO Organization URL or the ADO Project URL.When providing an ADO Organization URL, the API discovers all projects under the specified organization and does not configure any projects. When providing an ADO Project URL, the API discovers entities related to the project like \(pipelines, repositories, and plans\) and also configures a project if the **credentials** object is present. To explicitly tell the API to skip the project configuration, configure a flag **configureTool** \(type: boolean\) to `false`. If **configureTool** is not explicitly provided in the payload or is set to `true`, the tool is automatically configured.

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|202|Onboarding request was successfully created.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Results of the onboarding request.Data type: Object

```
"result": {
  "code": "String",
  "details": "String",
  "errors": {Object},
  "onboardingRequestID": "String",
  "status": "String"
}
```

</td></tr><tr><td>

result.code

</td><td>

HTTP status code.Data type: String

</td></tr><tr><td>

result.details

</td><td>

Detailed message about the onboarding request.Data type: String

</td></tr><tr><td>

result.errors

</td><td>

Description of any error that occurred.Data type: Object

</td></tr><tr><td>

result.error.message

</td><td>

Error message.Data type: String

</td></tr><tr><td>

result.onboardingRequestID

</td><td>

Unique identifier of the onboarding request. Use this value when calling the /devops/onboarding/status endpoint to obtain the status of the associated tool onboarding process.Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status of the onboarding request, either Success or Failed.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to onboard GitHub.

```
curl -X POST "https://servicenow-instance/api/sn_devops/v1/devops/onboarding/tool" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-u "username":"password" \
-d {
  "tool":[{
    "name": "Primary GitHub",
    "type": "GitHub",
    "url": "https"//api.github.com",
    "username": "username",
    "password": "password",
    "useMidServer": false 
  }]
  "credentials" : {
    "name": "devops_user",
    "password": "devops_password"
  }
}
```

```
{
  "result":{
    "status": "Success",
    "details": "Onboarding request has been created. Please use the /status api and the onboarding request number to get the status of the request",
    "onboardingRequestID": "IBE0001041",
    "code": "202"
  }
}
```

## DevOps - POST /devops/orchestration/changeControl

Registers a callback with a ServiceNow instance for an orchestration task under change control, which can be called once a decision has been made on the change request.

Before you call this endpoint, you must have an orchestration task created in your ServiceNow instance. You can create this task either through Discovery or by calling the [DevOps - POST /devops/orchestration/stepMapping](devops-api.md#) endpoint. You must also ensure that the orchestration task is associated to a previously defined pipeline step and that change control is enabled \(by selecting the **Change control** option on the App Stage form.\) For details, see Accelerating DevOps change.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/orchestration/changeControl`

Default URL: `/api/sn_devops/devops/orchestration/changeControl`

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

toolId

</td><td>

Required. Sys\_id of the DevOps tool for which to place the specified task under change control.Data type: String

Table: Orchestration Tool \[sn\_devops\_orchestration\_tool\]

</td></tr><tr><td>

toolType

</td><td>

Type of tool.Valid value: Any value that identifies the tool, such as "jenkins".

Data type: String

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-orch-callBackURL-devops"><td>

callbackURL

</td><td>

Required. URL that the ServiceNow instance can call back once the associated change request approval process is complete. This callback should let the pipeline execution continue or not, based on the approval result. Data type: String

</td></tr><tr><td>

changeRequestDetails

</td><td>

Name-value pairs of the fields to set when closing a change request. This object can contain any fields in the Change Request record except the following:-   impact
-   number
-   risk
-   risk\_impact\_analysis
-   sys\_id

If these fields are included in the request, the endpoint returns a 400 error and the change request is not updated. Also, if you include fields that require other mandatory fields to be set, and those fields are not sent, the request will fail during later processing of the pipeline. This failure is noted in the work notes of the change request, along with an error message for that particular change request, such as: `Change request update failed with reason: <Error Message from platform>. Canceling change request and the related step execution.`

You can also pass the boolean parameter **setCloseCode** in this object to specify whether to set closure information on the associated Change Request record.

-   If set to true, the close\_code field is set to the status of the job and the close\_notes field is set to a link to the step execution in the associated Change Request record. The default value is true.
-   If set to false, the close\_code and close\_notes fields are not set and a link to the step execution is set in the work\_notes field.

Data type: Object

</td></tr><tr id="row-stepMap-isMultiBranch"><td>

isMultiBranch

</td><td>

If the orchestration tool is Jenkins, flag that indicates whether the project is of type Multibranch. Valid values:

-   true: Project is of type Multibranch.
-   false: Project is not of type Multibranch.

Data type: Boolean

Default: false

</td></tr><tr><td>

orchestrationTaskDetails

</td><td>

Required. Description of the orchestration task. Data type: Object

```
"orchestrationTaskDetails": {
  "message": "String",
  "triggerType": "String",
  "upstreamTaskExecutionURL": "String"
}
```

</td></tr><tr id="row-orch-orchestrationTaskDetails-message-devops"><td>

orchestrationTaskDetails.message

</td><td>

Free-form text message. Data type: String

</td></tr><tr id="row-orch-orchestrationTaskDetails-triggerType-devops"><td>

orchestrationTaskDetails.triggerType

</td><td>

Required. The way the orchestration task was started. Valid values:

-   scm: Git/scm tool code commit triggered the job.
-   upstream: Upstream job triggered this job.
-   user: User manually started the job.

Data type: String

</td></tr><tr id="row-orch-orchestrationTaskDetails-upstreamTaskExecutionURL-devops"><td>

orchestrationTaskDetails.upstreamTaskExecutionURL

</td><td>

Required if **triggerType** is set to `upstream`. Upstream task execution URL. For example: https://jenkins.mycompany.com:8080/job/Mobile-Platform-test/40/

Data type: String

</td></tr><tr><td>

orchestrationTaskURL

</td><td>

Required. URL of the orchestration task for which to create the call back. For example: https://jenkins.mycompany.com:8080/orchestration\_task/Mobile-Platform-deploy/

Data type: String

</td></tr><tr><td>

parentNode

</td><td>

If the orchestration task is a child nested inside a parent orchestration task, this value contains the parent node details. Data type: Object

```
"parentNode": {
  "id": "String",
  "name": "String",
  "upstreamStageName": "String",
  "upstreamTaskExecutionURL": "String"
}
```

</td></tr><tr><td>

parentNode.id

</td><td>

Unique ID for the parent node. In Jenkins, this value corresponds to a pipeline stage ID.

 Data type: String

</td></tr><tr><td>

parentNode.name

</td><td>

Name of the parent node.In Jenkins, this value corresponds to a pipeline stage name.

 Data type: String

</td></tr><tr><td>

parentNode.upstreamStageName

</td><td>

Name of the parent node’s upstream orchestration task.In Jenkins, this value corresponds to a pipeline stage name.

 Data type: String

</td></tr><tr><td>

parentNode.upstreamTaskExecutionURL

</td><td>

URL of the parent node’s upstream task execution.In Jenkins, this value corresponds to a pipeline stage execution URL.

 Data type: String

</td></tr><tr id="row-stepMap-parentStageName"><td>

parentStageName

</td><td>

If the orchestration task is a child nested inside a parent orchestration task, the name of the parent orchestration task. Data type: String

</td></tr><tr id="row-stepMap-parentStageURL"><td>

parentStageURL

</td><td>

If the orchestration task is a child nested inside a parent orchestration task, the URL of the parent orchestration task. Data type: String

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

Authorization

</td><td>

Starting with v2, this API supports token-based authentication. Tokens can be acquired by clicking the **Copy token** button on the tool record, located in the Tool \[sn\_devops\_tool\] table. The token can then be used in an authorization header in the format `Authorization: sn_devops.DevOpsToken <tool_sys_id>:<tool_token>`.

**Note:** If Basic Auth details \(user name and password\) are provided in addition to an authorization header with token, Basic Auth takes precedence.

If the **devops.system** user is not available in your instance, use the **Switch to this user after token based authentication is successful** property. This property enables setting any user that has the sn\_devops.integration role, which is needed to complete the token authentication. For information, see DevOps Change Velocity properties.

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
|201|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Invalid or missing authentication.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changeControl

</td><td>

Flag that indicates whether the orchestration task is under change control. Possible values:

-   true: Under change control.
-   false: Not under change control.

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

```
curl -X POST "https://instance.servicenow.com/api/sn_devops/v1/devops/orchestration/changeControl?toolId=f0ca45679323008b52f3b457415ae6&toolType=jenkins"
-H "accept: application/json"\
-H "Content-Type: application/json"\
-u "username":"password"\
-d "{
  \"orchestrationTaskURL\":\"https://jenkins.mycompany.com:8080/orchestration task/Mobile-Platform-deploy/\",
  \"callbackURL\":\"https://jenkins.mycompany.com:8080/sn-devops/964aca59-0cae-4d9b-a36d-5929f426cf31\",
  \"orchestrationTaskDetails\":{
    \"message\":\"Started by upstream project \\\"Mobile-Platform-test\\\" build number 40\",
    \"triggerType\":\"upstream\",
    \"upstreamTaskExecutionURL\":\"https://jenkins.mycompany.com:8080/job/Mobile-Platform-test/40/\"}
}"
```

Response body.

```
{
"result": {
   "changeControl": true,
   "status": "Success"
   }
}
```

### cURL request

This example shows how to pass fields in the **changeRequestDetails** object when closing a change request.

```
curl -X POST "https://instance.servicenow.com/api/sn_devops/v1/devops/orchestration/changeControl?toolId=f0ca45679323008b52f3b457415ae6&toolType=jenkins"
-H "accept: application/json"\
-H "Content-Type: application/json"\
-u "username":"password"\
-d "{
  "callbackURL":"http://192.168.0.4:3000/jenkins/sn-devops/pipeline_839b7605-b98d-4831-bc87-96829de7da37",
  "orchestrationTaskURL":"http://192.168.0.4:3000/jenkins/job/java_sample_tests#deploy/",
  "isMultiBranch":"false",
  "orchestrationTaskName":"java_sample_tests#deploy",
  "orchestrationTaskDetails":{
    "triggerType":"upstream",
    "upstreamTaskExecutionURL":"http://192.168.0.4:3000/jenkins/job/java_sample_tests/129/execution/node/35/wfapi/describe",
    "taskExecutionURL":"http://192.168.0.4:3000/jenkins/job/java_sample_tests/129/execution/node/50/wfapi/describe"
  },
  "changeRequestDetails":{
    "setCloseCode":false,
    "attributes":{
      "sys_created_by":"1832fbe1d701120035ae23c7ce610369",
      "sys_updated_by":"56826bf03710200044e0bfc8bcbe5dca",
      "requested_by":{
         "name":"test user1"
      },
      "watch_list":[
        {
          "name":"test user1"
        },
        {
          "name":"test user2"
        },
        {
          "name":"Alejandra Prenatt"
        },
          "56826bf03710200044e0bfc8bcbe5dca"
      ],
      "work_notes_list":[
        "56826bf03710200044e0bfc8bcbe5dca",
        "46c6f9efa9fe198101ddf5eed9adf6e7",
        "d8f57f140b20220050192f15d6673a98"
      ],
      "assigned_to":"1832fbe1d701120035ae23c7ce610369",
      "category":"Service",
      "sys_created_on":"2021-02-09 18:58:41",
      "priority":"2",
    }
  }
}"
```

Response body.

```
{
"result": {
   "changeControl": true,
   "status": "Success"
   }
}
```

## DevOps - POST /devops/orchestration/stepMapping

Verifies that the information being passed is valid for the creation of an orchestration task and is valid for association to a previously created step. If both are valid, it creates the orchestration task and makes the association.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/orchestration/stepMapping`

Default URL: `/api/sn_devops/devops/orchestration/stepMapping`

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

toolId

</td><td id="entry-stepMap-toolId">

Required. Sys\_id of the orchestration tool. Located in the Orchestration Tool \[sn\_devops\_orchestration\_tool\] table. Data type: String

</td></tr><tr><td>

toolType

</td><td id="entry-stepMap-toolType">

Required. Type of tool. Valid values: jenkins

Data type: String

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-stepMap-branchName"><td>

branchName

</td><td>

Name of the branch associated with the orchestration task. Data type: String

</td></tr><tr id="row-stepMap-isMultiBranch"><td>

isMultiBranch

</td><td>

If the orchestration tool is Jenkins, flag that indicates whether the project is of type Multibranch. Valid values:

-   true: Project is of type Multibranch.
-   false: Project is not of type Multibranch.

Data type: Boolean

Default: false

</td></tr><tr><td>

parentNode

</td><td>

If the orchestration task is a child nested inside a parent orchestration task, this value contains the parent node details. Data type: Object

 ```
"parentNode": {
  "id": "String",
  "name": "String",
  "upstreamStageName": "String",
  "upstreamTaskExecutionURL": "String"
}
```

</td></tr><tr><td>

parentNode.id

</td><td>

Unique ID for the parent node. In Jenkins, this value corresponds to a pipeline stage ID.

 Data type: String

</td></tr><tr><td>

parentNode.name

</td><td>

Name of the parent node.In Jenkins, this value corresponds to a pipeline stage name.

 Data type: String

</td></tr><tr><td>

parentNode.upstreamStageName

</td><td>

Name of the parent node’s upstream orchestration task.In Jenkins, this value corresponds to a pipeline stage name.

 Data type: String

</td></tr><tr><td>

parentNode.upstreamTaskExecutionURL

</td><td>

URL of the parent node’s upstream task execution.In Jenkins, this value corresponds to a pipeline stage execution URL.

 Data type: String

</td></tr><tr id="row-stepMap-parentStageName"><td>

parentStageName

</td><td>

If the orchestration task is a child nested inside a parent orchestration task, the name of the parent orchestration task. Data type: String

</td></tr><tr id="row-stepMap-parentStageURL"><td>

parentStageURL

</td><td>

If the orchestration task is a child nested inside a parent orchestration task, the URL of the parent orchestration task. Data type: String

</td></tr><tr><td>

orchestrationTaskName

</td><td>

Required. Name of the orchestration task. This is the same task referenced in the**orchestrationTaskURL**. Data type: String

</td></tr><tr id="row-orch-orchestrationTaskURL-devops"><td>

orchestrationTaskURL

</td><td>

Required. URL of the orchestration task. For example: https://jenkins.mycompany.com:8080/orchestration\_task/Mobile-Platform-deploy/

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

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Authorization

</td><td>

Starting with v2, this API supports token-based authentication. Tokens can be acquired by clicking the **Copy token** button on the tool record, located in the Tool \[sn\_devops\_tool\] table. The token can then be used in an authorization header in the format `Authorization: sn_devops.DevOpsToken <tool_sys_id>:<tool_token>`.

**Note:** If Basic Auth details \(user name and password\) are provided in addition to an authorization header with token, Basic Auth takes precedence.

If the **devops.system** user is not available in your instance, use the **Switch to this user after token based authentication is successful** property. This property enables setting any user that has the sn\_devops.integration role, which is needed to complete the token authentication. For information, see DevOps Change Velocity properties.

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
|201|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="table_y32_sc3_bmb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Flag that indicates whether the verification was successful.Valid values:

-   true: Verification was successful.
-   false: Verification wasn't successful.

Data type: Boolean

</td></tr><tr><td>

stepValid

</td><td>

Flag that indicates whether the information sent is valid.Valid values:

-   true: Information sent is valid.
-   false: Information sent isn't valid.

Data type: Boolean

</td></tr></tbody>
</table>### Sample cURL request

```
curl -X POST "https://instance.servicenow.com/api/sn_devops/v1/devops/orchestration/stepMapping?toolId=f0ca45679323008b52f3b457415ae6&toolType=jenkins"
-H "Accept: application/json"\
-H "Content-Type: application/json"\
-u "username":"password"\
-d "{
  \"orchestrationTaskURL\":\" http://127.0.0.1:8090/jenkins/job/CorpSite/job/primary#deploy PROD/\",
  \"orchestrationTaskName\":\" primary#deploy PROD\"
}"
```

Results if information is valid.

```
{
  "result": {
    "stepValid": true,
    "status": "Success"
  }
}
```

Results if information is invalid.

```
{
  "result": {
    "stepValid": false,
    "status": "Success"
  }
}
```

## DevOps - POST /devops/package/registration

Enables orchestration tools to create new artifact packages that contain specified artifact versions.

Artifact packages are used to display commits to change approvers when they view a change request. For commits to show in change requests, the package must be created in the stage prior to the stage containing the change approval.

Any artifact versions included in the package registration request should already be registered with DevOps. For details on registering artifact versions, see [DevOps - POST /devops/artifact/registration](devops-api.md#).

Typically, you will pass in the **artifacts.version** and **artifacts.name** parameters when identifying an artifact version to include in a package. You can also use the advanced features of this endpoint which allows you to pass the build details for each artifact version instead of the version itself. Artifact-specific build details include the following parameters:

-   **artifacts.pipelineName** or **artifacts.projectName**
-   **artifacts.taskExecutionNumber**
-   **artifacts.stageName**
-   **artifacts.branchName**

The endpoint uses these artifact-specific build details to look up task execution information and then copies the associated versions to the package. It uses non-artifact specific build details \(**pipelineName** or **projectName**, **taskExecutionNumber**, **branchName**, and **stageName**\) to associate the created package to a pipeline execution.

**Note:** This endpoint does not support updates. It always creates a new package even if one with same name already exists.

For additional information on artifact packages, see Using DevOps change acceleration for releases.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/package/registration`

Default URL: `/api/sn_devops/devops/package/registration`

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

orchestrationToolId

</td><td>

Required. Sys\_id of the orchestration tool associated with the artifact package. The endpoint uses this information to locate task execution information.Data type: String

Table: Orchestration Tool \[sn\_devops\_orchestration\_tool\]

</td></tr><tr><td>

toolId

</td><td>

Sys\_id of the artifact tool associated with the artifact package.Data type: String

Table: Artifact Tool \[sn\_devops\_artifact\_tool\]

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

artifacts

</td><td>

At least one entry required. Array of objects in which each object uniquely identifies an artifact version to include in the package.Data type: Array of Objects

```
"artifacts": [
{
  "branchName": "String",
  "name": "String",
  "pipelineName": "String",
  "projectName": "String",
  "repositoryName": "String",
  "stageName": "String",
  "taskExecutionNumber": "String",
  "version": "String"
]
```

</td></tr><tr><td>

artifacts.branchName

</td><td>

Required if **artifact.version** is not passed and it is a multi-branch setup. Name of branch in which the artifact versions are stored.Data type: String

Maximum length: 160

Default: Null

</td></tr><tr><td>

artifacts.name

</td><td>

Required. Artifact file name.Data type: String

Maximum length: 160 characters

</td></tr><tr><td>

artifacts.pipelineName

</td><td>

Required if **artifact.version** and **artifacts.projectName** are not passed. Pipeline name.Data type: String

Maximum length: 160

Default: Null

</td></tr><tr><td>

artifacts.projectName

</td><td>

Required if **artifact.version** and **artifact.pipelineName** are not passed. Free-form project name.Data type: String

Maximum length: 160

Default: Null

</td></tr><tr><td>

artifacts.repositoryName

</td><td>

Required. Artifact repository name.Data type: String

Maximum length: 160 characters

</td></tr><tr><td>

artifacts.stageName

</td><td>

Required if **artifact.version** is not passed. Stage name. Data type: String

Maximum length: 160

Default: Null

</td></tr><tr><td>

artifacts.taskExecutionNumber

</td><td>

Required if **artifact.version** is not passed. Pipeline run number.Data type: String

Default: Null

</td></tr><tr><td>

artifacts.version

</td><td>

Required if build details are not provided. Version of the artifacts.Data type: String

Format: &lt;Major&gt;.&lt;Minor&gt;

Default: Null

</td></tr><tr><td>

branchName

</td><td>

Required if it is multi-branch project. Name of the branch in the repository where the artifacts are stored. Data type: String

Maximum length: 200 characters

Default: Null

</td></tr><tr><td>

name

</td><td>

Required. Name of package.Data type: String

Maximum length: 160 characters

</td></tr><tr><td>

pipelineName

</td><td>

Required if **projectName** is not passed. Pipeline name.Data type: String

Maximum length: 160 characters

Default: Null

</td></tr><tr><td>

projectName

</td><td>

Required if **pipelineName** is not passed. Free-form project name.Data type: String

Maximum length: 160

Default: Null

</td></tr><tr><td>

stageName

</td><td>

Required if **pipelineName** is passed. Stage name. Data type: String

Maximum length: 160 characters

Default: Null

</td></tr><tr><td>

taskExecutionNumber

</td><td>

Required. Pipeline run number.Data type: String

Maximum length: 128 characters

Default: Null

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Authorization

</td><td>

Starting with v2, this API supports token-based authentication. Tokens can be acquired by clicking the **Copy token** button on the tool record, located in the Tool \[sn\_devops\_tool\] table. The token can then be used in an authorization header in the format `Authorization: sn_devops.DevOpsToken <tool_sys_id>:<tool_token>`.

**Note:** If Basic Auth details \(user name and password\) are provided in addition to an authorization header with token, Basic Auth takes precedence.

If the **devops.system** user is not available in your instance, use the **Switch to this user after token based authentication is successful** property. This property enables setting any user that has the sn\_devops.integration role, which is needed to complete the token authentication. For information, see DevOps Change Velocity properties.

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
|200|Success. Success with response body.|
|201|Created. Success with response body.|
|400|Bad Request. The request URI does not match the APIs in the system, or the operation failed for unknown reasons. Invalid headers can also cause this error.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

response

</td><td>

Results of the package registration request.Data type: Object

```
"response": {
  "artifact_register_requests": {Object},
  "sn_devops_m2m_artifact_version_package": {Object},
  "sn_devops_package": {Object}
}
```

</td></tr><tr><td>

response.artifact\_register\_requests

</td><td>

Results for any register requests that have not completed processing and have been stored in the Artifact Staged Request \[sn\_devops\_artifact\_staging\] table.Data type: Object

```
"artifact_register_requests": {
  "create": [Array],
  "found": [Array],
  "update": [Array]
}
```

</td></tr><tr><td>

response.artifact\_register\_requests.create

</td><td>

If the request created package staging records, the list of sys\_ids of the created staging records.Data type: Array of Objects

```
"create": [
  {
    "id": "String"
  }
]
```

</td></tr><tr><td>

response.artifact\_register\_requests.create.id

</td><td>

Sys\_id of the package staging record created by the request.Data type: String

</td></tr><tr><td>

response.artifact\_register\_requests.found

</td><td>

If the associated package staging records already exist, the list of sys\_ids of the existing records. **Note:** No modifications are made to existing packages.

Data type: Array of Objects

```
"found": [
  {
    "id": "String"
  }
]
```

</td></tr><tr><td>

response.artifact\_register\_requests.found.id

</td><td>

Sys\_id of an existing package staging record.Data type: String

</td></tr><tr><td>

response.artifact\_register\_requests.update

</td><td>

Currently unused.

</td></tr><tr><td>

response.artifact\_register\_requests.update.id

</td><td>

Currently unused.

</td></tr><tr><td>

response.sn\_devops\_m2m\_artifact\_version\_package

</td><td>

Results for each artifact version associated with a package.Data type: Object

```
"sn_devops_m2m_artifact_version_package": {
  "create": [Array],
  "found": [Array],
  "update": [Array]
}
```

</td></tr><tr><td>

response.sn\_devops\_m2m\_artifact\_version\_package.create

</td><td>

If the request created records linking artifact versions to packages, the list of sys\_ids of the created records.Data type: Array of Objects

```
"create": [
  {
    "id": "String"
  }
]
```

Table: Artifact Version to Package \[sn\_devops\_m2m\_artifact\_version\_package\]

</td></tr><tr><td>

response.sn\_devops\_m2m\_artifact\_version\_package.create.id

</td><td>

Sys\_id of the Artifact Version to Package record created by the request.Data type: String

</td></tr><tr><td>

response.sn\_devops\_m2m\_artifact\_version\_package.found

</td><td>

If a linking record already exists in the Artifacts Version to Package table, the list of sys\_ids of the existing linking records.**Note:** No modifications are made to existing records.

Data type: Array of Objects

```
"found": [
  {
    "id": "String"
  }
]
```

</td></tr><tr><td>

response.sn\_devops\_m2m\_artifact\_version\_package.found.id

</td><td>

Sys\_id of the existing Artifact Version to Package record.Data type: String

</td></tr><tr><td>

response.sn\_devops\_m2m\_artifact\_version\_package.update

</td><td>

Currently unused.

</td></tr><tr><td>

response.sn\_devops\_m2m\_artifact\_version\_package.update.id

</td><td>

Currently unused.

</td></tr><tr><td>

response.sn\_devops\_package

</td><td>

Results for any package records in the Packages \[sn\_devops\_package\] table that were manipulated during the processing of the request.Data type: Object

```
"sn_devops_package": {
  "create": [Array],
  "found": [Array],
  "update": [Array]
}
```

</td></tr><tr><td>

response.sn\_devops\_package.create

</td><td>

If package records were created by the request, the list of sys\_ids of the created records.Data type: Array of Objects

```
"create": [
  {
    "id": "String"
  }
]
```

</td></tr><tr><td>

response.sn\_devops\_package.create.id

</td><td>

Sys\_id of the package record created by the request.Data type: String

</td></tr><tr><td>

response.sn\_devops\_package.found

</td><td>

If package records used in the register request already exist, the list of sys\_ids of the existing records.**Note:** No modifications are made to existing records.

Data type: Array of Objects

```
"found": [
  {
    "id": "String"
  }
]
```

</td></tr><tr><td>

response.sn\_devops\_package.found.id

</td><td>

Sys\_id of an existing package record referenced by the request.Data type: String

</td></tr><tr><td>

response.sn\_devops\_package.update

</td><td>

Currently unused.

</td></tr><tr><td>

response.sn\_devops\_package.update.id

</td><td>

Currently unused.

</td></tr><tr><td>

status

</td><td>

Status of the registration request.Possible values:

-   Error: Response body contains list of all errors.
-   Success: Response body contains return results.

Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
# Example passing the artifact version
curl -X POST "https://instance.servicenow.com/api/sn_devops/devops/package/registration?toolId=f0ca45679323008b52f3b457415ae6"\
-H "accept: application/json"\
-H "Content-Type: application/json"\
-u "username":"password"\
-d "{\
"name": "sentimentpackage",\
"artifacts": [\
{\
"name": "sa-web.jar",\
"repositoryName": "services-1031",\
"version": "3.1"\
},\
{\
"name": "sa-frontend.jar",\
"repositoryName": "services-1031",\
"version": "9.2"\
}\
],\
"pipelineName": "spring-boot-app",\
"taskExecutionNumber": "160",\
"stageName": "Build",\
"branchName": "primary"\
}"
```

Response - package created:

```
"result": {
"status": "Success",
"response": {
  "sn_devops_package": {
    "create": [
        {
          "id": "0d57367a532e00107109ddeeff7b122a"
        } 
      ],
    "update": [],
    "found": []
  },
  "sn_devops_m2m_artifact_version_package": {
    "create": [
      {
        "id": "c957367a532e00107109ddeeff7b122b"
      },
      {
        "id": "8157367a532e00107109ddeeff7b122c"
      }
    ],
    "update": [],
    "found": []
    }
  },
  "responseCode": 201
  }
}
```

### Sample cURL request

```
# Example passing the build details
curl -X POST "https://instance.servicenow.com/api/sn_devops/devops/package/registration?toolId=f0ca45679323008b52f3b457415ae6"
-H "accept: application/json"\
-H "Content-Type: application/json"\
-u "username":"password"\
-d "{\
"name": "sentimentpackage",\
"artifacts": [\
{\
"name": "sa-web.jar",\
"repositoryName": "services-1031",\
"pipelineName": "spring-boot-app",\
"taskExecutionNumber": "160",\
"stageName": "Build",\
"branchName": "primary"\
},\
{\
"name": "sa-frontend.jar",\
"repositoryName": "services-1031",\
"pipelineName": "spring-boot-fe",\
"taskExecutionNumber": "991",\
"stageName": "Build",\
"branchName": "primary"\
}\
],\
"pipelineName": "spring-boot-app",\
"taskExecutionNumber": "160",\
"stageName": "Build",\
"branchName": "primary"\
}"
```

Response - request created a staged package:

```
{
"result": {
  "status": "Success",
  "response": {
    "artifact_register_requests": {
      "create": [
        { 
          "id": "4628f276532e00107109ddeeff7b1245"
        },
        {
          "id": "4e28f276532e00107109ddeeff7b1245"
        },
        {
          "id": "ce28f276532e00107109ddeeff7b1245"
        }
      ],
      "update": [],
      "found": []
    }
  }, 
  "responseCode": 201 
 }
}
```

## DevOps - POST /devops/tool/\{capability\}

Posts the passed in payload to the Inbound Event \[sn\_devops\_inbound\] table for processing by a custom DevOps subflow.

Call this endpoint from the associated webhook in your tool, specified by the passed in **capability** parameter. A custom subflow, to process the passed in payload, must already be defined in your ServiceNow instance. Based on a predefined schedule, the DevOps Master Flow picks up the webhook event information from the Inbound Event table and passes it to the custom subflow, which then process the payload. For more information on creating a custom subflow, see Creating DevOps subflows.

For additional information on test tool integration, see DevOps test tool integration.

Before calling this endpoint for a custom DevOps tool, you must implement the handleTool\(\) and getNativeIdForOrchestrationTask\(\) methods from sn\_devops.DevOpsOrchestrationToolIntegrationHandler. For more information, see [DevOpsOrchestrationToolIntegrationHandler - Scoped](../../../app-store/dev_portal/API_reference/DevOpsOrchToolIntHandlerScoped/concept/DevOpsOrchToolIntHandlerScopedAPI.md#)[DevOpsOrchestrationToolIntegrationHandler - Scoped](https://developer.servicenow.com/go_to_api.do?ID=DevOpsOrchToolIntHandlerScopedAPI&v=washingtondc).

**Note:** Starting with 1.34.1 version, a new version of this API has been introduced. With this API, Adaptive Authentication policies may not execute as expected. For more information about these policies, see Adaptive authentication.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/tool/{capability}`

Default URL: `/api/sn_devops/devops/tool/{capability}`

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

capability

</td><td>

Type of tool passing in the payload to store in the Inbound Event table.Valid values \(not case-sensitive\):

-   artifact
-   code
-   orchestration
-   plan
-   test

Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

orchestrationToolId

</td><td>

Optional. Sys\_id of the orchestration tool to which the related pipeline belongs. **orchestrationToolId** is required if the **capability** request parameter is set to `test` or `softwarequality`.The value in the **toolId** parameter is the default orchestration tool if the **orchestrationToolId** parameter isn't passed.

Data type: String

</td></tr><tr><td>

testType

</td><td>

Required if **capability** is set to `test`. Type of test being run. Data type: String

Table: The valid values for this parameter are those in the Test type column of the Test Types \[sn\_devops\_test\_type\] table.

</td></tr><tr><td>

toolId

</td><td>

Required. Sys\_id of the tool for which the endpoint is being called.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|Tool dependant|The tool determines the content of the payload.|

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Authorization

</td><td>

Starting with v2, this API supports token-based authentication. Tokens can be acquired by clicking the **Copy token** button on the tool record, located in the Tool \[sn\_devops\_tool\] table. The token can then be used in an authorization header in the format `Authorization: sn_devops.DevOpsToken <tool_sys_id>:<tool_token>`.

**Note:** If Basic Auth details \(user name and password\) are provided in addition to an authorization header with token, Basic Auth takes precedence.

If the **devops.system** user is not available in your instance, use the **Switch to this user after token based authentication is successful** property. This property enables setting any user that has the sn\_devops.integration role, which is needed to complete the token authentication. For information, see DevOps Change Velocity properties.

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
|201|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Invalid or missing authentication.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

details

</td><td>

Entry for all error conditions. Data type: Object

```
"details": {
  "errors": [Array]
}
```

</td></tr><tr><td>

details.errors

</td><td>

Description of a single error. Data type: Array of Objects

```
"errors": [
  {
    "message": "String"
  }
]
```

</td></tr><tr><td>

details.errors.message

</td><td>

Detailed error message. -   `The request does not have any path parameters`: No path parameters are included in the call.
-   `The request does not have capability path parameter`: The capability path parameter was not included in the call.
-   `Unsupported capability type`: The specified capability parameter is not a valid value.

 Data type: String

</td></tr><tr><td>

status

</td><td>

Response status such as "Success" or "Data Error".Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the record created in the Inbound Event table.Data type: String

</td></tr></tbody>
</table>### Sample cURL request for artifact

```
curl -X POST "https://instance.service-now.com/api/sn_devops/v1/tool/artifact?toolId=3b59043ee4ea556e6850d61bc1a77e8a" 
-H "accept: application/json"\
-H "Content-Type: application/json"\
-u "username":"password"\
-d "{
   "artifacts": [
      {
         "name": "sp-boot-app",
         "version": "1.320",
         "semanticVersion": "1.320.0",
         "repositoryName": "sp-boot-app-repo"
      }
   ],
   "pipelineName": "spring-boot-app-gitea",
   "taskExecutionNumber": "320",
   "stageName": "Build"
}"
```

Success response:

```
{
   "result": {
      "status": "Success",
      "sysId": "33c57245dbf68410bc8cdd384b961966"
   }
}
```

### Sample cURL request for artifact

```
curl -X POST "https://instance.service-now.com/api/sn_devops/v1/tool/artifact?toolId=3b59043ee4ea556e6850d61bc1a77e8a" 
-H "accept: application/json"\
-H "Content-Type: application/json"\
-u "username":"password"\ 
-d "{\
   "timestamp": "2020-01-11T00:52:01.541+0000",\
   "nodeId": "137BEECF-E1BF7BC1-90212D1C-0749A6D4-BC670F6B",\
   "initiator": "admin/172.17.0.1",\
   "repositoryName": "maven-releases29",\
   "action": "CREATED",\
   "component": {\
      "id": "2a59043ed2ea556e6850d61bc1a77c7b",\
      "componentId": "c3AtYm9vdC1hcHAtcmVwbzoyYTU5MDQzZWQyZWE1NTZlNjg1MGQ2MWJjMWE3N2M3Yg",\
      "format": "maven2",\
      "name": "sentiment-analysis-web",\
      "group": "com.spboot",\
      "version": "1.1"\
   }\
}"
```

Error response:

```
{
   "result": {
      "status": "Data Error",
      "details": {
         "errors": [
            {
               "message": "Unsupported capability type"
            }
         ]
      }
   }
}
```

### Sample cURL request for code

```
curl "https://instance.service-now.com/api/sn_devops/devops/tool/code?toolId=8d4f56598702c510f894419d0ebb35aa&testType=junit" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "commits": [
      {
         "totalFiles": 1,
         "nativeIdList": [
            "49",
            "50"
         ],
         "id": "f14732d0cc854ce3ec374b97ecd4ec3c383386cd",
         "url": "https://dev.azure.com/xyzabcd/adoTests/_git/DeployableRepo/commit/f14732d0cc854ce3ec374b97ecd4ec3c383386cd",
         "apiURL": "https://dev.azure.com/xyzabcd/9fe32a65-60a5-46fe-bc8d-11a92bf059f9/_apis/git/repositories/8d7ba019-1739-431c-beb4-6025dd41f1ac/commits/f14732d0cc854ce3ec374b97ecd4ec3c383386cd",
         "message": "Fixes #49 and #50",
         "committedDate": "2022-03-23T11:59:46Z",
         "committer": {
            "email": "xyz.abcd@email.com"
         },
         "details": [
            {
               "action": "edit",
               "changes": "",
               "file": "/LICENSE",
               "additions": 0,
               "deletions": 0,
               "totalChanges": 0
            }
         ]
      }
   ],
   "repository": {
      "id": "8d7ba019-1739-431c-beb4-6025dd41f1ac",
      "name": "DeployableRepo",
      "url": "https://dev.azure.com/xyzabcd/adoTests/_git/DeployableRepo"
   },
   "branch": {
      "name": "refs/heads/master",
      "url": "https://dev.azure.com/xyzabcd/adoTests/_git/DeployableRepo?version=GBmaster"
   }
}" \
--user 'username':'passsword'

```

Success response:

```
{
   "result": {
      "status": "Success",
      "sysId: "1f8e586b879e85100f71cbfc0ebb3526"
   }
}
```

### Sample cURL request for orchestration

```
curl "https://instance.service-now.com/api/sn_devops/devops/tool/orchestration?toolId=8d4f56598702c510f894419d0ebb35aa&testType=junit" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  "toolId": "d450f5c887e609100f71cbfc0ebb35e5",
  "buildNumber": 5676,
  "nativeId": "adoTests/DeployableRepo#deploy#5676",
  "pipelineId": "2",
  "name": "adoTests/DeployableRepo#deploy",
  "id": "adoTests/DeployableRepo#deploy#5676",
  "url": "https://dev.azure.com/xyzabcd/_build/results?buildId=5676#deploy/",
  "previousAttemptUrl": "",
  "attemptNumber": 1,
  "pipelineExecutionUrl": "https://dev.azure.com/xyzabcd/_build/results?buildId=5676",
  "orchestrationTaskUrl": "https://dev.azure.com/xyzabcd/adoTests/_build?name=DeployableRepo#deploy",
  "orchestrationTaskName": "adoTests/DeployableRepo #deploy",
  "orchestrationTask": {
    "orchestrationTaskName": "adoTests/DeployableRepo#deploy",
    "toolId": "d450f5c887e609100f71cbfc0ebb35e5",
    "orchestrationTaskURL": "https://dev.azure.com/xyzabcd/adoTests/_build?name=DeployableRepo#deploy",
    "stageName": "deploy"
  },
  "upstreamTaskUrl": [],
  "result": "building",
  "startDateTime": "2022-03-23 12:01:31",
  "log": "https://dev.azure.com/xyzabcd/adoTests/_build/results?buildId=5676&view=logs&j=5264e576-3c6f-51f6-f055-fab409685f20",
  "logUrl": "https://dev.azure.com/xyzabcd/adoTests/_build/results?buildId=5676&view=logs&j=5264e576-3c6f-51f6-f055-fab409685f20"
}" \
--user 'username':'password'

```

Success response:

```
{
   "result": {
      "status": "Success",
      "sysId: "37dfd8a7879e85100f71cbfc0ebb35c0"
   }
}
```

### Sample cURL request for plan

```
curl "https://instance.service-now.com/api/sn_devops/devops/tool/plan?toolId=8d4f56598702c510f894419d0ebb35aa&testType=junit" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "id": "1053",
   "type": "bug",
   "state": "planned",
   "shortDescription": "Title - Work Item test in 1.33.3",
   "createdDateTime": "2022-03-23T10:45:53.02Z",
   "parentId": "",
   "url": "https://dev.azure.com/xyzabcd/9fe32a65-60a5-46fe-bc8d-11a92bf059f9/_workitems/edit/1053",
   "version": {
      "id": "adoTests",
      "shortDescription": "adoTests",
      "createdDateTime": "2022-03-23T10:46:12.355Z",
      "url": "https://dev.azure.com/xyzabcd/adoTests",
      "app": {
         "id": "adoTests",
         "shortDescription": "adoTests",
         "createdDateTime": "2022-03-23T10:46:12.355Z",
         "url": "https://dev.azure.com/xyzabcd/9fe32a65-60a5-46fe-bc8d-11a92bf059f9/_workitems/edit/1053"
      }
   },
   "app": {
      "id": "adoTests",
      "shortDescription": "adoTests",
      "createdDateTime": "2022-03-23T10:46:12.355Z",
      "url": "https://dev.azure.com/xyzabcd/adoTests"
   },
   "native_type": "Issue",
   "native_state": "To Do",
   "assignedTo": {
      "name": "Xyz Abcd",
      "userName": "xyz.abcd@email.com",
      "id": "84c92fcd-e08b-6a5f-a8a6-ccda27055560",
      "email": "xyz.abcd@email.com"
   },
   "createdBy": {
      "name": "Xyz Abcd",
      "userName": "xyz.abcd@email.com",
      "id": "84c92fcd-e08b-6a5f-a8a6-ccda27055560",
      "email": "xyz.abcd@email.com"
   }
}" \
--user 'username':'password'

```

Success response:

```
{
   "result": {
      "status": "Success",
      "sysId: "533020eb879e85100f71cbfc0ebb3591"
   }
}
```

### Sample cURL request for test

```
curl "https://instance.service-now.com/api/sn_devops/devops/tool/test?toolId=8d4f56598702c510f894419d0ebb35aa&testType=junit" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "attemptNumber": 1,
   "blockedTests": 0,
   "buildNumber": 675,
   "duration": 0.079,
   "failedTests": 0,
   "finishTime": "2022-03-23T12:02:25.957Z",
   "name": "adoTests/DeployableRepo/Test #675-2982",
   "passedTests": 20,
   "pipelineName": "adoTests/DeployableRepo",
   "skippedTests": 0,
   "stageName": "Test",
   "startTime": "2022-03-23T12:02:24.36Z",
   "taskExecutionUrl": "https://dev.azure.com/xyzabcd/adoTests/_build/results?buildId=675#Test/{Job name}",
   "totalTests": 20,
   "url": "https://dev.azure.com/xyzabcd/adoTests/_TestManagement/Runs?runId=2982&_a=runCharts"
}" \
--user 'username':'password'

```

Success response:

```
{
   "result": {
      "status": "Success",
      "sysId: "fd3fdc6b879e85100f71cbfc0ebb356a"
   }
}
```

## DevOps - POST /devops/tool/event/\{sn\_tool\_id\}

Posts the passed in payload from GitHub, Jira, or Bitbucket to the Events \[sn\_devops\_event\] table for processing by a pre-built subflow.

Before calling this endpoint, you must create an integration with the tool you're using.

-   GitHub integration with DevOps
-   Jira integration with DevOps
-   Bitbucket integration with DevOps

To process events from any other tool besides GitHub, Jira, or Bitbucket, use the [DevOps - POST /devops/tool/\{capability\}](devops-api.md#) endpoint instead.

**Note:** Starting with 1.34.1 version, a new version of this API has been introduced. With this API, Adaptive Authentication policies may not execute as expected. For more information about these policies, see Adaptive authentication.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/tool/event/{sn_tool_id}`

Default URL: `/api/sn_devops/devops/tool/event/{sn_tool_id}`

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

sn\_tool\_id

</td><td>

Sys\_id of the tool to use for the request.Data type: String

Table: Devops Tools \[sn\_devops\_tool\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|Tool dependent|The tool determines the content of the payload. The payload can be located in the tool under the webhook information.|

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_zbt_c4y_1tb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Authorization

</td><td>

Starting with v2, this API supports token-based authentication. Tokens can be acquired by clicking the **Copy token** button on the tool record, located in the Tool \[sn\_devops\_tool\] table. The token can then be used in an authorization header in the format `Authorization: sn_devops.DevOpsToken <tool_sys_id>:<tool_token>`.

**Note:** If Basic Auth details \(user name and password\) are provided in addition to an authorization header with token, Basic Auth takes precedence.

If the **devops.system** user is not available in your instance, use the **Switch to this user after token based authentication is successful** property. This property enables setting any user that has the sn\_devops.integration role, which is needed to complete the token authentication. For information, see DevOps Change Velocity properties.

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
|201|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Invalid or missing authentication.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters

<table id="table_y5g_vhc_btb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Response status.Possible values:

-   `failure`: Incorrect tool ID. Event not created.
-   `success`: Event created in the Events \[sn\_devops\_event\] table. However, the event state may be **Error** if an incorrect payload was provided.

Data type: String

</td></tr></tbody>
</table>### cURL request

GitHub

```
curl "https://instance.service-now.com/api/sn_devops/devops/tool/event/46a07b2f471e011028c23a34846d43b2" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "ref": "refs/heads/master",
   "before": "59078a17cad1f4129754971c808d6c399b6141a5",
   "after": "b7957bab20835449c4d597fee24075a9a5a2c099",
   "repository": {
      "id": 252146476,
      "node_id": "MDEwOlJlcG9zaXRvcnkyNTIxNDY0NzY=",
      "name": "test",
      "full_name": "Xyz002/test",
      "private": false,
      "owner": {
         "name": "Xyz002",
         "email": "62993516+Xyz002@users.noreply.github.com",
         "login": "Xyz002",
         "id": 62993516,
         "node_id": "MDQ6VXNlcjYyOTkzNTE2",
         "avatar_url": "https://avatars.githubusercontent.com/u/62993516?v=4",
         "gravatar_id": "",
         "url": "https://api.github.com/users/Xyz002",
         "html_url": "https://github.com/Xyz002",
         "followers_url": "https://api.github.com/users/Xyz002/followers",
         "following_url": "https://api.github.com/users/Xyz002/following{/other_user}",
         "gists_url": "https://api.github.com/users/Xyz002/gists{/gist_id}",
         "starred_url": "https://api.github.com/users/Xyz002/starred{/owner}{/repo}",
         "subscriptions_url": "https://api.github.com/users/Xyz002/subscriptions",
         "organizations_url": "https://api.github.com/users/Xyz002/orgs",
         "repos_url": "https://api.github.com/users/Xyz002/repos",
         "events_url": "https://api.github.com/users/Xyz002/events{/privacy}",
         "received_events_url": "https://api.github.com/users/Xyz002/received_events",
         "type": "User",
         "site_admin": false
      },
      "html_url": "https://github.com/Xyz002/test",
      "description": null,
      "fork": false,
      "url": "https://github.com/Xyz002/test",
      "forks_url": "https://api.github.com/repos/Xyz002/test/forks",
      "keys_url": "https://api.github.com/repos/Xyz002/test/keys{/key_id}",
      "collaborators_url": "https://api.github.com/repos/Xyz002/test/collaborators{/collaborator}",
      "teams_url": "https://api.github.com/repos/Xyz002/test/teams",
      "hooks_url": "https://api.github.com/repos/Xyz002/test/hooks",
      "issue_events_url": "https://api.github.com/repos/Xyz002/test/issues/events{/number}",
      "events_url": "https://api.github.com/repos/Xyz002/test/events",
      "assignees_url": "https://api.github.com/repos/Xyz002/test/assignees{/user}",
      "branches_url": "https://api.github.com/repos/Xyz002/test/branches{/branch}",
      "tags_url": "https://api.github.com/repos/Xyz002/test/tags",
      "blobs_url": "https://api.github.com/repos/Xyz002/test/git/blobs{/sha}",
      "git_tags_url": "https://api.github.com/repos/Xyz002/test/git/tags{/sha}",
      "git_refs_url": "https://api.github.com/repos/Xyz002/test/git/refs{/sha}",
      "trees_url": "https://api.github.com/repos/Xyz002/test/git/trees{/sha}",
      "statuses_url": "https://api.github.com/repos/Xyz002/test/statuses/{sha}",
      "languages_url": "https://api.github.com/repos/Xyz002/test/languages",
      "stargazers_url": "https://api.github.com/repos/Xyz002/test/stargazers",
      "contributors_url": "https://api.github.com/repos/Xyz002/test/contributors",
      "subscribers_url": "https://api.github.com/repos/Xyz002/test/subscribers",
      "subscription_url": "https://api.github.com/repos/Xyz002/test/subscription",
      "commits_url": "https://api.github.com/repos/Xyz002/test/commits{/sha}",
      "git_commits_url": "https://api.github.com/repos/Xyz002/test/git/commits{/sha}",
      "comments_url": "https://api.github.com/repos/Xyz002/test/comments{/number}",
      "issue_comment_url": "https://api.github.com/repos/Xyz002/test/issues/comments{/number}",
      "contents_url": "https://api.github.com/repos/Xyz002/test/contents/{+path}",
      "compare_url": "https://api.github.com/repos/Xyz002/test/compare/{base}...{head}",
      "merges_url": "https://api.github.com/repos/Xyz002/test/merges",
      "archive_url": "https://api.github.com/repos/Xyz002/test/{archive_format}{/ref}",
      "downloads_url": "https://api.github.com/repos/Xyz002/test/downloads",
      "issues_url": "https://api.github.com/repos/Xyz002/test/issues{/number}",
      "pulls_url": "https://api.github.com/repos/Xyz002/test/pulls{/number}",
      "milestones_url": "https://api.github.com/repos/Xyz002/test/milestones{/number}",
      "notifications_url": "https://api.github.com/repos/Xyz002/test/notifications{?since,all,participating}",
      "labels_url": "https://api.github.com/repos/Xyz002/test/labels{/name}",
      "releases_url": "https://api.github.com/repos/Xyz002/test/releases{/id}",
      "deployments_url": "https://api.github.com/repos/Xyz002/test/deployments",
      "created_at": 1585737871,
      "updated_at": "2022-01-04T14:37:36Z",
      "pushed_at": 1648103939,
      "git_url": "git://github.com/Xyz002/test.git",
      "ssh_url": "git@github.com:Xyz002/test.git",
      "clone_url": "https://github.com/Xyz002/test.git",
      "svn_url": "https://github.com/Xyz002/test",
      "homepage": null,
      "size": 1378,
      "stargazers_count": 0,
      "watchers_count": 0,
      "language": "Java",
      "has_issues": true,
      "has_projects": true,
      "has_downloads": true,
      "has_wiki": true,
      "has_pages": false,
      "forks_count": 0,
      "mirror_url": null,
      "archived": false,
      "disabled": false,
      "open_issues_count": 2,
      "license": null,
      "allow_forking": true,
      "is_template": false,
      "topics": [],
      "visibility": "public",
      "forks": 0,
      "open_issues": 2,
      "watchers": 0,
      "default_branch": "master",
      "stargazers": 0,
      "master_branch": "master"
   },
   "pusher": {
      "name": "Xyz002",
      "email": "62993516+Xyz002@users.noreply.github.com"
   },
   "sender": {
      "login": "Xyz002",
      "id": 62993516,
      "node_id": "MDQ6VXNlcjYyOTkzNTE2",
      "avatar_url": "https://avatars.githubusercontent.com/u/62993516?v=4",
      "gravatar_id": "",
      "url": "https://api.github.com/users/Xyz002",
      "html_url": "https://github.com/Xyz002",
      "followers_url": "https://api.github.com/users/Xyz002/followers",
      "following_url": "https://api.github.com/users/Xyz002/following{/other_user}",
      "gists_url": "https://api.github.com/users/Xyz002/gists{/gist_id}",
      "starred_url": "https://api.github.com/users/Xyz002/starred{/owner}{/repo}",
      "subscriptions_url": "https://api.github.com/users/Xyz002/subscriptions",
      "organizations_url": "https://api.github.com/users/Xyz002/orgs",
      "repos_url": "https://api.github.com/users/Xyz002/repos",
      "events_url": "https://api.github.com/users/Xyz002/events{/privacy}",
      "received_events_url": "https://api.github.com/users/Xyz002/received_events",
      "type": "User",
      "site_admin": false
   },
   "created": false,
   "deleted": false,
   "forced": false,
   "base_ref": null,
   "compare": "https://github.com/Xyz002/test/compare/59078a17cad1...b7957bab2083",
   "commits": [
      {
         "id": "b7957bab20835449c4d597fee24075a9a5a2c099",
         "tree_id": "fa8d699762ec0a25868fa1ab4d299da392f0a974",
         "distinct": true,
         "message": "updated this file",
         "timestamp": "2022-03-24T12:08:59+05:30",
         "url": "https://github.com/Xyz002/test/commit/b7957bab20835449c4d597fee24075a9a5a2c099",
         "author": {
            "name": "Xyz002",
            "email": "62993516+Xyz002@users.noreply.github.com",
            "username": "Xyz002"
         },
         "committer": {
            "name": "GitHub",
            "email": "noreply@github.com",
            "username": "web-flow"
         },
         "added": [],
         "removed": [],
         "modified": [
            "README.me"
         ]
      }
   ],
   "head_commit": {
      "id": "b7957bab20835449c4d597fee24075a9a5a2c099",
      "tree_id": "fa8d699762ec0a25868fa1ab4d299da392f0a974",
      "distinct": true,
      "message": "updated this file",
      "timestamp": "2022-03-24T12:08:59+05:30",
      "url": "https://github.com/Xyz002/test/commit/b7957bab20835449c4d597fee24075a9a5a2c099",
      "author": {
         "name": "Xyz002",
         "email": "62993516+Xyz002@users.noreply.github.com",
         "username": "Xyz002"
      },
      "committer": {
         "name": "GitHub",
         "email": "noreply@github.com",
         "username": "web-flow"
      },
      "added": [],
      "removed": [],
      "modified": [
         "README.me"
      ]
   },
   "sn_tool_id": "46a07b2f471e011028c23a34846d43b2"
}" \
--user 'username':'password'

```

Success response:

```
{
   "result": "success"
}
```

### cURL request

Jira

```
curl "https://instance.service-now.com/api/sn_devops/devops/tool/event/9ed237af471e011028c23a34846d4327" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "timestamp": 1648104684180,
   "webhookEvent": "jira:issue_created",
   "issue_event_type_name": "issue_created",
   "user": {
      "self": "http://jira1.sndevops.xyz/rest/api/2/user?username=admin",
      "name": "admin",
      "key": "admin",
      "emailAddress": "username@email.com",
      "avatarUrls": {
         "48x48": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=48",
         "24x24": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=24",
         "16x16": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=16",
         "32x32": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=32"
      },
      "displayName": "Administrator",
      "active": true,
      "timeZone": "America/Los_Angeles"
   },
   "issue": {
      "id": "84800",
      "self": "http://jira1.sndevops.xyz/rest/api/2/issue/84800",
      "key": "BAL-2",
      "fields": {
         "issuetype": {
            "self": "http://jira1.sndevops.xyz/rest/api/2/issuetype/10002",
            "id": "10002",
            "description": "A task that needs to be done.",
            "iconUrl": "http://jira1.sndevops.xyz/secure/viewavatar?size=xsmall&avatarId=10318&avatarType=issuetype",
            "name": "Task",
            "subtask": false,
            "avatarId": 10318
         },
         "timespent": null,
         "project": {
            "self": "http://jira1.sndevops.xyz/rest/api/2/project/10507",
            "id": "10507",
            "key": "BAL",
            "name": "balu_devops",
            "projectTypeKey": "software",
            "avatarUrls": {
               "48x48": "http://jira1.sndevops.xyz/secure/projectavatar?avatarId=10324",
               "24x24": "http://jira1.sndevops.xyz/secure/projectavatar?size=small&avatarId=10324",
               "16x16": "http://jira1.sndevops.xyz/secure/projectavatar?size=xsmall&avatarId=10324",
               "32x32": "http://jira1.sndevops.xyz/secure/projectavatar?size=medium&avatarId=10324"
            }
         },
         "fixVersions": [],
         "aggregatetimespent": null,
         "resolution": null,
         "customfield_10302": null,
         "customfield_10105": null,
         "resolutiondate": null,
         "workratio": 0,
         "lastViewed": null,
         "watches": {
            "self": "http://jira1.sndevops.xyz/rest/api/2/issue/BAL-2/watchers",
            "watchCount": 0,
            "isWatching": false
         },
         "created": "2022-03-24T06:51:22.896+0000",
         "priority": {
            "self": "http://jira1.sndevops.xyz/rest/api/2/priority/3",
            "iconUrl": "http://jira1.sndevops.xyz/images/icons/priorities/medium.svg",
            "name": "Medium",
            "id": "3"
         },
         "customfield_10100": "0|i0cprw:",
         "customfield_10101": "SCRUMBOARD-14",
         "customfield_10300": null,
         "labels": [],
         "timeestimate": 240,
         "aggregatetimeoriginalestimate": 300,
         "versions": [],
         "issuelinks": [
            {
               "id": "10701",
               "self": "http://jira1.sndevops.xyz/rest/api/2/issueLink/10701",
               "type": {
                  "id": "10000",
                  "name": "Blocks",
                  "inward": "is blocked by",
                  "outward": "blocks",
                  "self": "http://jira1.sndevops.xyz/rest/api/2/issueLinkType/10000"
               },
               "outwardIssue": {
                  "id": "84741",
                  "key": "BAL-1",
                  "self": "http://jira1.sndevops.xyz/rest/api/2/issue/84741",
                  "fields": {
                     "summary": "log4jtesting",
                     "status": {
                        "self": "http://jira1.sndevops.xyz/rest/api/2/status/3",
                        "description": "This issue is being actively worked on at the moment by the assignee.",
                        "iconUrl": "http://jira1.sndevops.xyz/images/icons/statuses/inprogress.png",
                        "name": "In Progress",
                        "id": "3",
                        "statusCategory": {
                           "self": "http://jira1.sndevops.xyz/rest/api/2/statuscategory/4",
                           "id": 4,
                           "key": "indeterminate",
                           "colorName": "yellow",
                           "name": "In Progress"
                        }
                     },
                     "priority": {
                        "self": "http://jira1.sndevops.xyz/rest/api/2/priority/3",
                        "iconUrl": "http://jira1.sndevops.xyz/images/icons/priorities/medium.svg",
                        "name": "Medium",
                        "id": "3"
                     },
                     "issuetype": {
                        "self": "http://jira1.sndevops.xyz/rest/api/2/issuetype/10004",
                        "id": "10004",
                        "description": "A problem which impairs or prevents the functions of the product.",
                        "iconUrl": "http://jira1.sndevops.xyz/secure/viewavatar?size=xsmall&avatarId=10303&avatarType=issuetype",
                        "name": "Bug",
                        "subtask": false,
                        "avatarId": 10303
                     }
                  }
               }
            }
         ],
         "assignee": {
            "self": "http://jira1.sndevops.xyz/rest/api/2/user?username=admin",
            "name": "admin",
            "key": "admin",
            "emailAddress": "username@email.com",
            "avatarUrls": {
               "48x48": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=48",
               "24x24": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=24",
               "16x16": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=16",
               "32x32": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=32"
            },
            "displayName": "Administrator",
            "active": true,
            "timeZone": "America/Los_Angeles"
         },
         "updated": "2022-03-24T06:51:22.896+0000",
         "status": {
            "self": "http://jira1.sndevops.xyz/rest/api/2/status/10000",
            "description": "",
            "iconUrl": "http://jira1.sndevops.xyz/",
            "name": "To Do",
            "id": "10000",
            "statusCategory": {
               "self": "http://jira1.sndevops.xyz/rest/api/2/statuscategory/2",
               "id": 2,
               "key": "new",
               "colorName": "blue-gray",
               "name": "To Do"
            }
         },
         "components": [],
         "timeoriginalestimate": 300,
         "description": "Task description",
         "timetracking": {
            "originalEstimate": "5m",
            "remainingEstimate": "4m",
            "originalEstimateSeconds": 300,
            "remainingEstimateSeconds": 240
         },
         "customfield_10203": null,
         "customfield_10204": null,
         "customfield_10205": null,
         "attachment": [],
         "aggregatetimeestimate": 240,
         "summary": "Task Summary",
         "creator": {
            "self": "http://jira1.sndevops.xyz/rest/api/2/user?username=admin",
            "name": "admin",
            "key": "admin",
            "emailAddress": "username@email.com",
            "avatarUrls": {
               "48x48": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=48",
               "24x24": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=24",
               "16x16": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=16",
               "32x32": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=32"
            },
            "displayName": "Administrator",
            "active": true,
            "timeZone": "America/Los_Angeles"
         },
         "subtasks": [],
         "reporter": {
            "self": "http://jira1.sndevops.xyz/rest/api/2/user?username=admin",
            "name": "admin",
            "key": "admin",
            "emailAddress": "username@email.com",
            "avatarUrls": {
               "48x48": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=48",
               "24x24": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=24",
               "16x16": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=16",
               "32x32": "https://www.gravatar.com/avatar/eccd6ec2c978f1f1d4a1fed4e81265eb?d=mm&s=32"
            },
            "displayName": "Administrator",
            "active": true,
            "timeZone": "America/Los_Angeles"
         },
         "customfield_10000": "{summaryBean=com.atlassian.jira.plugin.devstatus.rest.SummaryBean@2ccf8c6[summary={pullrequest=com.atlassian.jira.plugin.devstatus.rest.SummaryItemBean@fbc42d4[overall=PullRequestOverallBean{stateCount=0, state='OPEN', details=PullRequestOverallDetails{openCount=0, mergedCount=0, declinedCount=0}},byInstanceType={}], build=com.atlassian.jira.plugin.devstatus.rest.SummaryItemBean@71e33347[overall=com.atlassian.jira.plugin.devstatus.summary.beans.BuildOverallBean@1c24654d[failedBuildCount=0,successfulBuildCount=0,unknownBuildCount=0,count=0,lastUpdated=<null>,lastUpdatedTimestamp=<null>],byInstanceType={}], review=com.atlassian.jira.plugin.devstatus.rest.SummaryItemBean@1ea8fb17[overall=com.atlassian.jira.plugin.devstatus.summary.beans.ReviewsOverallBean@6dc95939[stateCount=0,state=<null>,dueDate=<null>,overDue=false,count=0,lastUpdated=<null>,lastUpdatedTimestamp=<null>],byInstanceType={}], deployment-environment=com.atlassian.jira.plugin.devstatus.rest.SummaryItemBean@55826cc[overall=com.atlassian.jira.plugin.devstatus.summary.beans.DeploymentOverallBean@3ae93527[topEnvironments=[],showProjects=false,successfulCount=0,count=0,lastUpdated=<null>,lastUpdatedTimestamp=<null>],byInstanceType={}], repository=com.atlassian.jira.plugin.devstatus.rest.SummaryItemBean@6340012e[overall=com.atlassian.jira.plugin.devstatus.summary.beans.CommitOverallBean@44678cee[count=0,lastUpdated=<null>,lastUpdatedTimestamp=<null>],byInstanceType={}], branch=com.atlassian.jira.plugin.devstatus.rest.SummaryItemBean@4dbce8[overall=com.atlassian.jira.plugin.devstatus.summary.beans.BranchOverallBean@737ee1cb[count=0,lastUpdated=<null>,lastUpdatedTimestamp=<null>],byInstanceType={}]},errors=[],configErrors=[]], devSummaryJson={\"cachedValue\":{\"errors\":[],\"configErrors\":[],\"summary\":{\"pullrequest\":{\"overall\":{\"count\":0,\"lastUpdated\":null,\"stateCount\":0,\"state\":\"OPEN\",\"details\":{\"openCount\":0,\"mergedCount\":0,\"declinedCount\":0,\"total\":0},\"open\":true},\"byInstanceType\":{}},\"build\":{\"overall\":{\"count\":0,\"lastUpdated\":null,\"failedBuildCount\":0,\"successfulBuildCount\":0,\"unknownBuildCount\":0},\"byInstanceType\":{}},\"review\":{\"overall\":{\"count\":0,\"lastUpdated\":null,\"stateCount\":0,\"state\":null,\"dueDate\":null,\"overDue\":false,\"completed\":false},\"byInstanceType\":{}},\"deployment-environment\":{\"overall\":{\"count\":0,\"lastUpdated\":null,\"topEnvironments\":[],\"showProjects\":false,\"successfulCount\":0},\"byInstanceType\":{}},\"repository\":{\"overall\":{\"count\":0,\"lastUpdated\":null},\"byInstanceType\":{}},\"branch\":{\"overall\":{\"count\":0,\"lastUpdated\":null},\"byInstanceType\":{}}}},\"isStale\":false}}",
         "aggregateprogress": {
            "progress": 0,
            "total": 240,
            "percent": 0
         },
         "customfield_10200": null,
         "customfield_10201": null,
         "customfield_10202": null,
         "environment": null,
         "duedate": "2022-03-24",
         "progress": {
            "progress": 0,
            "total": 240,
            "percent": 0
         },
         "comment": {
            "comments": [],
            "maxResults": 0,
            "total": 0,
            "startAt": 0
         },
         "votes": {
            "self": "http://jira1.sndevops.xyz/rest/api/2/issue/BAL-2/votes",
            "votes": 0,
            "hasVoted": false
         },
         "worklog": {
            "startAt": 0,
            "maxResults": 20,
            "total": 0,
            "worklogs": []
         }
      }
   },
   "changelog": {
      "id": "14401",
      "items": [
         {
            "field": "Link",
            "fieldtype": "jira",
            "from": null,
            "fromString": null,
            "to": "BAL-1",
            "toString": "This issue blocks BAL-1"
         }
      ]
   },
   "sn_tool_id": "9ed237af471e011028c23a34846d4327"
}" \
--user 'username':'password'

```

Success response:

```
{
   "result": "success"
}
```

### cURL request

Bitbucket

```
curl "https://instance.service-now.com/api/sn_devops/devops/tool/event/6975ecaf879e85100f71cbfc0ebb3575" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "eventKey": "repo:refs_changed",
   "date": "2022-03-23T15:57:05+0000",
   "actor": {
      "name": "admin",
      "emailAddress": "username@email.com",
      "id": 1,
      "displayName": "Admin",
      "active": true,
      "slug": "admin",
      "type": "NORMAL",
      "links": {
         "self": [
            {
               "href": "http://bitbucket2.sndevops.xyz/users/admin"
            }
         ]
      }
   },
   "repository": {
      "slug": "testautomationrepo1",
      "id": 12,
      "name": "TestAutomationRepo1",
      "scmId": "git",
      "state": "AVAILABLE",
      "statusMessage": "Available",
      "forkable": true,
      "origin": {
         "slug": "testautomationrepo1",
         "id": 1,
         "name": "TestAutomationRepo1",
         "scmId": "git",
         "state": "AVAILABLE",
         "statusMessage": "Available",
         "forkable": true,
         "project": {
            "key": "TES",
            "id": 1,
            "name": "TestAutomation",
            "public": false,
            "type": "NORMAL",
            "links": {
               "self": [
                  {
                     "href": "http://bitbucket2.sndevops.xyz/projects/TES"
                  }
               ]
            }
         },
         "public": false,
         "links": {
            "clone": [
               {
                  "href": "ssh://git@bitbucket2.sndevops.xyz:7999/tes/testautomationrepo1.git",
                  "name": "ssh"
               },
               {
                  "href": "http://bitbucket2.sndevops.xyz/scm/tes/testautomationrepo1.git",
                  "name": "http"
               }
            ],
            "self": [
               {
                  "href": "http://bitbucket2.sndevops.xyz/projects/TES/repos/testautomationrepo1/browse"
               }
            ]
         }
      },
      "project": {
         "key": "~ADMIN",
         "id": 3,
         "name": "Admin",
         "type": "PERSONAL",
         "owner": {
            "name": "admin",
            "emailAddress": "username@email.com",
            "id": 1,
            "displayName": "Admin",
            "active": true,
            "slug": "admin",
            "type": "NORMAL",
            "links": {
               "self": [
                  {
                     "href": "http://bitbucket2.sndevops.xyz/users/admin"
                  }
               ]
            }
         },
         "links": {
            "self": [
               {
                  "href": "http://bitbucket2.sndevops.xyz/users/admin"
               }
            ]
         }
      },
      "public": false,
      "links": {
         "clone": [
            {
               "href": "http://bitbucket2.sndevops.xyz/scm/~admin/testautomationrepo1.git",
               "name": "http"
            },
            {
               "href": "ssh://git@bitbucket2.sndevops.xyz:7999/~admin/testautomationrepo1.git",
               "name": "ssh"
            }
         ],
         "self": [
            {
               "href": "http://bitbucket2.sndevops.xyz/users/admin/repos/testautomationrepo1/browse"
            }
         ]
      }
   },
   "changes": [
      {
         "ref": {
            "id": "refs/heads/master",
            "displayId": "master",
            "type": "BRANCH"
         },
         "refId": "refs/heads/master",
         "fromHash": "b482b2e232f5fbdee73feed8ca1cfb774de6976e",
         "toHash": "d783254fe6f77bc7cc079358158aeef52a457587",
         "type": "UPDATE"
      }
   ],
   "sn_tool_id": "6975ecaf879e85100f71cbfc0ebb3575"
}" \
--user 'username':'password'

```

Success response:

```
{
   "result": "success"
}
```

## DevOps - PUT /devops/orchestration/changeControl/\{changeControlId\}

Updates the change control information for the specified orchestration task.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/orchestration/changeControl/{changeControlId}`

Default URL: `/api/sn_devops/devops/orchestration/changeControl/{changeControlId}`

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

changeControlId

</td><td>

Sys\_id of the change control task. Located in the Callback \[sn\_devops\_callback\] table. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

toolId

</td><td>

Required. Sys\_id of the DevOps tool associated with the change control task.Data type: String

Table: Orchestration Tool \[sn\_devops\_orchestration\_tool\]

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-orch-callBackURL-devops"><td>

callbackURL

</td><td>

Required. URL that the ServiceNow instance can call back once the associated change request approval process is complete. This callback should let the pipeline execution continue or not, based on the approval result. Data type: String

</td></tr><tr><td>

orchestrationTaskDetails

</td><td>

Required. Description of the orchestration task. Data type: Object

 ```
"orchestrationTaskDetails": {
  "message": "String",
  "triggerType": "String",
  "upstreamTaskExecutionURL": "String"
}
```

</td></tr><tr id="row-orch-orchestrationTaskDetails-message-devops"><td>

orchestrationTaskDetails.message

</td><td>

Free-form text message. Data type: String

</td></tr><tr id="row-orch-orchestrationTaskDetails-triggerType-devops"><td>

orchestrationTaskDetails.triggerType

</td><td>

Required. The way the orchestration task was started. Valid values:

-   scm: Git/scm tool code commit triggered the job.
-   upstream: Upstream job triggered this job.
-   user: User manually started the job.

Data type: String

</td></tr><tr id="row-orch-orchestrationTaskDetails-upstreamTaskExecutionURL-devops"><td>

orchestrationTaskDetails.upstreamTaskExecutionURL

</td><td>

Required if **triggerType** is set to `upstream`. Upstream task execution URL. For example: https://jenkins.mycompany.com:8080/job/Mobile-Platform-test/40/

Data type: String

</td></tr><tr id="row-orch-orchestrationTaskURL-devops"><td>

orchestrationTaskURL

</td><td>

Required. URL of the orchestration task. For example: https://jenkins.mycompany.com:8080/orchestration\_task/Mobile-Platform-deploy/

Data type: String

</td></tr><tr><td>

toolType

</td><td>

Type of DevOps tool.Valid value: jenkins

 Data type: String

</td></tr><tr><td>

taskExecutionURL

</td><td>

Required. URL of the task to execute.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr id="accept-row-RESTAPI"><td>

Accept

</td><td>

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Authorization

</td><td>

Starting with v2, this API supports token-based authentication. Tokens can be acquired by clicking the **Copy token** button on the tool record, located in the Tool \[sn\_devops\_tool\] table. The token can then be used in an authorization header in the format `Authorization: sn_devops.DevOpsToken <tool_sys_id>:<tool_token>`.

**Note:** If Basic Auth details \(user name and password\) are provided in addition to an authorization header with token, Basic Auth takes precedence.

If the **devops.system** user is not available in your instance, use the **Switch to this user after token based authentication is successful** property. This property enables setting any user that has the sn\_devops.integration role, which is needed to complete the token authentication. For information, see DevOps Change Velocity properties.

</td></tr><tr id="content_type-row-RESTAPI"><td>

Content-Type

</td><td>

Data format of the request body. Only supports **application/json**.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Invalid or missing authentication.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

change\_control

</td><td>

Flag that indicates whether the orchestration task is under change control. Possible values:

-   true: Under change control.
-   false: Not under change control.

Data type: Boolean

</td></tr><tr><td>

details

</td><td>

Entry for all error conditions. Data type: Object

```
"details": {
  "errors": [Array]
}
```

</td></tr><tr><td>

details.errors

</td><td>

Description of a single error. Data type: Array of Objects

```
"errors": [
  {
    "message": "String"
  }
]
```

</td></tr><tr><td>

details.errors.message

</td><td>

Detailed error message. Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl -X PUT "https://instance.service-now.com/api/sn_devops/v1/devops/orchestration/changeControl/f0ca45679323008b52f3b457415ae6?toolId=f0ca45679323008b52f3b457415ae6"
-H "accept: application/json"\
-H "Content-Type: application/json"\
-u "username":"password"\
-d "{
  \"orchestrationTaskURL\":\"https://jenkins.mycompany.com:8080/job/Mobile-Platform-deploy/\",
  \"toolType\":\"jenkins\",
  \"callbackURL\":\"https://jenkins.mycompany.com:8080/sn-devops/964aca59-0cae-4d9b-a36d-5929f426cf31\",
\"taskExecutionURL\":\"https://jenkins.mycompany.com:8080/job/Mobile-Platform-test/40/\",  
"\orchestrationTaskName\":\"StageName\",
  \"orchestrationTaskDetails\":{
    \"message\":\"Started by upstream project \\\"Mobile-Platform-test\\\" build number 40\",
    \"triggerType\":\"upstream\",
    \"upstreamTaskExecutionURL\":\"https://jenkins.mycompany.com:8080/job/Mobile-Platform-test/40/\"}
}"
```

Response:

```
{
    "result": {
        "change_control": true
    }
}
```

## DevOps - PUT /devops/orchestration/changeInfo/\{changeInfo\}

Updates fields in a specified change request.

### URL format

Versioned URL: `/api/sn_devops/{api_version}/devops/orchestration/changeInfo/{changeInfo}`

Default URL: `/api/sn_devops/devops/orchestration/changeInfo/{changeInfo}`

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

changeRequestNumber

</td><td>

Required. Change request number associated with the orchestration task to update.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Required. Name-value pairs for the field\(s\) to update in the associated change request. For example, to update the short description file, enter a name-value pair similar to the following:

```
 "{\"short_description\": \"my short desc\" }"
```

For the **state** parameter, only the following transitions are supported:-   cancel:
    -   Change request state must be implemented to move the state to cancel.
    -   The **reason** parameter is a mandatory input to update the state to canceled.
-   closed:
    -   Change request state must be implement or post implement to move the state to close.
    -   close\_code and close\_notes are mandatory input for updating the state to closed.

Possible values:

        -   4: Cancel \(Value set in the sn\_devops.change\_request.cancel\_state property.\)
        -   3: Closed \(Value set in the sn\_devops.change\_request.closed\_state property.\)

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

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Authorization

</td><td>

Starting with v2, this API supports token-based authentication. Tokens can be acquired by clicking the **Copy token** button on the tool record, located in the Tool \[sn\_devops\_tool\] table. The token can then be used in an authorization header in the format `Authorization: sn_devops.DevOpsToken <tool_sys_id>:<tool_token>`.

**Note:** If Basic Auth details \(user name and password\) are provided in addition to an authorization header with token, Basic Auth takes precedence.

If the **devops.system** user is not available in your instance, use the **Switch to this user after token based authentication is successful** property. This property enables setting any user that has the sn\_devops.integration role, which is needed to complete the token authentication. For information, see DevOps Change Velocity properties.

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
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Description of the results of the update.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the request.Possible values:

-   Success: Change request was found and change details were updated successfully.
-   Error: Change request was not found and change details were not updated.

 Data type: String

</td></tr><tr><td>

updateStatus

</td><td>

Status of the update.Possible values:

-   Done
-   Error

 Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to update various fields in the CHG0030023 change request.

```
curl -X PUT"
https://instance.servicenow.com/api/sn_devops/v1/devops/orchestration/changeInfo?changeRequestNumber=CHG0030023

-H "accept: application/json"\
-u "username":"password" 
- D
{
  "short_description": "Test description",
  "priority": "1",
  "start_date": "2021-02-05 08:00:00",
  "end_date": "2022-04-05 08:00:00",
  "justification": "test justification",
  "description": "test description",
  "cab_required": true,
  "comments": "This update for work notes is from jenkins file",
  "work_notes": "test work notes",
  "assignment_group": "a715cd759f2002002920bde8132e7018"
}
```

Response:

```
{
  "result": {
    "updateStatus": "Done",
    "status": "Success",
    "message": "change request update successful"
  }
}
```

