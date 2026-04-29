---
title: Creating DevOps subflows
description: For user-created integrations, create a DevOps Workflow Studio subflow to collect and transform data from the tool you are integrating.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [User created, Integrate, DevOps Change Velocity, IT Service Management]
---

# Creating DevOps subflows

For user-created integrations, create a DevOps Workflow Studio subflow to collect and transform data from the tool you are integrating.

ServiceNow [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=australia&pubname=australia-application-development&ft:locale=en-US) is a ServiceNow AI Platform feature your integration developer can use to automate processes using a sequence of actions. Trigger conditions start the flow, and variables pass information between actions.

See [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=australia&pubname=australia-application-development&ft:locale=en-US) [Subflows](https://www.servicenow.com/docs/access?context=subflows&version=australia&pubname=australia-build-workflows&ft:locale=en-US) for information on how to create a subflow.

## Notification capability subflow

<table id="table_hbx_dn1_1kb"><thead><tr><th>

Item

</th><th>

Expected value

</th></tr></thead><tbody><tr><td>

Inputs

</td><td>

Label: current

 Type: Reference.Inbound Event

</td></tr><tr><td>

Outputs

</td><td>

N/A

</td></tr></tbody>
</table>Transform the original payload, and save the final payload in the **transformed\_payload** field.

-   **Expected standard JSON Notification capability payload - Planning tool**

    **Note:** The version attribute in the JSON payload is optional. Even if you do not provide the version attribute, the payload is processed successfully.

    ```
    {
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
    // The Version attribute is optional
      "version": {
          "id": "REL1234",
          "shortDescription": "APIs Release",
          "createdDateTime": "1970-01-01T08:15:30-05:00",
          "app": {
              "id": "PRODUCT1234",
              "shortDescription": "Mobile UI",
              "createdDateTime": "1970-01-01T08:15:30-05:00",
              "url": "https://jira.com/mycompany/browse/PRODUCT-125"
            },
          "url": "https://jira.com/mycompany/browse/REL-125"
        },
      "app": {
          "id": "PRODUCT1234",
          "shortDescription": "Mobile UI",
          "createdDateTime": "1970-01-01T08:15:30-05:00",
          "url": "https://jira.com/mycompany/browse/PRODUCT-125"
        },
      "url": "https://jira.com/mycompany/browse/HALOKEY-25"
    }
    ```

-   **Expected standard JSON Notification capability payload - Coding tool**

    ```
    {
      "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
      "url": "https://github.com/mycompany/mobileplatform/commit/3fa85f6457174562b3fc2c963f66afa6",
      "committedDate": "1970-01-01T08:15:30-05:00",
      "repository": {
        "name": "Platform-Mobile",
        "url": "https://github.com/mycompany/mobileplatform"
      },
     "branch": {
        "name": "master",
        "path": "refs/heads/master"
      },
      "committer": {
        "email": "lenn@smithworksinc.com"
      },
      "details": [
        {
          "additions": 0,
          "deletions": 0,
          "totalChanges": 0,
          "file": "src/test/java/com/mycompany/app/App.java",
          "action": "modified",
          "changes": "%40%40%20-30%2C6%20%2B30%2C18%20%40%40%20public%20void%20testAppConstructor%28%29%20%7B%0A%20%20%20%20%20%20%20%20%20%7D%0A%20%20%20%20%20%7D%0A%20%0A%2B%20%20%20%20%40Test%0A%2B%20%20%20%20public%20void%20testDatabase%28%29%0A%2B%20%20%20%20%7B%0A%2B%09%2F%2FThis%20is%20a%20test%20function%0A%2B%20%20%20%20%20%20%20%20App.main%28null%29%3B%0A%2B%20%20%20%20%20%20%20%20try%20%7B%0A%2B%20%20%20%20%20%20%20%20%20%20%20%20assertEquals%28%22Hello%20World%21%22%20%2B%20System.getProperty%28%22line.separator%22%29%2C%20outContent.toString%28%29%29%3B%0A%2B%20%20%20%20%20%20%20%20%7D%20catch%20%28AssertionError%20e%29%20%7B%0A%2B%20%20%20%20%20%20%20%20%20%20%20%20fail%28%22%22message%22%20is%20not%20%22Hello%20World%21%22%22%29%3B%0A%2B%20%20%20%20%20%20%20%20%7D%0A%2B%20%20%20%20%7D%0A%2B%0A%20%20%20%20%20%40Test%0A%20%20%20%20%20public%20void%20testAppMain%28%29%0A%20%20%20%20%20%7B"
        }
      ]
    }
     
    ```

-   **Expected standard JSON Notification capability payload - Orchestration tool**

    ```
    {
      "toolId": "bc1d9454dbdb0810ae77f3c61d9619d1",
      "buildNumber": "100",
      "nativeId": "HILR/Prod #100",
      "name": "HILR/Prod",
      "id": "HILR/Prod #100",
      "url": "https://dev.azure.com/lenn/CorpSite-ADO/_build/results?buildId=100#Prod/",
      "isMultiBranch": "false",
      "orchestrationTaskUrl": "https://dev.azure.com/lenn/CorpSite-ADO/_build?name=HILR#Prod",
      "orchestrationTaskName": "CorpSite-ADO/HILR#Prod",
      "upstreamTaskUrl": "https://dev.azure.com/lenn/CorpSite-ADO/_build/results?buildId=100#UAT/",
      "upstreamId": "CorpSite-ADO/HILR#UAT",
      "result": "building",
      "startDateTime": "2020-03-20 22:59:27"
    }
    
    ```

-   **Expected standard JSON Notification capability payload - Test tool**

    Functional:

    ```
    { 
    "name": "CorpSite-selenium#55", 
    "duration": 78.802, 
    "passedTests": 4, 
    "failedTests": 0, 
    "skippedTests": 0, 
    "blockedTests": 0, 
    "totalTests": 4, 
    "startTime": "2020-06-30T18:12:31Z", 
    "finishTime": "2020-06-30T18:12:31Z", 
    "passingPercent": 100, 
     
     
    // Use Artifact OR Package OR Build + Stage + PipelineName Attributes 
    "packages": [{"name": "CorpSite-pkg1"}], 
    "artifacts": [{"name": "CorpSite-artifact", "version": "1.0.0"}], 
    "buildNumber": "55", 
    "stageName": "test", 
    "pipelineName": "CorpSite-selenium", 
    } 
    
    ```

    Performance:

    ```
    { 
    "name": "Performance Tests", 
    "url": "http://abc.com", 
    "startTime": "2020-06-30T18:12:31Z", 
    "finishTime": "2020-06-30T18:12:31Z", 
    "duration": 78.802, 
    "maximumVirtualUsers": "", 
    "throughput": "", 
    "maximumTime": "", 
    "minimumTime": "", 
    "averageTime": "", 
    "ninetyPercent": "", 
    "standardDeviation": "", 
     
    // Use Artifact OR Package OR Build + Stage + PipelineName Attributes 
    "packages": [{"name": "CorpSite-pkg1"}], 
    "artifacts": [{"name": "CorpSite-artifact", "version": "1.0.0"}], 
    "buildNumber": "55", 
    "stageName": "test", 
    "pipelineName": "CorpSite-Performance", 
    } 
    
    ```

-   **Expected standard JSON Notification capability payload - Artifact tool**

    Pipelines:

    ```
    {
      "artifacts": [
        {
          "name": "acm.jar",
          "version": "1.82",
          "semanticVersion": "1.82.0",
          "repositoryName": "acm-repo"
        }
      ],
      "pipelineName": "testMultiBranch/master",
      "taskExecutionNumber": "82",
      "stageName": "buildmbmaster",
      "branchName": "master"
    }
    
    ```

    Jenkins Freestyle/Maven Project:

    ```
    {
      "artifacts": [
        {
          "name": "mav1.jar",
          "version": "1.11",
          "semanticVersion": "1.11.0",
          "repositoryName": "mav-repo"
        }
      ],
      "projectName": "maven-test-proj",
      "taskExecutionNumber": "11"
    }
    
    ```


![DevOps Notification Coding Tool Flow](../image/dev-ops-notification-coding-flow.png "DevOps Notification capability flow diagram example - Coding tool")

## Connect capability subflow

The Connect capability is supported.

<table id="table_xys_nm1_1kb"><thead><tr><th>

Item

</th><th>

Expected value

</th></tr></thead><tbody><tr><td>

Inputs

</td><td>

Label: current

 Type: Reference.DevOps Tool

 Tool record for which the **Connect** button action is clicked.

</td></tr><tr><td>

Outputs

 See [subflow outputs](https://www.servicenow.com/docs/access?context=subflows&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td><td>

-   Label: connected

Flag indicating the success or failure of the connection made to the target tool \(true/false\).

-   Label: errormessage

String message displayed on the form for connection failure. The variable is an empty string if the connection is successful.


</td></tr></tbody>
</table>Connect errors shown on the DevOps tool form:

-   **Connection failed**

    Subflow was executed successfully but the connection could not be made.

-   **Error: Failed to get failure details from the tool specific connect flow**

    Subflow execution failed for an unknown reason.

-   **Error updating the tool connect status**

    The connection\_state attribute could not be updated for an unknown reason.


![DevOps Connect Orchestration Tool](../image/dev-ops-connect-orch-flow.png "DevOps Connect capability flow diagram example - Orchestration tool")

## Discover capability subflow

The Discover capability is supported.

<table id="table_acq_yj1_1kb"><thead><tr><th>

Item

</th><th>

Expected value

</th></tr></thead><tbody><tr><td>

Inputs

</td><td>

Label: current

 Type: Reference.DevOps Tool

</td></tr><tr><td>

Outputs

 See [subflow outputs](https://www.servicenow.com/docs/access?context=subflows&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td><td>

Without pagination:

 Label: discoverpayload

 Type: Array of objects as JSON string.

 `(JSON.stringify([{},{}]))`

 Planning tool without pagination:

 ```
[
{
   "id":"REL1234567",
   "name": "REL NUMBERS",
   "url":"https://jira.com/vult/browse/REL1234567",
   "nativeId": "1790e6cc-085b-4529-9cb8-47f393182226"
},
{
   "id":"TOR67",
   "name": "TOR 67",
   "url":"https://jira.com/welp/browse/TOR67",
   "nativeId": "482ce864-085b-4529-9cb8-47f393767eb2"
}
]
```

 Coding tool without pagination:

```
[
  {
      "name": "nvm_repo",
      "url": "https://github.com/nvm_repo/"
  },
  {
      "name": "golang_util",
      "url": "https://github.com/golang_util/"
  }
];
```

 Orchestration tool without pagination:

```
{
  "orchestrationTasks": [
    {
      "name": "Build_APC_1",
      "url": "https://jenkins.wsf.xyz/job/Build_APC_1",
      "projectName": "Build_APC_1"
    },
    {
      "name": "CI_CD_Jenkins",
      "url": "https://pt1.jenkins.com/job/CI_CD_Jenkins",
      "projectName": "CI_CD_Jenkins"
    },
    {
      "name": "CI_deploy",
      "url": "https://pt2.jenkins.com/job/CI_deploy",
      "projectName": "CI_deploy"
    }
  ],
  "pipelines": [
    {
      "name": "Build_APC_1",
      "url": "https://jenkins.wsf.xyz/job/Build_APC_1",
      "projectName": "Build_APC_1"
    },
    {
      "name": "CI_CD_Jenkins",
      "url": "https://pt1.jenkins.com/job/CI_CD_Jenkins",
      "projectName": "CI_CD_Jenkins"
    },
    {
      "name": "CI_deploy",
      "url": "https://pt2.jenkins.com/job/CI_deploy",
      "projectName": "CI_deploy"
    }
  ]
}
```

 With pagination:

 Label: discoverpayload

 Type: Array of objects as JSON string.

 `(JSON.stringify([{},{}]))`

 Sample JSON format:

 ```
"pageInfo" : {
    "isLastPage" : true, 
    "discoverPayload" : {},
    “pageDetails” : {}
}
```

 Planning tool with pagination:

```
{               
    "pageInfo": {
        "isLastPage": false,
        "discoverPayload": [
            {
               "id":"REL1234567",
               "name": "REL NUMBERS",
        "url":"https://jira.com/vult/browse/REL1234567",
               "nativeId": "1790e6cc-085b-4529-9cb8-47f393182226"
            },
            {
               "id":"TOR67",
               "name": "TOR 67",
               "url":"https://jira.com/welp/browse/TOR67",
               "nativeId": "482ce864-085b-4529-9cb8-47f393767eb2"
            }
            ],
        "pageDetails": {
            "curPage" : 1,
            "nextPage": 2
        }
    }
}
```

 Coding tool with pagination:

```
{
    "pageInfo": {
        "isLastPage": false,
        "discoverPayload": [
            {
                "name": "nvm_repo",
                "url": "https://github.com/nvm_repo/"
            },
            {
                "name": "golang_util",
                "url": "https://github.com/golang_util/"
            }
        ],
        "pageDetails": {
            "curPage" : 1,
            "nextPage": 2
        }
    }
}
```

 Orchestration tool with pagination:

```
{ 
    "pageInfo": { 
        "isLastPage": false, 
        "discoverPayload": { 
            "orchestrationTasks": [ 
              { 
                "name": "Build_APC_1", 
                "url": "https://jenkins.wsf.xyz/job/Build_APC_1", 
                "projectName": "Build_APC_1" 
              }, 
              { 
                "name": "CI_CD_Jenkins", 
                "url": "https://pt1.jenkins.com/job/CI_CD_Jenkins", 
                "projectName": "CI_CD_Jenkins" 
              } 
            ], 
            "pipelines": [ 
              { 
                "name": "Build_APC_1", 
                "url": "https://jenkins.wsf.xyz/job/Build_APC_1", 
                "projectName": "Build_APC_1" 
              } 
            ] 
          }, 
        "pageDetails": { 
            "curPage" : 1, 
            "nextPage": 2 
        } 
    } 
} 
```

</td></tr></tbody>
</table>The Discover main flow is triggered during import request record creation. An import request has these states and messages.

<table id="table_pjc_x5t_jkb"><thead><tr><th>

State

</th><th>

Message

</th></tr></thead><tbody><tr><td>

Requested

</td><td>

--

</td></tr><tr><td>

Processing

</td><td>

--

</td></tr><tr><td>

Completed

</td><td>

Updated &lt;number&gt; object\(s\)

 Found &lt;number&gt; objects with invalid toolId

 Found &lt;number&gt; objects failed validation

</td></tr><tr><td>

Error

</td><td>

-   Unable to parse payload string from Subflow
-   discoverpayload is expected to be an array of objects
-   ImportRequest record does not have reference to tool table

</td></tr><tr><td>

Paused

</td><td>

--

</td></tr><tr><td>

Canceled

</td><td>

--

</td></tr><tr><td>

Unmatched

</td><td>

--

</td></tr></tbody>
</table>![DevOps Discover Plan Tool Flow](../image/dev-ops-discover-planning-flow.png "DevOps Discover capability flow diagram example - Planning tool")

![Flow diagram of a typical discover flow with pagination support](../image/dev-ops-user-integrations-pagination.png "DevOps Discover capability with pagination support flow diagram")

## Update Import Request Workflow Studio action

You can use the Update Import Request action in your Discover subflow to modify the Import Request record state, if desired.

<table id="table_ncn_xs1_1kb"><thead><tr><th>

Input label

</th><th>

Type

</th></tr></thead><tbody><tr><td>

current

</td><td>

Reference.Import Request

</td></tr><tr><td>

state

</td><td>

\(String\)-   requested
-   processing

**Note:** Flow execution is stopped \(once the return is received from the subflow\) when the state is set to processing.

-   completed
-   error
-   paused
-   canceled
-   unmatched

</td></tr><tr><td>

details

</td><td>

\(String\)

</td></tr></tbody>
</table>**Parent Topic:**[User-created integrations in DevOps Change Velocity](dev-ops-tool-integration.md)

