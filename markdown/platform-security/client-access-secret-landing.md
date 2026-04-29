---
title: Configuring client accessible secrets
description: Learn how to configure your instance to use client accessible secrets.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Secrets Management, Platform Security]
---

# Configuring client accessible secrets

Learn how to configure your instance to use client accessible secrets.

Use this example implementation to configure Secrets Management without using proxies, or giving ServiceNow access to your decrypted data.

For more detail on using client-side Secrets Management to manage access to passwords and groups, see [Understanding client side Secrets Management](understand-sec-man.md).

These instructions assume you have a MID server configured on your local network. For information on this process see [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Process overview

-   **1. [Create encryption keys and certificate](../task/client-access-example-1.md)**

    Create encryption keys and a certificate using terminal commands on your local environment.

-   **2. [Add your certificate to the ServiceNow Trusted Key Store](../task/client-access-example-2.md)**

    Upload your key and certificate to the ServiceNow Trusted Key Store.

-   **3. [Create a secret group with criteria](../task/client-access-example-3.md)**

    Create a group for your secrets. Secret groups to organize your secrets into groups. Using these groups you can apply access policies to those secrets at a group level. Then associate your secrets group to an identity group, and add your MID server to that identity group.

-   **4. [Upload the public/private keypair to the MID Server](../task/client-access-example-5.md)**

    Upload your public/private keypair to your MID server. This keypair enables the MID server to handle authentication requests from your instance.

-   **5. [Create credentials and test credential encryption](../task/client-access-example-4.md)**

    Create a credential to authenticate into a third-party system and test that ServiceNow can't access the credential.

-   **6. [Configure Flow Designer to manage the integration](../task/client-access-example-6.md)**

    On your instance, use Workflow Studio to manage an integration between your local network and your instance.

-   **7. [Test the end-to-end client-side encrypted secrets integration](../task/client-access-example-7.md)**

    Test your integration, and review the execution details to confirm your configuration is working.


-   **[Create encryption keys and certificate](../task/client-access-example-1.md)**  
Create encryption keys and a certificate using terminal commands on your local environment.
-   **[Add your certificate to the ServiceNow Trusted Key Store](../task/client-access-example-2.md)**  
Upload your key and certificate to the ServiceNow Trusted Key Store.
-   **[Create a secret group with criteria](../task/client-access-example-3.md)**  
Create a group for your secrets. Secret groups to organize your secrets into groups, and enable you to apply access policies to those secrets at a group level. Then associate your secrets group to an identity group, and add your MID Server to that identity group.
-   **[Upload the public/private keypair to the MID Server](../task/client-access-example-5.md)**  
Upload your public/private keypair to your MID Server. This keypair enables the MID Server to handle authentication requests from your instance.
-   **[Create credentials and test credential encryption](../task/client-access-example-4.md)**  
Create a credential to authenticate into a third-party system.
-   **[Configure Flow Designer to manage the integration](../task/client-access-example-6.md)**  
On your instance, use Workflow Studio to manage an integration between your local network and your instance.
-   **[Test the end-to-end client-side encrypted secrets integration](../task/client-access-example-7.md)**  
Test your integration, and review the execution details to confirm your configuration is working.
-   **[Test a Windows Management Instrumentation credential encrypted with Secrets Management](../task/client-access-example-8.md)**  
Verify that your Windows Management Instrumentation \(WMI\) credential is encrypted with Secrets Management and use an Integration Hub workflow to complete end-to-end testing.
-   **[Cloning and Secrets Management](../reference/cloning-and-secrets-mgmt.md)**  
Learn how to reconfigure secrets groups and client secrets groups after a clone.

**Parent Topic:**[Secrets Management](secrets-management.md)

