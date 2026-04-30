---
title: GlideElement - Scoped
description: The scoped GlideElement API provides a number of convenient script methods for dealing with fields and their values. Scoped GlideElement methods are available for the fields of the current glide record.Determines if the user's role permits the creation of new entries in the associated field.Indicates whether the user's role permits them to read the associated GlideRecord.Determines whether the user's role permits them to write to the associated GlideRecord.Determines if the current field has been modified. This functionality is available for all available data types, except Journal fields.Determines if the previous value of the current field matches the specified object.Determines if the new value of a field, after a change, matches the specified object.Returns the number of milliseconds since January 1, 1970, 00:00:00 GMT for a duration field. Does not require the creation of a GlideDateTime object because the duration field is already a GlideDateTime object.Returns the value of the specified attribute from the dictionary.Returns the Boolean value of the specified attribute from the dictionary.Returns the choice list for a specified field.Returns the choice label for the current choice.Returns the clear text value for Password \(2 way encrypted\) fields in scoped applications.Returns the formatted display value of a specified field from an associated GlideRecord object.Gets the display value of the field in the language passed as a parameter.Returns the field's element descriptor.Returns the phone number in international format.Returns the HTML value of a field.Returns either the most recent journal entry or all journal entries.Returns the object label.Gets the label value of the field in the language passed as a parameter.Returns the name of the field.Gets the table name for a reference element.Returns a GlideRecord object for a given reference element.Returns the name of the table on which the field resides.Determines if a field is null.Sets the value of a date/time element to the specified number of milliseconds since January 1, 1970 00:00:00 GMT.Sets the display value of the field.Adds an error message. Available in Fuji patch 3.Sets the field to the specified phone number.Sets the value of a field.Converts the value of a GlideRecord field to a string.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 19
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideElement- Scoped

The scoped GlideElement API provides a number of convenient script methods for dealing with fields and their values. Scoped GlideElement methods are available for the fields of the current glide record.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped GlideElement - canCreate\(\)

Determines if the user's role permits the creation of new entries in the associated field.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_iq2_gmp_fz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the current user has permissions to create new entries in the associated field.Possible values:

-   true: User can create new entries.
-   false: User cannot create new entries.

</td></tr></tbody>
</table>The following example shows how to determine if the user has permissions to create entries for the three most recent records in the Problem \[problem\] table.

```
var gr = new GlideRecord('problem');

// Get records in new state in Problem Table
gr.addQuery('state','101');

// Sort records in order of recent to earlier Created Date
gr.orderByDesc('sys_created_on');

// Limit the query to three records
gr.setLimit(3); 
gr.query();

while(gr.next()){
  if(gr.short_description.canCreate()){ ///check to see if the current user is allowed to create the record
  gs.info("I can create new records for the field Problem statement for - " + gr.number);
  }
}
```

Output:

```
I can create new records for the field Problem statement for - PRB0000004
I can create new records for the field Problem statement for - PRB0001000
I can create new records for the field Problem statement for - PRB0001001
```

### Scoped equivalent

