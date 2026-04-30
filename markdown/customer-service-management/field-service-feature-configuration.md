---
title: Field service feature configuration
description: Understand the configuration of the field service feature in Engagement Messenger module to configure the values.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Engagement Messenger reference, Customer Service Management reference, Customer Service Management]
---

# Field service feature configuration

Understand the configuration of the field service feature in Engagement Messenger module to configure the values.

To enable the field service feature, ensure that you activate the Field Service Management - Customer Experience plugin \(com.snc.fsm\_customer\_experience\) in your ServiceNow instance.

Once the plugin is active, navigate to the Features section of the guided configuration view of your Engagement Messenger module and enable the Field service feature.

![Field service features window with an option to add a custom feature or activate an existing feature with the help of a toggle switch.](../image/em-enable-fsm-feature.png "Field service features")

|Field|Description|
|-----|-----------|
|Title text|Title for the feature widget in the messenger.|
|Subtitle text|Description for the feature widget in the messenger.|

## Enabling technician tracking from Engagement Messenger

When a technician is assigned to resolve your customer's field service request, they can track their technician from Engagement Messenger. ![Chat window showing the Track my technician feature.](../image/em-track-my-technician.png)

To enable this functionality, ensure that you meet the following criteria:

-   Activate the Field Service Management - Customer Experience plugin \(com.snc.fsm\_customer\_experience\).
-   in the sys\_user table, enable the **Geolocation tracked** field for all your field service agents who would be assigned to the customer work orders.

    For more information, see [Location tracking](https://www.servicenow.com/docs/access?context=r_LocationTracking&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


