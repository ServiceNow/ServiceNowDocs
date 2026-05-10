---
title: RSS basic authentication
description: To enforce basic authentication on each request for an RSS feed, set the property glide.basicauth.required.rss to true.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Feed generator, RSS web service, Inbound, Web services, API implementation, API implementation and reference]
---

# RSS basic authentication

To enforce basic authentication on each request for an RSS feed, set the property **glide.basicauth.required.rss** to true.

RSS request would have to contain the Authorization header as specified in the Authentication protocol. Because the request is non-interactive, we always require the Authorization header during a request.

**Note:** If you plan to disable RSS basic authentication, make sure that tables in the platform have the right ACL entries to protect from unauthorized access.

To specify basic authentication on the URL, put the username and password pair separated by a colon in front of the server name before an @ character. For example, to submit the demo credentials for the ITIL user, use the following URL.

```
https://itil:itil@<instance name>.service-now.com/incident.do?RSS
```

Some older browsers, such as Microsoft IE 7 do not support direct URL authentication. If the site uses basic authentication, Internet Explorer automatically prompts users for a user name and a password. In some cases, users can click the Remember my password box in the prompt to save their credentials for later visits to that site.

**Parent Topic:**[RSS feed generator](c_RSSFeedGenerator.md)

**Related topics**  


[http://www.w3.org/Protocols/HTTP/1.0/draft-ietf-http-spec.html\#BasicAABasic](http://www.w3.org/Protocols/HTTP/1.0/draft-ietf-http-spec.html#BasicAABasic)

[http://support.microsoft.com/kb/834489](http://support.microsoft.com/kb/834489)

[RSS request authorization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-rss-request-authorization.md)

