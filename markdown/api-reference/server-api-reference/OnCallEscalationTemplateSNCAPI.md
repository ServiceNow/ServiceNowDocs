---
title: OnCallEscalationTemplateSNC - Global
description: The OnCallEscalationTemplateSNC script include provides methods to apply escalation policy templates to escalation sets.Instantiates an OnCallEscalationTemplateSNC object.Applies an escalation policy template to an escalation set.Deletes all escalation step definition records associated with an escalation set.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OnCallEscalationTemplateSNC- Global

The OnCallEscalationTemplateSNC script include provides methods to apply escalation policy templates to escalation sets.

For more information about the escalation process, see [Defining On-Call Scheduling escalation process](https://www.servicenow.com/docs/access?context=defining-escalation-process-and-template&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

This script include requires the On-Call Scheduling plugin \(com.snc.on\_call\_rotation\).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OnCallEscalationTemplateSNC - OnCallEscalationTemplateSNC\(\)

Instantiates an OnCallEscalationTemplateSNC object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

This example instantiates an OnCallEscalationTemplateSNC object.

```
var escTemp = new global.OnCallEscalationTemplateSNC();
```

## OnCallEscalationTemplateSNC - copyEscalationTemplatetoEscalationSet\(String templateSysId, String escalationSetSysId\)

Applies an escalation policy template to an escalation set.

When the template is applied to the escalation set, escalation step definition records are created in the Shift Escalation Step Definition \[cmn\_rota\_esc\_step\_def\] table.

Before calling this method, call the deleteEscalationSetSteps\(\) method to delete existing escalation step definitions. If existing records are not deleted first, this method returns an error.

|Name|Type|Description|
|----|----|-----------|
|templateSysId|String|Sys\_id of the escalation policy template in the On-Call Escalation Policy Template \[on\_call\_template\_escalation\_policy\] table.|
|escalationSetSysId|String|Sys\_id of the escalation set in the Shift Escalation Set \[cmn\_rota\_escalation\_set\] table.|

<table id="table_xh5_3td_3xb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing error and warning messages. If the operation was successful, this object is empty.

**Note:** If an error occurs, the operation stops and the template is not applied. If a warning occurs, the operation continues and some records are still created.

 ```
{
  "error": "String", 
  "warning": {Object} 
}
```

</td></tr><tr><td>

&lt;Object&gt;.error

</td><td>

Error message.Possible errors:

-   Escalation policy template sys\_id is not correct.
-   Escalation set sys\_id is not correct.
-   Escalation step definitions already exist on escalation set.

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.warning

</td><td>

Information about any warnings.Data type: Object

```
{
  "message": "String", 
  "skipped_steps": [Array],
  "not_matching_steps": {Object},
}
```

</td></tr><tr><td>

&lt;Object&gt;.warning.message

</td><td>

Warning message.Possible warnings:

-   Roster position does not match the rosters on the shift
-   There are no audiences defined on the escalation step template

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.warning.skipped\_steps

</td><td>

Indexes of any escalation steps that were skipped \(1-based\).Data type: Array

</td></tr><tr><td>

&lt;Object&gt;.warning.not\_matching\_steps

</td><td>

Object containing information about any escalation steps that do not have available rosters in the format `{"step number":[roster number]}`.For example, if the return value is `{"3":[3]}`, then at escalation step three the tertiary roster is not available.

Data type: Object

</td></tr></tbody>
</table>This example applies the Rotate through rosters escalation policy template to the Service Desk – Default escalation set. The return object is empty because there are no errors or warnings.

```
var escSetSysId = "32820dc3eb422110249e8d835d5228c3";
var templateSysId = "a89e2982eb592110249e8d835d522825";
var escTemp = new global.OnCallEscalationTemplateSNC();

// delete existing escalation step definitions before applying the template
escTemp.deleteEscalationSetSteps(escSetSysId);

var result = escTemp.copyEscalationTemplatetoEscalationSet(templateSysId, escSetSysId);
gs.info(JSON.stringify(result));
```

Output:

```
{}
```

This example applies the Rotate through roster escalation policy template to the Working Hours – Default escalation set. In this case, the Application Development shift has only two rosters but the template tries to assign a third roster. Since the number of rosters doesn't match, a warning is thrown. Two records are still created in the Shift Escalation Step Definition \[cmn\_rota\_esc\_step\_def\] table.

```
var escSetSysId = "e4f8f73deb562110249e8d835d522852";
var templateSysId = "a89e2982eb592110249e8d835d522825";
var escTemp = new global.OnCallEscalationTemplateSNC();

// delete existing escalation step definitions before applying the template
escTemp.deleteEscalationSetSteps(escSetSysId);

var result = escTemp.copyEscalationTemplatetoEscalationSet(templateSysId, escSetSysId);
gs.info(JSON.stringify(result));
```

Output:

```
{
   "warning": {
      "message": "Skipped copying templates for some of the steps since no audiences are defined",
      "not_matching_steps": {
         "3": [
            3
         ]
      },
      "skipped_steps": [
         "3"
      ]
   }
}
```

## OnCallEscalationTemplateSNC - deleteEscalationSetSteps\(String escalationSetSysId\)

Deletes all escalation step definition records associated with an escalation set.

|Name|Type|Description|
|----|----|-----------|
|escalationSetSysId|String|Sys\_id of the escalation set in the Shift Escalation Set \[cmn\_rota\_escalation\_set\] table.|

|Type|Description|
|----|-----------|
|None| |

This example deletes all escalation step definitions associated with the Service Desk – Default escalation set.

```
var escSetSysId = "32820dc3eb422110249e8d835d5228c3";

var escTemp = new global.OnCallEscalationTemplateSNC();

escTemp.deleteEscalationSetSteps(escSetSysId);
```

