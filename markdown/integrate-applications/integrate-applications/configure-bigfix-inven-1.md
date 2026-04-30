---
title: Generate an API key
description: Generate an API key that enables your ServiceNow instance to request access to the BigFix Inventory instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Generate an API key

Generate an API key that enables your ServiceNow instance to request access to the BigFix Inventory instance.

## Before you begin

BigFix Inventory requirements:

-   BigFix Inventory account
-   Role required: BigFix Inventory administrator

Complete these steps from your BigFix Inventory environment. For more information on installation and configuration, see [BigFix V9.5 Inventory Documentation](https://help.hcltechsw.com/bigfix/9.5/inventory/welcome/BigFix_Inventory_welcome.html).

## Procedure

1.  Log in to your BigFix Inventory portal.

2.  On the Overview page, select the Profile icon \(![Profile icon.](../image/bigfix-inventory-spoke-profile-icon.png)\).![BigFix Inventory portal Overview page.](../image/bigfix-inventory-spoke-overview-page.png)

3.  Select Profile.

4.  On the Edit User page, select the Show token link in the API Token field.![Show token link in the API Token field.](../image/bigfix-inventory-spoke-api-token-link.png)

5.  Copy the API token and store at a secure place.

6.  Navigate to **Management** &gt; **Configuration** &gt; **Mail Setting**.

7.  Configure the mail settings.

    ![Mail settings.](../image/bigfix-mailsettings.png)

8.  Schedule exports of the required reports.

    1.  Navigate to the required report under **Reports**, for example, **Computers**.

        ![BigFix reports.](../image/bigfix-report.png)

    2.  Select **Schedule Export**.

        ![Schedule export.](../image/bigfix-comp-rep.png)

    3.  On the form, specify the ServiceNow instance email address to which the report must be sent and the frequency and time at which the report must be emailed.

        ![Schedule Export configurations.](../image/bigfix-scheduleexp.png)

    4.  Save the configurations.


