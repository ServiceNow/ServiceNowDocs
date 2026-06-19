---
title: Generate a Certificate Signing Request
description: Use the Generate Certificate Signing \(CSR\) page to create a certificate signing request to support customer-signed certificates for your instance load balancer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/platform-encryption/inf-sec-generate-csr.html
release: zurich
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 1
breadcrumb: [Infrastructure Security, Key Management Framework, Encryption]
---

# Generate a Certificate Signing Request

Use the Generate Certificate Signing \(CSR\) page to create a certificate signing request to support customer-signed certificates for your instance load balancer.

## Before you begin

Role required: admin

The Infrastructure Security \(com.glide.infrastructure\_security\) plugin must be installed to perform these steps. See[Infrastructure Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/infrastructure-security.md) for details on this plugin.

For information on using custom URLs with ServiceNow, see [Set a custom URL as the instance URL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/configure-custom-url.md).

## Procedure

1.  Navigate to **All** &gt; **Infrastructure Security Settings** &gt; **Generate CSR**.

2.  Add one or more domains to your request.

    1.  Select the **Add** button under the **Domains** heading.

    2.  In the pop-up window, enter the domain and select **OK**.

    3.  Repeat these steps as needed to add more domains.

        **Note:** Domains can be removed by selecting the X button to the left of each domain entry.

3.  Enter any information that you want included in your request in the **Optional Certificate Fields**.

4.  Select **Submit**.

    **Warning:** You can't submit a request while another request is being generated. If this issue occurs, you see a "Resource in Conflict" error. To process, cancel the current request or wait for the current request to process before submitting another.

    After selecting **Submit**, your instance will generate the certificate signing request. The request appears in the **Generated CSR** field.

    \[Omitted image "generate-csr.png"\] Alt text: Generate CSR page with a completed request

5.  Copy the contents of the **Generated CSR** field.


## What to do next

After generating the CSR, complete the following steps to install the signed certificate on your instance:

1.  Submit the CSR to your Certificate Authority \(CA\). The CA signs the request and returns a signed certificate file.
2.  Upload the signed certificate to your instance. See [Uploading a certificate to an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/t_UploadACertificateToAnInstance.md).

**Parent Topic:**[Infrastructure Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/infrastructure-security.md)

