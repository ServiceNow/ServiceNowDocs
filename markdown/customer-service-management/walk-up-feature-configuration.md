---
title: Walk-up feature configuration
description: Understand the configuration of the Walk-up feature in Engagement Messenger module to configure the field values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/walk-up-feature-configuration.html
release: australia
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 1
breadcrumb: [Engagement Messenger reference, Reference, Customer Service Management]
---

# Walk-up feature configuration

Understand the configuration of the Walk-up feature in Engagement Messenger module to configure the field values.

To enable the walk-up feature for your customers, activate the following plugins in your ServiceNow instance:

-   Walk-up for CSM plugin \(com.snc.walkup\_for\_csm\) for authenticated users
-   Guest Walk-up Experience for Customer Service plugin \(sn\_guest\_walkup\_cs\) for unauthenticated users

Once the plugin is active:

1.  Navigate to the Features section of the guided configuration view of your Engagement Messenger module.
2.  Enable the **Walk-up** feature.

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
</table>3.  Select **Configure walk-up here** to configure details of your customer support centers. For more information, see [Configure Walk-up Experience locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/csm-walkup-define-location.md).

