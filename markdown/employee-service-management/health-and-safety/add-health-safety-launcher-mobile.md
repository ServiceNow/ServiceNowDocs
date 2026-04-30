---
title: Add Health and Safety launcher tab to Now Mobile app configuration
description: Add a Health and Safety launcher screen tab to your Now Mobile app configuration. With this launcher tab, your employees can open the Health and Safety Incident Management application in the Now Mobile app on their mobile device.
locale: en-US
release: xanadu
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile experience for Health and Safety, Health and Safety, Employee Service Management]
---

# Add Health and Safety launcher tab to Now Mobile app configuration

Add a Health and Safety launcher screen tab to your Now Mobile app configuration. With this launcher tab, your employees can open the Health and Safety Incident Management application in the Now Mobile app on their mobile device.

## Before you begin

Role required: sn\_ohs\_im.admin and admin

## About this task

-   Use this procedure only if the demo data isn't included in the Health and Safety Incident Management application on your ServiceNow instance that needs to be configured on the Now Mobile app.

    The demo data for this application includes the launcher required to open it in the Now Mobile app.

-   The Now Mobile app is built using ServiceNow Mobile App Builder, so make sure you’re familiar with the [Mobile App Builder](https://www.servicenow.com/docs/access?context=mab-concept&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US) basics.


For more information about configuring a tab on the navigation bar of Now Mobile app, see [Configure the navigation bar and navigation tabs](https://www.servicenow.com/docs/access?context=config-sg-application-menu&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

2.  In the application scope selection screen, select the application scope as **Health and Safety Incident Management**.

3.  Select **All mobile records** in the left menu.

4.  From the Record type list, select **Launcher tab \[sys\_sg\_applet\_launcher\_tab\]**, and then select **New**.

    The new launcher tab screen appears where you can create a tab for Health and Safety.

5.  On the form, fill in the fields.

<table id="table_s3j_3jh_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Name that displays for your navigation bar tab. For Health and Safety, enter `Safety`.

</td></tr><tr><td>

Active

</td><td>

Toggle that sets whether the navigation bar tab is active. Inactive navigation bar tabs aren't visible.

</td></tr><tr><td>

Launcher

</td><td>

Launcher screen that appears when you tap the tab.Click **Choose** and select **OHS Launcher**.

</td></tr><tr><td>

Icon

</td><td>

Icon that displays for your navigation tab.

</td></tr></tbody>
</table>6.  Select **Save**.


**Parent Topic:**[Mobile experience for Health and Safety](../concept/hs-health-safety-mobile.md)

