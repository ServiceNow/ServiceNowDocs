---
title: Automatically generate a Certificate Signing Request
description: You can generate a Certificate Signing Request \(CSR\) on the instance by providing the required information on the catalog form.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated certificate management for TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Automatically generate a Certificate Signing Request

You can generate a Certificate Signing Request \(CSR\) on the instance by providing the required information on the catalog form.

Creating a CSR manually can be a cumbersome and error-prone process. Automatic CSR generation can be enabled on the **Request New Certificate** and **Request New Ceriticate \(Automated\)** forms. This feature is disabled by default for security.

To enable automatic CSR generation, set the system property **sn\_disco\_certmgmt.enable\_csr\_generation** to true. See [Discovery properties](../reference/r_DiscoveryProperties.md) for more information.

Once enabled, a **Want to generate CSR?** checkbox is displayed in the certificate request form. Selecting the checkbox enables the required input fields to generate the CSR. Provide the necessary information and select **Generate**. The input data is validated and the CSR is formated accordingly.

The CSR is generated in the **Certificate Signing Request \(CSR\)** field, and a private key is generated in the **Private Key** field. Select the **Download** link to save the private key for later use. By default, the private key size is 2048 but can be changed using the system property **sn\_disco\_certmgmt.private\_key\_size**. See [Discovery properties](../reference/r_DiscoveryProperties.md) for more information.

When selecting **Submit**, the form provides a warning to download and save the private key. For security, ServiceNow does not store private keys, so the private key must be saved before leaving the form or else it is lost.

