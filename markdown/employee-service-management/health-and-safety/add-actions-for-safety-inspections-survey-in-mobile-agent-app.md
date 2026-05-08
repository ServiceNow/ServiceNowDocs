---
title: Add actions for safety inspections survey in Mobile Agent app
description: Learn how to use the Mobile Agent app to create actions for an inspection survey in online or offline mode.
locale: en-US
release: australia
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage the safety inspection and audit surveys through mobile app, Manage safety inspections and audits through the mobile apps, Mobile experience for Health and Safety, Health and Safety, Employee Service Management]
---

# Add actions for safety inspections survey in Mobile Agent app

Learn how to use the Mobile Agent app to create actions for an inspection survey in online or offline mode.

## Before you begin

Verify the following conditions:

-   The system properties for the offline mode behavior of the mobile application are configured. For more information, see Configure offline mode behavior.
-   The offline mode for the Mobile Agent app on your mobile device is turned on. For more information, see [Offline mode for Mobile Agent](../concept/hs-health-safety-mobile.md#section_hs_mobile_offline_mode).
-   The **glide.sg.offline.scheduled\_download.enabled** system property for scheduled offline caching is set. If the property is not set, manually update cache before you go offline. To update cache, navigate to **Settings** and tap **Update Cache**. This ensures that the survey is downloaded and it's ready for you to complete.

Role required: sn\_hs\_rm.safety\_inspection\_agent

## About this task

Surveys completed offline are synchronized once an internet connection is established.

For more information on how offline mode works in the mobile app, see Offline mode for mobile.

For more information on how an admin configures which survey field type should display the **Create action** check box, see [Configure the create action check box for safety inspection survey in the Mobile Agent app](hs-configure-create-action-checkbox-mobile-survey.md).

## Procedure

1.  Open the Mobile Agent app on your mobile device.

2.  In the navigation bar, tap **Home**.

3.  To open surveys,

<table id="choicetable_adf_tqn_lfc"><thead><tr><th align="left" id="d783985e147">

Section

</th><th align="left" id="d783985e150">

Steps

</th></tr></thead><tbody><tr><td id="d783985e156">

**My Surveys**

</td><td>

Tap **My Assessments and Surveys**.All surveys that were downloaded before you went offline are listed.

</td></tr><tr><td id="d783985e170">

**Inspections**

</td><td>

1.  Tap **See all** or select the inspection record visible on the page.
2.  Tap the inspection record and select **Open inspection record**.
3.  Tap **Open inspection survey**.


</td></tr></tbody>
</table>4.  In the list, tap the inspection survey that you want to complete.

5.  Conduct a safety walk and fill in the survey.

    To add actions for survey responses perform the following steps:

    1.  Select the **Create action** check box for responses to the questions for which you want to add the action.
    2.  Add the **Short description**, **Type**, and **Due date**.
    3.  In the **Assigned to** field, enter the name of the agent the survey should be assigned to.
6.  Tap **Submit**.


## Result

The action created appears in the **Actions** tab of the inspection record and can be edited or deleted by using the More actions \(![more actions icon](../../legal-request-management/image/more-button-icon.png)\) icon.

**Parent Topic:**[Manage the safety inspection and audit surveys through mobile app](../concept/hs-configure-manage-safety-inspections-audits-mobile.md)

