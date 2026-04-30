---
title: Provide source credentials for the Sterling service
description: Provide the source and REST credentials for the Sterling service so that it can be accessed for integration.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Sterling Talent Solutions service, HR Integrations, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Provide source credentials for the Sterling service

Provide the source and REST credentials for the Sterling service so that it can be accessed for integration.

## Before you begin

Role required: sn\_hr\_integrations.admin

So the Sterling service can be accessed for integration, you must provide:

-   REST credentials, including the endpoint URL
-   user\_id
-   client\_reference\_id
-   integration\_id
-   password
-   account

## Procedure

1.  Navigate to **All** &gt; **HR Integrations** &gt; **Sources**.

2.  Open the **Sterling Background Check** record.

3.  In the **REST credentials** related list, do not provide the credentials to use with your integration.

    Instead, you must provide those credentials in the **HR Integrations Additional Inputs** related list.

    **Important:** In the corresponding HR REST service, you must provide the unique endpoint URL that you get from your third-party provider.

4.  Right-click the form header and click **Save**.

5.  In the **HR Integrations Additional Inputs** related list, provide the value for each key.

    -   user\_id
    -   client\_reference\_id
    -   integration\_id
    -   password
    -   account
6.  In the **HR integrations source properties** related list, you can add the following source property.

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
**Parent Topic:**[Integrating with the Sterling Talent Solutions service](../concept/integrate-with-sterling-service.md)

**Previous topic:**[Integrating with the Sterling Talent Solutions service](../concept/integrate-with-sterling-service.md)

**Next topic:**[Verify integration for the Sterling service](verify-base-integration-for-sterling.md)

