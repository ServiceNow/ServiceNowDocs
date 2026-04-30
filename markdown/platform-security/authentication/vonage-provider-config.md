---
title: Vonage Provider custom configuration \(Tutorial\)
description: Configure a SMS with Vonage Provider to ensure every user can login securely.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Multi-factor authentication Providers, Multi-factor authentication with SMS, Configuring MFA, supported methods, and workflow, Multi-factor authentication \(MFA\), Authentication, Access Management]
---

# Vonage Provider custom configuration \(Tutorial\)

Configure a SMS with Vonage Provider to ensure every user can login securely.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message** and perform the REST message configuration based on the information from Vonage API Dashboard.

    ![Vonage API Dashboard](../../../administer/security-center/images/vonage-dashboard.png)

2.  Click **New** to create a new **REST Message**.

3.  Provide a **Name** and **Endpoint**.

    ![Vonage REST Message configuration](../../../administer/security-center/images/vonage-rest.png)

4.  Click **Submit**.

5.  Open the created record, in the **HTTP Methods** related list, click **New** and select the HTTP method as **POST**.

6.  Fill the following fields:

    -   Endpoint: `https://${baseURL}/sms/json`
    -   Content:`api_key=${apiKey}&api_secret=${apiSecret}&text=${text}&from=${from}&to=${to}`
    -   Content-Type: `application/x-www-form-urlencoded`
    ![HTTP Method](../../../administer/security-center/images/vonage-http-method.png)

7.  Update the record.

8.  Click **Auto-generate variables** from the **Related Links** section.

9.  Import SI shared in the folder and copy the apiKey and secret from the Vonage API dashboard.

    **Note:**

    The apiKey and secret are located in your Vonage account settings in the Vonage Dashboard.

    ![Script](../../../administer/security-center/images/vonage-script.png)

10. Create a custom Table Phone Numbers with two columns, For example:

    -   **Column Label**: User, **Type**: Reference, **Reference**: User \(sys\_user\).
    -   **Column Label**: Phone Number, **Type**: Phone Number\(E164\).
    ![Phone Number](../../../administer/security-center/images/vonage-phone-number.png)

11. Create a custom provider in Multi-Factor Provider table.

    ![Provider Configuration page](../../../administer/security-center/images/vonage-provider-config.png)

    To know more about provider configuration, see [Configure MFA Provider](configure-mfa-provider.md).


