---
title: Certificate Routing Policy form
description: Fill in the Certificate Routing Policy form to set up the routing policy for ACME.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up the routing policy for ACME, Configuring ACME, Automated Certificate Management Environment, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate Routing Policy form

Fill in the Certificate Routing Policy form to set up the routing policy for ACME.

<table id="table_hx4_qxq_gbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the routing policy.

</td></tr><tr><td>

Certificate Authority

</td><td>

CA used to create a new certificate or to renew or revoke certificates. The supported CAs based on your credentials are:-   Let's Encrypt
-   Entrust

</td></tr><tr><td>

Assignment Group

</td><td>

Group to which a manual certificate task is assigned.

</td></tr><tr><td>

DNS Challenge Action

</td><td>

Flow designer option to resolve DNS challenges automatically \(for example, base script - **ACME DNS Challenge - GoDaddy**\).**Note:** You can also create a new action similar to the base script to support any other DNS provider. The flow\_designer role or action\_designer role is required for this action.

If **None** is selected, then the new or renew certificates are done using ACME manual flow of DNS challenge.

</td></tr><tr><td>

Credential Alias

</td><td>

Credential alias linked to the CA credential.

</td></tr><tr><td>

Certificate Purpose

</td><td>

Indicates whether the certificate request is for an internal or external purpose.

</td></tr><tr><td>

Task Approval Group

</td><td>

Group to which the task approval is assigned.

</td></tr><tr><td>

DNS Task Assignment Group

</td><td>

Group to which the DNS challenge for this task is assigned.

</td></tr><tr><td>

Mid Server

</td><td>

MID Server for certificate actions.

</td></tr><tr><td colspan="2">

**Note:**

The **Organization**, **Organizational Unit**, **Locality**, **State**, **Country**, and **Email Address** fields accept comma-separated values. The **Subject Common Name** and **Subject Alternative Name** fields take regex expressions. The regex format has the following restrictions:

-   Shouldn’t contain commas.
-   Shouldn’t start or end with a forward slash \(/\).

</td></tr></tbody>
</table>