---
title: GlideScopedEvaluator - Global
description: The GlideScopedEvaluator API allows you to evaluate scripts in a GlideRecord field from both scoped and global server scripts.Instantiates a GlideScopedEvaluator object.Evaluates a script from a GlideRecord field.Returns a variable from a GlideScopedEvaluator object.Puts a variable into the GlideScopedEvaluator object. These variables are available to the script that this GlideScopedEvaluator object runs.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideScopedEvaluator- Global

The GlideScopedEvaluator API allows you to evaluate scripts in a GlideRecord field from both scoped and global server scripts.

This API evaluates scripts within the script field type. The scope of the record defines the scope of the script.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideScopedEvaluator - GlideScopedEvaluator\(\)

Instantiates a GlideScopedEvaluator object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

### Scoped equivalent

To use the GlideScopedEvaluator\(\) method in a scoped application, use the corresponding scoped method: [GlideScopedEvaluator\(\)](../../glideEvaluatorScoped/concept/c_GlideEvaluatorScopedAPI.md#).

## GlideScopedEvaluator - evaluateScript\(GlideRecord grObj, String scriptField, Object variables\)

Evaluates a script from a GlideRecord field.

|Name|Type|Description|
|----|----|-----------|
|grObj|GlideRecord|The GlideRecord containing a script expression.|
|scriptField|String|\(Optional\) The name of the field containing the script expression.|
|variables|Object|\(Optional\) A map of variables with name-value pairs. These variables are available to the script during execution of this method.|

|Type|Description|
|----|-----------|
|Object|The result of the script execution.|

```
//For this example, we created a table: "x_app_table" with two columns: "short_description", "test_script"
// "test_script" will store the script to be evaluated by GlideScopedEvaluator.
var now_GR = new GlideRecord('x_app_table');
now_GR.short_description = 'Testing GlideScopedEvaluator';
now_GR.test_script = "gs.getUser().getName() + ' says ' + greeting; ";
now_GR.insert();

//setup variables to be used by the script
var vars = {'greeting' : 'hello'};

//Evaluate the script from the field
var evaluator = new GlideScopedEvaluator();
gs.info(evaluator.evaluateScript(now_GR, 'test_script', vars));

// Now retrieve the result
evaluator.evaluateScript(gr, 'u_test_script', null);
gs.info(evaluator.getVariable('result'));
```

Output:

```
admin says hello
```

### Scoped equivalent

To use the evaluateScript\(\) method in a scoped application, use the corresponding scoped method: [evaluateScript\(\)](../../glideEvaluatorScoped/concept/c_GlideEvaluatorScopedAPI.md#).

## GlideScopedEvaluator - getVariable\(String name\)

Returns a variable from a GlideScopedEvaluator object.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the variable.|

|Type|Description|
|----|-----------|
|Object|The value of the specified variable.|

```
//setting up a record that contains the script to be executed.
var now_GR = new GlideRecord('global'); 
now_GR.u_short_description = 'Calculate Addition';  
now_GR.u_test_script = "result = x + y"; 
evaluator.evaluateScript(now_GR, "script")
now_GR.insert(); 
 
var evaluator = new GlideScopedEvaluator();
evaluator.putVariable('x', 100);
evaluator.putVariable('y', 200);
evaluator.putVariable('result', null);
evaluator.evaluateScript(now_GR, "script")
now_GR.insert();
```

Output:

```
300
```

### Scoped equivalent

To use the getVariable\(\) method in a scoped application, use the corresponding scoped method: [getVariable\(\)](../../glideEvaluatorScoped/concept/c_GlideEvaluatorScopedAPI.md#).

## GlideScopedEvaluator - putVariable\(String name, Object value\)

Puts a variable into the GlideScopedEvaluator object. These variables are available to the script that this GlideScopedEvaluator object runs.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the variable.|
|value|Object|The value of the variable.|

|Type|Description|
|----|-----------|
|void| |

```
//setting up a record that contains the script to be executed.
var now_GR = new GlideRecord('u_global_table'); 
now_GR.u_short_description = 'Calculate Addition';  
now_GR.u_test_script = "result = x + y";
evaluator.evaluateScript(now_GR, "script") 
now_GR.insert(); 
 
var evaluator = new GlideScopedEvaluator();
evaluator.putVariable('x', 100);
evaluator.putVariable('y', 200);
evaluator.putVariable('result', null);
evaluator.evaluateScript(now_GR, "script")
now_GR.insert();
```

Output:

```
300
```

### Scoped equivalent

To use the putVariable\(\) method in a scoped application, use the corresponding scoped method: [putVariable\(\)](../../glideEvaluatorScoped/concept/c_GlideEvaluatorScopedAPI.md#).

