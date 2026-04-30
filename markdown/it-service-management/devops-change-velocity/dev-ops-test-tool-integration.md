---
title: DevOps test tool integration
description: Test tool integration lets you view test results in DevOps for Jenkins, Azure DevOps, GitHub, GitHub Enterprise, and GitLab unit, functional, and performance tests.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [User created, Integrate, DevOps Change Velocity, IT Service Management]
---

# DevOps test tool integration

Test tool integration lets you view test results in DevOps for Jenkins, Azure DevOps, GitHub, GitHub Enterprise, and GitLab unit, functional, and performance tests.

For GitLab and Jenkins, only JUnit test type integration is supported.

**Note:** For other test types, use the [DevOps - POST /devops/tool/\{capability\}](https://www.servicenow.com/docs/access?context=devops-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) endpoint of the [DevOps API](https://www.servicenow.com/docs/access?context=devops-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

-   Selenium tests run and published using TestNG are reported by the Jenkins plugin for ServiceNow DevOps.
-   Test type categorization is supported.
-   Additional tests results reported by tools, such as Apache JMeter, can be processed in DevOps using custom Workflow Studio subflows \(no pipeline changes required\).

<table id="table_xxq_lcx_pnb"><thead><tr><th>

Category

</th><th>

Test type

</th></tr></thead><tbody><tr><td>

Unit

</td><td>

JUnit \(default\)

 NUnit

 XUnit

 Unit test

 **Note:**

-   For GitLab and Jenkins, only the JUnit test type integration is supported.
-   For ADO, GitHub, and GitHub Enterprise, the JUnit, NUnit, XUnit, and Unit test type integrations are supported.

 You can change the default test type by modifying the **\[sn\_devops.default\_test\_type\]** [DevOps property](dev-ops-administration.md).

</td></tr><tr><td>

Functional

</td><td>

-   Integration
-   Regression
-   Smoke
-   System
-   User Acceptance

</td></tr><tr><td>

Performance

</td><td>

Load

</td></tr></tbody>
</table>## Test type mapping

The test type mapping connects the test type and entity being tested with the DevOps tool \(**DevOps** &gt; **Integrations** &gt; **Test Type Mappings** module.\)

![Test type mappings](../image/test-type-mappings.png)

An accurate test type mapping ensures that the test type always appears as intended in the test summary results.

<table id="table_j2s_nkv_pnb"><thead><tr><th colspan="2">

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Test type

</td><td>

-   JUnit
-   Nunit
-   Xunit
-   Unit test

**Note:**

    -   For GitLab and Jenkins, only the JUnit test type integration is supported.
    -   For ADO, GitHub, and GitHub Enterprise, the JUnit, NUnit, XUnit, and Unit test type integrations are supported.
-   Integration
-   Regression
-   Smoke
-   System
-   User Acceptance
-   Load

</td></tr><tr><td rowspan="2">

DevOps Entity Id

</td><td>

Table name

</td><td>

DevOps table name that contains the entity linked to the test results \(in the test report payload\).

 -   Step \[sn\_devops\_step\]
-   Pipeline \[sn\_devops\_pipeline\]

 **Note:** Only DevOps Step and Pipeline tables are supported.

</td></tr><tr><td>

Document

</td><td>

Name of the entity specified in the selected table.

 For example, the name of the step, pipeline, artifact, or package.

</td></tr><tr><td colspan="2">

Test File Paths

 \(Jenkins tests only\)

</td><td>

Path to the generated test result file on the Jenkins server.

 This is useful so test reports with attributes that don't conform to JUnit or TestNG implementation, such as JMeter for example, can still be leveraged by DevOps.

 Separate multiple files by a comma.

 **Note:** You must use a Workflow Studio subflow to transform a raw test payload.

</td></tr><tr><td colspan="2">

Tool integration

</td><td>

Tool that's running the test.

</td></tr><tr><td colspan="2">

DevOps Table

</td><td>

DevOps table that corresponds to the table name in the **DevOps Entity Id** setting.

</td></tr></tbody>
</table>![DevOps test type mapping](../image/dev-ops-test-type-mapping.png "DevOps test type mapping")

![Example yaml file of ADO unit test](../image/ado-unit-test.png "Example yaml file of ADO unit test")

![Example yaml file of GitHub unit test](../image/github-unit-test.png "Example yaml file of GitHub unit test")

## Transforming a raw test payload

You can transform a raw test report \(a report containing attributes that do not conform to JUnit or TestNG implementation\), such as JMeter for example, by configuring the **DevOps Test Subflow Policy** decision table to call a custom subflow \(**Decision Tables** &gt; **Decision Tables** module\).

**Note:** You must create the custom Workflow Studio subflow that transforms the raw test payload.

If there is more than one test type in a performance stage, you can use the **DevOps Test Type Policy** decision table to configure the test type for each test so the test result payloads are transformed correctly.

![DevOps decision tables](../image/dev-ops-test-decision-policies.png "DevOps decision tables")

<table id="table_c54_kcw_pnb"><thead><tr><th>

Decision table

</th><th>

Purpose

</th><th>

Configuration

</th></tr></thead><tbody><tr><td>

DevOps Test Subflow Policy

</td><td>

To automatically call a custom subflow that transforms the raw payload received by the tool.

 Decision inputs:

 -   Test Result Payload
-   Test Type

</td><td>

Create a decision that specifies the custom subflow to call when the raw payload is received.

 Set the conditions to contain fields that would be included in the raw payload.

 For example, to call Jenkins BZ Performance Test custom subflow:

 Conditions:

-   `Test Type is Load`

\(Load is the test type configured for performance tests\)

-   `Test Result Payload contains throughput`
-   `Test Result Payload contains concurrency`

 Answer: FLow: Jenkins BZ Performance Test

</td></tr><tr><td>

DevOps Test Type Policy

</td><td>

To automatically set test types when more than one type of test is configured in a performance test stage.

 This is necessary so the results for the second test type get transformed correctly.

 For example, when both a Load performance test and a JUnit performance test are mapped in the same DevOps step, the JUnit test results won't get formatted correctly unless a decision is created.

 Decision inputs:

-   Step
-   Test Result Payload
-   Tool Integration
-   Pipeline

</td><td>

Create a decision for each type of test in the performance test stage to set the test type.

 Load test:

-   Conditions:
    -   `Step is Perf Tests`
    -   `Test Result Payload contains throughput`
    -   `Test Result Payload contains concurrency`
-   Answer: `TestType: Load`


 JUnit test:

 -   Conditions:
    -   `Step is Perf Tests`
    -   `Test Result Payload does not contain throughput`
    -   `Test Result Payload does not contain concurrency`
-   Answer: `TestType: JUnit`


</td></tr></tbody>
</table>![DevOps multiple performance test types](../image/dev-ops-multiple-test-types.png "DevOps multiple performance test types")

![DevOps test type mappings](../image/dev-ops-mult-test-types-map.png "DevOps multiple test type mappings")

![DevOps decision table decision](../image/dev-ops-decision-table.png "DevOps decision table decision")

## Test summary results

You can view test summary results these ways.

-   **DevOps** &gt; **Test Results** module \(Test Summaries and Performance Test Summaries\).
-   [DevOps change request](dev-ops-change-acceleration.md) - Test Results related list.
-   [DevOps Pipeline UI](dev-ops-pipeline-ui.md) - Quality tile.

![DevOps performance test summary](../image/dev-ops-perf-test-summary.png "DevOps performance test summary example")

## Expected standard JSON Notification capability payload - Test tool

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

Send only one Attribute combination. For example, send Attributes of either  Artifact or Package, or the combination of Build + Stage + PipelineName.

If you send more than one Attribute, priority is given in the following order and the low priory one is ignored. For example, if you send attribute for both packages and artifacts, then attribute of package is considered and the attribute of artifacts is ignored.

1.packages
2.artifcats
3.buildNumber + stageName + pipelineName

"packages": [{"name": "CorpSite-pkg1"}], 
"artifacts": [{"name": "CorpSite-artifact", "version": "1.0.0"}], 
"buildNumber": "55", 
"stageName": "test", 
"pipelineName": "CorpSite-selenium", 
} 

