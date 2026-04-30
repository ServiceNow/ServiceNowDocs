---
title: System properties for password expiration
description: You can configure the system properties that support operations in password expiration.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# System properties for password expiration

You can configure the system properties that support operations in password expiration.

To navigate to the system properties, you can select **All** and then enter **sys\_properties.list** in the navigation filter.

<table id="table_agw_xmw_rsb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

pwd\_reset.enable.password\_expiration\_reminder

</td><td>

Use this property to enable or turn off a password expiration feature. By default, the value of this property is **false**, which means that password expiration is turned off by default.

</td></tr><tr><td>

pwd\_reset.enable.dbListener

</td><td>

Use this property to enable or turn off the password reset DB listener \(to raise events\). The default value is **true**, which means that the property is enabled by default.

 **Note:** If this property is enabled, the password expiration records are managed automatically while inserting or deleting user data. While importing bulk data, for each sys\_user or sys\_user\_grmember insertion or deletion, password expiration records are inserted or updated for each password reset process that users are entitled to. Even if updating the expiration data is an asynchronous activity, this activity might impact the performance, if the number of users is high. In that case, disable the **pwd\_reset.enable.dbListener** property by setting it to **false** so that there is not an event on insertion or deletion of sys\_user or sys\_user\_grmember.

</td></tr><tr><td>

pwd\_reset.password\_expiration.error\_count

</td><td>

Number of maximum attempts \(if there is failure\) while retrieving the expiration details from the external credential store for a user.

 The default value is **5**. The expiration record is deactivated if the error count exceeds the value of this property.

 This property is not available by default. To use the property, you must create it.

</td></tr><tr><td>

pwd\_reset.refresh\_expiration\_data.duration

</td><td>

Duration, in days, to refresh the expiration details for a user whose password never expires. The default value is **30 days**.

 This property is not available by default. To use the property, you must create it.

</td></tr></tbody>
</table>**Related topics**  


[Configure password expiration reminder](../task/password-reset-expiration-setup.md)

