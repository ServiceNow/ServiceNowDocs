---
title: Infrastructure Security
description: Use Infrastructure security tools to create, upload, and manage certificates your instance uses to encrypt traffic from client to server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/platform-encryption/infrastructure-security.html
release: australia
product: Platform Encryption
classification: platform-encryption
topic_type: concept
last_updated: "2026-05-29"
reading_time_minutes: 1
breadcrumb: [Key Management Framework, Encryption]
---

# Infrastructure Security

Use Infrastructure security tools to create, upload, and manage certificates your instance uses to encrypt traffic from client to server.

The Infrastructure Security plugin provides the tools that you can use to manage the Transport Layer Security \(TLS\) ciphers and certificates. Your instance uses TLS to encrypt traffic from the client to your server.

-   **Select the ciphers used on your instance**

    Navigate to **All** &gt; **Infrastructure Security Settings** &gt; **TLS Settings** to configure which TLS 1.2 ciphers your instance uses and the order in which they are tried. TLS 1.3 ciphers are fixed and cannot be modified. Custom ciphers can be configured through Customer Support.

-   **Generate and upload your own certificates**

    Use the infrastructure security tools to generate your own certificate signing requests, which can be signed by the certificate authority of your choice. Navigate to **All** &gt; **Infrastructure Security Settings** &gt; **Upload Certificate** to upload the signed certificate to your instance's load balancer. See [Generate a Certificate Signing Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/inf-sec-generate-csr.md).

-   **Monitor the status of your ciphers and certificates**

    Use the **All** &gt; **Infrastructure Security Settings** &gt; **TLS Settings History** and **All** &gt; **Infrastructure Security Settings** &gt; **View SYOC Settings** pages to view the status of changes you have made to your ciphers and certificates.


## Install the Infrastructure Security plugin

Install the ServiceNow Infrastructure Security Settings \(com.glide.infrastructure\_security\) plugin to get started using these features. For details on plugin activation, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).

After installing the plugin, enable Sign Your Own Security \(SYOC\) functionality by setting the **sn\_infra\_sec.syoc.enabled** system property to `true`.

**Note:** If the **sn\_infra\_sec.syoc.enabled** property isn't available on your instance, you must create it. For details on this process see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md).

-   **[Generate a Certificate Signing Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/inf-sec-generate-csr.md)**  
Use the Generate Certificate Signing \(CSR\) page to create a certificate signing request to support customer-signed certificates for your instance load balancer.

**Parent Topic:**[Key Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/encryption.md)

