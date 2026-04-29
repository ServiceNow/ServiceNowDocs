---
title: Set up the GovNotify spoke
description: Integrate ServiceNow instance and GovNotify account using JWT authentication to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [GovNotify Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the GovNotify spoke

Integrate ServiceNow instance and GovNotify account using JWT authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the GovNotify spoke.
-   Role required: admin.

## Procedure

1.  In the GovNotify account, create an API key.

    1.  Log in to your GovNotify account as admin.

    2.  Navigate to **API integration** and click **API Keys**.

    3.  Click **Create an API key**.

    4.  On the form, provide a name for the API key and select the required key type.

        ![Create an API key.](../image/govnotify-api.png)

    5.  Click **Continue**.

        The API key is displayed in this format: `{key_name}-{iss-uuid}-{secret-key-uuid}`. For example, if the API key is `my_test_key-26785a09-ab16-4eb0-8407-a37497a57506-3d844edf-8d35-48ac-975b-e847b4f122b0`:

        -   API key name is: `my_test_key`
        -   iss \(service id\) is: `26785a09-ab16-4eb0-8407-a37497a57506`
        -   secret key or signing key is: `3d844edf-8d35-48ac-975b-e847b4f122b0`
        For more information, see [Headers](https://docs.notifications.service.gov.uk/rest-api.html#headers) in [GovNotify REST API documentation](https://docs.notifications.service.gov.uk/rest-api.html#rest-api-documentation).

    6.  Click **Copy API key to clipboard** and record the value for later use.

        ![Copy the API key.](../image/govnotify-copy-api.png)

2.  Configure the default JWT key record in your ServiceNow instance.

    1.  Navigate to **System OAuth** &gt; **JWT Keys**.

    2.  Open the record, **GovNotify Key**.

    3.  Enter the signing key you had copied from the API key in **Signing key**.

    4.  Click **Update**.

3.  Configure the default JWT provider record in your ServiceNow instance.

    1.  Navigate to **System OAuth** &gt; **JWT Providers**.

    2.  Open the record, **GovNotify JWT Provider**.

    3.  In the **Standard claims** tab, click the **iss** record.

    4.  Enter the iss \(service id\) value you had copied from the API key in **Claim value**.

    5.  Click **Update**.

4.  Configure the default credential record in your ServiceNow instance.

    1.  Navigate to **GovNotify Spoke** &gt; **Credentials**.

    2.  Open the record, **GovNotify Cred**.

    3.  For **JWT Provider**, select the JWT provider you had configured.

    4.  Click **Update**.

5.  Configure the default connection and credential alias record in your ServiceNow instance.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Open the record, **GovNotify**.

    3.  In the **Connections** tab, click **New**.

    4.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Credential|Credential record you had configured. For example, `GovNotify Cred`.|
        |Connection URL|URL to connect to GovNotify account. Enter `https://api.notifications.service.gov.uk`.|

    5.  Click **Submit**.


