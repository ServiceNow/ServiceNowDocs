---
title: Engagement Messenger properties
description: You can configure the system properties for your Engagement Messenger module so that you can enable Virtual Agent chat, multi-provider SSO, and set a user session time-out value.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Engagement Messenger, Set up self-service, Configure, Customer Service Management]
---

# Engagement Messenger properties

You can configure the system properties for your Engagement Messenger module so that you can enable Virtual Agent chat, multi-provider SSO, and set a user session time-out value.

## Properties installed with Engagement Messenger

After you configure an Engagement Messenger module, set the following system properties that are based on your configuration of the messenger module.

**Tip:** In the navigation filter, enter `sys_properties.list` to view the list of all the system properties and search for the property that you want to update.

<table id="table_qbv_3d4_pwb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**com.glide.cs.embed.csp\_frame\_ancestors**

</td><td>

After activating the Glide Virtual Agent plugin \(com.glide.cs.chatbot\), you must use the **com.glide.cs.embed.csp\_frame\_ancestors** system property to enable the configuration of the frame-ancestors policy for the website where you want to host Engagement Messenger.Set the value of the **com.glide.cs.embed.csp\_frame\_ancestors** system property 'self' &lt;`your website URL`&gt;. For example, 'self' `https://www.example.com`

-   Type: string
-   Value: self
-   Location: System Properties

</td></tr><tr><td>

**glide.authenticate.multisso.enabled**

</td><td>

Set the **glide.authenticate.multisso.enabled** system property to true to enable multiple provider SSO.-   Type: true \| false
-   Value: self
-   Location: System Properties

**Note:** If you want to enable only a guest user experience for your customer service portal, you can ignore this configuration.

</td></tr><tr><td>

User session time-out **glide.ui.session\_timeout**

</td><td>

Set a user session timeout value for the **glide.ui.session\_timeout** system property to a value that is greater than or equal to your website time-out.-   Type: integer
-   Value: 30
-   Location: System Properties

**Note:** If you want to enable only a guest user experience for your customer service portal, you can ignore this configuration.

</td></tr><tr><td>

**sn\_customerservice.emails.customportal**

</td><td>

Set the URL of your third-party customer support portal so that the notification emails that your customers get contain URLs that redirect them to the exact request record that they submitted.

These notification emails are sent in scenarios such as submitting a case, requesting a service, requesting a field technician, or booking a walk-up appointment.

-   Type: string
-   Value: None
-   Location: System Properties

For example, if your customer support portal is `https://www.example.com/support`, then set the property value to `https://www.example.com/support`.

</td></tr><tr><td>

**sn\_csm\_ec.proactive\_inactivity\_time**

</td><td>

Set the inactive period \(in seconds\) to trigger proactive help in Engagement Messenger.-   Type: integer
-   Value: 2
-   Location: System Properties

</td></tr><tr><td>

**glide.knowman.serviceportal.use\_numbered\_url**

</td><td>

The property contains a comma-separated list of service portal record sys\_ids. For any portal record specified in this property, the article link will be displayed with the sysparm\_number URL parameter instead of sys\_kb\_id.-   Type: string
-   Value: None
-   Location: System Properties

</td></tr></tbody>
</table>