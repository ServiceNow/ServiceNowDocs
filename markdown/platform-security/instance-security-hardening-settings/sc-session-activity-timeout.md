---
title: Minimize session activity timeout duration \[Updated in Security Center 1.3\]
description: Use the glide.ui.session\_timeout property to designate, in minutes, activity timeout value.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/instance-security-hardening-settings/sc-session-activity-timeout.html
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Minimize session activity timeout duration \[Updated in Security Center 1.3\]

Use the **glide.ui.session\_timeout** property to designate, in minutes, activity timeout value.

There are several functional impacts from setting this property:

-   The longer the specified session time-out, the greater the amount of memory is utilized during a processing session. The base system uses a default Apache Tomcat timeout duration of 30 minutes.
-   The ServiceNow AI Platform still logs out users out with Remember Me. After 30 minutes of inactivity in the application, the platform logs the user out automatically, unless the **Remember Me** check box in the login page is selected. What ’s different is that they don’t log in again to continue.
-   If there are gauges or content on users' home pages that refresh automatically, then this timeout may never be reached.

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.ui.session\_timeout**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Category|[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-session-management.md)|
|Purpose|To enforce session timeout.|
|Recommended value|User specified timeout in minutes. 60 minutes is the recommended value, but this value may vary depending on functionality and security requirement. Do not set this value to more than one day.|
|Security risk rating|7.5|
|Functional impact|This remediation enforces timely expiration of user account. No functionality impact, however User experience is altered.|
|Security risk|\(High\) User sessions being active for indefinite amount of time is a security risk and should expire on a time-based configuration.|
|References|[Manage user sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/user-administration/c_ManageUserSessions.md)|

To learn more about adding or creating a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md).

**Parent Topic:**[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/instance-security-hardening-settings/sc-session-management.md)

