---
title: Request certificates using ACME automated DNS challenge flow
description: Request a new certificate and automatically retrieve the certificates for an application using an Automated Certificate Management Environment \(ACME\) automated flow of DNS challenge.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/request-new-certificate-using-acme-automated-flow-dns.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Automated certificate management with ACME, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Request certificates using ACME automated DNS challenge flow

Request a new certificate and automatically retrieve the certificates for an application using an Automated Certificate Management Environment \(ACME\) automated flow of DNS challenge.

## Before you begin

-   Ensure that a credential has been set up. For more information, see [Create credentials for ACME certificate authority](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-credential-for-acme-ca.md)
-   The Certificate Management catalog has been enabled.
-   A routing policy with a DNS challenge action exists. For more information, see [Set up routing policies for ACME](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/set-up-routing-policy-for-acme.md).
-   Role required: Certificate requester \[sn\_disco\_certmgmt.certificate\_requester\], certificate administrator \[sn\_disco\_certmgmt.pki\_admin\], certificate user \[sn\_disco\_certmgmt.pki\_user\], flow\_designer, action\_designer, or admin.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Service Catalog**.

2.  Access the form for requesting a new certificate.

    1.  Select **Certificate Management**.

    2.  Select **Automated Flow**.

    3.  Select **Request New Certificate \(Automated\)**.

3.  For the **Select how to manage your certificate** value, select **ServiceNow**.

4.  On the form, fill in the fields.

<table id="table_hx4_qxq_gbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Certificate Purpose

</td><td>

Determines whether the Certificate is internal or external.-   Internal: Requires a completed form
-   External: Requires importing the CSR and private key from an external source


</td></tr><tr><td>

Environment

</td><td>

Environment where the certificate must be deployed or installed. The available options are Development, Disaster recovery, Production, or Sub-Production.

</td></tr><tr><td>

Validity Period for Certificate \(In Days\)

</td><td>

Number of days the certificate is valid. The number of days the certificate is valid. This field appears only when External is selected from the Certificate Purpose field.

</td></tr><tr><td>

Validity Period for Certificate \(In Days\)

</td><td>

The number of days the certificate is valid. This field appears only when External is selected from the Certificate Purpose field.

</td></tr><tr><td>

Certificate Signing Request \(CSR\)

</td><td>

Details about the CSR containing certificate information.

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

    After the request is submitted, a task is created for completing the DNS challenge. The task is completed automatically.


## Result

-   If a value is selected in the DNS Challenge Action field in the routing policy, the system creates the required DNS record automatically through the configured DNS provider. After DNS record propagation is complete \(two minutes by default\), the DNS challenge is completed. The automated flow sends a request to the CA to get the certificate. Admins can change this duration by modifying the **sn\_disco\_certmgmt.wait\_time\_for\_dns\_record\_propagation** system property.
-   If no value is selected in the DNS Challenge Action field and the domain is already validated with the CA, the DNS challenge task completes without additional action.
-   If no value is selected in the DNS Challenge Action field and the domain is not validated, you must manually add the required DNS TXT record to complete the validation. The certificate is attached to a certificate task. The request certificate task status changes to Completed.

