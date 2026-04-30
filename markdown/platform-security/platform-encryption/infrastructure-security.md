---
title: Infrastructure Security
description: Use Infrastructure security tools to create, upload, and manage certificates your instance uses to encrypt traffic from client to server.
locale: en-US
release: zurich
product: Platform Encryption
classification: platform-encryption
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Key Management Framework, Encryption]
---

# Infrastructure Security

Use Infrastructure security tools to create, upload, and manage certificates your instance uses to encrypt traffic from client to server.

The Infrastructure Security plugin provides the tools that you can use to manage the Transport Layer Security \(TLS\) ciphers and certificates. Your instance uses TLS to encrypt traffic from the client to your server.

-   **Select the Ciphers used on your instance**

    Using the **TLS page**, admins can configure which datacenter ciphers to use on their instance, as well as select the order in which ciphers are tried.

-   **Generate and upload your own certificates**

    Use the infrastructure security tools to generate your own certificate signing requests, which can be signed by the certificate authority of your choice. Then, you can use the tools to upload the signed certificate to your instance's load balancer.

-   **Monitor the status of your ciphers and certificates**

    Use the **TLS Settings** and **SYOC Settings** pages to view the status of changes you have made to your ciphers and certificates.


## Install the Infrastructure Security plugin

Install the ServiceNow Infrastructure Security Settings \(com.glide.infrastructure\_security\) plugin to get started using these features. For details on plugin activation, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

After installing the plugin, enable Sign Your Own Security \(SYOC\) functionality by setting the **sn\_infra\_sec.syoc.enabled** system property to `true`.

**Note:** If the **sn\_infra\_sec.syoc.enabled** property isn’t available on your instance, you must create it. For details on this process see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

-   **[Generate a Certificate Signing Request](../task/inf-sec-generate-csr.md)**  
Use the Generate Certificate Signing \(CSR\) page to create a certificate signing request to support customer-signed certificates for your instance load balancer.

**Parent Topic:**[Key Management Framework](../../encryption/concept/encryption.md)

