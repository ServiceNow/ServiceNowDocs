---
title: Components installed with Engagement Messenger
description: Several types of components are installed with activation of the Engagement Messenger application, including plugins, tables, and user roles.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Customer Service Management reference, Customer Service Management]
---

# Components installed with Engagement Messenger

Several types of components are installed with activation of the Engagement Messenger application, including plugins, tables, and user roles.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Engagement Messenger admin\[sn\_csm\_ec.ec\_admin\]

</td><td>

Creates and edits configurations for Embedded Messenger modules

</td><td>

-   sn\_csm\_ec.ec\_read
-   snc\_platform\_rest\_api\_access
-   virtual\_agent\_admin
-   image\_admin
-   sp\_admin
-   ais\_admin
-   catalog\_builder\_editor

</td></tr><tr><td>

Engagement Messenger read\[sn\_csm\_ec.ec\_read\]

</td><td>

Can view existing configurations for Embedded Messenger modules**Note:** This role should only be assigned to internal users.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Chat Feature Instance\[sn\_csm\_ec\_chat\_instance\]

</td><td>

Stores configuration details of the Chat feature of the messenger modules.

</td></tr><tr><td>

Engagement Messenger Module\[sn\_csm\_ec\_engmnt\_center\_module\]

</td><td>

Stores the list of all messenger modules.

</td></tr><tr><td>

Feature\[sn\_csm\_ec\_feature\]

</td><td>

Stores the feature definitions for the messenger. Every feature instance of a messenger module is created from its feature definition.

</td></tr><tr><td>

Feature Instance\[sn\_csm\_ec\_feature\_instance\]

</td><td>

Stores the details of feature instances of the messenger module.

</td></tr><tr><td>

Greeting Feature Instance\[sn\_csm\_ec\_greeting\_instance\]

</td><td>

Stores configuration details of the Greeting feature of the messenger modules.

</td></tr><tr><td>

Knowledge Feature Instance\[sn\_csm\_ec\_knowledge\_instance\]

</td><td>

Stores configuration details of the Knowledge feature of the messenger modules.

</td></tr><tr><td>

Search Feature Instance\[sn\_csm\_ec\_search\_instance\]

</td><td>

Stores configuration details of the Search feature of the messenger modules.

</td></tr></tbody>
</table>## Properties installed with Engagement Messenger

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
</table>## Plugins installed

-   Customer Service \(com.sn\_customerservice\)
-   Integration - Multiple Provider Single Sign-On Installer \(com.snc.integration.sso.multi.installer\)

