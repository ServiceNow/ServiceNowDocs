---
title: Use manual registration to establish the connection to the provider instance
description: The named contact administrator will establish a secure connection to the Impact Delivery Instance \(provider instance\) using Now Service Exchange to transmit data with the Impact Store Application.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use manual registration to IDI, Impact reference, Impact]
---

# Use manual registration to establish the connection to the provider instance

The named contact administrator will establish a secure connection to the Impact Delivery Instance \(provider instance\) using Now Service Exchange to transmit data with the Impact Store Application.

## Before you begin

-   Confirm the Impact Store Application is installed and the connection to the Impact Delivery Instance has been initiated. See [Initiate the connection to the Impact Delivery Instance with manual registration](../concept/initiate-the-connection-impact-delivery-instance.md) for details.
-   A registration email with a direct link to the IDI provider connection form is sent to the named contact administrator in order during the initial connection to IDI.

For more information on Service Bridge, see [Secure data transfer using Service Bridge](../concept/service-bridge-overview.md).

Role required: Any Impact Store App role, IDI admin

## Procedure

1.  As the named contact administrator, Open the **Welcome email**.![The Welcome email with the Connect to Impact IDI button displayed.](../image/registration-welcome-email.png)

    **Note:** If you didn’t receive the registration email, reach out to your Impact Squad.

2.  Select **Connect with Impact IDI** in the registration email to go to the Provider connection form to initiate the connection between the Impact Store Application and the Impact Delivery Instance.

    Detailed screens are available in the Impact Store Application manual registration steps.

    ![The manual registration step to establish a connection between IDI and the Impact Store App.](../image/manual-registration-establish-connection.png)

3.  Complete the form as described in the Provider connection fields table.

<table id="table_s2c_zvv_gdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Company

</td><td>

-   Select Impact in the company field. If not listed, add a new company. Only the company name is required to **Submit**.
-   A new ServiceNow company is required for each instance being configured.


</td></tr><tr><td>

URL

</td><td>

The URL to your Impact Store Application IDI provider instance that is pre-populated when accessing from the registration email. Use a unique company name for each Impact instance.

</td></tr><tr><td>

Outbound status

</td><td>

Read-only status of the connection of your Impact Store Application communicating to the IDI.-   Not Onboarded: Onboarding and data have not yet been connected to synchronize with the Impact Store Application.
-   Active Replication: Onboarding and data have been successfully connected to retrieve data from IDI to the Impact Store Application.
-   Closed Complete: Onboarding and synchronization is successful.


</td></tr><tr><td>

Inbound status

</td><td>

Read-only status of the connection of your Impact Store App receiving data from the IDI.-   Not Onboarded: Onboarding and data has not yet imported from IDI to the Impact Store Application.
-   Active Replication: Onboarding and data have been successfully imported from IDI to the Impact Store App.
-   Closed Complete: Onboarding and synchronization are successful.


</td></tr></tbody>
</table>4.  Select **Save** on the Provider Connection New Record form.

    The Provider connection form will be populated.

    ![Impact connect to provider option displays after the ServiceNow Impact company is created.](../image/connect-provider.png)

5.  Select **Connect to Provider**.

    **Note:** In the option menu for the Provider connection New record, verify that View &gt; Impact is selected. This option is only available in the Impact view for the Provider connection.

    You’re redirected to IDI to authenticate the registration.

6.  Log in to IDI, if not already logged in.

    The IDI admin role is required to access the registration options.

    ![The Service Bridge registration page displays.](../image/servicebridge-registration.png)

7.  Select **Authenticate** to authorize the registration process.

    ![Impact Store App allow ServiceBridge connection.](../image/impact-store-servicebridge-auth-allow.png)

    You’re redirected back to the Impact Store Application where a verification message displays to accept the authentication request.

8.  Select **Allow** to confirm the connection between the Impact Store Application and the IDI.

    An authorization success message displays in the Service Exchange registration page.![Service Bridge authorization successful message.](../image/service-bridge-connection-successful.png)

9.  Select **Submit** to complete the registration.

    **Note:** For information on troubleshooting with Service Bridge, see [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB1571549](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1571549).

    The registration page loads for the authorization. When the state updates to Closed Complete, the authorization is successful and you may continue with the remaining Guided Setup tasks.

    ![Registration status updates to Closed Complete.](../image/registration-complete.png)

    **Note:** The authorization and state may take several moments to update.


## What to do next

-   [Verify Impact data connection](verify-impact-data-connection.md)
-   [Initiate data migration from IDI](initiate-migration-idi.md)
-   [Grant temporary instance access to your Impact Squad](hop-access-impact-squad.md)

.

**Parent Topic:**[Use manual registration to configure the Impact Store Application](../concept/use_manual_registration_configure_impact_store_application.md)

