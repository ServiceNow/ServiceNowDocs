---
title: Bulk certificate upload template fields
description: The bulk certificate upload Excel template contains fields that map to the fields in the Unique Certificate \[cmdb\_ci\_certificate\] table. You can import up to 5000 SSL certificates in bulk using the Excel file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/bulk-certificate-upload-template-fields.html
release: brazil
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-09-09"
reading_time_minutes: 2
keywords: [bulk certificate upload, SSL certificates, certificate template]
breadcrumb: [Reference, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Bulk certificate upload template fields

The bulk certificate upload Excel template contains fields that map to the fields in the Unique Certificate \[cmdb\_ci\_certificate\] table. You can import up to 5000 SSL certificates in bulk using the Excel file.

|Field|Required|Description|
|-----|--------|-----------|
|valid\_to|Yes|Expiry date of the certificate. Must be greater than the **valid\_from** value.|
|root\_issuer|Yes|Reference of the root certificate in the certificate chain. For a self-signed certificate, enter the certificate's own fingerprint.|
|subject\_common\_name|Yes|Host name or domain associated with the certificate. For example, `www.servicenow.com`.|
|valid\_from|Yes|Date from which the certificate is valid.|
|state|Yes|State of the certificate. Enter `issued`, `installed`, `revoked`, `retired`, or `other`.|
|fingerprint|Yes|Hash value of the certificate. Enter the value as space-separated hexadecimal pairs.|
|fingerprint\_algorithm|Yes|Algorithm used to hash the certificate. For example, `SHA-256`.|
|issuer|Yes|Reference of the certificate that signed and issued the certificate. For a self-signed certificate, enter the certificate's own fingerprint.|
|issuer\_common\_name|Yes|Common name of the certificate issuer. For example, `Entrust Certification Authority - L1K`.|
|issuer\_distinguished\_name|Yes|Distinguished name of the certificate issuer. Includes the common name \(CN\) of the issuing authority, the organization \(O\) that issued the certificate, and the organizational unit \(OU\) with the legal rights to issue it.|
|serial\_number|No|Serial number of the certificate. Enter the value as space-separated hexadecimal pairs.|
|signature\_algorithm|Yes|Signature algorithm of the certificate. For example, `SHA256WITHRSA`.|
|subject\_alternative\_name|No|Alternative host names covered by the certificate. Enter a comma-separated list.|
|subject\_country|No|Country \(C\) of the organization that the certificate is issued to, as a two-letter country code.|
|subject\_distinguished\_name|Yes|Distinguished name of the entity that the certificate is issued to. Consists of the common name \(CN\), the organization \(O\) that owns the domain, and the organizational unit \(OU\) that owns the domain.|
|subject\_email|No|Email address of the organization that the certificate is issued to.|
|subject\_locality|No|City or location \(L\) of the organization that the certificate is issued to. For example, `San Diego`.|
|subject\_organization|No|Organization \(O\) that the certificate is issued to. For example, `ServiceNow, Inc.`|
|subject\_organizational\_unit|No|Organizational unit \(OU\) that the certificate is issued to.|
|subject\_state|No|Region, state \(ST\), or province of the organization that the certificate is issued to. For example, `California`.|
|version|No|X.509 version of the certificate. For example, `3`.|
|key\_size|Yes|Size of the certificate key, in bits. For example, `2048`.|
|is\_ca|No|Whether the certificate is a certificate authority certificate. Enter `TRUE` or `FALSE`.|

**Parent Topic:**[Certificate Inventory and Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/cert-invt-mgmt-references.md)

