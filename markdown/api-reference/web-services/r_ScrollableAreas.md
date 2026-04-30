---
title: Scrollable areas
description: A scrollable area is a div where contents scroll from the bottom up over time.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [RSS feed reader, RSS web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Scrollable areas

A scrollable area is a div where contents scroll from the bottom up over time.

You can scroll any HTML content, and anything inside the scroller is operational HTML with functioning links and images.

To make a scrollable areas, wrap the scrolling content inside of a scrollable\_area tag, likely in a UI Page:

```
    <g:scrollable_area height="100px">
        <g2:evaluate var="jvar_temp" expression="var kb = new GlideRecord('kb_knowledge');"/>
        <g:inline template="kb_section.xml"/>
    </g:scrollable_area>
```

The system will then create a 100 pixel high div and the contents will automatically scroll from bottom to top. If you have a 1000 pixel high block of text, for example, you'll see the top 100 pixels and then pixels 2-101, then 3-102, etc. Once it reaches the top it'll wrap back around to the bottom.

This sample code will create a scroller with a list of priority 1 incidents.

```
<?xml version="1.0" encoding="utf-8" ?>
<j:jelly trim="false" xmlns:j="jelly:core" xmlns:g="glide" xmlns:j2="null" xmlns:g2="null">
  <g2:evaluate var="jvar_inc">
    var inc = new GlideRecord('incident');
    inc.addActiveQuery();
    inc.addQuery('priority',1);
    inc.query();
  </g2:evaluate>

  <g2:scrollable_area height="100px"> 
    <table border="0" cellspacing="2" cellpadding="0" width="100%">
      <j2:while test="$[inc.next()]">
        <j2:set var="jvar_inc_link" value="incident.do?sys_id=$[inc.sys_id]"/>
        <j2:set var="jvar_inc_list_link" value="incident_list.do?sysparm_query=active=true"/>
	<tr>
	  <td>
            <a href="$[jvar_inc_link]">
              <IMG SRC="images/services.png" style="padding-right:10px"></IMG>
            </a>
            <a href="$[jvar_inc_link]" style="padding-right:10px; color:blue">$[inc.number]</a>
          </td>
          <td>$[inc.short_description]</td>
        </tr>
      </j2:while>
      <tr>
        <td align="center" colspan="2"><a href="$[jvar_inc_list_link]" style="color:blue">View all active incidents</a></td>
      </tr>
    </table>
  </g2:scrollable_area> 
</j:jelly>
```

-   **[Add scrolling elements in forms](../task/t_AddingScrollingElementsInForms.md)**  
You can add scrolling areas to forms as well as UI pages.

**Parent Topic:**[RSS feed reader](../concept/c_RSSFeedReader.md)