To use the canCreate\(\) method in a scoped application, use the corresponding scoped method: [canCreate\(\)](c_GlideElementScopedAPI.md#).

## Scoped GlideElement - canRead\(\)

Indicates whether the user's role permits them to read the associated GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the field can be read, false otherwise.|

The following example shows how to get a list of active Incident records with a readable Short Description field.

```
var grIncident = new GlideRecord('incident');
grIncident.addEncodedQuery("active=true"); //Query the Incident table for active incidents
grIncident.orderByDesc('number');
grIncident.setLimit(3); // limit to three results for example
grIncident.query();

while (grIncident.next()) {
    if (grIncident.short_description.canRead()) { //check to see if the current user is allowed to read the record
        gs.info('You have permission to read the short description of: ' + grIncident.number + ' ' + grIncident.short_description);
    }
}
```

Output:

```
*** Script: You have permission to read the short description of: INC0009009 Unable to access the shared folder.
*** Script: You have permission to read the short description of: INC0009005 Email server is down.
*** Script: You have permission to read the short description of: INC0009001 Unable to post content on a Wiki page
```

## Scoped GlideElement - canWrite\(\)

Determines whether the user's role permits them to write to the associated GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the user can write to the field, false otherwise.|

The following example shows how to get a list of active Incident records with a writeable Short Description field.

```
var grIncident = new GlideRecord('incident');
grIncident.addEncodedQuery("active=true"); //Query the Incident table for active incidents
grIncident.orderByDesc('number');
grIncident.setLimit(3); // limit to three results for example
grIncident.query();

while (grIncident.next()) {
    if (grIncident.short_description.canWrite()) { //check to see if the current user is allowed to write to the record
        gs.info('You have permission to write to the short description of: ' + grIncident.number + ' ' + grIncident.short_description);
    }
}
```

Output:

```
*** Script: You have permission to write to the short description of: INC0009009 Unable to access the shared folder.
*** Script: You have permission to write to the short description of: INC0009005 Email server is down.
*** Script: You have permission to write to the short description of: INC0009001 Unable to post content on a Wiki page
```

## Scoped GlideElement - changes\(\)

Determines if the current field has been modified. This functionality is available for all available data types, except Journal fields.

**Note:** The changes\(\) method is not supported within ACL scripts.

**Note:** If the GlideRecord on which you are performing this method has only been initialized and read, and has not been written, the underlying before-and-after values are the same. In this case, the method returns "false", as there has been no change to the data store.

-   **Business rule execution**

    The ServiceNow AI Platform invokes business rules \(**BEFORE** or **AFTER**\) before resetting the internal previous values for columns \(GlideElement objects\) to the current values.

    This sequence enables the following actions:

    -   Triggering an **AFTER** business rule on &lt;column&gt;.changes conditions.
    -   Accessing the previous GlideRecord object in the script section.
    Even in **AFTER** business rules, `current.<field>.changes()` returns `true` because the internal previous values haven’t been reset yet. The condition `current.<field>.value != previous.<field>.value` also returns `true`.

    Previous values are only reset after the following activities:

    -   The database update is complete.
    -   All **AFTER** business rules have been processed.
    Inside an AFTER business rule, the changes\(\) method still returns `true` if the field value was modified, even though the rule executes after the update.


|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the fields have been changed, false if the field has not.|

The following example from a business rule shows how to create an event in the EventQueue if the value of the **assigned\_to** field changes. For a comprehensive example, see [Sample scripts from the change events business rule](https://www.servicenow.com/docs/access?context=r_ChangeEventsSampleScripts&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

```
if (!current.assigned_to.nil() && current.assigned_to.changes()) {
  gs.eventQueue('incident.assigned', current, current.assigned_to.getDisplayValue(), previous.assigned_to.getDisplayValue());
}
```

## Scoped GlideElement - changesFrom\(Object o\)

Determines if the previous value of the current field matches the specified object.

**Note:** If the GlideRecord on which you are performing this method has only been initialized and read, and has not been written, the underlying before-and-after values are the same. In this case, the method returns "false", as there has been no change to the data store.

|Name|Type|Description|
|----|----|-----------|
|o|Object|An object value to check against the previous value of the current field.|

|Type|Description|
|----|-----------|
|Boolean|True if the previous value matches, false if it does not.|

```
// The following example shows that in a business rule, if "active" field is changed from true, 
// insert a event in the EventQueue.
if (current.active.changesFrom(true)) {
  gs.eventQueue("incident.inactive", current, current.incident_state, previous.incident_state);
}
```

## Scoped GlideElement - changesTo\(Object o\)

Determines if the new value of a field, after a change, matches the specified object.

**Note:** The changesTo\(\) method is not supported within ACL scripts.

**Note:** If the GlideRecord on which you are performing this method has only been initialized and read, and has not been written, the underlying before-and-after values are the same. In this case, the method returns "false", as there has been no change to the data store.

|Name|Type|Description|
|----|----|-----------|
|o|Object|An object value to check against the new value of the current field.|

|Type|Description|
|----|-----------|
|Boolean|True if the previous value matches, false if it does not.|

```
// The following example shows that in a business rule, if "active" field is changed to false, 
// insert a event in the EventQueue.
if (current.active.changesTo(false)) {
  gs.eventQueue("incident.inactive", current, current.incident_state, previous.incident_state);
}
```

## Scoped GlideElement - dateNumericValue\(\)

Returns the number of milliseconds since January 1, 1970, 00:00:00 GMT for a duration field. Does not require the creation of a GlideDateTime object because the duration field is already a GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Number of milliseconds since January 1, 1970, 00:00:00 GMT.|

```
var inc = new GlideRecord('incident');
inc.get('17c90efb13418700cc36b1422244b05d');
gs.info(inc.calendar_duration.dateNumericValue());
```

Output:

```
98000
```

## Scoped GlideElement - getAttribute\(String attributeName\)

Returns the value of the specified attribute from the dictionary.

If the attribute is a boolean attribute, use getBooleanAttribute\(String\) to get the value as a boolean rather than as a string.

|Name|Type|Description|
|----|----|-----------|
|attributeName|String|Attribute name|

|Type|Description|
|----|-----------|
|String|Attribute value|

```
doit();
function doit() {
  var now_GR = new GlideRecord('sys_user');
  now_GR.query("user_name","admin");
  if (now_GR.next()) {
    gs.info("we got one");
    gs.info(now_GR.location.getAttribute("tree_picker"));
  }
}
```

## Scoped GlideElement - getBooleanAttribute\(String attributeName\)

Returns the Boolean value of the specified attribute from the dictionary.

To get the value as a string, use getAttribute\(string\).

|Name|Type|Description|
|----|----|-----------|
|attributeName|String|Attribute name|

|Type|Description|
|----|-----------|
|Boolean|Boolean value of the attribute. Returns false if the attribute does not exist.|

The following example shows how to get Boolean values of the **ignore\_filter\_on\_new** attribute for two fields.

```
var inc = new GlideRecord('incident');
inc.query();

if (inc.next())
 {
   // opened_by field has attribute "ignore_filter_on_new = true"
   gs.info(inc.opened_by.getBooleanAttribute("ignore_filter_on_new"));

  // short_description field does not have attribute ignore_filter_on_new
   gs.info(inc.short_description.getBooleanAttribute("ignore_filter_on_new"));
 }
```

Output:

```
true
false
```

## Scoped GlideElement - getChoices\(String dependent\)

Returns the choice list for a specified field.

The field for which to return the choice list is specified in the method call. For example: `var choices = glideRecord.urgency.getChoices();`. For information on choice list field types and their associated capabilities, see [Choice list field type](https://www.servicenow.com/docs/access?context=c_ChoiceLists&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|dependent|String|Optional. Field within the associated record on which the choice list field depends.|

|Type|Description|
|----|-----------|
|Array|List of possible values for the choice list, which are the values in the Choice \[sys\_choice\] table. If the **dependent** parameter is passed, the return results reflect only those choices available for the specified dependent field.|

```
var glideRecord = new GlideRecord('incident'); 
glideRecord.query('priority','1'); 
glideRecord.next(); 
 
// urgency has choice list: 1 - High, 2 - Medium, 3 - Low, with value: 1, 2, 3
var choices = glideRecord.urgency.getChoices();
```

## Scoped GlideElement - getChoiceValue\(\)

Returns the choice label for the current choice.

A choice has a value \(number\) and a label \(string\). This method returns the label.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The selected choice's label.|

```
var glideRecord = new GlideRecord('incident'); 
glideRecord.query('priority','1'); 
glideRecord.next(); 
 
// urgency has choice list: 1 - High, 2 - Medium, 3 - Low, with value: 1, 2, 3
var choiceLabel = glideRecord.urgency.getChoiceValue(); 
gs.info(choiceLabel);
```

Output:

```
1 - High
```

## Scoped GlideElement - getDecryptedValue\(\)

Returns the clear text value for Password \(2 way encrypted\) fields in scoped applications.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The clear text password.|

```
var tablename = 'x_scoped_app_table'
var CI = new GlideRecord(tablename);  
CI.addQuery('number', '0001002'); 
CI.query(); 
CI.next(); 

var password = CI.password_field
var decrypted = password.getDecryptedValue(); 
gs.info(decrypted);
```

Output:

```
x_scoped_app: cleartextpassword
```

## Scoped GlideElement - getDisplayValue\(Number maxCharacters\)

Returns the formatted display value of a specified field from an associated GlideRecord object.

Display values are manipulated based on the actual value in the database and user or system settings and preferences.

The display value that is returned is dependent on the field type.

-   Choice fields: The database value may be a number, but the display value will be more descriptive.
-   Date fields: The database value is in UTC format, while the display value is based on the user's time zone.
-   Encrypted text: The database value is encrypted, while the displayed value is unencrypted based on the user's encryption context.
-   Reference fields: The database value is sys\_id, but the display value is a display field of the referenced record.

For more information on display values, see [Display values](https://www.servicenow.com/docs/access?context=c_DisplayValues&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

maxCharacters

</td><td>

Number

</td><td>

Optional. Maximum characters desired.Default: All

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Display value of the specified field.|

The following example shows how to retrieve the display value of the priority field in an incident record.

```
var glideRecord = new GlideRecord('incident');
glideRecord.query('priority','1');
glideRecord.next();
gs.info(glideRecord.priority.getDisplayValue());
```

Output:

```
1 - Critical
```

The following example shows how to retrieve both the display value and internal value of specified fields in the incident database.

```
var now_GR = new GlideRecord('incident');
now_GR.get('9c573169c611228700193229fff72400'); //INC0000001
gs.info('Display Values:');
gs.info('Opened at ' + now_GR.opened_at.getDisplayValue());
gs.info('Opened by ' + now_GR.opened_by.getDisplayValue());
gs.info('Priority ' + now_GR.priority.getDisplayValue());
gs.info('Values:');
gs.info('Opened at ' + now_GR.opened_at.getValue());
gs.info('Opened by ' + now_GR.opened_by.getValue());
gs.info('Priority ' + now_GR.priority.getValue());

```

Output:

```
Display Values:
Opened at 2022-02-01 15:09:51
Opened by Joe Employee
Priority 1 - Critical
Values:
Opened at 2022-02-01 23:09:51
Opened by 681ccaf9c0a8016400b98a06818d57c7
Priority 1

```

## Scoped GlideElement - getDisplayValueLang\(String language\)

Gets the display value of the field in the language passed as a parameter.

The result is only applicable to translatable field types such as **Choice**, **Translated Field**, and **Translated Text**. For other field types, the result defaults to [getDisplayValue\(\)](c_GlideElementScopedAPI.md#).

You must have the corresponding language plugin to retrieve a translated value. For information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

See also [Scoped GlideElement - getLabelLang\(String language\)](c_GlideElementScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|language|String|Language tag conforming with IETF BCP-47.|

|Type|Description|
|----|-----------|
|String|Display value of the field in the language passed. If a translation isn't available, the method retrieves a value translated in the language of the current user. If a translation isn’t available, the result defaults to English.|

The following example shows how to get the original text and German-translated text from the **Accept** \(UI View\) title field.

```
var uiView = new GlideRecord("sys_ui_view");
uiView.get("fa776f6d97700100f309124eda2975bc");

gs.info("getDisplayValue: " + uiView.getElement("title").getDisplayValue());
gs.info("getDisplayValueLang: " + uiView.getElement("title").getDisplayValueLang("de"));
```

Output:

```
getDisplayValue: Accept
getDisplayValueLang: Akzeptieren
```

## Scoped GlideElement - getED\(\)

Returns the field's element descriptor.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideElementDescriptor|The field's element descriptor.|

```
var grInc = new GlideRecord('incident');
grInc.query('priority', '1');
 
var field = grInc.getElement('priority');
var ed = field.getED();
```

## Scoped GlideElement - getGlobalDisplayValue\(\)

Returns the phone number in international format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Phone number in international format.|

The following example shows how to get the phone number of a walk-up location. This example requires the Walk-up Experience plugin.

```
// Passing walkup location name and closed phone number in parameters
setWalkupLocPhone('Santa Clara Tech Lounge','phone_number');

function setWalkupLocPhone(locName, field) {
  var walkupLoc = new GlideRecord('wu_location_queue');
  walkupLoc.addQuery('name',locName);
  walkupLoc.query();
  walkupLoc.next();

  // Returns the phone number of walk-up location queue in international format
  gs.info(walkupLoc[field].getGlobalDisplayValue());
}
```

Output:

```
+91 98124 56789
```

## Scoped GlideElement - getHTMLValue\(Number maxChars\)

Returns the HTML value of a field.

|Name|Type|Description|
|----|----|-----------|
|maxChars|Number|Optional. Maximum number of characters to return.|

|Type|Description|
|----|-----------|
|String|HTML value for the field.|

```
var inccause = new GlideRecord("incident");
inccause.short_description = current.short_description;
inccause.comments = current.comments.getHTMLValue();
inccause.insert();
```

## Scoped GlideElement - getJournalEntry\(Number mostRecent\)

Returns either the most recent journal entry or all journal entries.

|Name|Type|Description|
|----|----|-----------|
|mostRecent|Number|If 1, returns the most recent entry. If -1, returns all journal entries.|

<table id="table_mpt_2wp_fz" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

For the most recent entry, returns a string that contains the field label, timestamp, and user display name of the journal entry.

 For all journal entries, returns the same information for all journal entries ever entered as a single string with each entry delimited by "\\n\\n".

</td></tr></tbody>
</table>```
//gets all journal entries as a string where each entry is delimited by '\n\n'
var notes = current.work_notes.getJournalEntry(-1); 
//stores each entry into an array of strings
var na = notes.split("\n\n");  
                      
for (var i = 0; i < na.length; i++)                 
  gs.info(na[i]);
```

## Scoped GlideElement - getLabel\(\)

Returns the object label.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Object label|

```
var now_GR = new GlideRecord("sc_req_item");
now_GR.addQuery("request", current.sysapproval);
now_GR.query();
while(now_GR.next()) {
var nicePrice = now_GR.price.toString();
    if (nicePrice != ) {
        nicePrice = parseFloat(nicePrice);
        nicePrice = nicePrice.toFixed(2);
    }
    template.print(now_GR.number + ":  " + now_GR.quantity + " X " + now_GR.cat_item.getDisplayValue() + " at $" + nicePrice + " each \n");
    template.print("    Options:\n");
    var variables = now_GR.variables.getElements();    
    for (var key in variables) {
      var now_V = variables[key];
      if(now_V.getQuestion().getLabel() != ) {
         template.space(4);
         template.print('     ' +  now_V.getQuestion().getLabel() + " = " + now_V.getDisplayValue() + "\n");  
      }
    }
}
```

## Scoped GlideElement - getLabelLang\(String language\)

Gets the label value of the field in the language passed as a parameter.

You must have the corresponding language plugin to retrieve a translated value. For information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

See also:

-   [getDisplayValueLang\(\)](c_GlideElementScopedAPI.md#)
-   [getLabel\(\)](c_GlideElementScopedAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|language|String|Language tag conforming with IETF BCP-47.|

|Type|Description|
|----|-----------|
|String|Value of the field label in the language passed. If a translation isn't available, the method retrieves a value translated in the language of the current user. If a translation isn’t available, the result defaults to English.|

The following example shows how to get the original label text and its German translation of the **Accept** \(UI View\) title.

```
var uiView = new GlideRecord("sys_ui_view");
uiView.get("fa776f6d97700100f309124eda2975bc");

gs.info("getLabel: " + uiView.getElement("title").getLabel());
gs.info("getLabelLang: " + uiView.getElement("title").getLabelLang("de"));
```

Output:

```
getLabel: Title
getLabelLang: Titel
```

## Scoped GlideElement - getName\(\)

Returns the name of the field.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Field name.|

The following example shows how to get the name and other values for each field in a sys\_user record.

```
var userRec = new GlideRecord("sys_user"); // GlideRecord to sys_user table

userRec.get("5137153cc611227c000bbd1bd8cd2005"); // Sys Id of user: Fred Luddy

var fields = userRec.getFields();

for (var i = 0; i < fields.size(); i++) {

    var field = fields.get(i);
    var name = field.getName(); // Name of the field
    var label = field.getLabel(); // Label of the field
    var value = field.getDisplayValue(); // Value of the field

    gs.info((Number(i) + 1) + ".\n" + "Field Label: " + label + "\n" + "Field Name: " + name + "\n" + "Field Value: " + value);

};
```

Output. Results include 62 fields and have been truncated with ellipsis points \(…\) to save space.

```
*** Script: 1.
Field Label: Country code
Field Name: country
Field Value: 
*** Script: 2.
Field Label: Calendar integration
Field Name: calendar_integration
Field Value: Outlook
...
*** Script: 47.
Field Label: First name
Field Name: first_name
Field Value: Fred
...
*** Script: 54.
Field Label: Last name
Field Name: last_name
Field Value: Luddy
...
```

## Scoped GlideElement - getReferenceTable\(\)

Gets the table name for a reference element.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Table name of the reference.|

```
var grINC = new GlideRecord('incident');
grINC.query('number','INC0010041'); // record assignment group assigned to "CAB Approval"
if (grINC.next()) { 
  // Get the table name 
  var tableName = grINC.assignment_group.getReferenceTable();
  gs.info( tableName ); 
}
```

## Scoped GlideElement - getRefRecord\(\)

Returns a GlideRecord object for a given reference element.

For calculated fields, this method fetches the referenced record and runs a calculation on a scripted default value.

**Warning:** If the reference element does not contain a value, it returns an empty GlideRecord object, not a NULL object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideRecord|A GlideRecord object|

```

var grINC = new GlideRecord('incident'); 
grINC.addNotNullQuery('caller_id'); 
grINC.query(); 
if (grINC.next()) { 

// Get a GlideRecord object for the referenced sys_user record 
var grUSER = grINC.caller_id.getRefRecord(); 
if (grUSER.isValidRecord()) 
  gs.info(grUSER.getValue('name')); 

} 
```

## Scoped GlideElement - getTableName\(\)

Returns the name of the table on which the field resides.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the table. The returned value may be different from the table Class that the record is in. See Tables and Classes in the product documentation.|

```
if (current.approver.getTableName() == "sysapproval_approver") {
  if (current.approver == email.from_sys_id)  {
     current.comments = "reply from: " + email.from + "\n\n" + email.body_text;
 
   // if it's been cancelled, it's cancelled.
  var doit = true;
  if (current.state=='cancelled')
      doit = false;
 
  if (email.body.state != undefined)
     current.state= email.body.state;
 
   if (doit)
      current.update();
} else {
   gs.log("Approval for task ("+current.sysapproval.getDisplayValue()+") rejected because user sending 
           email( "+email.from+") does not match the approver ("+current.approver.getDisplayValue()+")");
}
 
}
```

## Scoped GlideElement - nil\(\)

Determines if a field is null.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_bdf_zfr_2r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the field is null.Possible values:

-   true: Field is null.
-   false: Field is not null.

</td></tr></tbody>
</table>```
var glideRecord = new GlideRecord('incident'); 
glideRecord.query('priority','1'); 
glideRecord.next(); 
gs.info(glideRecord.state.nil());
```

Output:

```
false
```

## Scoped GlideElement - setDateNumericValue\(Number milliseconds\)

Sets the value of a date/time element to the specified number of milliseconds since January 1, 1970 00:00:00 GMT.

When called, setDateNumericValue\(\) automatically creates the necessary GlideDateTime/GlideDate/GlideDuration object, and then sets the element to the specified value.

**Note:** Before calling this method, the element must already exist by querying an existing record or by using the now\_GR.initialize\(\) method to initialize a new record.

|Name|Type|Description|
|----|----|-----------|
|milliseconds|Number|Number of milliseconds since 1/1/1970|

|Type|Description|
|----|-----------|
|void| |

```
var now_GR = new GlideRecord("incident");
now_GR.initialize();
now_GR.opened_at.setDateNumericValue(10000);
```

## Scoped GlideElement - setDisplayValue\(Object value\)

Sets the display value of the field.

|Name|Type|Description|
|----|----|-----------|
|value|Object|The value to set for the field.|

|Type|Description|
|----|-----------|
|void| |

```
var glideRecord = new GlideRecord('incident'); 
glideRecord.query('priority','1'); 
glideRecord.next();
 
//change the urgency to 3 
glideRecord.urgency.setDisplayValue('3 - Low');
gs.info(glideRecord.urgency);
```

## Scoped GlideElement - setError\(String errorMessage\)

Adds an error message. Available in Fuji patch 3.

|Name|Type|Description|
|----|----|-----------|
|errorMessage|String|The error message.|

|Type|Description|
|----|-----------|
|void| |

```
var glideRecord = new GlideRecord('incident');
glideRecord.query('priority','1');
glideRecord.next();
 
glideRecord.short_description.setError('Error text');
```

## Scoped GlideElement - setPhoneNumber\(Object phoneNumber, Boolean strict\)

Sets the field to the specified phone number.

This method is only available on a phone number GlideElement.

|Name|Type|Description|
|----|----|-----------|
|phoneNumber|Object|The phone number to set. This can be in either the international or local format.|
|strict|Boolean|When true, specifies that the number specified must match the correct format. When false, the system attempts to correct an improperly formatted phone number.|

<table id="table_fxy_3m2_bx" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the phone number value was set.Possible values:

 -   true: Value was set.
-   false: Value was not set.

</td></tr></tbody>
</table>The following example shows how to set the phone number of a walk-up location. This example requires the Walk-up Experience plugin.

```
setWalkupLocPhone('Santa Clara Tech Lounge','+91 9812456789'); 

function setWalkupLocPhone(locName, phoneNumber) {
  var walkupLoc = new GlideRecord('wu_location_queue');
  walkupLoc.addQuery('name', locName);
  walkupLoc.query();
  walkupLoc.next();
  
  // Set phone number of walk-up location
  var isPhoneNumberSet = walkupLoc.phone_number.setPhoneNumber(phoneNumber, true);
  walkupLoc.update();
  gs.info('Phone Number: ' + walkupLoc.phone_number);
  gs.info('Is phone number specified match the correct format: ' + isPhoneNumberSet);
}
```

Output:

```
Phone Number: +919812456789
Is phone number specified match the correct format: true
```

## Scoped GlideElement - setValue\(Object value\)

Sets the value of a field.

**Note:** Before calling this method, the element must already exist by querying an existing record or by using the now\_GR.initialize\(\) method to initialize a new record.

-   **Not for authentication with password2 fields**

    The setValue\(\) method passes password2 data as clear text, which results in an error about expecting encrypted data. Additionally, using the setValue\(\) method for password2 fields exposes data that should be encrypted.

    For password2 authentication, use the setDisplayValue\(\) method instead.

    See also:

    -   [Deprecate GlideEncrypter usage of 3DES for password2 fields](https://www.servicenow.com/docs/access?context=password2-3des-deprecation&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)
    -   [Alternatives to GlideEncrypter usage in knowledge base article KB1320986](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1320986)
    -   [Password2 encryption with the Key Management Framework \(KMF\)](https://www.servicenow.com/docs/access?context=password-2way-encrypted-fields&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

|Name|Type|Description|
|----|----|-----------|
|value|Object|Object value to set the field to.|

|Type|Description|
|----|-----------|
|None| |

Set the value passing a string.

```
var glideRecord = new GlideRecord('incident');
glideRecord.query('priority','1');
glideRecord.next();
glideRecord.short_description.setValue('Network failure');
```

Set the value passing an object.

```
var now_GR  = new GlideRecord('student');
now_GR.initialize();
now_GR.setValue('first_name', 'Joe');
now_GR.setValue('last_name', 'Smith');
now_GR.insert();
```

## Scoped GlideElement - toString\(\)

Converts the value of a GlideRecord field to a string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Value as a string.|

```
var glideRecord = new GlideRecord('incident');
glideRecord.query('priority','1');
glideRecord.next();
gs.info(glideRecord.opened_at.toString());
```

Output:

```
2019-08-31 23:09:51
```

