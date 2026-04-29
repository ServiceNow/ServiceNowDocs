---
title: Cloud Configuration Governance scripting reference
description: Cloud Configuration Governance provides several objects and variables that you can use to create script-based policies and CI finder mapping scripts.
locale: en-US
release: australia
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloud Configuration Governance reference, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Configuration Governance scripting reference

Cloud Configuration Governance provides several objects and variables that you can use to create script-based policies and CI finder mapping scripts.

## Scripting reference for the Cloud Configuration Governance policies

<table id="table_mjy_3jk_hsb"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Schema

</th></tr></thead><tbody><tr><td>

`configSettings`

</td><td>

Represents the configuration data imported from the cloud.

</td><td>

```
[
  {
    "config_key":"configuration_key",
    "type":"data_type",
    "value":"configuration_value"
  },
  ...
]

```

</td></tr><tr><td>

`current`

</td><td>

Represents the current glide record object for the select resource type.

</td><td>

It contains the following fields: -   Name: Name of the resource
-   Type: Resource type
-   Identifier: Unique identifier of the cloud resource
-   Details: Cloud resource-specific details

</td></tr><tr><td>

`resourceInformation`

</td><td>

Resource record and its attributes.

</td><td>

```
[
  {
    "attribute": "Attribute name",
    "tableName" : "Referenced table",
    "documentId": "Referenced record",        
  },
  ...
] 

```

</td></tr><tr><td>

`auditResult`

</td><td>

Audit details that must be written to the Configuration Management Database \(CMDB\).

</td><td>

```
{
  "details": "Violation definition "’
  "severity": "severity of the violation",
  "auditViolationName": "Violation name" 
};

```

</td></tr></tbody>
</table><table id="table_pjy_trk_hsb"><thead><tr><th>

Name

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`answer`

</td><td>

Boolean

</td><td>

Variable to specify whether the policy reports the violation or not.-   `true`: Report the violation. Create the auditResult object to create a custom audit result record in the CMDB. If you do not create an audit result object, Cloud Configuration Governance reports the violation as per the violation definition specified in the policy.
-   `false`: Do not report the violation.

</td></tr><tr><td>

`violatingConfigSettings`

</td><td>

JSON

</td><td>

Reason of the policy violation.**Syntax**

 ```
{
  "config_key": "value" 
};

```

</td></tr></tbody>
</table>## Scripting reference for the CI finder mapping script

<table id="table_n3s_1cf_ktb"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Schema

</th></tr></thead><tbody><tr><td>

`attributes`

</td><td>

A map containing the resource attribute key and attribute value from the Resource Attribute table for the given resource.

</td><td>

```
{
"LogicalDatacenter": "Referenced record",
"ServiceAccount": "Referenced record"
}
```

</td></tr></tbody>
</table><table id="table_kxd_dcf_ktb"><thead><tr><th>

Name

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`Name`

</td><td>

String

</td><td>

Name of the resource.

</td></tr><tr><td>

`identifier`

</td><td>

Resource record

</td><td>

Identifier of the Cloud Configuration Governance resource record.

</td></tr><tr><td>

`type`

</td><td>

Resource record

</td><td>

Resource type of the Cloud Configuration Governance resource resource.

</td></tr><tr><td>

`answer`

</td><td>

JSON

</td><td>

CI class with which the resource needs to be mapped.The `answer` contains the following information:

-   `sysId` of the CI class.
-   `tableName` of the CI class.

 If the CI finder mapping fails to identify the CI class, set this variable to `null`.

 **Syntax**

 ```
{ sysId: "value", tableName: "value" }
```

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Configuration Governance reference](ccg-reference.md)

