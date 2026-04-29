---
title: Sample field value duration script
description: Review the existing Incident Open metric definition to see how you can create your own custom metric.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Metrics, Configure core features, Administer the ServiceNow AI Platform]
---

# Sample field value duration script

Review the existing Incident Open metric definition to see how you can create your own custom metric.

This script either provides a duration value or stops processing durations \(sets the answer variable to false\) when an incident is closed.

```
// script can set answer to false to terminate processing of the metric
    // mi - MetricInstance
    // answer
    if (!current.active) {
    answer = false;
    mi.endDuration();
    gs.log("Closing field durations");
    closeDurations(mi.current);
    }
    
    function closeDurations(current) {
    var now_GR = new GlideRecord('metric_instance');
    gr.addQuery('id', current.sys_id);
    gr.addQuery('calculation_complete', false);
    gr.addQuery('definition.type', 'field_value_duration');
    gr.query();
    while (gr.next()) {
    gs.log("closing: " + gr.definition.name + " for: " + current.number);
    var definition = new GlideRecord('metric_definition');
    definition.get(gr.definition);
    var mi = new MetricInstance(definition, current);
    mi.endDuration();
    }
    }
```

