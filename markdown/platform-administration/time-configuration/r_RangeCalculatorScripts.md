---
title: Range calculator scripts
description: You can specify a script include that calculates range restrictions and processes parent updates in a timeline page.
locale: en-US
release: zurich
product: Time Configuration
classification: time-configuration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Timeline pages, Viewing record information over time, Reference, Time configuration, Configure core features, Administer]
---

# Range calculator scripts

You can specify a script include that calculates range restrictions and processes parent updates in a timeline page.

## Range Calculator Scripts

Following are three examples of script includes that help specify range restrictions.

**ExampleUpdateParentsRangeCalculator**

Updates parent records when a child record span is moved or resized in the timeline.

```
var ExampleUpdateParentsRangeCalculator = Class.create();
ExampleUpdateParentsRangeCalculator.prototype = {
initialize: function() { },
updateParents: function(id, table, startDate, endDate){
 if (table == "rm_sprint"){
   var releaseID;
   var sprint = new GlideRecord(table);
   sprint.addQuery('sys_id', id);
   sprint.query();
   if (sprint.next())
     releaseID = sprint.release + "";
   if (releaseID) {
         var now_GR = new GlideRecord("rm_release_scrum");
         gr.addQuery("sys_id", releaseID);
         gr.query();
         if (gr.next()) {
           if (startDate  && startDate < this.getTimeMs(gr.start_date))
               gr.start_date = this.getTimeObject(startDate); 
           if (endDate && endDate > this.getTimeMs(gr.end_date))
              gr.end_date = this.getTimeObject(endDate);
              gr.update();
         }
    }
  }
},  
getMinRangeDetails: function(id, table){ return [-1, -1, "", ""]; },
getMaxRangeDetails: function(id, table){ return [-1, -1, ""]; },
getTimeMs: function(date){ 
  return new GlideScheduleDateTime(date).getMS(); },
getTimeObject: function(timeMS) { 
  var gdt = new GlideDateTime(); 
  gdt.setNumericValue(timeMS); 
  return gdt; },
logMessage: function(message){ gs.log(message); },
type: 'ExampleUpdateParentsRangeCalculator'
}
```

In this example, the span is identified based on the id and table from function\(id, table, startDate, endDate\).

**ExampleMinRangeCalculator**

Defines the earliest start date and the latest end date for a specified span.

```
var ExampleMinRangeCalculator = Class.create();
  ExampleMinRangeCalculator.prototype = {
      initialize: function() { },
      updateParents: function(id, table, startDate, endDate){ },
      getMinRangeDetails: function(id, table){
           var min = -1;
           var max = -1;
           var minID = "";
           var maxID = "";
           if (table == "rm_release_scrum"){
                    var now_GR = new GlideRecord("rm_sprint");
                    gr.addQuery("release", id);
                    gr.query();
                    while(gr.next()){
                         var start = this.getTimeMs(gr["start_date"]);
                         var end = this.getTimeMs(gr["end_date"]);
                         var id = gr["sys_id"];
                         if (min == - 1 || start <= min){
                                if (start != min)
                                     minID = "";
                         min = start;
                         minID += "," + id;
                         }
                         if (max == -1 || end >= max){
                                    if (end != max)
                                            maxID = "";
                                    max = end;
                                    maxID += "," + id;
                            }  
                     }
            }
        return [min, max, minID, maxID];
},
getMaxRangeDetails: function(id, table){ return [-1, -1, ""]; },
getTimeMs: function(date){ return new GlideScheduleDateTime(date).getMS(); },
getTimeObject: function(timeMS) { 
  var gdt = new GlideDateTime(); 
  gdt.setNumericValue(timeMS); 
  return gdt; },
logMessage: function(message){ gs.log(message); },
type: 'ExampleUpdateParentsRangeCalculator'
}
```

**ExampleMaxRangeCalculator**

Defines the earliest start date and the latest end date for a specified span.

```
var ExampleMaxRangeCalculator = Class.create();
ExampleMaxRangeCalculator.prototype = {
   initialize: function() { },
   updateParents: function(id, table, startDate, endDate){ },
   getMinRangeDetails: function(id, table){ return [-1, -1, "", ""]; },
   getMaxRangeDetails: function(id, table){
      if (table == "rm_sprint"){
         var sprint = new GlideRecord(table);
         sprint.addQuery('sys_id', id);
         sprint.query();
         if (sprint.next())
            releaseID = sprint.release + "";
         if (releaseID) {
            var now_GR = new GlideRecord("rm_release_scrum");
            gr.addQuery("sys_id", releaseID);
            gr.query();
            if (gr.next())
               return [this.getTimeMs(gr.start_date),
                this.getTimeMs(gr.end_date), gr.sys_id];
         }
      }
      return [-1, -1, ""];
   },
   getTimeMs: function(date){ return new ScheduleDateTime(date).getMS(); },
   getTimeObject: function(timeMS) { 
     var gdt = new GlideDateTime();
     gdt.setNumericValue(timeMS); 
     return gdt; },
   logMessage: function(message){ gs.log(message); },
   type: 'ExampleUpdateParentsRangeCalculator'
}
```

Use the following two functions to obtain the correct start and end dates in the three example script includes provided for reference.

```
getTimeMs: function(date){
        return new ScheduleDateTime(date).getMS();
    }
```

```
getTimeObject: function(timeMS) {
        var gdt = new GlideDateTime();
        gdt.setNumericValue(timeMS);
        return gdt;
    }
```

**Parent Topic:**[Timeline pages](../concept/c_TimelinePages.md)

