---
title: Activate custom URLs
description: Enable custom URLs to be set up on your ServiceNow instance. You can activate the Custom URL plugin \(com.snc.customurl\) if you have the admin role.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Custom instance URLs, Authentication, Access Management]
---

# Activate custom URLs

Enable custom URLs to be set up on your ServiceNow instance. You can activate the Custom URL plugin \(com.snc.customurl\) if you have the admin role.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Find and click the **Custom URL** plugin.

    **Note:** Do not select the **Custom URL - Internal** plugin, which is an internal component for scripted custom URL APIs.

3.  On the Custom URL record, click the **Activate/Repair** related link.

4.  In the Plugin Activation window, click **Activate**.

    When the Plugin Activation window reopens with a message that the plugin is activated, click **Close &amp; Reload Form** to stay on this form.

5.  In the Plugin Files related list, find the following property, and change the setting value:

<table id="choicetable_dhn_fnq_hz"><tbody><tr><td id="d56275e112">

**glide.customurl.enabled**

</td><td>

To enable custom URLs, set the value to **True**. By default, this property is set to **False**, which means that you cannot associate a custom URL.**Note:** To disable this feature, set this property back to **False**.

</td></tr></tbody>
</table>6.  Click **Update**.


