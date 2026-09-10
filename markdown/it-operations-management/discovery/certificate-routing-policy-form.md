---
title: Certificate Routing Policy form for CyberArk
description: The Certificate Routing Policy form enables you to configure routing policies for CyberArk Certificate Manager SaaS.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/certificate-routing-policy-form.html
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-06-03"
reading_time_minutes: 1
breadcrumb: [Reference, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate Routing Policy form for CyberArk

The Certificate Routing Policy form enables you to configure routing policies for CyberArk Certificate Manager SaaS.

|Field|Description|
|-----|-----------|
|Name|Descriptive name for the routing policy|
|Certificate Authority|This value should be CyberArk Certificate Manager SaaS.|
|Environment|Environment where the certificate is deployed or installed.|
|Assignment Group|Group to which certificate tasks created for this routing policy are assigned to automatically.|
|Vault Type|This should be None as CyberArk manages private key storage independently. Any other value provided will be ignored.|
|Application Name|Unique application name from the CyberArk portal. This field is case-sensitive.|
|Issuing Template Alias|API alias of the issuing template from the CyberArk portal. This field is case-sensitive.|
|Credential Alias|Credential alias associated with the certificate authority.|
|Certificate Purpose|Whether the certificate request is for internal or external use.|
|Certificate Format|Format in which the certificate is generated. The available options are: PEM, DER, and PKCS12. The default value is PEM.|
|PKCS12 Password Vault Reference|Reference to the PKCS\#12 key store password stored in your external vault. For HashiCorp Vault, enter the full path to the secret. This field is required when the Certificate Format field is set to PKCS12.|
|PKCS12 Password Vault Key|Name of the key within the vault secret that holds the PKCS\#12 key store password. This field is required when the Certificate Format field is set to PKCS12 and the Vault Type field is set to HashiCorp Vault.|
|Is Active|Option to determine whether the routing policy is active.|
|Allow Duplicate Request|Option to allow duplicate requests with the same Certificate Signing Request \(CSR\).|
|Approval Required|Option to require approval before the automated flow begins.|
|Task Approval Group|If Approval Required is selected, the task approval group with the pki\_approver role to provide approval.|
|Mid Server|Specific MID Server that handles all requests matching this routing policy.|
|Subject Common Name|Domain name secured by the certificate.|

**Parent Topic:**[Certificate Inventory and Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/cert-invt-mgmt-references.md)

