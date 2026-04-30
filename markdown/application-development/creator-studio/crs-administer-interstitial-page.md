---
title: Disable the App type page in Creator Studio
description: Hide the App type page that appears when users select to create an app by adding a system property to streamline the app creation process.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Disable the App type page in Creator Studio

Hide the App type page that appears when users select to create an app by adding a system property to streamline the app creation process.

## Before you begin

You must change your scope to global. For more information, see [Global scope](../../applications/concept/c_GlobalScope.md).

Role required: admin

## Procedure

1.  Open the **All** menu.

2.  Type `sys_properties.list` and press Enter.

3.  Select the **New** button.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter `apptype.selection.disabled`.|
    |Description|Disable the app type page in Creator Studio.|
    |Choices|Leave blank.|
    |Type|Select **true \| false**.|
    |Value|Enter `true`.|
    |Ignore cache|Leave as-is.|
    |Private|Leave as-is.|
    |Read roles|Leave as-is.|
    |Write roles|Leave as-is.|

    ![System Property form showing configuration fields for an example property](../image/crs-sys-property-interstitial.png "System property form")

5.  Select **Submit**.


## Result

Users on the instance will no longer see that App type selection page after they initiate creating an app.

To reinstate the App type page, set the **apptype.selection.disabled** property to `false`, or just delete it.

**Parent Topic:**[Administering Creator Studio](../concept/administering-creator-studio.md)

