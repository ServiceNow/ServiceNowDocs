---
title: Renew certificates using ACME automated DNS challenge flow
description: Request to renew certificates and automatically retrieve the certificates for an application using the Automated Certificate Management Environment \(ACME\) automated flow of DNS challenge.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/renew-certificate-using-acme-automated-flow-dns.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Automated certificate management with ACME, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Renew certificates using ACME automated DNS challenge flow

Request to renew certificates and automatically retrieve the certificates for an application using the Automated Certificate Management Environment \(ACME\) automated flow of DNS challenge.

## Before you begin

-   Ensure that a credential has been set up. For more information, see [Create credentials for ACME certificate authority](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/create-credential-for-acme-ca.md).

    **Note:** The GoDaddy credential is provided with the base system inside the credential page.

-   The Certificate Management catalog has been enabled.
-   A routing policy with a DNS challenge action exists. For more information, see [Set up routing policies for ACME](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/set-up-routing-policy-for-acme.md).
-   Role required: Certificate requester \[sn\_disco\_certmgmt.certificate\_requester\], certificate administrator \[sn\_disco\_certmgmt.pki\_admin\], certificate user \[sn\_disco\_certmgmt.pki\_user\], flow\_designer, action\_designer, or admin.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Service Catalog**.

2.  Access the form for renewing a certificate.

    1.  Select **Certificate Management**.

    2.  Select **Automated Flow**.

    3.  Select **Renew Certificate \(Automated\)**.

3.  In the **Issued Certificate** field, select the Lookup using list icon \[Omitted image "lookup-using-list.png"\] Alt text: to find and select the certificate.

    The date the certificate expires is displayed in the Certificate Expires On field.

4.  Review and update the details of the certificate as needed.

<table id="table_hx4_qxq_gbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Certificate Purpose

</td><td>

Request internal or external certificate.

</td></tr><tr><td>

Certificate Format

</td><td>

Format in which the certificate is generated. The available options are: PEM, DER, and PKCS12. The default value is PEM.**Note:** The format must match the Certificate Format configured on the routing policy that handles your request. If the formats don't match with the routing policy, you're notified that manual intervention is required

</td></tr><tr><td>

Validity Period for Certificate \(In Days\)

</td><td>

The number of days the certificate is valid. This field appears only when External is selected from the Certificate Purpose field.

</td></tr><tr><td>

Certificate Signing Request \(CSR\)

</td><td>

CSR containing certificate information.

</td></tr><tr><td>

Validity Period for Certificate \(In Days\)

</td><td>

The number of days the certificate is valid. This field appears only when External is selected in the Certificate Purpose field.

</td></tr><tr><td>

Certificate Owner Group

</td><td>

Owner group for the certificate.

</td></tr><tr><td>

Certificate Owner

</td><td>

Name or role of the person who owns the certificate.

</td></tr></tbody>
</table>    The following CSR attributes are matched and auto-populated based on the certificate information from CSR:

    -   Subject Common Name
    -   Subject Alternative Name
    -   Organization
    -   Organizational Unit
    -   Locality/City
    -   Province
    -   Country
    -   Email Address
5.  Select **Submit**.

    Once the request is submitted, a task is created for completing the DNS challenge. The task is completed automatically.


## Result

-   The certificate is attached to the certificate task in the format you selected.
    -   For PEM, the server, intermediate, and root certificates are each attached as separate PEM files.
    -   For DER, the same three certificates are attached in DER format. If conversion to DER fails, the certificates are attached in PEM format and a warning is recorded in the work notes of the certificate task. The certificate has already been issued by the certificate authority, so no certificate data is lost.
    -   For PKCS12, the server certificate is attached as a key store that contains the server, intermediate, and root certificates together with the private key, encrypted with the password you stored in your external vault. The intermediate and root certificates are also attached separately in PEM format, because no private key exists for them.
-   If a value is selected in the DNS Challenge Action field in the routing policy, the system creates the required DNS record automatically through the configured DNS provider. After DNS record propagation is complete \(two minutes by default\), the DNS challenge is completed. The automated flow sends a request to the CA to get the certificate. Admins can change this duration by modifying the **sn\_disco\_certmgmt.wait\_time\_for\_dns\_record\_propagation** system property.
-   If no value is selected in the DNS Challenge Action field and the domain is already validated with the CA, the DNS challenge task completes without additional action.
-   If no value is selected in the DNS Challenge Action field and the domain is not validated, you must manually add the required DNS TXT record to complete the validation. The certificate is attached to a certificate task. The request certificate task status changes to Completed.

