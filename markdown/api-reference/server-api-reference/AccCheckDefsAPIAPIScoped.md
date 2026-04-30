---
title: AccCheckDefsAPI - Scoped
description: The AccCheckDefsAPI script include enables managing check definitions and associated parameters.Gets a specified check definition with details.Gets a list of check definitions with details.Enables changing one or more field values of a specified check definition.Enables changing one or more field values of a specified check parameter.Enables changing one or more field values of a specified check secure parameter.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# AccCheckDefsAPI- Scoped

The AccCheckDefsAPI script include enables managing check definitions and associated parameters.

This script include requires the Agent Client Collector Framework \(sn\_agent\) store application and is provided within the `sn_agent` namespace. This script include requires the agent\_client\_collector\_admin role. For more information, refer to [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

This script include does not have a constructor for creating an instance. Call each method using the AccCheckDefsAPI static class in the following format:

`sn_agent.AccCheckDefsAPI.<method>`

For the REST API solution, refer to [Agent Client Collector API](../../../../../integrate/inbound-rest/concept/agnt_clnt_cll-api.md#).

This script include provides methods that enable the following:

-   Get a specified check definition
-   Get a list of check definitions
-   Update checks and check parameters

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## AccCheckDefsAPI - getCheck\(String checkDefId, Boolean withParams\)

Gets a specified check definition with details.

<table id="table_zk2_2g2_z4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

checkDefId

</td><td>

String

</td><td>

Sys\_id of the check definition listed in the Check Definitions \[sn\_agent\_check\_def\] table.

</td></tr><tr><td>

withParams

</td><td>

Boolean

</td><td>

Flag that indicates whether existing check parameter details are returned. Information for each standard and secure check parameter is included in a JSON object. Valid values:

-   true: Return check parameter details.
-   false: Do not return check parameter details.

 Default: False

</td></tr></tbody>
</table><table id="table_al2_2g2_z4b" class="returns"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

check

</td><td>

Details of the specified check definition.```
"check ": {
 "background": Boolean,
 "check_group": "String",
 "check_type": "String",
 "command": "String",
 "error": "String",
 "name": "String",
 "params": [Array],
 "plugins": [Array],
 "proxy_valid": Boolean,
 "secure_params": [Array],
 "sys_id": "String",
 "timeout": Number
}
```

</td></tr><tr><td>

check.background

</td><td>

Flag that indicates whether this check definition is a background check. A background check is a check which the agent starts execution of and doesn't wait for it to finish running. Valid values:

-   true: This check definition is a background check.
-   false: This check definition is not a background check.

 Data type: Boolean

</td></tr><tr><td>

check.check\_group

</td><td>

Group specified for this check definition. Data type: String

</td></tr><tr><td>

check.check\_type

</td><td>

Type of check. Possible values:

-   Events – Check results are transformed into an Event Management event.
-   Metrics – Values from the check result are transformed to metrics.

 Data type: String

</td></tr><tr><td>

check.command

</td><td>

Command that the Agent Client Collector executes. Data type: String

</td></tr><tr><td>

check.error

</td><td>

Message if there is an error. Null otherwise.Data type: String

</td></tr><tr><td>

check.name

</td><td>

Name of the check. Data type: String

</td></tr><tr><td>

check.params

</td><td>

List of parameter definitions associated with the check definition. These results are only included if the **withParams** parameter is set to true.```
"params": [
  {
    "active": Boolean,
    "default_value": "String",
    "mandatory": Boolean,
    "name": "String",
    "sys_id": "String"
   }
]
```

 Data type: Array

</td></tr><tr><td>

check.params.active

</td><td>

Flag that indicates whether the check parameter is active. Valid values:

-   true: The check parameter is active.
-   false: The check parameter is inactive.

 Data type: Boolean

</td></tr><tr><td>

check.params.default\_value

</td><td>

Specifies the default value for this check parameter. Data type: String

</td></tr><tr><td>

check.params.mandatory

</td><td>

Flag that indicates whether the check parameter is required. Valid values:

-   true: The check parameter is required.
-   false: The check parameter is optional.

 Data type: Boolean

</td></tr><tr><td>

check.params.name

</td><td>

Name of the check parameter. Data type: String

</td></tr><tr><td>

check.params.sys\_id

</td><td>

Sys\_id of the check parameter listed in the Check Secure Parameter Definitions \[sn\_agent\_check\_param\_def\] table. Data type: String

</td></tr><tr><td>

check.plugins

</td><td>

List of [Agent Client Collector plugins](https://www.servicenow.com/docs/access?context=acc-assets&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) associated with this check. Data type: Array

</td></tr><tr><td>

check.proxy\_valid

</td><td>

Flag that indicates whether the check definition policy is set to work as a proxy. Valid values:

-   true: This check definition policy is set to work as a proxy.
-   false: This check definition policy is not set to work as a proxy.

 Data type: Boolean

</td></tr><tr><td>

check.secure\_params

</td><td>

List of assigned to this check. These results are only included if the **withParams** parameter is set to true.```
"secure_params": [
  {
    "active": Boolean,
    "name": "String",
    "order": Number,
    "sys_id": "String"
   }
]
```

 Data type: Array

</td></tr><tr><td>

check.secure\_params.active

</td><td>

Flag that indicates whether the secure parameter is active. Valid values:

-   true: The secure parameter is active.
-   false: The secure parameter is inactive.

 Data type: Boolean

</td></tr><tr><td>

check.secure\_params.name

</td><td>

Name of the secure parameter. Data type: String

</td></tr><tr><td>

check.secure\_params.order

</td><td>

Order in which the parameter is sent to the check command/script. Data type: Number

</td></tr><tr><td>

check.secure\_params.sys\_id

</td><td>

Sys\_id of the secure parameter listed in the Check Secure Parameter Definitions \[sn\_agent\_check\_secure\_param\_def\] table. Data type: String

</td></tr><tr><td>

check.sys\_id

</td><td>

Sys\_id of the check definition listed in the Check Definitions \[sn\_agent\_check\_def\] table. Data type: String

</td></tr><tr><td>

check.timeout

</td><td>

Timeout in seconds. Data type: Number

</td></tr></tbody>
</table>The following example shows how to get information for a specified check definition.

```
var checkDefId = "94436b237f705300f128134f8dfa91a4";
var withParams = true;

var checkDef = sn_agent.AccCheckDefsAPI.getCheck(checkDefId, withParams);

gs.info(JSON.stringify(checkDef, null, 2));
```

Output:

```
{
  "check": {
    "name": "app.apache.metrics-apache",
    "command": "metrics-apache-graphite.rb -p {{.labels.params_port}} --path {{.labels.params_path}} -h {{.labels.params_host}}",
    "plugins": [
      "monitoring-plugin-common"
    ],
    "timeout": 60,
    "proxy_valid": true,
    "background": false,
    "check_type": "Metrics",
    "check_group": "Apache",
    "sys_id": "94436b237f705300f128134f8dfa91a4",
    "params": [
      {
        "name": "port",
        "active": true,
        "mandatory": true,
        "default_value": "80",
        "sys_id": "58436b237f705300f128134f8dfa91a8"
      },
      {
        "name": "path",
        "active": true,
        "mandatory": true,
        "default_value": "/server-status?auto",
        "sys_id": "98436b237f705300f128134f8dfa91aa"
      },
      {
        "name": "scheme",
        "active": false,
        "mandatory": false,
        "default_value": null,
        "sys_id": "a4e57a96db3bbb4035305c55dc9619f6"
      },
      {
        "name": "host",
        "active": true,
        "mandatory": true,
        "default_value": "127.0.0.1",
        "sys_id": "d4436b237f705300f128134f8dfa91a6"
      },
      {
        "name": "ssl_secure_connection",
        "active": false,
        "mandatory": false,
        "default_value": null,
        "sys_id": "e3b272c4530100106ffeddeeff7b1275"
      }
    ],
    "secure_params": [
      {
        "name": "cred_user_name",
        "active": true,
        "order": 1,
        "sys_id": "2494cd6e53170010f42cddeeff7b1273"
      },
      {
        "name": "cred_password",
        "active": true,
        "order": 2,
        "sys_id": "35948d6e53170010f42cddeeff7b127f"
      }
    ]
  },
  "error": null
}
```

## AccCheckDefsAPI - getChecksList\(String encodedQuery, Number limit, Boolean withParams\)

Gets a list of check definitions with details.

See also [Checks and policies](https://www.servicenow.com/docs/access?context=checks-policies&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

<table id="table_zk2_2g2_z4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

encodedQuery

</td><td>

String

</td><td>

An [encoded query string](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) to filter the check definition result list. Use null for an unfiltered list of check definitions in the system.

</td></tr><tr><td>

limit

</td><td>

Number

</td><td>

Limits the number of returned records. Set to null to use the default value. Default: 20,000

</td></tr><tr><td>

withParams

</td><td>

Boolean

</td><td>

Flag that indicates whether existing check parameter details are returned. Information for each standard and secure check parameter is included in a JSON object. Valid values:

-   true: Return check parameter details.
-   false: Do not return check parameter details.

 Default: False

</td></tr></tbody>
</table><table id="table_al2_2g2_z4b" class="returns"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

check definitions

</td><td>

List of check definition and details provided as JSON objects.```
[
  {
    "background": Boolean,
    "check_group": "String",
    "check_type": "String",
    "command": "String",
    "name": "String",
    "params": [Array],
    "plugins": [Array],
    "proxy_valid": Boolean,
    "secure_params": [Array],
    "sys_id": "String",
    "timeout": Number
  }
]
```

 Data type: Array

</td></tr><tr><td>

background

</td><td id="accCkDf-background-desc">

Flag that indicates whether this check definition is a background check. A background check is a check which the agent starts execution of and doesn't wait for it to finish running. Valid values:

-   true: This check definition is a background check.
-   false: This check definition is not a background check.

 Data type: Boolean

</td></tr><tr><td>

check\_group

</td><td id="accCkDf-chkGrp-desc">

Group specified for this check definition. Data type: String

</td></tr><tr><td>

check\_type

</td><td id="accCkDf-chkTyp-desc">

Type of check. Possible values:

-   Events – Check results are transformed into an Event Management event.
-   Metrics – Values from the check result are transformed to metrics.

 Data type: String

</td></tr><tr><td>

command

</td><td id="accCkDf-command-desc">

Command that the Agent Client Collector executes. Data type: String

</td></tr><tr><td>

name

</td><td id="accCkDf-name-desc">

Name of the check. Data type: String

</td></tr><tr><td>

params

</td><td id="accCkDf-p-desc">

List of parameter definitions associated with the check definition. These results are only included if the **withParams** parameter is set to true.```
"params": [
  {
    "active": Boolean,
    "default_value": "String",
    "mandatory": Boolean,
    "name": "String",
    "sys_id": "String"
   }
]
```

 Data type: Array

</td></tr><tr><td>

params.active

</td><td id="accCkDf-p-active-desc">

Flag that indicates whether the check parameter is active. Valid values:

-   true: The check parameter is active.
-   false: The check parameter is inactive.

 Data type: Boolean

</td></tr><tr><td>

params.default\_value

</td><td id="accCkDf-p-default-desc">

Specifies the default value for this check parameter. Data type: String

</td></tr><tr><td>

params.mandatory

</td><td id="accCkDf-p-mando-desc">

Flag that indicates whether the check parameter is required. Valid values:

-   true: The check parameter is required.
-   false: The check parameter is optional.

 Data type: Boolean

</td></tr><tr><td>

params.name

</td><td id="accCkDf-p-name-desc">

Name of the check parameter. Data type: String

</td></tr><tr><td>

params.sys\_id

</td><td id="accCkDf-p-id-desc">

Sys\_id of the check parameter listed in the Check Secure Parameter Definitions \[sn\_agent\_check\_param\_def\] table. Data type: String

</td></tr><tr><td>

plugins

</td><td id="accCkDf-plugins-desc">

List of [Agent Client Collector plugins](https://www.servicenow.com/docs/access?context=acc-assets&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) associated with this check. Data type: Array

</td></tr><tr><td>

proxy\_valid

</td><td id="accCkDf-proxy-desc">

Flag that indicates whether the check definition policy is set to work as a proxy. Valid values:

-   true: This check definition policy is set to work as a proxy.
-   false: This check definition policy is not set to work as a proxy.

 Data type: Boolean

</td></tr><tr><td>

secure\_params

</td><td id="accCkDf-sp-desc">

List of assigned to this check. These results are only included if the **withParams** parameter is set to true.```
"secure_params": [
  {
    "active": Boolean,
    "name": "String",
    "order": Number,
    "sys_id": "String"
   }
]
```

 Data type: Array

</td></tr><tr><td>

secure\_params.active

</td><td id="accCkDf-sp-active-desc">

Flag that indicates whether the secure parameter is active. Valid values:

-   true: The secure parameter is active.
-   false: The secure parameter is inactive.

 Data type: Boolean

</td></tr><tr><td>

secure\_params.name

</td><td id="accCkDf-sp-name-desc">

Name of the secure parameter. Data type: String

</td></tr><tr><td>

secure\_params.order

</td><td id="accCkDf-sp-order-desc">

Order in which the parameter is sent to the check command/script. Data type: Number

</td></tr><tr><td>

secure\_params.sys\_id

</td><td id="accCkDf-sp-id-desc">

Sys\_id of the secure parameter listed in the Check Secure Parameter Definitions \[sn\_agent\_check\_secure\_param\_def\] table. Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="accCkDf-id-desc">

Sys\_id of the check definition listed in the Check Definitions \[sn\_agent\_check\_def\] table. Data type: String

</td></tr><tr><td>

timeout

</td><td id="accCkDf-timeout-desc">

Timeout in seconds. Data type: Number

</td></tr></tbody>
</table>The following example shows how to retrieve a list of two check definitions with parameter values.

```
var encQuery = "nameSTARTSWITHchecks_";
var limit = 2;
var withParams = true;

var checkDefs = sn_agent.AccCheckDefsAPI.getChecksList(encQuery, limit, withParams);

gs.info(JSON.stringify(checkDefs, null, 2));
```

Output:

```
[
  {
    "name": "checks_api_test",
    "command": "echo hello",
    "plugins": [],
    "timeout": 9,
    "proxy_valid": true,
    "background": false,
    "check_type": "TestCheck",
    "check_group": "computer",
    "sys_id": "7f1f9026dba530106f4810284b96194f",
    "params": [],
    "secure_params": [
      {
        "name": "check_api_test_check_secure_param2",
        "active": true,
        "order": 2,
        "sys_id": "2d30a066dba530106f4810284b9619c1"
      },
      {
        "name": "check_api_test_check_secure_param1",
        "active": true,
        "order": 100,
        "sys_id": "4c20a066dba530106f4810284b9619a8"
      }
    ]
  },
  {
    "name": "checks_api_test222",
    "command": "echo hello1212121",
    "plugins": [],
    "timeout": 60,
    "proxy_valid": true,
    "background": false,
    "check_type": "TestCheck",
    "check_group": "computer",
    "sys_id": "99e12466dba530106f4810284b961976",
    "params": [
      {
        "name": "check_api_test_check_param_222",
        "active": true,
        "mandatory": false,
        "default_value": "test_test_test",
        "sys_id": "44026466dba530106f4810284b9619b2"
      }
    ],
    "secure_params": []
  }
]
```

## AccCheckDefsAPI - updateCheck\(String checkDefId, Object updateJson\)

Enables changing one or more field values of a specified check definition.

See also [Checks and policies](https://www.servicenow.com/docs/access?context=checks-policies&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

<table id="table_zk2_2g2_z4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

checkDefId

</td><td>

String

</td><td>

Sys\_id of the check definition listed in the Check Definitions \[sn\_agent\_check\_def\] table.

</td></tr><tr><td>

updateJson

</td><td>

Object

</td><td>

Map of check definition fields to be updated to their new values. Refer to the data dictionary for a comprehensive list of Check Definition fields and types.```
{
 "background": Boolean,
 "check_group": "String",
 "check_type": "String",
 "command": "String",
 "name": "String",
 "plugins": [Array],
 "proxy_valid": Boolean,
 "timeout": Number
}
```

</td></tr><tr><td>

updateJson.active

</td><td>

Number

</td><td>

Indicates whether this check definition is active.Valid values:

-   0: This check definition is inactive.
-   1: This check definition is active.

</td></tr><tr><td>

updateJson.background

</td><td>

Boolean

</td><td>

Flag that indicates whether this check definition is a background check. A background check is a check which the agent starts execution of and doesn't wait for it to finish running.Valid values:

-   true: This check definition is a background check.
-   false: This check definition is not a background check.

</td></tr><tr><td>

updateJson.check\_group

</td><td>

String

</td><td>

Group specified for this check definition.

</td></tr><tr><td>

updateJson.check\_type

</td><td>

String

</td><td>

Type of check.Possible values:

-   Events – Check results are transformed into an Event Management event.
-   Metrics – Values from the check result are transformed to metrics.

</td></tr><tr><td>

updateJson.command

</td><td>

String

</td><td>

Command that the Agent Client Collector executes.

</td></tr><tr><td>

updateJson.name

</td><td>

String

</td><td>

Name of the check.

</td></tr><tr><td>

updateJson.plugins

</td><td>

Array

</td><td>

List of [Agent Client Collector plugins](https://www.servicenow.com/docs/access?context=acc-assets&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) associated with this check.

</td></tr><tr><td>

updateJson.proxy\_valid

</td><td>

Boolean

</td><td>

Flag that indicates whether the check definition policy is set to work as a proxy.

 Valid values:

-   true: This check definition policy is set to work as a proxy.
-   false: This check definition policy is not set to work as a proxy.

</td></tr><tr><td>

updateJson.timeout

</td><td>

Number

</td><td>

Timeout in seconds.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None|Error message if unsuccessful.|

The following example shows how to deactivate a check definition.

```
var checkJson = sn_agent.AccCheckDefsAPI.getCheck(activeCheckDefs[0].sys_id, true);
if (!gs.nil(checkJson.error))
	gs.error(checkJson.error);

var updateJson = {active: "0"}; // deactivate the check definition
sn_agent.AccCheckDefsAPI.updateCheck(checkJson.check.sys_id, updateJson);
```

## AccCheckDefsAPI - updateCheckParam\(String checkDefParamId, Object updateJson\)

Enables changing one or more field values of a specified check parameter.

<table id="table_zk2_2g2_z4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

checkDefParamId

</td><td>

String

</td><td>

Sys\_id of the check parameter listed in the Check Parameter Definitions \[sn\_agent\_check\_param\_def\] table.

</td></tr><tr><td>

updateJson

</td><td>

Object

</td><td>

Map of check parameter fields to be updated to their new values. Refer to the data dictionary for a comprehensive list of Check Secure Parameter Definition fields and types.```
{
 "active": Boolean,
 "default_value": "String",
 "mandatory": Boolean,
 "name": "String"
}
```

</td></tr><tr><td>

updateJson.active

</td><td>

Boolean

</td><td>

Flag that indicates whether the check parameter is active.

 Valid values:

-   true: The check parameter is active.
-   false: The check parameter is inactive.

</td></tr><tr><td>

updateJson.default\_value

</td><td>

String

</td><td>

Specifies the default value for this check parameter.

</td></tr><tr><td>

updateJson.mandatory

</td><td>

Boolean

</td><td>

Flag that indicates whether the check parameter is required.

 Valid values:

-   true: The check parameter is required.
-   false: The check parameter is optional.

</td></tr><tr><td>

updateJson.name

</td><td>

String

</td><td>

Name of the check parameter.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None|Error message if unsuccessful.|

The following example shows how to activate a check parameter.

```
var checkParmSysId = "cd922ce6dba530106f4810284b961966";
var updateJson = {"active": "true"};
sn_agent.AccCheckDefsAPI.updateCheckSecureParam(checkParmSysId, updateJson);
```

## AccCheckDefsAPI - updateCheckSecureParam\(String checkDefSecureParamId, Object updateJson\)

Enables changing one or more field values of a specified check secure parameter.

<table id="table_zk2_2g2_z4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

checkDefSecureParamId

</td><td>

String

</td><td>

Sys\_id of the secure parameter listed in the Check Secure Parameter Definitions \[sn\_agent\_check\_secure\_param\_def\] table.

</td></tr><tr><td>

updateJson

</td><td>

Object

</td><td>

Map of check secure parameter fields to be updated to their new values. Refer to the data dictionary for a comprehensive list of Check Secure Parameter Definition fields and types.```
{
 "active": Boolean,
 "name": "String",
 "order": Number
}
```

</td></tr><tr><td>

updateJson.active

</td><td>

Boolean

</td><td>

Flag that indicates whether the secure parameter is active.

 Valid values:

-   true: The secure parameter is active.
-   false: The secure parameter is inactive.

</td></tr><tr><td>

updateJson.name

</td><td>

String

</td><td>

Name of the secure parameter.

</td></tr><tr><td>

updateJson.order

</td><td>

Number

</td><td>

Order in which the parameter is sent to the check command/script.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None|Error message if unsuccessful.|

The following example shows how to activate a check secure parameter.

```
var checkSecParmSysId = "<sys_id>";
var updateJson = {"active": "true"};
sn_agent.AccCheckDefsAPI.updateCheckSecureParam(checkSecParmSysId, updateJson);
```

