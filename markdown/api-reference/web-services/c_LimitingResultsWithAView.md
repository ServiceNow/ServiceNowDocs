---
title: Limiting results with a view
description: The description element in the returned RSS xml is constructed using the view as specified in the URL, when no view is specified, the default no-name view is used.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [RSS feed generator, RSS web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Limiting results with a view

The description element in the returned RSS xml is constructed using the view as specified in the URL, when no view is specified, the default no-name view is used.

To change this format, specify the **sysparm\_view** parameter on the URL. For example, the following request will return the incidents list. However the result will be restricted to only the fields available in the ess view:

```
 https://<instance name>.service-now.com/incident.do?sysparm_query=priority=1&sysparm_view=ess&RSS
```

Additionally, the RSS item title can be modified using the **sysparm\_title\_view** URL parameter. When specified, the item title will be constructed using the fields specified in the view. For example:

```
https://<instance name>.service-now.com/incident.do?sysparm_query=priority=1&sysparm_view=ess&sysparm_title_view=rss_title&RSS
```

**Parent Topic:**[RSS feed generator](c_RSSFeedGenerator.md)

