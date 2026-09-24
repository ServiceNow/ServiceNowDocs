---
title: Certificate Routing Policy form
description: The Certificate Routing Policy form enables you to configure routing policies for CyberArk Certificate Manager SaaS.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/certificate-routing-policy-form.html
release: brazil
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Reference, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate Routing Policy form

The Certificate Routing Policy form enables you to configure routing policies for CyberArk Certificate Manager SaaS.

<table id="table_cyberark_routing_policy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for the routing policy

</td></tr><tr><td>

Certificate Authority

</td><td>

This value should be CyberArk Certificate Manager SaaS.

</td></tr><tr><td>

Environment

</td><td>

Environment where the certificate is deployed or installed.

</td></tr><tr><td>

Assignment Group

</td><td>

Group to which certificate tasks created for this routing policy are assigned to automatically.

</td></tr><tr><td>

Vault Type

</td><td>

This should be set to CyberArk PVWA.

</td></tr><tr><td>

Application Name

</td><td>

Unique application name from the CyberArk portal. This field is case-sensitive.

</td></tr><tr><td>

Issuing Template Alias

</td><td>

API alias of the issuing template from the CyberArk portal. This field is case-sensitive.

</td></tr><tr><td>

Credential Alias

</td><td>

Credential alias associated with the certificate authority.

</td></tr><tr><td>

Certificate Purpose

</td><td>

Whether the certificate request is for internal or external use.

</td></tr><tr><td>

Certificate Format

</td><td>

Format in which the certificate is generated. The available options are: PEM, DER, and PKCS12. The default value is PEM.

</td></tr><tr><td>

PKCS12 Password Vault Reference

</td><td>

Reference to the PKCS\#12 key store password stored in your external vault. The format depends on your vault type: -   For HashiCorp Vault, enter the full path to the secret
-   For Azure Key Vault, enter the secret name
-   For CyberArk PVWA, enter the account name

This field is required when the Certificate Format field is set to PKCS12.

</td></tr><tr><td>

PKCS12 Password Vault Key

</td><td>

Name of the key within the vault secret that holds the PKCS\#12 key store password. This field is required when the Certificate Format field is set to PKCS12 and the Vault Type field is set to HashiCorp Vault.

</td></tr><tr><td>

Is Active

</td><td>

Option to determine whether the routing policy is active.

</td></tr><tr><td>

Allow Duplicate Request

</td><td>

Option to allow duplicate requests with the same Certificate Signing Request \(CSR\).

</td></tr><tr><td>

Approval Required

</td><td>

Option to require approval before the automated flow begins.

</td></tr><tr><td>

Task Approval Group

</td><td>

If Approval Required is selected, the task approval group with the pki\_approver role to provide approval.

</td></tr><tr><td>

Mid Server

</td><td>

Specific MID Server that handles all requests matching this routing policy.

</td></tr><tr><td>

Subject Common Name

</td><td>

Domain name secured by the certificate.

</td></tr></tbody>
</table>**Parent Topic:**[Certificate Inventory and Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/cert-invt-mgmt-references.md)

