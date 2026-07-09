---
title: ServiceNow Security Center announcements
description: Enable security banner announcements and notifications to stay informed about urgent and critical security alerts using high visibility banners visible to administrators within the instance UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/security-center/scc-banner.html
release: australia
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Center, Platform Security]
---

# ServiceNow Security Center announcements

Enable security banner announcements and notifications to stay informed about urgent and critical security alerts using high visibility banners visible to administrators within the instance UI.

\[Omitted image "sec-banner-example.png"\] Alt text: Security banner announcement on the security center dashboard

Security banner announcements and notifications are announcements that are sent by ServiceNow and displayed to customer administrators with the **sn\_vsc.security\_center\_admin** role, to keep you informed about fixes for potential security threats that were discovered recently. These alerts contain a summary of the security risk and include a link where you can learn more and act to secure your instance.

\[Omitted image "sec-notification.png"\] Alt text: Security notification on the security center dashboard

Administrators can dismiss banner by selecting the close \(x\) button, but the banner re-appears with each new session until the banner expiration date is passed. Administrators can disable banner announcements by setting the **sn\_vsc.configure\_customer\_push\_action** system property value to `false`. The duration for which the banner appears is controlled by **Start** and **End** field values for the banner. These fields are found in banner's record in the Banner Announcement \[sys\_ux\_banner\_announcement\] table.

## Enable or disable security banner announcements

The security banner feature is enabled by default. To enable or disable security banner announcements, navigate to **System Security** &gt; **Security Center** &gt; **Notifications**. From this page, select the **Manage announcement settings** button.

\[Omitted image "sc-banner-1.png"\] Alt text: Manage security banner announcements

**Parent Topic:**[Security Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/security-center/sec-center-v2.md)

