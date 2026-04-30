---
title: Mobile web screen
description: Mobile web screens open an external URL or a relative URL within your instance.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Mobile web screen

Mobile web screens open an external URL or a relative URL within your instance.

**Note:**

There are limitations associated with the use of mobile web screens on navigation tabs. Currently, if the mobile web screen is accessed and authentication has expired because the session has timed out, the device has locked, or the app has been backgrounded, you must re-authenticate in the mobile web screen.

In addition, pulling to refresh the mobile web screen is unavailable on Android devices. Instead, to refresh the app, you must close it, re-start it, and then return to the mobile web screen to see refreshed content. This limitation related to pulling to refresh doesn't exist on iOS devices, version 18.4 and later.

<table id="table_n1k_dbq_nlb"><tbody><tr><td>

Use a mobile web screen to Open a URL from within the ServiceNow app. You can configure relative URLs to open pages within the ServiceNow platform, or an external link. For example, a user can see a knowledge article on the instance via Service Portal.

 Relative URLs that direct your users to open pages within your instance display within mobile app. URLs that open external links open the link in the default browser of the user's mobile device.

</td><td>

![Browser screen showing a relative link within the app.](../image/url_screen.png "Browser screen showing a relative link")

</td></tr></tbody>
</table>