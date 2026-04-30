---
title: REST Message legacy workflow activity
description: The legacy REST Message activity enables an administrator to override the REST endpoint or supply the variables configured in the REST Message module.
locale: en-US
release: zurich
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Utility workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# REST Message legacy workflow activity

The legacy **REST Message** activity enables an administrator to override the REST endpoint or supply the variables configured in the REST Message module.

This activity is deprecated in the Zurich release and no longer shows up in the Workflow canvas for new workflow development. New workflows should use the [Orchestration](https://www.servicenow.com/docs/access?context=r-orchestration&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) REST Activity templates instead.

Existing workflows using it will continue to work as designed. To edit this activity in an existing workflow, you must [re-activate the activity](https://www.servicenow.com/docs/access?context=t_ReactivateDeprecatedActivity&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

The **REST Message** activity executes a dead link REST function \(POST, PUT, GET, or DELETE\) on an endpoint using values defined in the function record.

**Note:** If you want to use a MID Server to send the REST message, the MID Server must be accessible by the instance and configured to use SSH.

## Input variables

<table id="table_emf_3rl_sq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="subhead" colspan="2">

Rest Message

</td></tr><tr><td>

REST Message

</td><td>

Name of the [Create a REST message](https://www.servicenow.com/docs/access?context=t_ConfiguringARESTMessage&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) to run. This is a reference field to the REST Message \[sys\_rest\_message\] table \(**System Web Services** &gt; **Outbound** &gt; **REST Message**\).

</td></tr><tr><td>

REST Message Function

</td><td>

Function to call that is defined in a REST message function. This is a reference field to the HTTP Method \[sys\_rest\_message\_fn\] table \(**System Web Services** &gt; **Outbound** &gt; **REST Message**\). Available functions are **put**, **post**, **get**, or **delete**. You can edit functions in the **HTTP Methods** related list in each REST Message record.

</td></tr><tr><td>

REST Endpoint

</td><td>

REST endpoint to use instead of the **Endpoint** defined in the HTTP Method record. Leave this field blank to use the defined endpoint in the REST Message Function record.

</td></tr><tr><td class="subhead" colspan="2">

Rest Message Variables

</td></tr><tr><td>

Variables

</td><td>

Values to use for [Variable substitution in outbound REST messages](https://www.servicenow.com/docs/access?context=c_VariableSubstitutionREST&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) defined in the HTTP Method record. Use the following format for the string:

```
name1=value1, name2=value2, . . .
```

For example, use `name=${nameValue}, id=${idValue}` where *name* and *id* are function variables. If either the variable name or value contains a comma or equal sign, escape those characters with a backslash.

</td></tr><tr><td class="subhead" colspan="2">

Rest Message MID Server

</td></tr><tr><td>

Use MID Server

</td><td>

Check this box if you want to use a MID Server to send the REST message. A MID Server might be necessary to reach an endpoint within a firewall or a subnetwork that is not visible from the instance. If this check box is selected, but no MID Server is defined in the **MID Server** field, the workflow automatically attempts to find a MID Server based on IP range and the REST capability.

</td></tr><tr><td>

MID Server

</td><td>

Name of the MID Server to use. This field is available when **Use MID Server** is selected. The workflow ignores this parameter if the **use\_midserver** parameter is disabled.

</td></tr><tr><td class="subhead" colspan="2">

Rest Message Script

</td></tr><tr><td>

Sensor Script

</td><td>

The script to execute after the request has been made and a response has been received. You can access the full response body from the *activity.output* variable.

</td></tr></tbody>
</table>**Parent Topic:**[Utility workflow activities](../concept/c_UtilityActivities.md)

