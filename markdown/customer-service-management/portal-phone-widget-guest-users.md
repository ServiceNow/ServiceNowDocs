---
title: Guest user support for portal voice calls
description: Guest users can start and complete voice calls from the portal or Engagement Messenger without logging in.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/portal-phone-widget-guest-users.html
release: australia
topic_type: concept
last_updated: "2026-10-28"
reading_time_minutes: 1
keywords: [guest user, unauthenticated user, voice call widget, WebRTC, portal, rate limit]
breadcrumb: [Voice call widget, Configure voice, Configure omnichannel, Configure, Customer Service Management]
---

# Guest user support for portal voice calls

Guest users can start and complete voice calls from the portal or Engagement Messenger without logging in.

A guest user is a visitor who browses the portal without logging in. Guest users can start a voice call from the voice call widget and stay connected for the duration of the call. The steps to start a call are the same as for a logged-in user. Guest users can also authenticate during the call.

## Authentication during a guest call

A guest user can be asked to authenticate during a call, for example, when trying to initiate a purchase or return. The user authenticates by entering a PIN on the **dial pad**, which sends each digit to the voice service over the call's data channel as a Dual-tone multi-frequency \(DTMF\) message. After the user authenticates, the call continues as an authenticated session and the non-public AI agents available to authenticated users become available.

A user who declines to authenticate or can't authenticate stays on the call as a guest. The call continues, but the caller only has access to publicly-facing AI agents.

**Note:** Each voice call requires a session token, and the system limits how many token requests it generates in an hour. One limit applies to logged-in users and a separate limit applies to guest users; administrators define both as rate limit rules on the instance and can customize them. Guest calls don't use up the quota for logged-in users, and calls from logged-in users don't use up the quota for guest users.

**Related topics**  


[Enable WebRTC for Voice calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/portal-phone-widget.md)

[Dial pad for voice calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/portal-phone-widget-dial-pad.md)

[Cookie Auth API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/cookieauth-api.md)

