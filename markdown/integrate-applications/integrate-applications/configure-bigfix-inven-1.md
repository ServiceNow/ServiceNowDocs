---
title: Generate an API key
description: Generate an API key that enables your ServiceNow instance to request access to the BigFix Inventory instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
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

2.  On the Overview page, select the Profile icon \(\[Omitted image "bigfix-inventory-spoke-profile-icon.png"\] Alt text: Profile icon.\).\[Omitted image "bigfix-inventory-spoke-overview-page.png"\] Alt text: BigFix Inventory portal Overview page.

3.  Select Profile.

4.  On the Edit User page, select the Show token link in the API Token field.\[Omitted image "bigfix-inventory-spoke-api-token-link.png"\] Alt text: Show token link in the API Token field.

5.  Copy the API token and store at a secure place.

6.  Navigate to **Management** &gt; **Configuration** &gt; **Mail Setting**.

7.  Configure the mail settings.

    \[Omitted image "bigfix-mailsettings.png"\] Alt text: Mail settings.

8.  Schedule exports of the required reports.

    1.  Navigate to the required report under **Reports**, for example, **Computers**.

        \[Omitted image "bigfix-report.png"\] Alt text: BigFix reports.

    2.  Select **Schedule Export**.

        \[Omitted image "bigfix-comp-rep.png"\] Alt text: Schedule export.

    3.  On the form, specify the ServiceNow instance email address to which the report must be sent and the frequency and time at which the report must be emailed.

        \[Omitted image "bigfix-scheduleexp.png"\] Alt text: Schedule Export configurations.

    4.  Save the configurations.


