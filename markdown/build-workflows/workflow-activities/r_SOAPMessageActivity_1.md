---
title: SOAP Message legacy workflow activity
description: The legacy SOAP Message activity uses SOAP messages defined in the System Web Services plugin and can call the messages using a MID Server.
locale: en-US
release: xanadu
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Utility workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# SOAP Message legacy workflow activity

The legacy **SOAP Message** activity uses SOAP messages defined in the System Web Services plugin and can call the messages using a MID Server.

This activity is deprecated in the Xanadu release and no longer shows up in the Workflow canvas for new workflow development. New workflows should use the [Orchestration](https://www.servicenow.com/docs/access?context=r-orchestration&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) SOAP Activity templates instead.

Existing workflows using it will continue to work as designed. To edit this activity in an existing workflow, you must [re-activate the activity](https://www.servicenow.com/docs/access?context=t_ReactivateDeprecatedActivity&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

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

Check box for using a MID Server to send the SOAP message. A MID Server might be necessary to reach an endpoint within a firewall or a sub-network that is not visible from the instance. If this check box is selected \(true\), but no MID Server is defined in the **MID Server** field, Workflow automatically attempts to find a MID Server.

</td></tr><tr><td>

MID Server

</td><td>

midserver

</td><td>

Name of the MID Server to use. This field appears when you select the **Use MID Server** check box. The workflow ignores this parameter if the **use\_midserver** parameter is disabled.

</td></tr><tr><td>

Sensor Script

</td><td>

sensor\_script

</td><td>

The script to execute after the request has been made and a response has been received. You can access the full XML response body from the activity.output object.

</td></tr></tbody>
</table>**Parent Topic:**[Utility workflow activities](../concept/c_UtilityActivities.md)

