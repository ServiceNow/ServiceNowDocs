---
title: Configure a custom Vonage provider
description: Configure an SMS with Vonage Provider so that every user can log in securely.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/vonage-provider-config.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Multi-factor authentication providers, SMS as an MFA factor, MFA factor policies, MFA verification methods, Configuring MFA, Multi-factor authentication, Authentication, Access Management]
---

# Configure a custom Vonage provider

Configure an SMS with Vonage Provider so that every user can log in securely.

## Before you begin

Role required: adaptive\_auth\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message** and perform the REST message configuration based on the information from Vonage API Dashboard.

    \[Omitted image "vonage-dashboard.png"\] Alt text: Vonage API Dashboard

2.  Select **New** to create a new **REST Message**.

3.  Provide a **Name** and **Endpoint**.

    \[Omitted image "vonage-rest.png"\] Alt text: Vonage REST Message configuration

4.  Select **Submit**.

5.  Open the created record, in the **HTTP Methods** related list, select **New** and select the HTTP method as **POST**.

6.  Fill the following fields:

    -   Endpoint: `https://${baseURL}/sms/json`
    -   Content: `api_key=${apiKey}&api_secret=${apiSecret}&text=${text}&from=${from}&to=${to}`
    -   Content-Type: `application/x-www-form-urlencoded`
    \[Omitted image "vonage-http-method.png"\] Alt text: HTTP Method

7.  Update the record.

8.  Select **Auto-generate variables** from the **Related Links** section.

9.  Import SI shared in the folder and copy the apiKey and secret from the Vonage API dashboard.

    **Note:**

    The apiKey and secret are located in your Vonage account settings in the Vonage Dashboard.

    \[Omitted image "vonage-script.png"\] Alt text: Script

10. Create a custom Table Phone Numbers with two columns, for example:

    -   **Column Label**: User, **Type**: Reference, **Reference**: User \(sys\_user\).
    -   **Column Label**: Phone Number, **Type**: Phone Number\(E164\).
    \[Omitted image "vonage-phone-number.png"\] Alt text: Phone Number

11. Create a custom provider in Multi-Factor Provider table.

    \[Omitted image "vonage-provider-config.png"\] Alt text: Provider Configuration page

    To learn more about provider configuration, see [Configure MFA Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/configure-mfa-provider.md).


