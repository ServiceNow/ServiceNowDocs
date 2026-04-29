---
title: Set up authentication credentials for the Cribl integration in Health Log Analytics
description: Configure credentials for the authentication method used by the Cribl integration.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Health Log Analytics, Cribl, integration, authentication, credentials, basic auth, token-based]
breadcrumb: [Cribl, Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Set up authentication credentials for the Cribl integration in Health Log Analytics

Configure credentials for the authentication method used by the Cribl integration.

## Before you begin

Decide on the appropriate authentication method for your instance:

-   Basic authentication is preferred for self-hosted \(On-Prem\) Cribl instances.
-   Token-based authentication is required for Cribl Cloud instances.

    **Note:** Token-based authentication is also supported for self-hosted \(On-Prem\) Cribl instances.


For token-based authentication, create a client ID and a client secret on your Cribl instance and use them to generate a token. For example:

-   Client ID: 1234567890abcdef
-   Client secret: abcdef1234567890

For detailed information on the Cribl API, refer to the [Cribl API](https://docs.cribl.io/api/) documentation.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Select the default Cribl credential alias: Cribl\_Credential\_Alias.

3.  Select **New** to create a credential record.

4.  Select the appropriate credentials type for your Cribl instance:

    -   For basic authentication, select **Basic Auth Credentials**.
    -   For token-based authentication, select **Custom Header API Key Credential**.
5.  On the displayed form, fill in the fields.

    -   For basic authentication:

        |Field|Description|
        |-----|-----------|
        |Name|A name that describes the credentials.|
        |Username|Your Cribl server username. For example: admin.|
        |Password|Your Cribl server password. For example: admin123.|

    -   For token-based authentication:

        | | |
        |---|---|
        |Name|A name that describes the credential.|
        |API Key|The authentication token you generated on the Cribl instance.|

6.  Select **Save** to save the credentials configuration.


## What to do next

-   Verify that the provided credentials have appropriate permissions to access your Cribl instance.
-   Verify that only one active credential record of each credentials type exists under the credential alias.

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](../concept/hla-implement.md)

