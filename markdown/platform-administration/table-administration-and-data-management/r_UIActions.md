---
title: Task relationships with UI actions
description: After defining task relationships, you can use UI Actions to define the task relationship when a new task is being created from an old task.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Many-to-many task relations, Working with Task table, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Task relationships with UI actions

After defining task relationships, you can use UI Actions to define the task relationship when a new task is being created from an old task.

Below are a few examples.

**Warning:** These examples may not work on all instances. They are provided as illustrative examples.

## UI Actions examples

**Cause an incident**

This UI Action allows the change management team to log an incident directly from the change request and records that the change caused the incident.

Create a UI Action on the Change Request \[change\_request\] table and place the following into the script:

```
var inccaus =new GlideRecord("incident");
inccaus.short_description= current.short_description;
inccaus.comments= current.comments.getHTMLValue();
// inccaus.parent = current.sys_id;
inccaus.insert();
CauIncident();
 
gs.addInfoMessage("Incident "+ inccaus.number+" created");
action.setRedirectURL(current);
action.setReturnURL(inccaus);
 
 
function CauIncident(){
var m2m =new GlideRecord('task_rel_task');
m2m.initialize();
m2m.child= current.sys_id;
m2m.parent= inccaus.sys_id;
m2m.type.setDisplayValue("Caused by::Causes");
m2m.insert();}
```

**Cause a problem**

This UI Action allows the change management team to record a problem from a change request and record that the change caused the problem.

Create a UI Action on the Change Request \[change\_request\] table and paste the following script:

```
var probcaus =new GlideRecord("problem");
probcaus.short_description= current.short_description;
probcaus.comments= current.comments.getHTMLValue();
// probcaus.parent = current.sys_id;
probcaus.insert();
CauProblem();
 
gs.addInfoMessage("Problem "+ probcaus.number+" created");
action.setRedirectURL(current);
action.setReturnURL(probcaus);
 
 
function CauProblem(){
var m2m =new GlideRecord('task_rel_task');
m2m.initialize();
m2m.child= current.sys_id;
m2m.parent= probcaus.sys_id;
m2m.type.setDisplayValue("Caused by::Causes");
m2m.insert();}
```

**Fix a problem**

This UI Action allows a change request to be generated from a problem, recording that the change fixes the problem.

Create a UI Action on the Problem \[problem\] table, and paste the following code:

```
var fixchg =new GlideRecord("change_request");
fixchg.short_description= current.short_description;
fixchg.comments= current.comments.getHTMLValue();
// fixchg.parent = current.sys_id;
fixchg.insert();
FixChange();
 
gs.addInfoMessage("Change "+ fixchg.number+" created");
action.setRedirectURL(current);
action.setReturnURL(fixchg);
 
 
function FixChange(){
var m2m =new GlideRecord('task_rel_task');
m2m.initialize();
m2m.child= current.sys_id;
m2m.parent= fixchg.sys_id;
m2m.type.setDisplayValue("Fixes::Fixed by");
m2m.insert();}
```

**Parent Topic:**[Creating many-to-many task relations](../concept/c_ManyToManyTaskRelations.md)

