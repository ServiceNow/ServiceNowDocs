---
title: Security banner announcements
description: Enable security banner announcements to stay informed about urgent and critical security alerts using high visibility banners visible to administrators within the instance UI.
locale: en-US
release: australia
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Center, Platform Security]
---

# Security banner announcements

Enable security banner announcements to stay informed about urgent and critical security alerts using high visibility banners visible to administrators within the instance UI.

![Security banner announcement on the security center dashboard](../images/sec-banner-example.png)

Security banner announcements are announcements displayed to customer administrators, sent by ServiceNow, to keep you informed about fixes for potential security threats that were discovered recently. These alerts contain a summary of the security risk and include a link where you can learn more and act to secure your instance.

Administrators can dismiss banner by selecting the close \(x\) button, but the banner re-appears with each new session until the banner expiration date is passed. Administrators can disable banner announcements by setting the **sn\_vsc.configure\_customer\_push\_action** system property value to `false`. The duration for which the banner appears is controlled by **Start** and **End** field values for the banner. These fields are found in banner's record in the Banner Announcement \[sys\_ux\_banner\_announcement\] table.

## Enable or disable security banner announcements

The security banner feature is enabled by default. To enable or disable security banner announcements, navigate to **System Security** &gt; **Security Center** &gt; **Notifications**. From this page, select the **Manage announcement settings** button.

![Manage security banner announcements](../images/sc-banner-1.png)

**Parent Topic:**[Security Center](sec-center-v2.md)

