---
title: Configure a JSON Web Token \(JWT\) provider and token for Health Log Analytics
description: Configure a JWT provider and token to authenticate log streaming integrations sending data to Health Log Analytics \(HLA\) via ITOM Gateway. This configuration is required before you can activate any ITOM Gateway integration in Integrations Launchpad.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/hla-jwt-token-config.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-05-04"
reading_time_minutes: 3
keywords: [JSON Web Token provider, JWT provider, JSON Web Token token, JWT token, authenticate, Health Log Analytics, HLA, ITOM Gateway, MID-less log streaming]
breadcrumb: [MID-less log streaming, MID-less integrations, Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure a JSON Web Token \(JWT\) provider and token for Health Log Analytics

Configure a JWT provider and token to authenticate log streaming integrations sending data to Health Log Analytics \(HLA\) via ITOM Gateway. This configuration is required before you can activate any ITOM Gateway integration in Integrations Launchpad.

## Before you begin

-   Review the [MID-less log streaming via ITOM Gateway in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-midless-streaming.md) documentation.
-   Verify that Health Log Analytics version 36.0.19 or higher is installed on your instance.
-   Verify that the user creating the KeyStore has appropriate access permissions for the `sys_certificate`,`jwt_key_store`, `jwt_provider`, and `sn_ics_jwt_config` tables and for the relevant cryptographic modules. For ACL recommendations, see the [How to resolve Key Management Framework access denied errors for Password2 decryption \[KB1112530\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1112530) article in the Now Support Knowledge Base.

Role required: sys\_admin

## About this task

This procedure creates a JWT token for ITOM Cloud Services, which enables HLA to authenticate incoming log data from external sources via ITOM Gateway. For more information, see [MID-less log streaming via ITOM Gateway in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-midless-streaming.md).

## Procedure

1.  In a terminal or PowerShell session, generate a private key, certificate, and keystore.

    Use the following commands:

    ```
    # Generate the private key 
    openssl genrsa -out private.key 2048 
    
    # Create the certificate (metadata prompts are optional) 
    openssl req -new -x509 -key private.key -out public_key.cer -days 9125 -sha256 
    
    # Create the keystore 
    openssl pkcs12 -export -in public_key.cer -inkey private.key -out my_keystore.p12 -name my_keystore 
    ```

    These commands produce two output files used in later steps: `my_keystore.p12` and `public_key.cer`.

2.  On the ServiceNow instance, create a certificate record that stores the keystore.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**.

    2.  Select **New** to create a record.

    3.  Fill in the required fields.

    4.  Set **Type** to Java Key Store.

    5.  In the **Key store password** field, enter the keystore password generated in step 1.

    6.  Attach the `my_keystore.p12` file created in step 1.

    7.  Select **Submit**.

    **Note:**

    -   If you encounter keystore password errors, re-enter the password carefully and use the Validate Keystore option on the certificate record to confirm it is correct.
    -   If files are not attaching, confirm that both `my_keystore.p12` and `public_key.cer` are attached to their respective records.
3.  Create a JWT Key that links the signing credentials to the certificate.

    1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Keys**.

    2.  Select **New** to create a record.

    3.  Fill in the **Name** field.

    4.  Set **Signing Keystore** to the certificate record created in step 2.

    5.  In the **Signing Key** field, enter the keystore password generated in step 1.

    6.  Select **Submit**.

4.  Create a JWT Provider that defines how tokens are generated.

    1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Providers**.

    2.  Select **New** to create a record.

    3.  Fill in the **Name** field.

    4.  Set **Signing Configuration** to the JWT Key created in step 3.

    5.  Set **Expiry Interval \(sec\)** to `3600`.

    6.  Select **Submit**.

5.  Create an ICS JWT Config record that completes the connection between the JWT Provider and HLA.

    1.  Navigate to **All** &gt; **ITOM Cloud Services** &gt; **ICS JWT Config**.

    2.  Select **New** to create a record.

    3.  Fill in the **Name** field.

    4.  Set **JWT Provider** to the JWT Provider created in step 4.

    5.  Attach the `my_keystore.p12` file created in step 1.

        **Note:** This record requires its own copy of the `my_keystore.p12` file.

    6.  Select **Submit**.


## Result

The JWT provider and token are configured, enabling Health Log Analytics to authenticate incoming log data from external sources via ITOM Gateway.

## What to do next

[Set up log streaming via ITOM Gateway for Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-midless-streaming-setup.md).

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-implement.md)

