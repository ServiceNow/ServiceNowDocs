---
title: Formatting results
description: The description element in the returned RSS xml can be formatted by setting the URL parameter sysparm\_format=true and specifying the format string in the property glide.rss.description\_format.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Feed generator, RSS web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Formatting results

The description element in the returned RSS xml can be formatted by setting the URL parameter **sysparm\_format=true** and specifying the format string in the property **glide.rss.description\_format**.

By default, when the URL parameter is present, the description element will be formatted to contain the field label and value using the following format string:

```
<b>{1}</b>: {2}<br/>

```

-   \{0\} - field name
-   \{1\} - field label
-   \{2\} - field value

This default format string can be overridden using the property **glide.rss.description\_format**.

**Parent Topic:**[RSS feed generator](c_RSSFeedGenerator.md)

