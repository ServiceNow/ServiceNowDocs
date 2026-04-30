---
title: Walk-up feature configuration
description: Understand the configuration of the Walk-up feature in the Engagement Messenger module to configure the field values.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Engagement Messenger reference, Customer Service Management reference, Customer Service Management]
---

# Walk-up feature configuration

Understand the configuration of the Walk-up feature in the Engagement Messenger module to configure the field values.

To enable a walk-up feature for your customers, verify that you activate the following plugins in your ServiceNow instance:

-   Walk-up for CSM plugin \(com.snc.walkup\_for\_csm\) for authenticated users
-   Guest Walk-up Experience for Customer Service plugin \(sn\_guest\_walkup\_cs\) for unauthenticated users

Once the plugin is active, navigate to the Features section of the guided configuration view of your Engagement Messenger module and enable the Field service feature.

![Feature settings screen in Engagement messenger with an option to add a custom feature or toggle existing features to activate them. This example shows the Walk-up feature toggle.](../image/em-enable-walk-up.png "Walk-up feature")

<table id="table_opq_wb1_g4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title text

</td><td>

Title for the feature widget in the messenger.

</td></tr><tr><td>

Subtitle text

</td><td>

Description for the feature widget in the messenger.

</td></tr><tr><td>

Enable for unauthenticated users

</td><td>

Option for enabling the walk-up feature for guest users who visit the website that hosts the messenger.

</td></tr><tr><td>

Enable for authenticated users

</td><td>

Option for enabling the walk-up feature for users who sign in into the website that hosts the messenger.

</td></tr></tbody>
</table>Select **Configure walk-up here** to configure details of your customer support centers. For more information, see [Configure Walk-up Experience locations](../task/csm-walkup-define-location.md).

