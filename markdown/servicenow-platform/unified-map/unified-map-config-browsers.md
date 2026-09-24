---
title: Configure browsers
description: Configure which browser you use Unified Map in to avoid severe performance issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/unified-map/unified-map-config-browsers.html
release: brazil
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Administer, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure browsers

Configure which browser you use Unified Map in to avoid severe performance issues.

## Before you begin

The default behavior for each browser is controlled by the **unifiedmap.map\_search\_filter.map\_edge\_animations** property in the \[sn\_cmdb\_ws\_config\_property\] table, linked to the `Default` configuration identifier. The value is a JSON object mapping each browser to `true` \(animations on\) or false \(animations off\), with an `others` key as the fallback for any browser not explicitly listed:

```
{
"safari": false,
"chrome": true,
"edge": true,
"firefox": true,
"others": true
}
```

Role required: sn\_cmdb\_admin

## Procedure

1.  Navigate to the \[sn\_cmdb\_ws\_config\_property.list\] table.

2.  Open the unifiedmap.map\_search\_filter.map\_edge\_animations record.

3.  Update the value for the relevant browser key and save.

    **Note:** When you turn animations back on for Safari, it re-introduces the original performance issue on nodes with many connections. This setting disables all map animations in the affected browser, not only the edge animations.


**Parent Topic:**[Configuring Unified Map — admin settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/unified-map/administer-unified-map.md)

