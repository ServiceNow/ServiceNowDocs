---
title: GlideScopedEvaluator - Scoped
description: The GlideScopedEvaluator API allows you to evaluate scripts in a GlideRecord field from both scoped and global server scripts.Instantiates a GlideScopedEvaluator object.Evaluates a script that resides in a GlideRecord field.Returns a specified variable from a GlideScopedEvaluator object.Sets a variable into the GlideScopedEvaluator object. These variables are available to the script that this GlideScopedEvaluator object runs.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideScopedEvaluator- Scoped

The GlideScopedEvaluator API allows you to evaluate scripts in a GlideRecord field from both scoped and global server scripts.

This API evaluates records with script fields defined. The scope of the script is defined by the scope of the record.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideScopedEvaluator - GlideScopedEvaluator\(\)

Instantiates a GlideScopedEvaluator object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## GlideScopedEvaluator - evaluateScript\(GlideRecord grObj, String scriptField, Object variables\)

Evaluates a script that resides in a GlideRecord field.

|Name|Type|Description|
|----|----|-----------|
|grObj|[GlideRecord](../../glideRecordScoped/concept/c_GlideRecordScopedAPI.md#)|GlideRecord containing a script expression.|
|scriptField|String|Optional. Name of the field containing the script expression.|
|variables|Object|Optional. Map of variables with name-value pairs. These variables are available to the script during execution of this method.|

|Type|Description|
|----|-----------|
|Object|Result of the script execution.|

```
// Setting up a record that contains the script to be executed.
var now_GR = new GlideRecord('u_global_table'); 
now_GR.u_short_description = 'Calculate Addition';  
now_GR.u_test_script = "result = x + y"; 
now_GR.insert(); 
 
var evaluator = new GlideScopedEvaluator();
evaluator.putVariable('x', 100);
evaluator.putVariable('y', 200);
gs.info(evaluator.evaluateScript(now_GR, 'u_test_script'));
```

Output:

```
300
```

## GlideScopedEvaluator - getVariable\(String name\)

Returns a specified variable from a GlideScopedEvaluator object.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the variable to return.|

|Type|Description|
|----|-----------|
|Object|Value of the specified variable.|

The following example shows how to call the getVariable\(\) method to check the value of the *answer* variable.

```
(function executeRule(current, previous /*null when async*/) {
  var grAG = current.assignment_group.getRefRecord(); // Get the GlideRecord of the assignment group
  if (grAG.isValidRecord()) {
    var ge = new GlideScopedEvaluator();
    ge.putVariable("current", current); // Pass through the "current" variable as "current"
    ge.putVariable("group", grAG); // Pass through the "grAG" variable as "group"
    ge.putVariable("answer", true); // default "answer" to TRUE
    ge.evaluateScript(grAG, "u_assignment_condition"); // Run the script

    // Abort the transaction if the "answer" variable was set to FALSE explicitly (undefined doesn't count)
    if (ge.getVariable("answer") === false) { 
      gs.addErrorMessage("Assignment rule did not pass");
      current.setAbortAction(true);
    }
  }
})(current, previous);
```

## GlideScopedEvaluator - putVariable\(String name, Object value\)

Sets a variable into the GlideScopedEvaluator object. These variables are available to the script that this GlideScopedEvaluator object runs.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the variable.|
|value|Object|Value of the variable.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to call the putVariable\(\) method to set the *answer* variable to true.

```
(function executeRule(current, previous /*null when async*/) {
  var grAG = current.assignment_group.getRefRecord(); // Get the GlideRecord of the assignment group
  if (grAG.isValidRecord()) {
    var ge = new GlideScopedEvaluator();
    ge.putVariable("current", current); // Pass through the "current" variable as "current"
    ge.putVariable("group", grAG); // Pass through the "grAG" variable as "group"
    ge.putVariable("answer", true); // Set default "answer" to TRUE
    ge.evaluateScript(grAG, "u_assignment_condition"); // Run the script

    // Abort the transaction if the "answer" variable was set to FALSE explicitly (undefined doesn't count)
    if (ge.getVariable("answer") === false) { 
      gs.addErrorMessage("Assignment rule did not pass");
      current.setAbortAction(true);
    }
  }
})(current, previous);
```

