---
title: Certificate Inventory and Management patterns
description: Efficiently manage your Certificate Inventory with patterns to streamline the management of digital certificates. Patterns reduce the risk of vulnerabilities by bolstering security, compliance, and efficient lifecycle control.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Certificate Inventory and Management reference, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate Inventory and Management patterns

Efficiently manage your Certificate Inventory with patterns to streamline the management of digital certificates. Patterns reduce the risk of vulnerabilities by bolstering security, compliance, and efficient lifecycle control.

<table id="table_vph_p4w_31c"><thead><tr><th>

Pattern

</th><th>

Description

</th></tr></thead><tbody><tr><td>

GoDaddy – Certificate Management pattern

</td><td>

Part of the Certificate Inventory and Management application. Allows you to import and scan for certificates from your certificate authority \(CA\) GoDaddy.

</td></tr><tr><td>

DigiCert – Certificate Management pattern

</td><td>

Part of the Certificate Inventory and Management application. Allows you to import and scan for certificates from your certificate authority \(CA\) DigiCert.

</td></tr><tr><td>

Entrust - Certificate Management pattern

</td><td>

Part of the Certificate Inventory and Management application. Allows you to import and scan for certificates from your certificate authority \(CA\) Entrust.

</td></tr><tr><td>

Sectigo - Certificate Management pattern

</td><td>

Part of the Certificate Inventory and Management application. Allows you to import and scan for certificates from your certificate authority \(CA\) Sectigo.

</td></tr><tr><td>

Import SSL Certificate pattern

</td><td>

Allows you to discover certificates by importing certificates from files. [Run Certificate Discovery via certificate file import](../task/run-cert-inventory-mgmt-import.md).

</td></tr><tr><td>

**Amazon AWS - Certificate Manager** pattern and **Amazon AWS - Collect Certificates Tags** shared library.

 Certificate Inventory and Management, at least 3.4.0.

 Discovery and Service Mapping Patterns, at least 1.12.0.

</td><td>

Discovers certificates as part of AWS Cloud discovery. [AWS Certificate Manager discovery](../../service-mapping/reference/aws-certificate-manager-discovery-pattern.md).

</td></tr><tr><td>

**Google Cloud Platform \(GCP\) - Certificate Manager Certificates** pattern and **Google Cloud Platform \(GCP\) - Classic Certificates** pattern.

 Certificate Inventory and Management, at least 3.4.0.

 Discovery and Service Mapping Patterns, at least 1.12.0.

</td><td>

Discovers certificates as part of GCP Cloud discovery. [GCP Certificate Manager discovery](../../service-mapping/reference/gcp-certificate-discovery-pattern.md).

</td></tr><tr><td>

**Azure – Key Vault Certificates** pattern.

 Certificate Inventory and Management, at least 3.4.0.

 Discovery and Service Mapping Patterns, at least 1.12.0.

</td><td>

Discovers certificates as part of Azure Cloud discovery. [Azure Key Vault certificate discovery](azure-certificate-discovery-pattern.md).

</td></tr><tr><td>

Java KeyStore and Windows Certificates

</td><td>

Discovers certificates in the Java KeyStore or Windows Certificate Store. [Java KeyStore and Windows Certificate Store discovery](../../service-mapping/reference/x509-certificates-discovery.md).

</td></tr></tbody>
</table>-   **[AWS Certificate Manager discovery](../../service-mapping/reference/aws-certificate-manager-discovery-pattern.md)**  
Cloud Discovery uses Patterns to discover certificate data that the Amazon AWS Cloud Certificate Manager \(ACM\) manages. Discovering this data requires installing and updating Discovery and Service Mapping Patterns and Certificate Inventory and Management.
-   **[GCP Certificate Manager discovery](../../service-mapping/reference/gcp-certificate-discovery-pattern.md)**  
Cloud Discovery uses Patterns to discover certificate data that the GCP Certificate Manager manages. Discovering this data requires installing and updating Discovery and Service Mapping Patterns and Certificate Inventory and Management.
-   **[Azure Key Vault certificate discovery](azure-certificate-discovery-pattern.md)**  
Cloud Discovery uses Patterns to discover Azure Key Vault certificates. Discovering this data requires installing and updating Discovery and Service Mapping Patterns and Certificate Inventory and Management.
-   **[Java KeyStore and Windows Certificate Store discovery](../../service-mapping/reference/x509-certificates-discovery.md)**  
Discovery uses the **Collect Certificates** extension section of the **Linux Server** and **Windows OS – Servers** patterns to discover certificates stored in the Java KeyStore or Windows Certificate Store. Discovering the certificate information requires installing and updating Discovery and Service Mapping Patterns and Certificate Inventory and Management.

**Parent Topic:**[Certificate Inventory and Management reference](cert-invt-mgmt-references.md)

