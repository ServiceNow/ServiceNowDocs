---
title: OnCallContactPrefTemplate - Global
description: The OnCallContactPrefTemplate script include provides methods to apply contact preference templates to escalation sets.Instantiates an OnCallContactPrefTemplate object.Applies a contact preference template to an escalation set.Deletes all contact preferences associated with an escalation set.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# OnCallContactPrefTemplate- Global

The OnCallContactPrefTemplate script include provides methods to apply contact preference templates to escalation sets.

For more information about the escalation process, see [Defining On-Call Scheduling escalation process](https://www.servicenow.com/docs/access?context=defining-escalation-process-and-template&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

This script include requires the On-Call Scheduling plugin \(com.snc.on\_call\_rotation\).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## OnCallContactPrefTemplate - OnCallContactPrefTemplate\(\)

Instantiates an OnCallContactPrefTemplate object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

This example instantiates an OnCallContactPrefTemplate object.

```
var contactPrefTemp = new global.OnCallContactPrefTemplate();
```

## OnCallContactPrefTemplate - copyContactPreferences\(String templateSysId, String escalationSetSysId\)

Applies a contact preference template to an escalation set.

When the template is applied to the escalation set, contact attempt records are created in the Shift Contact Preference \[cmn\_rota\_contact\_preference\] table.

Before calling this method, call the deleteContactPreferenceAttempts\(\) method to delete existing contact attempt records. If existing records are not deleted first, this method returns an error.

|Name|Type|Description|
|----|----|-----------|
|templateSysId|String|Sys\_id of the contact preference template in the On-Call Contact Preference Template \[on\_call\_template\_contact\_preference\] table.|
|escalationSetSysId|String|Sys\_id of the escalation set in the Shift Escalation Set \[cmn\_rota\_escalation\_set\] table.|

<table id="table_dgl_2rd_3xb" class="returns"><thead><tr><th>

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
  "warning": "String" 
}
```

</td></tr><tr><td>

&lt;Object&gt;.error

</td><td>

Error message.Possible values:

-   Contact preference template sys\_id is not correct
-   Escalation set sys\_id is not correct
-   Contact attempts exist already

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.warning

</td><td>

Warning message.Data type: String

</td></tr></tbody>
</table>This example applies a contact preference template to the Service Desk – Default escalation set. The return object is empty because there are no errors or warnings.

```
var escSetSysId = "a47ac1abeb5a6110249e8d835d5228aa";
var templateSysId = "f8dac9ebeb5a6110249e8d835d522873";

var contactPrefTemp = new global.OnCallContactPrefTemplate();

// delete existing contact attempt records before applying the template
contactPrefTemp.deleteContactPreferenceAttempts(escSetSysId); 

var result = contactPrefTemp.copyContactPreferences(templateSysId, escSetSysId);
gs.info(JSON.stringify(result));
```

Output:

```
{}
```

## OnCallContactPrefTemplate - deleteContactPreferenceAttempts\(String escalationSetSysId\)

Deletes all contact preferences associated with an escalation set.

All contact attempt records for the escalation set are deleted from the Shift Contact Preference \[cmn\_rota\_contact\_preference\] table.

|Name|Type|Description|
|----|----|-----------|
|escalationSetSysId|String|Sys\_id of the escalation set in the Shift Escalation Set \[cmn\_rota\_escalation\_set\] table.|

|Type|Description|
|----|-----------|
|None| |

This example deletes all contact preferences associated with the Service Desk – Default escalation set.

```
var escSetSysId = "a47ac1abeb5a6110249e8d835d5228aa";
var contactPrefTemp = new global.OnCallContactPrefTemplate();

contactPrefTemp.deleteContactPreferenceAttempts(escSetSysId);
```

