---
title: Add ACME-compatible certificate authorities
description: Add a certificate authority \(CA\) that supports the ACME protocol to enable automated certificate request, renewal, and revocation flows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/add-acme-compatible-certificate-authorities.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 1
breadcrumb: [Automated certificate management with ACME, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Add ACME-compatible certificate authorities

Add a certificate authority \(CA\) that supports the ACME protocol to enable automated certificate request, renewal, and revocation flows.

## Before you begin

Role required: admin

## About this task

Certificate Inventory and Management supports the following ACME CAs: DigiCert, Entrust, Let's Encrypt, EJBCA, Sectigo Universal, and Sectigo Public. If your organization uses a different CA that is compatible with the ACME protocol, you can add it by creating a record in the Certificate Authority \[sn\_disco\_certmgmt\_ca\] table. No script changes are required.

**Note:** Errors can occur when using custom ACME-compatible CAs. Contact ServiceNow Support for assistance.

## Procedure

1.  Navigate to **All** &gt; **Certificate Management** &gt; **Certificate Automate Flows** &gt; **Certificate Authorities**.

2.  Select **New**.

3.  Fill in the fields on the **Certificate Authority** form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the CA.|
    |Base API URL|Base URL of the CA's ACME directory endpoint.|
    |ACME|Select this check box to enable the ACME flow for this CA.|

4.  Select **Submit**.


## What to do next

-   Create a certificate management credential for the new CA, see [Create credentials for ACME certificate authority](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/create-credential-for-acme-ca.md).
-   Set up a routing policy for the new CA, see [Set up routing policies for ACME](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/set-up-routing-policy-for-acme.md).

