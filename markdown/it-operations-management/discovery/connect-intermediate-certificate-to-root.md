---
title: Connect an intermediate certificate to its root certificate
description: Connect intermediate certificates to recently imported certificates or to root certificates located outside the servers to complete the certificate chain of trust.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Visibility to TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Connect an intermediate certificate to its root certificate

Connect intermediate certificates to recently imported certificates or to root certificates located outside the servers to complete the certificate chain of trust.

## Before you begin

If your root certificate is outside your server, you must first [Discover root certificates hosted outside your server](discover-root-certificate-browser.md). If you need to import certificate files, [Run Certificate Discovery via certificate file import](run-cert-inventory-mgmt-import.md).

**Note:** If your root certificates are already in your servers, they're discovered and connected to the certificate chain using the standard Discovery probes deployed to your servers.

Role required: Admin, discovery\_admin, Certificate administrator

## About this task

Your intermediate certificate and your end-entity certificate are on your server. Discovery scans and establishes a certificate chain of trust for these certificates. If your root certificate is stored outside your server, perform a special Discovery on it and connect it to your intermediate certificate. Failure to connect might result in intermediate certificates being identified as the root certificate.

## Procedure

1.  Navigate to **System Properties** &gt; **All Properties**.

2.  Select **sn\_disco\_certmgmt.find\_and\_attach\_root\_certificate**.

3.  Set the Value to **true** in the System Property record.

4.  Save the record by selecting **Update**.

5.  Rerun the Certificate discovery

    You can rerun the discovery using a port probe or a URL based Discovery.


## Result

Your intermediate certificate identifies its root certificate, completing Discovery of your certificate chain of trust.

