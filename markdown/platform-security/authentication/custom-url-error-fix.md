---
title: Custom URL errors and fixes
description: A list of common errors and associated fixes for a custom URL setup and configuration.Target Audience: ServiceNow Admin
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Custom URLs association to your instance, Authentication, Access Management]
---

# Custom URL errors and fixes

A list of common errors and associated fixes for a custom URL setup and configuration.

## Errors during setup

<table id="table_vvn_1vb_2db"><thead><tr><th>

Error message

</th><th>

Fix

</th></tr></thead><tbody><tr><td>

Unable to create a Custom URL. Try again later.

</td><td>

There might be an issue outside of your control interfering with the custom URL creation. Run at a different time before contacting support. **Note:** It usually takes 30 minutes to create a custom URL. If it is taking longer, contact [https://support.servicenow.com/now?draw=case](https://support.servicenow.com/now?draw=case).

</td></tr><tr><td>

Unable to submit your new Custom URL request because another Custom URL request for your instance is still in progress.

</td><td>

Check the status on your Custom URL Jobs before you submit a new request.

</td></tr><tr><td>

You must clear the following properties before the instance URL can be set: Glide Proxy, Glide Servlet.

</td><td>

 

</td></tr><tr><td>

The provisioning of &lt;custom\_domain&gt; is still in progress. This process can take up to X hours. Your instance administrator will receive a notification when this process completes.

</td><td>

After the provisioning on an instance starts for a custom URL, you must wait for the process to complete before the status changes.

</td></tr><tr><td>

&lt;custom\_domain&gt; is now set as the new instance URL. &lt;base.service-now.com&gt; is still in service, but all new URLs, such as in notifications, will use &lt;custom\_domain&gt;.

</td><td>

Only one URL can be designated as the instance URL. The other URLs that are associated with your instance can be active, but only the instance URL can use notifications.

</td></tr><tr><td>

The Custom URL &lt;custom\_domain&gt; is set to be immediately removed from the instance configuration and revert back to &lt;base.service-now.com&gt;. &lt;custom\_domain&gt; continues an association to this instance as long as the CNAME record in your DNS is set.

</td><td>

This message confirms that you intend to change your custom URL. By accepting this confirmation, you initiate the change of the URL to your instance. Any URL that is on your Domain Name list, as a custom URL, can be active unless you remove it from the CNAME record on your provider.

</td></tr><tr><td>

You cannot modify glide.servlet.uri. This property is set by Custom URL.

</td><td>



</td></tr><tr><td>

You cannot modify glide.proxy.host. This property is set by Custom URL.

</td><td>

 

</td></tr><tr><td>

The CNAME record for &lt;custom\_domain&gt; does not point to &lt;base.service-now.com&gt;.

</td><td>

The configuration on the URL provider side is not correct. Check your configuration on the CNAME record.

</td></tr><tr><td>

Missing CNAME record for &lt;custom\_domain&gt;.

</td><td>

The CNAME record must be configured from your URL provider before the custom URL can be set for your instance.

</td></tr></tbody>
</table>