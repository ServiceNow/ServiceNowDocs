---
title: Sample scripts from the change events business rule
description: Several scripts are found in the baseline change events business rule.
locale: en-US
release: xanadu
product: System Events
classification: system-events
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [System events reference, System Events, Configure core features, Administer the ServiceNow AI Platform]
---

# Sample scripts from the change events business rule

Several scripts are found in the baseline change events business rule.

This business rule defines events that fire after a change request is inserted or updated.

```
if (current.operation() == 'insert') {
 gs.eventQueue("change.inserted", current, gs.getUserID(), gs.getUserName());
}
 
if (current.operation() == 'update') {
 gs.eventQueue("change.updated", current, gs.getUserID(), gs.getUserName());
}
 
if (!current.assigned_to.nil() && current.assigned_to.changes()) {
  gs.eventQueue("change.assigned", current, current.assigned_to.getDisplayValue() , previous.assigned_to.getDisplayValue());
}
 
if (current.priority.changes() && current.priority == 1) {
  gs.eventQueue("change.priority.1", current, current.priority, previous.priority);
}
 
if (current.risk.changes() && current.risk== 1) {
  gs.eventQueue("change.risk.1", current, current.risk, previous.risk); 
}
 
if (current.start_date.changes() || current.end_date.changes() || current.assigned_to.changes()) {  
  if (!current.start_date.nil() && !current.end_date.nil() && !current.assigned_to.nil()) {
    gs.eventQueue("change.calendar.notify", current, current.assigned_to, previous.assigned_to);
  }
 
  // Remove from previous assigned to, due to assigned_to changing
  if (!previous.assigned_to.nil()) {
      if (!current.assigned_to.nil() && current.assigned_to.changes() && 
         (!previous.start_date.nil() && !previous.end_date.nil())) {      
        gs.eventQueue("change.calendar.notify.remove", current, current.assigned_to, previous.assigned_to);
      }
   }
  // Remove old calendar from current assigned to, due to date changing
  else if (!current.assigned_to.nil()) {
     if ((current.start_date.changes() && !previous.start_date.nil()) || 
         (current.end_date.changes() && !previous.end_date.nil())) {
       gs.eventQueue("change.calendar.notify.remove", current, current.assigned_to, current.assigned_to);
     } 
  }
}
```

**Parent Topic:**[System events reference](system-events-reference.md)

