---
title: Certificate routing policy form table
description: To automate the processes of your certificate life cycle, you must fill out a routing policy form that populates your Certificate Signing Requests. This table shows you the required fields and values.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [ACME reference, Automated Certificate Management Environment, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate routing policy form table

To automate the processes of your certificate life cycle, you must fill out a routing policy form that populates your Certificate Signing Requests. This table shows you the required fields and values.

<table id="table_lhb_ppz_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your routing policy.

</td></tr><tr><td>

Certificate Authority

</td><td>

Certificate authority. To see a list of supported Certificate Authorities, select the search icon. Choose **EJBCA ACME**. **Note:** The certificate authority determines if additional fields are necessary for your routing policy. Fill in this field first, to see what information you need for this form.

</td></tr><tr><td>

Environment

</td><td>

The environment that you want your certificate for. Options are:-   Development
-   Disaster recovery
-   Production
-   Sub-Production

.

</td></tr><tr><td>

Assignment Group

</td><td>

Assignment group. You can select an assignment group or make a new one.

</td></tr><tr><td>

DNS Challenge Action

</td><td>

Domain name system challenge action.

</td></tr><tr><td>

Credential Alias

</td><td>

Credential alias. Your options are based on the aliases that you create in the Certificate Management Credentials form.

</td></tr><tr><td>

Certification Purpose

</td><td>

Certification Purpose. Options are:-   Internal
-   External

</td></tr><tr><td>

Is Active

</td><td>

Option to activate the policy.

</td></tr><tr><td>

Allow Duplicate Request

</td><td>

Option to allow multiple requests to receive multiple certificates.

</td></tr><tr><td>

Approval Required

</td><td>

Option to require approval.

</td></tr><tr><td>

Task Approval Group

</td><td>

Task approval group. This field appears only when the **Approval Required** field is activated.

</td></tr><tr><td>

DNS Task Assignment Group

</td><td>

DNS Task Assignment Group. Select **Certificate Inventory and Management**

</td></tr><tr><td>

Domain

</td><td>

Domain of the policy. This field is automatically set to **global**

</td></tr><tr><td>

MID Server

</td><td>

MID Server you want to use.

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

Locality

</td><td>

Locality \(city\) of the organization making the certificate signing request for the given Subject Common Name. Enter the locality or `*`.

</td></tr><tr><td>

Country

</td><td>

Country of the organization making the certificate signing request for the given Subject Common Name. Enter the country or `*`.

</td></tr><tr><td>

Organizational Unit

</td><td>

Organizational unit making the certificate signing request for the given Subject Common Name. Enter the unit or `*`.

</td></tr><tr><td>

State

</td><td>

State of the organization making the certificate signing request for the given Subject Common Name. Enter the state or `*`.

</td></tr><tr><td>

Email Address

</td><td>

Email address of the administrator in the organization making the certificate signing request for the given Subject Common Name. Enter an email address or `*`.

</td></tr></tbody>
</table>