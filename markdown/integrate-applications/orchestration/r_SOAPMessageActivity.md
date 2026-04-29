---
title: SOAP Message workflow activity
description: The SOAP Message activity uses SOAP messages defined in the System Web Services plugin and can call the messages using a MID Server.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Deprecated Orchestration activities, Activate Orchestration, Classic Orchestration, Workflow Data Fabric]
---

# SOAP Message workflow activity

The **SOAP Message** activity uses SOAP messages defined in the System Web Services plugin and can call the messages using a MID Server.

Your instance must have access to a MID Server configured to use SOAP.

## Input variables

<table id="table_cnt_xvl_sq"><thead><tr><th>

Field

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SOAP Message

</td><td>

soap\_message

</td><td>

The SOAP Message defined under the System Web Services plugin's Outbound SOAP Message \[sys\_soap\_message\] table. \(**System Web Services** &gt; **Outbound** &gt; **SOAP Message**\)

</td></tr><tr><td>

SOAP Message Function

</td><td>

soap\_message\_function

</td><td>

The function to call that is defined in the SOAP Message. Functions are listed in the **SOAP Message Functions** related list in each SOAP Message record.

</td></tr><tr><td>

SOAP Endpoint

</td><td>

soap\_endpoint

</td><td>

Endpoint to use instead of the **SOAP endpoint** value in the SOAP Message Function record. Leave this field blank to use the defined endpoint in the SOAP Message Function record.

</td></tr><tr><td>

Variables

</td><td>

variables

</td><td>

Variables to substitute into the SOAP **Envelope** defined in the SOAP Message Function record. Use this format for the string: ```
name1=value1, name2=value2, . . .
```

If either the name or value contains a comma or equal sign, escape these characters with a backslash.

</td></tr><tr><td>

Use MID Server

</td><td>

use\_midserver

</td><td>

Check box for using a MID Server to send the SOAP message. A MID Server might be necessary to reach an endpoint within a firewall or a sub-network that is not visible from the instance. If this check box is selected \(true\), but no MID Server is defined in the **MID Server** field, workflow automatically attempts to find a MID Server.

</td></tr><tr><td>

MID Server

</td><td>

midserver

</td><td>

Name of the MID Server to use. This field appears when you select the **Use MID Server** check box. The workflow ignores this parameter if the **use\_midserver** parameter is disabled.**Note:** You can only select a specific MID Server in the legacy SOAP message activity and REST messages. These legacy activities do not use the [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) available starting with the Istanbul release.

</td></tr><tr><td>

Sensor Script

</td><td>

sensor\_script

</td><td>

The script to execute after the request has been made and a response has been received. You can access the full XML response body from the activity.output object.

</td></tr></tbody>
</table>**Parent Topic:**[Deprecated Orchestration activities](r_OrchestrationBasicActivities.md)

