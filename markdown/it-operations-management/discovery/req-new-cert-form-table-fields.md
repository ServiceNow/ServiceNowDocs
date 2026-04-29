---
title: Requesting a new certificate form table
description: A table of the necessary fields to request a new form.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Certificate Inventory and Management reference, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Requesting a new certificate form table

A table of the necessary fields to request a new form.

<table id="table_lhb_ppz_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Certificate Purpose

</td><td>

Internal \| External

The Internal option requires you to fill out the form. Options are **Internal** or **External**. The External option requires you to import the Certificate Signing Request \(CSR\) and private key from an external source like certificatetools.com.

</td></tr><tr><td>

Certificate Signing Request \(CSR\)

</td><td>

The CSR is sent to the Certificate Authority \(CA\) to request the new certificate. This field is auto-populated when you select the **Want to generate CSR?** check box.

</td></tr><tr><td>

Private Key

</td><td>

Private key for the certificate. This field appears only when you select the **Want to generate CSR?** check box, and it is auto-populated.

</td></tr><tr><td>

Want to generate CSR?

</td><td>

Option to generate a certificate signing request \(CSR\). If activated, the CSR form must be filled.

</td></tr><tr><td>

Subject Common Name

</td><td>

Specific entity or domain name that the certificate is issued to. Enter a name or `*`.

</td></tr><tr><td>

Subject Alternative Name

</td><td>

Domain or subdomain included in the Subject Common Name. Enter an alternative name or `*`.

</td></tr><tr><td>

Organization

</td><td>

Organization making the certificate signing request for the given Subject Common Name. Enter the organization or `*`.

</td></tr><tr><td>

Organizational Unit

</td><td>

Organizational unit making the certificate signing request for the given Subject Common Name. Enter the unit or `*`.

</td></tr><tr><td>

Locality/City

</td><td>

Locality \(city\) of the organization making the certificate signing request for the given Subject Common Name. Enter the locality or `*`.

</td></tr><tr><td>

Province

</td><td>

State or province of the organization making the certificate signing request for the given Subject Common Name. Enter the state or `*`.

</td></tr><tr><td>

Country

</td><td>

Country of the organization making the certificate signing request for the given Subject Common Name. Enter the country or `*`.

</td></tr><tr><td>

Email Address

</td><td>

Email address of the administrator in the organization making the certificate signing request for the given Subject Common Name. Enter an email address or `*`.

</td></tr><tr><td>

Application Services

</td><td>

Application services for the certificate.

</td></tr><tr><td>

Servers

</td><td>

Servers the certificate can be hosted on.

</td></tr><tr><td>

Application Names

</td><td>

Specific application the certificate is issued for.

</td></tr><tr><td>

Application Servers

</td><td>

Application servers the certificate is hosted on.

</td></tr><tr><td>

Certificate Owner Group

</td><td>

Certificate owner group for the certificate.

</td></tr><tr><td>

Certificate Owner

</td><td>

Specific entity that the certificate is issued to.

</td></tr><tr><td>

Environment

</td><td>

The environment that you want your certificate for. Options are: -   Development
-   Disaster recovery
-   Production
-   Sub-Production

</td></tr><tr><td>

Renewal Tracking

</td><td>

Option to enable automatic-renewal of your certificate. This option only applies if you don’t select the **Renew automatically** field.

</td></tr><tr><td>

Renew Automatically

</td><td>

Option to set the automatically renew your certificate.

</td></tr><tr><td>

How many days before expiry does the certificate need to be renewed?

</td><td>

Numerical value.

Number of days before the expiration of your certificate, such that you want to renew the certificate before those days.

</td></tr></tbody>
</table>**Parent Topic:**[Certificate Inventory and Management reference](cert-invt-mgmt-references.md)

