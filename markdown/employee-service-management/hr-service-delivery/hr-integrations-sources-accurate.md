---
title: Provide source credentials for the Accurate service
description: Provide the source and REST credentials for the Accurate service so that it can be accessed for integration.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrating with the Accurate Background service, HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Provide source credentials for the Accurate service

Provide the source and REST credentials for the Accurate service so that it can be accessed for integration.

## Before you begin

**Important:** Integrating with the Accurate Background service is being prepared for deprecation. It will be hidden and unavailable for activation from Zurich, but will continue to be supported till Brazil. If you have an active subscription, you can still activate the plugin by submitting a [plugin activation request](https://docs.servicenow.com/bundle/paris-platform-administration/page/administer/plugins/task/t_RequestAPlugin.html). For more details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

Role required: sn\_hr\_integrations.admin

So the Accurate service can be accessed for integration, you must provide:

-   REST credentials, including the endpoint URL, user name, and password

## Procedure

1.  Navigate to **All** &gt; **HR Integrations** &gt; **Sources**.

2.  Open the **Accurate Background Check** record.

3.  In the **REST credentials** related list, provide the Basic authentication profile credentials to use with your integration.

    **Important:** In the corresponding HR REST service, you must provide the unique endpoint URL that you get from your third-party provider.

    1.  In the **Basic auth profile list** field, click the **Unlock** icon.

    2.  Select the **Accurate BG Check Credentials** profile, and then click **Preview** and open the record.

        ![Open the Accurate BG Check Credentials record.](../image/accurate-rest.png)

    3.  In the **Basic Auth Configuration** form, provide the user name and password.

        ![Provide the user name and password for the Basic auth profile for Accurate.](../image/accurate-basic-auth.png)

    4.  Click **Update**.

4.  Right-click the form header and click **Save**.

5.  In the **HR integrations source properties** related list, you can turn on or off the following source properties.

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
**Parent Topic:**[Integrating with the Accurate Background service](../concept/integrate-with-accurate-service.md)

**Previous topic:**[Integrating with the Accurate Background service](../concept/integrate-with-accurate-service.md)

**Next topic:**[Verify integration for the Accurate service](verify-base-integration-for-accurate.md)

