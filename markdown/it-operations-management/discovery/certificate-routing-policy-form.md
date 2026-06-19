---
title: Certificate Routing Policy form
description: The Certificate Routing Policy form enables you to configure routing policies for CyberArk Certificate Manager SaaS.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/certificate-routing-policy-form.html
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-06-03"
reading_time_minutes: 1
breadcrumb: [Certificate Inventory and Management reference, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate Routing Policy form

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
|Is Active|Option to determine whether the routing policy is active.|
|Allow Duplicate Request|Option to allow duplicate requests with the same Certificate Signing Request \(CSR\).|
|Approval Required|Option to require approval before the automated flow begins.|
|Task Approval Group|If Approval Required is selected, the task approval group with the pki\_approver role to provide approval.|
|Mid Server|Specific MID Server that handles all requests matching this routing policy.|
|Subject Common Name|Domain name secured by the certificate.|

**Parent Topic:**[Certificate Inventory and Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/cert-invt-mgmt-references.md)

