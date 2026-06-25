---
title: Persist an HTTP session across all SOAP calls
description: In circumstances when a SOAP client makes many calls in a short amount of time, you may want to re-use a single HTTP session for all SOAP calls.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/persist-session-all-soap-calls.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Direct services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Persist an HTTP session across all SOAP calls

In circumstances when a SOAP client makes many calls in a short amount of time, you may want to re-use a single HTTP session for all SOAP calls.

Each SOAP call creates a new user session that persists until it expires. To create a single user session and re-use it for all inbound SOAP calls, develop your SOAP client following these guidelines:

-   Use a module like HTTP::Cookies to create a "cookie jar."
-   Save the cookies returned by ServiceNow after each request \(handled automatically by HTTP::Cookies\).
-   Re-send the cookies in the cookie jar with each subsequent request.

**Note:** If you have enabled the session rotation high security setting, it will immediately invalidate the JSESSIONID returned from the server with the first response header. The second response includes a new JSESSIONID.

In perl, you can automatically save and send cookies with the following code:

```
use HTTP::Cookies;

#we want to store and re-send cookies
my $cookies = HTTP::Cookies->new(ignore_discard => 1);

my $soap = SOAP::Lite
    -> proxy('http://localhost:8080/glide/ecc_queue.do?SOAP');

#Set the cookie jar
$soap->transport->cookie_jar($cookies);
```

**Parent Topic:**[Direct web services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_DirectWebServices.md)

**Related topics**  


[Use forms to limit or extend the query response]()

[Return the display value for reference variables]()

[Clear values from a target instance]()

[Retrieve journal entries using direct web services]()

[Retrieve choice fields using direct web services]()

[SOAP direct web service API functions]()

