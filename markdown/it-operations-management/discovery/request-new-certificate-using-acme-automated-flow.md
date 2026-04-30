---
title: Request new certificate using ACME manual flow of DNS challenge
description: Request a new certificate and automatically retrieve the certificates for an application using ACME manual flow of DNS challenge.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using ACME, Automated Certificate Management Environment, ITOM Visibility, IT Operations Management]
---

# Request new certificate using ACME manual flow of DNS challenge

Request a new certificate and automatically retrieve the certificates for an application using ACME manual flow of DNS challenge.

## Before you begin

-   The Certificate Management catalog should be enabled.
-   A routing policy without any DNS challenge action must exist.

Role required: Certificate requester, PKI admin, PKI user, or admin

**Note:**

Certificate requester is a user who does not have the PKI admin or PKI user role.

## Procedure

1.  Access the certificate request automated flow.

    1.  Navigate to **All** &gt; **Service Catalog**.

    2.  Select **Certificate Management**.

    3.  Select **Automated Flow**.

2.  Select **Request New Certificate \(Automated\)**.

3.  On the form, fill in the fields.

<table id="table_hx4_qxq_gbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Certificate Purpose

</td><td>

Indicates whether the request is for an internal or external certificate.For CAs \(for example, Let's Encrypt\), select **External**.

</td></tr><tr><td>

Certificate Signing Request \(CSR\)

</td><td>

CSR containing the certificate information.

</td></tr><tr><td>

Validity Period for Certificate \(In Days\)

</td><td>

Number of days the certificate is valid.For Let's Encrypt, the maximum validity period is 90 days.

</td></tr><tr><td>

Certificate Owner Group

</td><td>

Group for which the certificate tasks will be generated.

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

    Once the request is submitted, a task is created and an activity is assigned for you to complete the DNS challenge and mark it complete.

5.  On the **New certificate task** page, in the **DNS Task** field, select the record.

6.  On the **DNS Task** page, add a DNS TXT record for the attached DNS challenge.

    1.  In the **DNS Challenges** pane, copy the DNS value.

    2.  On the web browser, go to the domain and add the DNS value as a TXT record.

        For example, the domain can be **godaddy.com** &gt; **thedisconow.com**.

    3.  Fill in the other mandatory fields.

    4.  Select **Save**.

    **Note:** Most DNS updates take effect within an hour but it could take up to 48 hours to update.

7.  On the **DNS Task** page, change the status of the record to **Completed**.

8.  Check whether the DNS record has propagated successfully.

    To check if it’s propagated successfully, use the `dig` command.

9.  Select **Save**.


## Result

-   Once the DNS challenge is completed, the automated flow makes the request to the CA to get the certificate.
-   The certificate is attached to the New certificate task.
-   The certificate task status changes to Completed.

