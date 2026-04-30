---
title: Provide source credentials for the First Advantage service
description: Provide the source and SOAP credentials for the First Advantage service so that it can be accessed for integration.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrating with the First Advantage service, HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Provide source credentials for the First Advantage service

Provide the source and SOAP credentials for the First Advantage service so that it can be accessed for integration.

## Before you begin

**Important:** Integrating with the First Advantage service is being prepared for deprecation. It will be hidden and unavailable for activation from Zurich, but will continue to be supported till Brazil. If you have an active subscription, you can still activate the plugin by submitting a [plugin activation request](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/plugins/task/t_RequestAPlugin.html). For more details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

Role required: sn\_hr\_integrations.admin

So the First Advantage service can be accessed for integration, you must provide:

-   SOAP credentials, including the endpoint URL, user name, and password
-   Parent account
-   Account
-   Requestor email address

## Procedure

1.  Navigate to **All** &gt; **HR Integrations** &gt; **Sources**.

2.  Open the **First Advantage** record.

3.  In the **SOAP credentials** related list, provide the SOAP credentials to use with your integration.

<table id="table_ad3_kyn_pdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Endpoint URL

</td><td>

Unique endpoint URL provided by the third-party system.**Note:**

-   The default value is a placeholder URL only. Make sure to replace it with the unique endpoint URL that you get from your third-party provider.
-   Data that is transferred between the customer instance and the third-party system is secured through standard SSL. For a secure connection, provide an encrypted HTTPS link.


</td></tr><tr><td>

Inbound Username

</td><td>

User name for inbound data pull.

</td></tr><tr><td>

Inbound Password

</td><td>

Password for inbound user name.**Note:** You must enter an explicit value for this field. The value you enter is encrypted with the key for the instance, so values imported from other instances using XML files or update sets do not work.

</td></tr><tr><td>

Outbound Username

</td><td>

User name for outbound data push.

</td></tr><tr><td>

Outbound Password

</td><td>

Password for outbound user name.**Note:** You must enter an explicit value for this field. The value you enter is encrypted with the key for the instance, so values imported from other instances using XML files or update sets do not work.

</td></tr></tbody>
</table>4.  Right-click the form header and click **Save**.

5.  In the **HR Integrations Additional Inputs** related list, provide the value for each key.

    -   parent\_account
    -   account
    -   requestor\_email\_address
6.  In the **HR integrations source properties** related list, you can turn on or off the following source properties.

<table id="table_tsj_szp_4cb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_hr\_integrations.debug

</td><td>

Enables the debug log to display responses from the third-party system. Turn on to troubleshoot and debug the integration on an as-needed basis.-   Type: true or false
-   Default value: false
-   Location: Navigate to **HR Integrations** &gt; **Logs** to view the development logs.


</td></tr></tbody>
</table>
**Parent Topic:**[Integrating with the First Advantage service](../concept/hr-integrations-with-first-advantage.md)

**Previous topic:**[Integrating with the First Advantage service](../concept/hr-integrations-with-first-advantage.md)

**Next topic:**[Verify integration for the First Advantage service](verify-base-inbound-integration-for-first-advantage.md)

