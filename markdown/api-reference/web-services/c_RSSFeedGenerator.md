---
title: RSS feed generator
description: ServiceNow supports the dynamic generation of RSS feeds.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [RSS web service, Inbound, Web services, API implementation, API implementation and reference]
---

# RSS feed generator

ServiceNow supports the dynamic generation of RSS feeds.

Much like our Web Services implementation, the retrieval of an RSS feed representation of information is simply done by specifying an RSS parameter at the end of the URL to a table list. For example, the following will return a list of all incidents in RSS 2.0 format.:

## Adding a Query

To associate a query to the list so that a filtered list is returned, use the **sysparm\_query** parameter. For example, the following will return a list of all incidents where the priority field is 1 \(Critical\):

```
 https://<instance name>.service-now.com/incident.do?sysparm_query=priority=1&RSS
```

If you have a multi part query then you would separate the parts with the ^ character. For example to get all priority 1 incidents with a category of software you would:

```
https://<instance name>.service-now.com/incident.do?sysparm_query=priority=1^category=software&RSS
```

If you want to query on a field that is a reference to another file then you need to use javascript to resolve the reference to the other file. For example, the assigned\_to field in incident is a reference to a user record. If you wanted to find all the incidents assigned to "ITIL User" then you would do the following:

```
https://<instance name>.service-now.com/incident.do?sysparm_query=assigned_to=javascript:GetIDValue('sys_user','ITIL%20User')&RSS
```

**Note:** You can in most cases simply append "&amp;RSS" to a URL that you generate in the U.I. or that of your favorite module. The easiest way to get the URL is to simply click the last breadcrumb from the list view. After appending "&amp;RSS" then you can use this URL in your RSS feed reader

![](../image/GetBreadURL.png "Get Bread URL")

-   **[Limiting results with a view](c_LimitingResultsWithAView.md)**  
The description element in the returned RSS xml is constructed using the view as specified in the URL, when no view is specified, the default no-name view is used.
-   **[Formatting results](c_FormattingResults.md)**  
The description element in the returned RSS xml can be formatted by setting the URL parameter **sysparm\_format=true** and specifying the format string in the property **glide.rss.description\_format**.
-   **[RSS basic authentication](c_BasicAuthentication.md)**  
To enforce basic authentication on each request for an RSS feed, set the property **glide.basicauth.required.rss** to true.
-   **[RSS title override](c_OverridingTheRSSTitle.md)**  
You may optionally override the automatically generated title of the RSS feed by added the **sysparm\_title** parameter to the request URL.

**Parent Topic:**[RSS web service](../topic/p_RSS.md)

