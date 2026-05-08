---
title: GlideElement - Global
description: The GlideElement API provides a number of convenient script methods for dealing with fields and their values. GlideElement methods are available for the fields of the current glide record.Determines if the user's role permits the creation of new entries in the associated field.Determines whether the user's role permits them to read the associated GlideRecord.Determines whether the user's role permits them to write to the associated GlideRecord.Determines if the current field has been modified. This functionality is available for all available data types, except Journal fields.Determines if the previous value of the current field matches the specified object.Determines if the new value of a field, after a change, matches the specified object.Returns the number of milliseconds since January 1, 1970, 00:00:00 GMT for a duration field. Does not require the creation of a GlideDateTime object because the duration field is already a GlideDateTime object.Debugs the object and adds debug messages using setError\(String\).Returns the value of the specified attribute from the dictionary.Gets the base table of the field.Returns a specified Boolean-type attribute from the dictionary as a Boolean value.Generates a choice list for a field. Returns the choice values from the base table only, not from the extended table.Gets the choice label for the current choice value.Gets the number of debug messages logged by debug\(\).Returns the field \(element\) that a specified field is dependent on.Returns the name of the table that a field is dependent on.Returns the formatted display value of the field.Returns the formatted display value of a field, or a specified substitute value if the display value is null or empty.Gets the display value of the field in the language passed as a parameter.Returns a dynamic attribute definition for this GlideElement.Returns a dynamic namespace object that is configured for the GlideElement.Gets the name of the dynamic namespace configured for the GlideElement.Returns an element descriptor, which provides information about specific fields, rather than the data inside of those fields.Returns the value for the specified element.Returns any error message associated with the specified element.Gets the escaped value for the current element.Gets the CSS style for the field.Retrieves the platform object associated with the field's value.Gets a glide record.Returns the HTML value of a field.Returns the HTML value of a field, or a specified substitute value if the HTML value is null or empty.Returns either the most recent journal entry or all journal entries.Returns the object's label.Gets the label value of the field in the language passed as a parameter.Returns the name of the field.Returns a GlideRecord object for a given reference element.Get the CSS style for the value.Returns the name of the table that contains the field.Retrieves the display value for the associated field and escapes the HTML.Returns the value of the field in the database.Retrieves the XHTML value of a field.Gets the XML value of a field as a string.Determines if a field has a specified attribute.Determines if the user has the right to perform a particular operation.Determines if the field has a value.Determines whether the field is null.Sets the duration field to a number of milliseconds since January 1, 1970, 00:00:00 GMT for a duration field. Does not require the creation of a GlideDateTime object because the duration field is already a GlideDateTime object.Sets the display value of the field.Adds an error message to the associated field.Sets the initial value of a field.Adds a journal entry and author as a work note or comment field.Sets the value of a field.Converts the field's value to a string.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 38
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideElement- Global

The GlideElement API provides a number of convenient script methods for dealing with fields and their values. GlideElement methods are available for the fields of the current glide record.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideElement - canCreate\(\)

Determines if the user's role permits the creation of new entries in the associated field.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_xln_v51_kt" class="returns"><thead><tr><th>

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

