---
title: Visibility to TLS certificates
description: The Certificate Inventory and Management application allows Discovery to automatically scan for certificates on specific ports through your existing CI-based Discovery schedules. In addition, you can create Discovery schedules to scan for specific URLs.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Visibility to TLS certificates

The Certificate Inventory and Management application allows Discovery to automatically scan for certificates on specific ports through your existing CI-based Discovery schedules. In addition, you can create Discovery schedules to scan for specific URLs.

The ServiceNow Store regularly releases new applications and updates to applications that are created by ServiceNow. If you already have the application, you can download the latest version to enhance your existing experience with our products. Since different features are available or enhanced each time an application is released in the Store, the content and features available in a particular release are indicated by version number in this document.

In Certificate Inventory and Management, you can add a list of imported certificates to [Run Certificate Discovery via certificate file import](../task/run-cert-inventory-mgmt-import.md), and scan for certificates from your Certificate Authority \(CA\) such as GoDaddy and DigiCert. You can also scan Sectigo and Entrust CAs.

The existing certificate authority patterns for DigiCert to collect the following fields as part of the CA Trust Certificate discovery. These fields are required to create an automated flow \(request, renew, or revoke\) for certificates discovered by Digicert CA Discovery and are stored in the Certificate Extensions \[sn\_disco\_certmgmt\_certificate\_extension\] table.

-   Certificate Id
-   Order id
-   Thumbprint
-   Serial Number
-   Certificate Status

Using the Certificate Inventory and Management, you can [Run Certificate Discovery via port scans](../task/run-cert-inventory-mgmt-ports.md). You can also [Run Certificate Discovery via individual URL scans](../task/run-cert-inventory-mgmt-urls.md).

To Import Certificates or Discovery CA Trust with more than 1500 certificates, create the discovery schedule with more than one serverless patterns configured. Each pattern execution supports a maximum of 1500 certificates discovery.

![execution pattern](../image/multiple-serverless-executions.png)

To discover all the certificates, the limit \(defaults to 1500\) and start\_offset \(defaults to 0\), must be configured accordingly. For example, to fetch up to 6,000 certificates, add four serverless patterns with start\_offset 0, 1500, 3000, and 4500. Start\_offset and limit parameters are configured as shown.

![pattern config](../image/execution-patterns-config.png)

