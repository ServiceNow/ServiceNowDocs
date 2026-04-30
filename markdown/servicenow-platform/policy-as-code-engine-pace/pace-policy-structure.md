---
title: Structure of a PaCE policy script
description: This section describes the structure of a PaCE policy script.
locale: en-US
release: zurich
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Write and test policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Structure of a PaCE policy script

This section describes the structure of a PaCE policy script.

When a policy is executed, a set of parameters is passed and the policy developer can use these parameters in this policy script to make a decision whether it is compliant, non-compliant, or compliant-exception and return this decision back to the calling service. The following image shows a sample script:

![Sample script policy.](../image/pace-sample-script-new-names.jpg "Sample policy script")

To debug the script, select the Debugger script icon ![Debugger icon](../image/pace-debug-icon.jpg). For more information, see [Script Debugger API](https://www.servicenow.com/docs/access?context=scriptdebugger-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

The following table lists the policy function parameters and how can they be used in your policy script.

<table id="table_jk5_xlt_jrb"><thead><tr><th>

Variable Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

logger

</td><td>

`Logger` is an object that the policy coder can use to log messages. The log messages are stored in the `sn_pace_execution_log` table. You can review these log messages for debugging, tracking, or monitoring purposes. The log messages can be logged with one of the following levels: -   1: info
-   2: debug
-   3: warning
-   4: error

 When a policy is invoked through the API, you can specify the desired log level. For example:The format is as follows:

 `logger.info("** snapshotId is: "+snapshotId);`

</td></tr><tr><td>

currentRecord

</td><td>

`currentRecord` is an object of the current version of the policy that is executed when the policy is used. To view the `currentRecord` details, navigate to the **Versions** tab on the Policy Home page and locate the policy whose version state is set to **Current**. In the image below, you can see that the current active version of the policy highlighted. It shows the following details:

-   version number
-   last update date
-   the name of the user who updated the version
-   the number of times it was executed by the calling application
-   the number of times it was run in the test environment

The policy script can access this data during policy execution time by interacting with the `currentRecord` object passed to the policy.

 ![PaCE Version Details](../image/pace-version-details.jpg)

 This example shows how a policy developer can access the properties of the policy version record:

```
(function(logger, currentRecord, documentRecord, apiVars, configParams, recordRefs, dataCollectors, childrenOutputs, output) {
     //retrieve the input values
     logger.info(currentRecord.getValue('name'));
  }
 )(logger, currentRecord, documentRecord, apiVars, configParams, recordRefs, dataCollectors, childrenOutputs, output);

```

</td></tr><tr><td>

documentRecord

</td><td>

The `documentRecord` is used to map the policy to the relevant object \(table and documentID\) that is being validated. The `documentRecord` is a combination of the table\_name and sysID. Based on the properties of the object, the policy logic is used to manage and interact with the object being validated to determine the right decision.For example: In the DevOps Config environment, a policy can be mapped to the deployable. When the API is invoked, a query is initiated on the document \(deployable\) table and the Sys ID of the deployable.

```
{
           "table": "sn_cdm_deployable",
           "sysId": "d1be8f5e87d80110eec7dbdd3fbb357d"
		}
```

This example shows how the documentRecord can be used in a policy script:```
(function(logger, currentRecord, documentRecord, apiVars, configParams, recordRefs, dataCollectors, childrenOutputs, output) 
{
//assuming that associated document has state field
  var documentState = documentRecord.getValue(“state”);
if (documentState == “new”)
   …
else
   …
}
)(logger, currentRecord, documentRecord, apiVars, configParams, recordRefs, dataCollectors, childrenOutputs, output);

```

</td></tr><tr><td>

apiVars

</td><td>

The apiVars is passed to the PaCE API when it is invoked. It includes all the API variables defined in the policy version. See &lt;Defining Caller Inputs&gt; section for details

 The [Sample policy script](pace-policy-structure.md#fig_qfr_z1z_yrb) shows how policies can be used to validate configuration data in the DevOps environment. In the sample script, the apiVars variable is defined as

```
var snapshotId = apiVars.snapshotId;
```

where the specified `snapshotId` is mapped to the corresponding `snapshotId` of the DevOps Config deployable being validated based on specified criteria.

 The policy developer can define logic in the policy script to use the apiVars values passed when the API is invoked to determine the decision. For example, the SnapshotID passed is used to identify key-values related to the specific snapshotID for a deployable passed in the documentRecord object.

</td></tr><tr><td>

configParams

</td><td>

Config Parameters are variables are passed when mapping the policy and includes all the Config Parameters variables defined for a specific version of the policy.

 The `configParams` variable is defined as follows in the [Sample policy script](pace-policy-structure.md#fig_qfr_z1z_yrb).

```
var dbPort = configParams.dbPort;
```

The policy developer can define the logic in the policy script to use the values passed at mapping to determine the decision. For example, the `dbPort` number must be less than 30000, otherwise the policy is considered to be non\_compliant.

</td></tr><tr><td>

recordRefs

</td><td>

Record references define queries to extract data from any ServiceNow® tables and use the data to configure the policy logic. There is an auto-completion function that can select the record reference in the Javascript editor.

</td></tr><tr><td>

dataCollectors

</td><td>

The data collectors function collects input process data from ServiceNow or an external data source to provide an output.

</td></tr><tr><td>

childrenOutputs

</td><td>

Not supported in this version.

</td></tr><tr><td colspan="2">

outputThis parameter is used to pass the output of the policy execution that includes the decision back to the calling service. It provides a decision related to this policy, with additional information such as errors, warnings, and result details.

 This example shows a sample output with compliant and non\_compliant decisions:

```

{
    "decision": "compliant",
    "results": [],
    "warnings": [],
    "failures": [],
    "state": "complete"
}


{
    "decision": "non_compliant",
    "results": [],
    "warnings": [],
    "failures": [“Failed to validate key”],
    "state": "complete"
}

```

</td></tr><tr><td>

output.decision

</td><td>

The decision property can be set to:-   Compliant: Determines that the policy complies with requirements.
-   Non-compliant: Determines that the policy does not comply with the requirements.
-   Compliant-exception: Determines that an exception to the policy has been approved and any policies that are non-compliant are set to the compliant-exception state.

 The decision is returned in a JSON format back to the calling service.

 **Note:** If a value is not specified in the `output.decision` field in the script, when the policy is executed, by default this field is set to **compliant** if there are no failures.

</td></tr><tr><td>

output.results

</td><td>

The `results` property can be used to pass data back to the calling service on decisions made during the policy validation phase. A list object with a list of results can be passed back to the calling service.

</td></tr><tr><td>

output.warnings

</td><td>

The `warnings` property can be used to pass data back to the calling service on any warnings that occurred during the policy validation phase.

</td></tr><tr><td>

output.failures

</td><td>

The `failures` property can be used to pass data back to the calling service on any errors that occurred during the policy validation phase.

</td></tr><tr><td colspan="2">

**Note:** The following fields are automatically filled in when the PaCE policy script is executed.

</td></tr><tr><td>

output.name

</td><td>

The name \(current version\) of the policy being executed.

</td></tr><tr><td>

output.state

</td><td>

It indicates the state of the policy invocation.-   Complete: The invocation was completed successfully.
-   Pending: Indicates that the policy could not be successfully executed and is an incomplete state.

</td></tr></tbody>
</table>**Note:**

-   Auto-complete suggestions are available in the policy script editor for the `logger, callerInput` and `mappedInput` parameter.
-   To view additional information for a parameter, enter the parameter name and select one of the options as follows:

    ![PaCE additional parameter details](../image/pace-hover-text.jpg)


