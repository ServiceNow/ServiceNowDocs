---
title: Set up the CIC Plus integration
description: Integrate with the CIC Plus service by configuring a SAML connection between your third-party identity provider \(IDP\) and CIC Plus accounts.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating with the CIC Plus service, HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Set up the CIC Plus integration

Integrate with the CIC Plus service by configuring a SAML connection between your third-party identity provider \(IDP\) and CIC Plus accounts.

## Before you begin

Role required: sn\_hr\_core.admin

Your CIC Plus partner must then set up your account to get employee profiles for US-based employees through the get\_usa\_employee\_profile REST endpoint, as well as verify that the callback is properly configured. Finally, you must configure the source credentials to include the login URL of the identity provider service you are using with the CIC Plus integration.

To set up your integration with the CIC Plus service, you must first:

-   Be integrated with a third-party identity provider \(IDP\) service. That provider must have user records for the new hire in their system.
-   Create a user with the sn\_hr\_core.usa\_employee\_only role.
-   Gather the following information from your CIC Plus partner:
    -   SAML configuration details
    -   Company ID
-   Provide the following information to your CIC Plus partner:
    -   IP address range
    -   Platform instance URL
    -   Credentials for a user with the sn\_hr\_core.usa\_employee\_only role

Role required: sn\_hr\_integrations.admin

## Procedure

1.  Configure a SAML connection between your third-party identity provider \(IDP\) and CIC Plus accounts.

    **Important:** Make sure to configure the SAML connection with the name identifier as the employee number.

    For information on how to configure the SAML connection, refer to the CIC Plus documentation.

2.  Your CIC Plus partner must then:

    1.  Configure your account to get employee profiles for US-based employees through the get\_usa\_employee\_profile REST endpoint.

        For information and examples on the get\_usa\_employee\_profile REST endpoint, see [get\_usa\_employee\_profile](https://www.servicenow.com/docs/access?context=hr-core-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

    2.  Verify that the callback is properly configured within your CIC Plus account.

3.  Configure the source credentials to include the login URL of the identity provider service:

    1.  Navigate to **HR Integrations** &gt; **Sources**.

    2.  Open the **CIC Plus** record.

    3.  In the **HR integrations source properties** related list, open the **CIC Plus URL** source property.

    4.  In the **Value** field, provide the login URL of the identity provider service you are using with the CIC Plus integration.

        ![Provide the login URL of the identity provider service you are using with the CIC Plus integration.](../image/cic-plus-source-credentials-idp-url.png)


