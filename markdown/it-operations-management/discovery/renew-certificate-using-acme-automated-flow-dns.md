---
title: Renew certificate using ACME automated flow of DNS challenge
description: Request to renew the certificate and automatically retrieve the certificates for an application using an Automated Certificate Management Environment \(ACME\) automated flow of DNS challenge.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using ACME, Automated Certificate Management Environment, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Renew certificate using ACME automated flow of DNS challenge

Request to renew the certificate and automatically retrieve the certificates for an application using an Automated Certificate Management Environment \(ACME\) automated flow of DNS challenge.

## Before you begin

Ensure that a credential has been set up.

**Note:** The GoDaddy credential is provided with the base system inside the credential page.

The Certificate Management catalog has been enabled.

A routing policy with a DNS challenge action exists.

Role required: Certificate requester, PKI admin, PKI user, flow\_designer, action\_designer, or admin

**Note:**

A certificate requester is a user who doesn’t have the PKI admin or PKI user role.

## Procedure

1.  Access the certificate renew automated flow.

    1.  Navigate to **All** &gt; **Service Catalog**.

    2.  Select **Certificate Management**.

    3.  Select **Automated Flow**.

2.  Select **Renew Certificate \(Automated\)**.

3.  On the form, fill in the fields.

<table id="table_hx4_qxq_gbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Issued Certificate

</td><td>

Certificate to renew.

</td></tr><tr><td>

Certificate Purpose

</td><td>

Request internal or external certificate.For CAs \(for example, Let's Encrypt\), select **External**.

</td></tr><tr><td>

Certificate Signing Request \(CSR\)

</td><td>

CSR containing certificate information.

</td></tr><tr><td>

Validity Period for Certificate \(In Days\)

</td><td>

Number of days the certificate is valid.For Let's Encrypt, the maximum validity period is 90 days.

</td></tr><tr><td>

Certificate Owner Group

</td><td>

Group for which the certificate tasks are generated.

</td></tr><tr><td>

Certificate Owner

</td><td>

Name or role of the person who will own the certificate.

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
4.  Select **Submit**.

    Once the request is submitted, a task is created for completing the DNS challenge. The task is completed automatically.


## Result

-   Once DNS record propagation has completed after two minutes, the DNS challenge is completed automatically and the automated flow sends a request to the CA to get the certificate.

    Admins can change this duration by modifying the **sn\_disco\_certmgmt.wait\_time\_for\_dns\_record\_propagation** system property.

-   The certificate is attached to the New certificate task.
-   The request certificate task status changes to Completed.

