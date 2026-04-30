---
title: Create a custom SLA condition rule
description: You can create custom SLA condition rules to determine whether an SLA should attach, pause, complete, reattach, or cancel. SLA condition classes contain script to define processing for an SLA condition rule. Create an SLA condition rule after the SLA condition class is defined.
locale: en-US
release: xanadu
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Extend SLA condition rules, Configuring Service Level Management, Service Level Management, IT Service Management]
---

# Create a custom SLA condition rule

You can create custom SLA condition rules to determine whether an SLA should attach, pause, complete, reattach, or cancel. SLA condition classes contain script to define processing for an SLA condition rule. Create an SLA condition rule after the SLA condition class is defined.

## Before you begin

Role required: admin

## Procedure

1.  Define an SLA Condition Class.

    Navigate to **System Definition** &gt; **Script Includes** and click **New**.

    Within the script in the SLA Condition Class, provide methods to modify one or more of the default SLA transitions \(attach, pause, complete, reattach, cancel\), defining the conditions for SLA processing. For example, the **attach** method defines when an SLA is created and attached to a task. The methods need to test a condition, referencing the condition fields on the SLA Definition form.

2.  Create an SLA Condition Rule.

    1.  Navigate to **Service Level Management** &gt; **SLA Condition Rules** and click **New**.

    2.  Name the SLA Condition Rule.

    3.  Select the Script Include defined above in the **Class Name** reference field.


## Example of an SLA Condition Class

For example, including the following method in an SLA Condition Class attaches the SLA if its condition matches the SLA's `start_condition` field:

```
attach: function() {
      return (this._conditionMatches(this.sla.start_condition));
   },
```

The following is an example which shows the format of a script include that would extend the SLAConditionBase class and provide methods for each of the SLA transitions:

```
var SLAConditionLocal = Class.create();
 
SLAConditionLocal.prototype = Object.extendsObject(SLAConditionBase, {
 
   attach: function() {
     // insert script here
   },
 
   pause: function() {
     // insert script here
   },
 
   complete: function() {
     // insert script here
   },
 
   reattach: function() {
     // insert script here
   },
 
   cancel: function() {
     // insert script here
   },
});
```

**Parent Topic:**[Extend SLA condition rules](../concept/c_ExtendSLAConditionRules.md)

