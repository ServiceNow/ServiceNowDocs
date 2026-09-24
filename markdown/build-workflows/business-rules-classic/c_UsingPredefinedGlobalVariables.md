---
title: Global variables in business rules
description: Predefined global variables are available for use in business rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/business-rules-classic/c\_UsingPredefinedGlobalVariables.html
release: brazil
product: Business rules \(Classic\)
classification: business-rules-classic
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Classic Business rules, Build workflows]
---

# Global variables in business rules

Predefined global variables are available for use in business rules.

Use the following predefined global variables to reference the system in a business rule script.

|Global variable|Description|
|---------------|-----------|
|*current*|Current state of the record being referenced. See "Prevent null pointer exceptions" below to check for nulls before using this variable.|
|*previous*|State of the referenced record prior to any updates made during the execution context, where the execution context begins with the first update or delete operation and ends after the script and any referenced business rules are executed. If multiple updates are made to the record within one execution context, *previous* will continue to hold the state of the record before the first update or delete operation. Available on update and delete operations only. Not available on async operations. See "Prevent null pointer exceptions" below to check for nulls before using this variable.|
|*g\_scratchpad*|Scratchpad object is available on display business rules, and is used to pass information to the client to be accessed from client scripts.|
|*gs*|References to GlideSystem functions.|

The variables *current*, *previous*, and *g\_scratchpad* are global across all business rules that run for a transaction.

## Prevent null pointer exceptions

In some cases, there may not be a *current* or *previous* state for the record when a business rule runs, which means that the variables will be null. To check for null before using a variable, add the following code to your business rule:

```
if (current == null) // to prevent null pointer exceptions.
return; 
```

## Define variables

User-defined variables are globally scoped by default. If a new variable is declared in an order 100 business rule, the business rule that runs next at order 200 also has access to the variable. This may introduce unexpected behavior.

To prevent such unexpected behavior, always wrap your code in a function. This protects your variables from conflicting with system variables or global variables in other business rules that are not wrapped in a function. Additionally, variables such as *current* must be available when a function is invoked in order to be used.

The following script is vulnerable to conflicts with other code. If the variable *now\_GR* is used in other rules, the value of the variable may unexpectedly change.

```
var now_GR = new GlideRecord('incident');
now_GR.query(); 
while(now_GR.next()) {
 
   //do something
 
}
```

When this script is wrapped in a function, the variable is available only within the function and does not conflict with other functions using a variable named *now\_GR*.

```
myFunction();
 
function myFunction() { 
  var now_GR = new GlideRecord('incident');
  now_GR.query(); 
  while(now_GR.next()) { 
    //do something 
} }
```

**Parent Topic:**[Classic Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/business-rules-classic/c_BusinessRules.md)