To use the canCreate\(\) method in a scoped application, use the corresponding scoped method: [canCreate\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - canRead\(\)

Determines whether the user's role permits them to read the associated GlideRecord.

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

### Scoped equivalent

To use the canRead\(\) method in a scoped application, use the corresponding scoped method: [canRead\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - canWrite\(\)

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

### Scoped equivalent

To use the canWrite\(\) method in a scoped application, use the corresponding scoped method: [canWrite\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - changes\(\)

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
|Boolean|True if the field has changed, false otherwise.|

The following example from a business rule shows how to create an event in the EventQueue if the value of the **assigned\_to** field changes. For a comprehensive example, see Sample scripts from the change events business rule.

```
if (!current.assigned_to.nil() && current.assigned_to.changes()) {
  gs.eventQueue('incident.assigned', current, current.assigned_to.getDisplayValue(), previous.assigned_to.getDisplayValue());
}
```

### Scoped equivalent

To use the changes\(\) method in a scoped application, use the corresponding scoped method: [changes\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - changesFrom\(Object value\)

Determines if the previous value of the current field matches the specified object.

**Note:** If the GlideRecord on which you are performing this method has only been initialized and read, and has not been written, the underlying before-and-after values are the same. In this case, the method returns "false", as there has been no change to the data store.

|Name|Type|Description|
|----|----|-----------|
|value|Object|An object value to check against the previous value of the current field.|

|Type|Description|
|----|-----------|
|Boolean|True if the previous value matches the parameter, false if it does not.|

```
if (theState.changesTo(resolvedState)) {
  operation = 4; //Resolved
}
else if (theState.changesTo(closedState)) {
  operation = 11; //Resolution Accepted
}
else if (theState.changesFrom(resolvedState) || theState.changesFrom(closedState)) {
  operation = 10; //Re-open
}
else {
  operation = 6; //Update
}
```

### Scoped equivalent

To use the changesFrom\(\) method in a scoped application, use the corresponding scoped method: [changesFrom\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - changesTo\(Object value\)

Determines if the new value of a field, after a change, matches the specified object.

**Note:** The changesTo\(\) method is not supported within ACL scripts.

**Note:** If the GlideRecord on which you are performing this method has only been initialized and read, and has not been written, the underlying before-and-after values are the same. In this case, the method returns "false", as there has been no change to the data store.

|Name|Type|Description|
|----|----|-----------|
|value|Object|An object value to check against the new value of the current field.|

|Type|Description|
|----|-----------|
|Boolean|True if the new value matches the parameter, false if it does not.|

```
if (theState.changesTo(resolvedState)) {
  operation = 4; //Resolved
}
else if (theState.changesTo(closedState)) {
  operation = 11; //Resolution Accepted
}
else if (theState.changesFrom(resolvedState) || theState.changesFrom(closedState)) {
  operation = 10; //Re-open
}
else {
  operation = 6; //Update
}
```

### Scoped equivalent

To use the changesTo\(\) method in a scoped application, use the corresponding scoped method: [changesTo\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - dateNumericValue\(\)

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

Output: 98000

### Scoped equivalent

To use the dateNumericValue\(\) method in a scoped application, use the corresponding scoped method: [dateNumericValue\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - debug\(Object o\)

Debugs the object and adds debug messages using setError\(String\).

|Name|Type|Description|
|----|----|-----------|
|o|Object|An object to debug.|

|Type|Description|
|----|-----------|
|None| |

## GlideElement - getAttribute\(String attributeName\)

Returns the value of the specified attribute from the dictionary.

For Boolean attributes, you can use the getBooleanAttribute\(\) method to return the value as a Boolean instead of a string.

|Name|Type|Description|
|----|----|-----------|
|attributeName|String|Name of the attribute. The attribute name is listed in the Dictionary Entries \[sys\_dictionary\] table.|

|Type|Description|
|----|-----------|
|String|Value of the specified attribute.|

The following example shows how to get the value of the **tree\_picker** attribute in the **location** column of the User \[sys\_user\] table as a string.

```
var now_GR = new GlideRecord('sys_user');
now_GR.query("user_name","admin");

if (now_GR.next()) {
   gs.info("The value of the tree_picker attribute in the location column is " + now_GR.location.getAttribute("tree_picker"));
}
```

Output:

```
The value of the tree_picker attribute in the location column is true
```

### Scoped equivalent

To use the getAttribute\(\) method in a scoped application, use the corresponding scoped method: [getAttribute\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getBaseTableName\(\)

Gets the base table of the field.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the base table. This name might be different from the table that the field is defined on. See Table extension and classes in the product documentation.|

The following example shows how to the base table for the Assignment Group field of an Incident record.

```
var gr = new GlideRecord('incident');

//query the Incident Records which have category as Inquiry/Help
gr.addQuery('category','inquiry');

// sort them in the order of earlier to recent created date
gr.orderBy('sys_created_on');
gr.query();

if(gr.next()){ //If at least any one record exists matching this query

  //Print the base table for the Assignment Group field
  gs.print("The Base Table for the field Assignment Group is - " + gr.assignment_group.getBaseTableName()); 
};
```

Output:

```
The Base Table for the field Assignment Group is - task
```

## GlideElement - getBooleanAttribute\(String attributeName\)

Returns a specified Boolean-type attribute from the dictionary as a Boolean value.

To return the attribute value as a string, use the getAttribute\(\) method.

|Name|Type|Description|
|----|----|-----------|
|attributeName|String|Name of the attribute. The attribute name is listed in the Dictionary Entries \[sys\_dictionary\] table.|

|Type|Description|
|----|-----------|
|Boolean|Specifies the value of the attribute as Boolean true or false.|

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

### Scoped equivalent

To use the getBooleanAttribute\(\) method in a scoped application, use the corresponding scoped method: [getBooleanAttribute\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getChoices\(String dependent\)

Generates a choice list for a field. Returns the choice values from the base table only, not from the extended table.

|Name|Type|Description|
|----|----|-----------|
|dependent|String|Optional. Field within the associated record on which the choice list field depends.|

|Type|Description|
|----|-----------|
|array list|The choice values for the field.|

```
var glideRecord = new GlideRecord('incident'); 
glideRecord.query('priority','1'); 
glideRecord.next(); 
 
// urgency has choice list: 1 - High, 2 - Medium, 3 - Low, with value: 1, 2, 3
var choices = glideRecord.urgency.getChoices();
```

### Scoped equivalent

To use the getChoices\(\) method in a scoped application, use the corresponding scoped method: [getChoices\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getChoiceValue\(\)

Gets the choice label for the current choice value.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The choice label.|

The following example shows how to get the choice label for change request records with the a priority value of Normal.

```
var gr = new GlideRecord('change_request');

//query for the change records with change type as "Normal"
gr.addQuery('type','normal');

// sort them in the order of recent to earlier Created Date
gr.orderByDesc('sys_created_on'); 

// limit the query to 4 records
gr.setLimit(4); 
gr.query();

while(gr.next()){
 //Printing the choice label for those records
 gs.print("The label of the current priority '"+ gr.priority+"' for the change request - " + gr.number + " is - "+ gr.priority.getChoiceValue()); 
}
```

Output:

```
The label of the current priority '4' for the change request - CHG0000014 is - 4 - Low
The label of the current priority '4' for the change request - CHG0000013 is - 4 - Low
The label of the current priority '4' for the change request - CHG0000012 is - 4 - Low
The label of the current priority '4' for the change request - CHG0000011 is - 4 - Low
```

### Scoped equivalent

To use the getChoiceValue\(\) method in a scoped application, use the corresponding scoped method: [getChoiceValue\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getDebugCount\(\)

Gets the number of debug messages logged by debug\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of debug messages.|

## GlideElement - getDependent\(\)

Returns the field \(element\) that a specified field is dependent on.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the field on which the current field depends. Null if no dependencies.|

The following example shows how to find the parent field of the Configuration Item field using the getDependent\(\) method.

```
var inc_gr = new GlideRecord('incident');
inc_gr.get('985f53d82fab301032e8808cf699b6e8'); // Get a particular Incident

var field_element = inc_gr.getElement('cmdb_ci'); // Get the Configuration Item element
var dependent_field = field_element.getDependent(); // Read the dependent field
gs.info("Dependent field: " + dependent_field);
if(dependent_field)
  {
    var dependent_field_value = inc_gr.getValue(dependent_field);  
    if(!dependent_field_value)
      {
        var base_table = field_element.getRefRecord(); // Retrieve the reference record
        var dependent_field_value = base_table.getValue(dependent_field); // Read the parent field value
      }
    inc_gr.setValue(dependent_field, dependent_field_value); // Update the parent field on the Incident
    inc_gr.update();
  }
```

Output:

```
company
```

## GlideElement - getDependentTable\(\)

Returns the name of the table that a field is dependent on.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the table if a field has a dependent table; null otherwise.|

The following example shows how to determine if a field named **model\_id** has a dependent table.

```
var gr = new GlideRecord('cmdb_ci_hardware');
gr.setLimit(1);
gr.query();

if (gr.next()) {
    var field_element = gr.getElement('model_id'); // Get the model_id field element
    var dependent_table = field_element.getDependentTable(); // Get the table that drives filtering

    gs.info("Field: " + field_element.getLabel());
    gs.info("Dependent table: " + dependent_table); // cmdb_model_category

    if (dependent_table) {
        // Use the dependent table to query what's controlling the filter
        var dep_gr = new GlideRecord(dependent_table);
        if (dep_gr.get(gr.getValue('model_category'))) {
            gs.info("Controlling record: " + dep_gr.getDisplayValue());
            gs.info("Only models belonging to category '" + dep_gr.getDisplayValue() + "' are valid for this CI");
        }
    }
}
```

Output:

```
Field: Model ID
Dependent table: null
```

## GlideElement - getDisplayValue\(Number maxChar\)

Returns the formatted display value of the field.

Display values are manipulated based on the actual value in the database and user or system settings and preferences.

The display value that is returned is dependent on the field type.

-   Choice fields: The database value may be a number, but the display value will be more descriptive.
-   Date fields: The database value is in UTC format, while the display value is based on the user's time zone.
-   Encrypted text: The database value is encrypted, while the displayed value is unencrypted based on the user's encryption context.
-   Reference fields: The database value is sys\_id, but the display value is a display field of the referenced record.

|Name|Type|Description|
|----|----|-----------|
|maxChar|Number|Optional. Maximum number of characters to return.|

|Type|Description|
|----|-----------|
|String|Display value of the field.|

```
var fields = current.getFields();
for (var i = 0; i < fields.size(); i++) { 
  var field = fields.get(i);
  var name = field.getName(); 
  var value = field.getDisplayValue(); 
  gs.print(i + ". " + name + "=" + value); 
}
```

### Scoped equivalent

To use the getDisplayValue\(\) method in a scoped application, use the corresponding scoped method: [getDisplayValue\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getDisplayValueExt\(Number maxChar, String nullSub\)

Returns the formatted display value of a field, or a specified substitute value if the display value is null or empty.

Display values are manipulated based on the actual value in the database and user or system settings and preferences.

The display value that is returned is dependent on the field type.

-   Choice fields: The database value may be a number, but the display value will be more descriptive.
-   Date fields: The database value is in UTC format, while the display value is based on the user's time zone.
-   Encrypted text: The database value is encrypted, while the displayed value is unencrypted based on the user's encryption context.
-   Reference fields: The database value is sys\_id, but the display value is a display field of the referenced record.

<table id="table_q5w_5hc_kt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

maxChar

</td><td>

Number

</td><td>

Optional. Maximum number of characters to be returned.Default: All

</td></tr><tr><td>

nullSub

</td><td>

String

</td><td>

Value to return if the display value is null or empty.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Formatted display value of the field, or the specified substitute value.|

The following example shows how to display the two most recent active records in the Incident \[incident\] table.

```
var gr = new GlideRecord('incident');
gr.addQuery('active', true);      // get the active records
gr.orderByDesc('sys_updated_on'); // sort the records from most recent to oldest updated date
gr.setLimit(2);                   // limit the query to 2 records
gr.query();

while(gr.next()){ // Printing the Display Value of the Configuration Item field. 
  // If the Display Value is Null/Empty, then it will be substituted with Default value "I with Null/Empty Display Value"
  gs.info("The Display Value of the Configuration Item for the incident - "+ gr.number+ " is " + gr.cmdb_ci.getDisplayValueExt(40, " CI with Null/Empty Display Value"));
}
```

Output:

```
The Display Value of the Configuration Item for the incident - INC0007001 is  CI with Null/Empty Display Value
The Display Value of the Configuration Item for the incident - INC0000069 is NYC RAC
```

## GlideElement - getDisplayValueLang\(String language\)

Gets the display value of the field in the language passed as a parameter.

The result is only applicable to translatable field types such as **Choice**, **Translated Field**, and **Translated Text**. For other field types, the result defaults to [getDisplayValue\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

You must have the corresponding language plugin to retrieve a translated value. For information, see Activate a language.

See also [Scoped GlideElement - getLabelLang\(String language\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

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

### Scoped equivalent

To use the getDisplayValueLang\(\) method in a scoped application, use the corresponding scoped method: [getDisplayValueLang\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getDynamicAttribute\(\)

Returns a dynamic attribute definition for this GlideElement.

Dynamic attributes have a defined data type and a sys\_id. For more details on dynamic attributes, see Dynamic schema.

See also:

-   [GlideDynamicAttribute - Global](../../GlideDynamicAttribute/concept/GlideDynamicAttributeAPI.md#)
-   [GlideDynamicAttributeStore - Global](../../GlideDynamicAttributeStore/concept/GlideDynamicAttStoreAPI.md#)
-   [GlideDynamicNamespace - Global](../../GlideDynamicNamespace/concept/GlideDynamicNamespaceAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|IDynamicAttribute|Object describing the attribute that the GlideElement represents.|

The following example shows how to get values of the make attribute from the u\_inc\_dynamic\_schema dynamic attribute store column on the incident table.

```
var gr_Inc = new GlideRecord('incident');
gr_Inc.query();
if(gr_Inc.next()) {
    var attr = gr_Inc.getDynamicAttribute('inc_dynamic_schema->make');
    gs.info(attr.getValue());
}
```

## GlideElement - getDynamicNamespace\(\)

Returns a dynamic namespace object that is configured for the GlideElement.

Dynamic attributes have a defined data type and a sys\_id. For more details on dynamic attributes, see Dynamic schema.

See also:

-   [GlideDynamicAttribute - Global](../../GlideDynamicAttribute/concept/GlideDynamicAttributeAPI.md#)
-   [GlideDynamicAttributeStore - Global](../../GlideDynamicAttributeStore/concept/GlideDynamicAttStoreAPI.md#)
-   [GlideDynamicNamespace - Global](../../GlideDynamicNamespace/concept/GlideDynamicNamespaceAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|IDynamicNamespace|Object describing the dynamic namespace.|

The following example shows how to retrieve the namespace object configured for the inc\_dynamic\_schema dynamic attribute store column on the incident table.

```
var gr_Inc = new GlideRecord('incident');
gr_Inc.query();
if (gr_Inc.next()) {
    var ge_Make = gr_Inc.getElement('inc_dynamic_schema->make');
    var namespace = ge_Make.getDynamicNamespace();
 
    gs.info("toString:    " + namespace);
    gs.info("name:        " + namespace.getName());
    gs.info("isActive:    " + namespace.isActive());
    gs.info("isTransient: " + namespace.isTransient());
}
```

Output:

```
toString:    incident/inc_dynamic_schema
name:        incident/inc_dynamic_schema
isActive:    true
isTransient: false
```

## GlideElement - getDynamicNamespaceName\(\)

Gets the name of the dynamic namespace configured for the GlideElement.

Dynamic attributes have a defined data type and a sys\_id. For more details on dynamic attributes, see Dynamic schema.

See also:

-   [GlideDynamicAttribute - Global](../../GlideDynamicAttribute/concept/GlideDynamicAttributeAPI.md#)
-   [GlideDynamicAttributeStore - Global](../../GlideDynamicAttributeStore/concept/GlideDynamicAttStoreAPI.md#)
-   [GlideDynamicNamespace - Global](../../GlideDynamicNamespace/concept/GlideDynamicNamespaceAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the dynamic namespace.|

The following example shows how to return the dynamic attribute namespace name.

```
// Gets the name of the namespace from the inc_dynamic_schema dynamic_attribute_store column on the incident table
 
var gr_Inc = new GlideRecord('incident');
gr_Inc.query();
if (gr_Inc.next()) {
    var ge_Make = gr_Inc.getElement('inc_dynamic_schema->make');
    gs.info(ge_Make.getDynamicNamespaceName());
}
```

Output:

```
number,short_description,active
```

## GlideElement - getED\(\)

Returns an element descriptor, which provides information about specific fields, rather than the data inside of those fields.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|ElementDescriptor|The field's element descriptor.|

This example gets the fields and field descriptors for the current record.

```
var fields = current.getFields();
for (i=0; i<fields.size(); i++) { 
  var field = fields.get(i);
  var descriptor = field.getED(); 
  gs.print("type=" + descriptor.getType() + 
    " internalType=" + descriptor.getInternalType()); 
}
```

### Scoped equivalent

To use the getED\(\) method in a scoped application, use the corresponding scoped method: [getED\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getElementValue\(String value\)

Returns the value for the specified element.

|Name|Type|Description|
|----|----|-----------|
|value|String|Element whose value you want returned.|

|Type|Description|
|----|-----------|
|String|Value of the element.|

```
var fields = current.getFields();
for (var i = 0; i < fields.size(); i++) {
  var field = fields.get(i);
  var name = field.getName();

  // Returns the unformatted value of the element
  var value = field.getElementValue(name);
  var disValue = field.getDisplayValue();
  gs.print(i + ". " + name + " = " + value + ' display value = ' + disValue);
}
```

Output

```
1. cmdb_ci = 109562a3c611227500a7b7ff98cc0dc7 display value = Storage Area Network 001
2. impact = 2 display value = 2 - Medium
```

## GlideElement - getError\(\)

Returns any error message associated with the specified element.

Use the [setError\(\)](c_GlideElementAPI.md#) method to set an error on a specific field \(element\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Error message currently set for the specified element.|

This example shows how to set an error on the short\_description element and then read the error back.

```
var incidentGR = new GlideRecord('incident');
incidentGR.setLimit(1);
incidentGR.query();
if (incidentGR.next()) {
    incidentGR.short_description.setError('The description is too short.');
    gs.info(incidentGR.short_description.getError()); // 'The description is too short.'
}
```

Output:

```
The description is too short.
```

This example shows how to use **getError\(\)** in a function call.

```
// Before query business rule (order = 100)
(function executeRule(current, previous /*null when async*/) {
    var shortDescription = current.getValue('short_description');
    if (shortDescription.length < 10) {
        current.short_description.setError('The description is too short.');
        current.setAbortAction(true);
    }
})(current, previous);

// Before query business rule (order = 200)
(function executeRule(current, previous /*null when async*/) {
    var shortDescriptionErrMsg = current.short_description.getError();
    if (shortDescriptionErrMsg) {
        // Some error was set in one of the previous business rules.
    }
})(current, previous);
```

## GlideElement - getEscapedValue\(\)

Gets the escaped value for the current element.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The escaped value of the current element.|

The following example shows how to use the getEscapedValue\(\) method to display the contents of an Incident short description field with escape characters.

```
/*** Overview - Update incident short description with escape characters and printing ***/
var inc = new GlideRecord('incident');
inc.query();
inc.next();
inc.short_description = 'Can\'t log into SAP from my laptop today'; 
inc.update();
gs.info("Short Description: "+inc.getElement('short_description').toString()); //without escape characters
gs.info("Escaped Short Description: "+inc.getElement('short_description').getEscapedValue()); // with escape characters
```

Output:

```
Short Description: Can't log into SAP from my laptop today
Escaped Short Description: Can\'t log into SAP from my laptop today
```

## GlideElement - getFieldStyle\(\)

Gets the CSS style for the field.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The CSS style for the field.|

```
var fields = current.getFields();
for (var i = 0; i < fields.size(); i++) { 
  var field = fields.get(i);
  var css_style = field.getFieldStyle();  
  gs.print("CSS style" + "=" + css_style); 
}
```

## GlideElement - getGlideObject\(\)

Retrieves the platform object associated with the field's value.

For a use case, see [Modify GlideDateTime field values](../../../../../script/useful-scripts/reference/r_UsefulFieldScripts.md#section_mod-gdt-fields).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|A platform object corresponding to the field's data type, such as GlideDateTime. You can use this object for type-specific operations on the value. For example, date arithmetic, formatting, and timezone conversions that are not available when accessing the field value as a plain string.|

The following example shows how to calculate the duration between the opened date and Service Level Agreement \(SLA\) due date of an incident record.

```
// Query an incident record with both opened_at and sla_due populated
var incGr = new GlideRecord('incident');
incGr.addQuery('opened_at', '!=', '');
incGr.addQuery('sla_due', '!=', '');
incGr.setLimit(1);
incGr.query();

if (incGr.next()) {
    gs.info("Incident: " + incGr.getValue('number'));
    gs.info("Opened at: " + incGr.getValue('opened_at'));
    gs.info("SLA due: " + incGr.getValue('sla_due'));

    var duration = calcDateDelta(incGr.opened_at, incGr.sla_due);
    if (duration) {
        gs.info("Duration in seconds: " + duration.getNumericValue() / 1000);
        gs.info("Duration display value: " + duration.getDisplayValue());
    }
}

function calcDateDelta(start, end) {
    var realStart = start.getGlideObject();
    var realEnd = end.getGlideObject();

    // Use GlideDuration to calculate the difference between two GlideDateTime objects
    var startMS = realStart.getNumericValue();
    var endMS = realEnd.getNumericValue();
    var deltaMS = endMS - startMS;

    // Create a GlideDuration from the millisecond difference
    var duration = new GlideDuration(deltaMS);
    return duration;
}
```

Output:

```
Incident: INC0000031
Opened at: 2025-03-06 00:18:03
SLA due: 2025-03-06 08:18:03
Duration in seconds: 28800
Duration display value: 8 Hours
```

### Scoped equivalent

To use the getGlideObject\(\) method in a scoped application, use the corresponding scoped method: [getGlideObject\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getGlideRecord\(\)

Gets a glide record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideRecord|A glide record object.|

```
var grInc = new GlideRecord('incident');
grInc.get('sys_id','ef43c6d40a0a0b5700c77f9bf387afe3');
gs.info("Initial grInc - " + grInc.getDisplayValue());

var caller = grInc.getElement("caller_id");
doit(caller);

function doit(caller) {
  var now_GR = caller.getGlideRecord();
  gs.info("doit gr is - " + now_GR.getDisplayValue());
}
```

Output

```
*** Script: Initial grInc - INC0000050
*** Script: doit gr is - INC0000050
```

## GlideElement - getHTMLValue\(Number maxChars\)

Returns the HTML value of a field.

|Name|Type|Description|
|----|----|-----------|
|maxChars|Number|Optional. Maximum number of characters to return.|

|Type|Description|
|----|-----------|
|String|HTML value for the field.|

The following example shows how to get the HTML content of a meeting note.

```
/*
  getHTMLValueExt() This Function is used to get HTML Value of a field. It accepts 2 Parameters

a. maxChar- Number - The maximum number of characters to return.
b. nullSub - String - The value to return if the HTML value is null or empty.

*/


// get a cab meeting record by its sys_id
var gr = new GlideRecord('cab_meeting');
gr.addQuery('sys_id','7777777b6d2a20100sys70id534330f6');
gr.query();

if(gr.next()){
  var substituteString = 'Meeting Notes Unavailable';
  var maxLength = 50;
  gs.print(gr.meeting_notes.getHTMLValueExt(maxLength, substituteString));
}
```

### Scoped equivalent

To use the getHTMLValue\(\) method in a scoped application, use the corresponding scoped method: [getHTMLValue\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getHTMLValueExt\(Number maxChar, String nullSub\)

Returns the HTML value of a field, or a specified substitute value if the HTML value is null or empty.

|Name|Type|Description|
|----|----|-----------|
|maxChar|Number|The maximum number of characters to return.|
|nullSub|String|The value to return if the HTML value is null or empty.|

|Type|Description|
|----|-----------|
|String|The HTML value or the specified substitute value.|

The following example shows how to get the HTML content of a meeting note.

```
// get a cab meeting record by its sys_id
var gr = new GlideRecord('cab_meeting');
gr.addQuery('sys_id','7777777b6d2a20100sys70id534330f6');
gr.query();

if(gr.next()){
  var substituteString = 'Meeting Notes Unavailable';
  var maxLength = 50;
  gs.print(gr.meeting_notes.getHTMLValueExt(maxLength, substituteString));
}
```

Output if the meeting note for the record selected is not empty:

```
<p>Meeting note content.</p>
```

## GlideElement - getJournalEntry\(Number mostRecent\)

Returns either the most recent journal entry or all journal entries.

|Name|Type|Description|
|----|----|-----------|
|mostRecent|Number|If 1, returns the most recent entry. If -1, returns all journal entries.|

<table id="table_av3_wmc_kt" class="returns"><thead><tr><th>

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
  gs.print(na[i]);
```

### Scoped equivalent

To use the getJournalEntry\(\) method in a scoped application, use the corresponding scoped method: [getJournalEntry\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getLabel\(\)

Returns the object's label.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Object's label|

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

### Scoped equivalent

To use the getLabel\(\) method in a scoped application, use the corresponding scoped method: [getLabel\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getLabelLang\(String language\)

Gets the label value of the field in the language passed as a parameter.

You must have the corresponding language plugin to retrieve a translated value. For information, see Activate a language.

See also:

-   [getDisplayValueLang\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#)
-   [getLabel\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#)

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

### Scoped equivalent

To use the getLabelLang\(\) method in a scoped application, use the corresponding scoped method: [getLabelLang\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getName\(\)

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

### Scoped equivalent

To use the getName\(\) method in a scoped application, use the corresponding scoped method: [getName\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getRefRecord\(\)

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
grINC.notNullQuery('caller_id'); 
grINC.query(); 
if (grINC.next()) { 

// Get a GlideRecord object for the referenced sys_user record 
var grUSER = grINC.caller_id.getRefRecord(); 
if (grUSER.isValidRecord()) 
  gs.print( grUSER.getValue('name') ); 

} 
```

### Scoped equivalent

To use the getRefRecord\(\) method in a scoped application, use the corresponding scoped method: [getRefRecord\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getStyle\(\)

Get the CSS style for the value.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The CSS style for the value.|

```
// Get string of style field from Field Style record
var cssStyle = now_GR.state.getStyle();
```

## GlideElement - getTableName\(\)

Returns the name of the table that contains the field.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the table that contains the field that is called on. The returned value might be different from the table class that the record is in. For more information, see Table extension and classes.|

```
if (current.approver.getTableName() == "sysapproval_approver") {
    if (current.approver == email.from_sys_id) {
        current.comments = "reply from: " + email.from + "\n\n" + email.body_text;

        // if it's been cancelled, it's cancelled.
        var doit = true;
        if (current.state == 'cancelled')
            doit = false;

        if (email.body.state != undefined)
            current.state = email.body.state;

        if (doit)
            current.update();
    } else {
        gs.log("Approval for task " + current.sysapproval.getDisplayValue() +
            " rejected because user sending email " + email.from +
            " does not match the approver " + current.approver.getDisplayValue());
    }
}
```

### Scoped equivalent

To use the getTableName\(\) method in a scoped application, use the corresponding scoped method: [getTableName\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getTextAreaDisplayValue\(\)

Retrieves the display value for the associated field and escapes the HTML.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Escaped display value HTML for the associated field.|

The following example retrieves the display value of a KB article.

```
var grh = new GlideRecord('kb_knowledge');
grh.get('c85cd2519f77230088aebde8132e70c2');  // Knowledge record sys_id
var t = grh.text.getTextAreaDisplayValue(); // Text is HTML type field
var d = GlideXMLUtil.parseHTML(t); // Parse the HTML
var b = d.getDocumentElement().getTextContent().trim();
gs.info(b);
```

Output:

```
This article explains how to use automatic replies in Outlook 2010 for Exchange accounts.

Setting Up Automatic Replies

Click the 
File tab.
Click 
Automatic Replies.
Select 
Send automatic replies.
If desired, select the 
Only send during this time range check box to schedule when your out of office replies are active. If you do not specify a start and end time, auto-replies will be sent until you select the
 Do not send automatic replies check box.
On the 
Inside My Organization tab, type the response that you want to send to colleagues while you are out of the office.
On the 
Outside My Organization tab, select the 
Auto-reply to people outside my organization check box, and then type the response that you want to send while you are out of the office. Select whether you want replies sent to 
My contacts only or to 
Anyone outside my organization who sends you messages.

NOTE:
If you select 
My Contacts only in step 6, replies will be sent 
only to contacts that exist in your Contacts folder.



Using Rules With Automatic Replies
It is also possible to use rules to manage your messages while you are out of office. For example, you can create rules to automatically move or copy messages to other folders, to delete messages, to send custom replies, and so on.

Click the 
File tab.
Click 
Automatic Replies.
Click 
Rules, and then click 
Add Rule.
Under 
When a message arrives that meets the following conditions, specify the conditions that the message must meet for the rule to be applied. If you want to specify more conditions, click 
Advanced, enter or select the options that you want, and then click 
OK.
If you want to specify that this rule must be applied last, select the 
Do not process subsequent rules check box.
Under 
Perform these actions, select the actions that you want. You can select more than one action.
Click 
OK three times.

NOTES:

Automatic Replies rules can also be edited by following the above procedure.
To turn Automatic Replies rules on or off, in the Automatic Reply Rules dialog box, select or clear the check box of the rule that you want to turn on or off.

```

## GlideElement - getValue\(\)

Returns the value of the field in the database.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The value of the field.|

The following example retrieves the value of a specified field in the database.

```
var now_GR = new GlideRecord('incident');
now_GR.get('9c573169c611228700193229fff72400'); //INC0000001
gs.info('Display Values');
gs.info('Opened at ' + now_GR.opened_at.getDisplayValue());
gs.info('Opened by ' + now_GR.opened_by.getDisplayValue());
gs.info('Priority ' + now_GR.priority.getDisplayValue());
gs.info('Values');
gs.info('Opened at ' + now_GR.opened_at.getValue());
gs.info('Opened by ' + now_GR.opened_by.getValue());
gs.info('Priority ' + now_GR.priority.getValue());

```

Output:

```
Display Values
Opened at 2022-02-01 15:09:51
Opened by Joe Employee
Priority 1 - Critical
Values
Opened at 2022-02-01 23:09:51
Opened by 681ccaf9c0a8016400b98a06818d57c7
Priority 1

```

### Scoped equivalent

To use the getValue\(\) method in a scoped application, use the corresponding scoped method: [Scoped GlideElement - getValue\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - getXHTMLValue\(\)

Retrieves the XHTML value of a field.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The XHTML value|

## GlideElement - getXMLValue\(\)

Gets the XML value of a field as a string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The XML value|

## GlideElement - hasAttribute\(String attributeName\)

Determines if a field has a specified attribute.

|Name|Type|Description|
|----|----|-----------|
|attributeName|String|Name of the attribute. The attribute name is listed in the Dictionary Entries \[sys\_dictionary\] table.|

<table id="table_sbf_zrc_kt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether a field has the specified attribute.Valid values:

-   true: The field has the specified attribute.
-   false: The field does not have the specified attribute.

</td></tr></tbody>
</table>The following example shows how to get fields from the User \[sys\_user\] table with the **edge\_encryption\_enabled** attribute.

```
var fields = new GlideRecord('sys_user');

fields.query();

var userFields = fields.getFields();

for (var num = 0; num < userFields.size(); num++) {
    var ed = userFields.get(num).getED();

    if (ed.hasAttribute("edge_encryption_enabled")) {
        gs.info(userFields.get(num).getName());
    }
}
```

Output:

```
*** Script: hashed_user_id
*** Script: federated_id
```

## GlideElement - hasRightsTo\(String operationName\)

Determines if the user has the right to perform a particular operation.

|Name|Type|Description|
|----|----|-----------|
|operationName|String|Name of the operation to check for|

<table id="table_tpp_msc_kt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

True if the user has permission to perform the operation, false otherwise.Flag that indicates whether a user has permission to perform an operation.

 Valid values:

-   true: User has permissions.
-   false: User does not have permissions.

</td></tr></tbody>
</table>The following example shows how to determine if a user has rights to read a specific table.

```
// Pass table name and userId to check if user has read access against given table name
checkAccess('incident', 'adela.cervantsz');

function checkAccess(tableName, userID) {

    var inc = new GlideRecordSecure(tableName);
    inc.get('$[sys_id]');

    var secureManager = GlideSecurityManager.get();

    //fetch a different user, using user_name field on the target user record
    var userObj = gs.getUser().getUserByID(userID); 
    secureManager.setUser(userObj);

    var access = 'record/incident/read';

    //check if user has right to access
    var canRead = secureManager.hasRightsTo(access, inc); 
    gs.info('canRead: ' + canRead);
}
```

Output:

```
canRead: false
```

## GlideElement - hasValue\(\)

Determines if the field has a value.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the field has a value, false otherwise.|

## GlideElement - nil\(\)

Determines whether the field is null.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the field is null or an empty string, false otherwise.|

```
if (current.start_date.changes() || current.end_date.changes() || current.assigned_to.changes()) { 
  if (!current.start_date.nil() && !current.end_date.nil() && !current.assigned_to.nil()) {
 gs.eventQueue("change.calendar.notify", current, current.assigned_to, previous.assigned_to);
 
}
```

### Scoped equivalent

To use the nil\(\) method in a scoped application, use the corresponding scoped method: [nil\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - setDateNumericValue\(Number milliseconds\)

Sets the duration field to a number of milliseconds since January 1, 1970, 00:00:00 GMT for a duration field. Does not require the creation of a GlideDateTime object because the duration field is already a GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|milliseconds|Number|Number of milliseconds spanned by the duration.|

|Type|Description|
|----|-----------|
|void| |

```
var inc = new GlideRecord('incident');
inc.get('17c90efb13418700cc36b1422244b05d');
var timems = inc.calendar_duration.dateNumericValue();
timems = timems + 11*1000; 
inc.calendar_duration.setDateNumericValue(timems)
gs.info(inc.calendar_duration.getValue());
```

Output:

```
1970-01-01 00:01:38
```

### Scoped equivalent

To use the setDateNumericValue\(\) method in a scoped application, use the corresponding scoped method: [setDateNumericValue\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - setDisplayValue\(Object displayValue\)

Sets the display value of the field.

|Name|Type|Description|
|----|----|-----------|
|displayValue|Object|Value to be displayed.|

|Type|Description|
|----|-----------|
|void| |

### Scoped equivalent

To use the setDisplayValue\(\) method in a scoped application, use the corresponding scoped method: [setDisplayValue\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - setError\(String errorMessage\)

Adds an error message to the associated field.

You can retrieve the error message using the [getError\(\)](c_GlideElementAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|errorMessage|String|The error message.|

|Type|Description|
|----|-----------|
|None| |

```
if ((!current.u_date1.nil()) && (!current.u_date2.nil())) {
  var start = current.u_date1.getGlideObject().getNumericValue();
  var end = current.u_date2.getGlideObject().getNumericValue();
  if (start > end) {
    gs.addInfoMessage('start must be before end');
    current.setAbortAction(true);
    current.u_date1.setError('start must be before end');
  }
}
```

### Scoped equivalent

To use the setError\(\) method in a scoped application, use the corresponding scoped method: [setError\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - setInitialValue\(Object value\)

Sets the initial value of a field.

This method had been deprecated. Use [GlideElement - setValue\(Object value\)](c_GlideElementAPI.md#) for this functionality.

|Name|Type|Description|
|----|----|-----------|
|value|Object|Initial value for the field.|

|Type|Description|
|----|-----------|
|void| |

## GlideElement - setJournalEntry\(String entry, String userName\)

Adds a journal entry and author as a work note or comment field.

|Name|Type|Description|
|----|----|-----------|
|entry|String|Content of the journal entry.|
|userName|String|Optional. The user to attribute the journal entry to.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a work note and its author to a record.

```
var now_GR = new GlideRecord("incident");

now_GR.addQuery("sys_id", "<sys_id_value>");
now_GR.query();

if(now_GR.next()){
  now_GR.work_notes.setJournalEntry("Content of the journal entry.", "abel.tuter");  
  now_GR.update();
}
```

## GlideElement - setValue\(Object value\)

Sets the value of a field.

**Note:** Before calling this method, the element must already exist by querying an existing record or by using the now\_GR.initialize\(\) method to initialize a new record.

-   **Not for authentication with password2 fields**

    The setValue\(\) method passes password2 data as clear text, which results in an error about expecting encrypted data. Additionally, using the setValue\(\) method for password2 fields exposes data that should be encrypted.

    For password2 authentication, use the setDisplayValue\(\) method instead.

    See also:

    -   Deprecate GlideEncrypter usage of 3DES for password2 fields
    -   [Alternatives to GlideEncrypter usage in knowledge base article KB1320986](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1320986)
    -   Password2 encryption with the Key Management Framework \(KMF\)

|Name|Type|Description|
|----|----|-----------|
|value|Object|The value the field is to be set to.|

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

### Scoped equivalent

To use the setValue\(\) method in a scoped application, use the corresponding scoped method: [setValue\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

## GlideElement - toString\(\)

Converts the field's value to a string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The field's value as a string.|

```
doit();
 
function doit() { 
 
  var now_GR = new GlideRecord('sys_user');
  now_GR.query();
  while (now_GR.next()) {
  if ((now_GR().length != now_GR.first_name.toString().trim().length) || (now_GR.last_name.toString().length 
         != now_GR.last_name.toString().trim().length)) {
      now_GR.first_name = now_GR.first_name.toString().trim();
      now_GR.last_name = now_GR.last_name.toString().trim();
      now_GR.autoSysFields(false);
      now_GR.update();
    }
  }
 
}
```

### Scoped equivalent

To use the toString\(\) method in a scoped application, use the corresponding scoped method: [toString\(\)](../../glideElement/concept/c_GlideElementScopedAPI.md#).

