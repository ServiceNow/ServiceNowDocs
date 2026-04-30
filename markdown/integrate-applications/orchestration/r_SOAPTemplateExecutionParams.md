---
title: SOAP template execution parameters
description: You use execution parameters to create the input process script in the Pre processing form of the activity designer.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a SOAP web service activity, Orchestration custom activity templates, Orchestration activity designer, Classic Orchestration, Workflow Data Fabric]
---

# SOAP template execution parameters

You use execution parameters to create the input process script in the **Pre processing** form of the activity designer.

For descriptions of the SOAP web service command fields, see the table in [Configure the SOAP execution command](../task/t_MapSOAPVariablesToExecutionComm.md).

**Note:** You must use the `executionParam.` prefix with all variables in this table.

<table id="table_bnp_vzn_cr"><thead><tr><th>

Name

</th><th>

Variable

</th><th>

Type

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Web service message

</td><td>

web\_service\_message

</td><td>

Reference

</td><td>

The sys\_id of the corresponding SOAP message.

</td></tr><tr><td>

Web service message function

</td><td>

web-service\_message\_function

</td><td>

Reference

</td><td>

The sys\_id of the SOAP message function.

</td></tr><tr><td>

Web service endpoint

</td><td>

web\_service\_endpoint

</td><td>

String

</td><td>

URL of the SOAP endpoint.

</td></tr><tr><td>

Parameters

</td><td>

parameters

</td><td>

Array of JavaScript objects

</td><td>

Array of JavaScript objects, expressed with the `executionParam`. prefix. For instructions on creating arrays using this parameter, see [Create a JavaScript array in a SOAP template](../task/t_CrtJvScrArrSTemplate.md).

</td></tr><tr><td>

Use mid server

</td><td>

use\_mid\_server

</td><td>

Boolean

</td><td>

When true, indicates that a MID Server is used.

</td></tr><tr><td>

MidCapabilities

</td><td>

midCapabilities

</td><td>

String \(comma separated\)

</td><td>

List of references to required MID Server capabilities.

</td></tr><tr><td>

Time out

</td><td>

time\_out

</td><td>

String

</td><td>

Allowed duration of the SOAP web service request before it times out, in seconds. The default is **10**.

</td></tr><tr><td>

ValueCapabilities

</td><td>

valueCapabilities

</td><td>

Array of hashmap

</td><td>

Capability values used to select the MID Server. For more information, see [MID Server capabilities](https://www.servicenow.com/docs/access?context=t_ConfigureCapabilities&version=zurich&pubname=zurich-servicenow-platform&section=r_MIDServerCapabilities&ft:locale=en-US). Use this example to customize the MID Server selection if there are additional capabilities that are assigned by value: ```
var valueCapability = {'NEW_MID_CAPABIILTY':'NEW_MID_CAPABILITY_VALUE'}; executionParam.valueCapabilities.push(valueCapability);
```

</td></tr><tr><td>

Auth Type

</td><td>

auth\_type

</td><td>

Boolean

</td><td>

Type of credentials to use. The choices are:-   basic\_auth\_pick\_credentials
-   use\_existing\_credentials

</td></tr><tr><td>

Credentials

</td><td>

credentials

</td><td>

Reference

</td><td>

Credentials to use for this SOAP message when the `auth_type` is `basic_auth_pick_credentials`.

</td></tr></tbody>
</table>**Parent Topic:**[Create a SOAP web service activity](../task/t_CreateASOAPWebServiceActivity.md)