Notes:
- The pipelineName attribute value must be same as the value in the **Orchestration pipeline** field of the Pipeline [sn_devops_pipeline] table.
- The stageName attribute value must be same as the value in the **Orchestration stage** field of the Step [sn_devops_step] table.
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

Send only one Attribute combination. For example, send Attributes of either  Artifact or Package, or the combination of Build + Stage + PipelineName.

If you send more than one Attribute, priority is given in the following order and the low priory one is ignored. For example, if you send attribute for both packages and artifacts, then attribute of package is considered and the attribute of artifacts is ignored.

1.packages
2.artifcats
3.buildNumber + stageName + pipelineName

"packages": [{"name": "CorpSite-pkg1"}], 
"artifacts": [{"name": "CorpSite-artifact", "version": "1.0.0"}], 
"buildNumber": "55", 
"stageName": "test", 
"pipelineName": "CorpSite-Performance", 
} 

Notes:
- The pipelineName attribute value must be same as the value in the **Orchestration pipeline** field of the Pipeline [sn_devops_pipeline] table.
- The stageName attribute value must be same as the value in the **Orchestration stage** field of the Step [sn_devops_step] table.
```

-   **[Configure a test tool in DevOps](../task/create-test-tool-dev-ops.md)**  
Configure a test tool in DevOps to view unit, functional, and performance test results.
-   **[Add test results to change requests using test API](../reference/test-api-tools.md)**  
Add test results to DevOps change requests using the test capability of the DevOps - POST /devops/tool/\{capability\} API. The API is available for all test types for various tools connected to DevOps Change Velocity.
-   **[Add attachments to change requests using attachment API](../reference/attachment-api-chg.md)**  
Add test report xmls as attachments to DevOps change requests using the attachment API.

**Parent Topic:**[User-created integrations in DevOps Change Velocity](dev-ops-tool-integration.md)

