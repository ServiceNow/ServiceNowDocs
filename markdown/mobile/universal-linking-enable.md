---
title: Enable mobile universal linking
description: Enable the universal linking option if you want a web banner displayed on specified pages of the ServiceNow platform website. By default the mobile universal linking option is not available in the base system.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Universal linking for mobile, Mobile URLs, Configuring the Mobile Platform, Mobile Platform]
---

# Enable mobile universal linking

Enable the universal linking option if you want a web banner displayed on specified pages of the ServiceNow platform website. By default the mobile universal linking option is not available in the base system.

## Before you begin

Role required: admin

## Procedure

1.  In the web-based UI, enter `sys_properties.list` in the filter navigator, to open a list of system properties.

2.  In the **Name** field, search for the term `*universal`.

3.  Select the property `glide.sg.universal_links.enabled`.

4.  In the universal links system property table, set the **Value** field to `true`.

5.  Right-click in the header and select **Save**.

6.  In the web-based UI, enter `sys_sg_mobile_application.list` in the filter navigator to open a list of mobile applications in the `sys_sg_mobile_application` table.

7.  Select the **Request** record, and open the **Deep Link Configuration** tab.

8.  Select the **Route to Public Store if not installed** check box to enable it.

9.  Right-click in the header and select **Save**.

10. Repeat Steps 6 through 9 for the **Agent** record.


## What to do next

After you have enabled the mobile universal linking feature, you can perform the following configuration:

Define specific ServiceNow platform website pages to display the web banner, where the user does not have a specific mobile app installed. See, [Mobile universal linking for supported URLs](../concept/universal-linking-support-urls.md).

**Parent Topic:**[Universal linking for mobile](../concept/universal-links-mobile.md)

