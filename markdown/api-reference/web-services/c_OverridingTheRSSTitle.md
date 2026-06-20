---
title: RSS title override
description: You may optionally override the automatically generated title of the RSS feed by added the sysparm\_title parameter to the request URL.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/api-reference/web-services/c\_OverridingTheRSSTitle.html
release: xanadu
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [RSS feed generator, RSS web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# RSS title override

You may optionally override the automatically generated title of the RSS feed by added the **sysparm\_title** parameter to the request URL.

For example, you can specify the title `Priority One Incidents` using the following request URL.

```
 https://<instance name>.service-now.com/incident.do?sysparm_query=priority=1&sysparm_view=ess&RSS&sysparm_title=Priority%20One%20Incidents

```

This will produce results as follows:

\[Omitted image "RssOut.jpg"\] Alt text:

**Parent Topic:**[RSS feed generator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/api-reference/web-services/c_RSSFeedGenerator.md)

