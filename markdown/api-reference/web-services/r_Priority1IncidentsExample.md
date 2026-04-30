---
title: Priority 1 incidents example
description: This example scrolling element demonstrates how to create a UI macro to a scrolling list of priority 1 incidents.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Add scrolling form elements, Scrollable areas, Feed reader, RSS web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Priority 1 incidents example

This example scrolling element demonstrates how to create a UI macro to a scrolling list of priority 1 incidents.

Use the following example code:

```
<?xml version="1.0" encoding="utf-8" ?>
<j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
  <g2:evaluate var="jvar_inc">
    var inc = new GlideRecord('incident');
    inc.addActiveQuery();
    inc.addQuery('priority',1);
    inc.query();
  </g2:evaluate>
 
  <div style="background-color:DDDDDD; padding-left:10px; line-height:19px; border:2px white solid" width="100%" nowrap="true">
    Priority 1 Incidents:
    <input id="make_spacing_ok" style="visibility:hidden;width:0px:" title=""/>
  </div>
  <g2:scrollable_area height="100px" width="100%"> 
 
      <j2:while test="$[inc.next()]">
        <j2:set var="jvar_inc_link" value="incident.do?sys_id=$[inc.sys_id]"/>
        <j2:set var="jvar_inc_list_link" value="incident_list.do?sysparm_query=active=true"/>
        <span style="line-height: 10px; padding-left:10px">    
          <a href="$[jvar_inc_link]">
            <IMG SRC="images/services.png" style="padding-right:10px"></IMG>
          </a>
          <a href="$[jvar_inc_link]" style="padding-right:10px; color:blue">$[inc.number]</a>
            $[inc.short_description]
        </span>
        <br style="line-height:5px"/>
      </j2:while>
      <span>
        <a href="$[jvar_inc_list_link]" style="color:blue; padding-left:10px">View all active incidents</a>
      </span>
 
  </g2:scrollable_area> 
</j:jelly>
```

Navigate to **System UI** &gt; **Formatters** and create a Formatter that refers to the UI Macro above.

**Parent Topic:**[Add scrolling elements in forms](../task/t_AddingScrollingElementsInForms.md)

