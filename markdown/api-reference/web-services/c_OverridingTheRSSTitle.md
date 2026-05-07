---
title: RSS title override
description: You may optionally override the automatically generated title of the RSS feed by added the sysparm\_title parameter to the request URL.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Feed generator, RSS web service, Inbound, Web services, API implementation, API implementation and reference]
---

# RSS title override

You may optionally override the automatically generated title of the RSS feed by added the **sysparm\_title** parameter to the request URL.

For example, you can specify the title `Priority One Incidents` using the following request URL.

```
 https://<instance name>.service-now.com/incident.do?sysparm_query=priority=1&sysparm_view=ess&RSS&sysparm_title=Priority%20One%20Incidents

```

This will produce results as follows:

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
  <channel>
    <title>Priority One Incidents</title>
    <link>http://www.service-now.com/demo/nav_to.do?uri=incident.do?sysparm_query=priority=1</link>
    <description>Priority One Incidents</description>
    <copyright>Copyright 2006 Service-now.com</copyright>
    <pubDate>Mon, 12 Jun 2006 11:04:44 PDT</pubDate>
    <lastBuildDate>Mon, 12 Jun 2006 11:04:44 PDT</lastBuildDate>
    <generator>jRSSGenerator by Henrique A. Viecili</generator>
    <docs>http://blogs.harvard.edu/tech/rss</docs>
    <item>
      <title>INC00009</title>
      <link>http://www.service-now.com/demo/nav_to.do?uri=incident.do?
        sys_id=46b66a40a9fe198101f243dfbc79033d%26sysparm_stack=incident_list.do%
        3Fsysparm_query=active=true</link>
      <description>INC00009 2006-02-01 14:50:23 Reset my password</description>
      <author>glide.maint</author>
      <guid>46b66a40a9fe198101f243dfbc79033d</guid>
      <pubDate>Wed, 17 May 2006 18:20:57 PDT</pubDate>
    </item>
  </channel>
</rss>
```

**Parent Topic:**[RSS feed generator](c_RSSFeedGenerator.md)

