---
title: Configure mobile apps to access Health and Safety applications
description: Configure the ServiceNow mobile apps to access Health and Safety applications for submitting safety incidents, observations, and job safety analyses \(JSAs\).
locale: en-US
release: zurich
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile experience for Health and Safety, Health and Safety, Employee Service Management]
---

# Configure mobile apps to access Health and Safety applications

Configure the ServiceNow mobile apps to access Health and Safety applications for submitting safety incidents, observations, and job safety analyses \(JSAs\).

## Before you begin

Ensure that the ServiceNow instance to be configured on Now Mobile app and Mobile Agent app has the following applications installed with the demo data:

-   Health and Safety Incident Management for submitting safety incidents and observations.

    **Note:** The demo data for Health and Safety Incident Management includes the launcher required to open it in the Now Mobile app.

-   Health and Safety Risk Management to submit JSAs, view safety registers, and conduct inspection and audit surveys.

Role required: none

## Procedure

1.  Download the following mobile apps for the iOS platform from the Apple App Store or for the Android platform from the Google Play Store.

    -   Now Mobile app for submitting safety incidents, observations, and JSAs, and viewing safety register documents.

        For more information on using this mobile app, see [Now Mobile app](../../../administer/mobile-employee/concept/mobile-employee-experience.md).

    -   ServiceNow Agent mobile app for conducting inspection and audit surveys offline.

        For more information on using this mobile app, see [Mobile Agent app](https://www.servicenow.com/docs/access?context=mobile-experience&version=zurich&pubname=zurich-mobile&ft:locale=en-US) app.

2.  Open the Now Mobile appor Mobile Agent app and tap the plus icon \(**+**\).

3.  Add your ServiceNow instance by entering the instance address.

4.  In the **Enter nickname** field, enter an alias for quickly identifying the instance.

5.  Tap **Save and login**.

6.  Log in to your instance.


## Result

-   For an instance with the Health and Safety Incident Management application, the **Safety** option appears in the navigation bar of the Now Mobile app in your mobile device. This option enables you to access the Health and Safety Incident Management application through the mobile device.

    **Note:** The **Safety** option appears only if the demo data is installed with the Health and Safety Incident Management on the configured ServiceNow instance.

-   For an instance with the Health and Safety Risk Management application, the **Create a job safety analysis** quick link appears in the **Home** tab of the Now Mobile app in your mobile device.

**Parent Topic:**[Mobile experience for Health and Safety](../concept/hs-health-safety-mobile.md)

