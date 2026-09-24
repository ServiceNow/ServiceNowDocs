---
title: Maintaining certificate chain relationships
description: Maintaining certificate chain relationships via certificate import verifies the integrity and security of digital certificates, validating their authenticity in a system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/maintain-cert-chain-relationships.html
release: brazil
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Visibility to TLS certificates, Configure, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Maintaining certificate chain relationships

Maintaining certificate chain relationships via certificate import verifies the integrity and security of digital certificates, validating their authenticity in a system.

When you run certificate discovery by importing certificate files, the file extension and the order of the certificates within the file determine whether the system can build the chain relationships between the server, intermediate, and root certificates. This behavior applies only to certificates discovered through certificate file import. For information about this discovery method, see [Run Certificate Discovery via certificate file import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/run-cert-inventory-mgmt-import.md).

Only files with the `.txt` extension preserve certificate chain relationships. Certificates in a `.txt` chain file must appear in this order: Server certificate, intermediate certificate, and root certificate.The following outcomes apply when a file doesn't meet these requirements:

|File contents|Result|
|-------------|------|
|Two or more certificates in a format, such as `.cert` or `.pem`|The system processes only the first certificate. It doesn't process the remaining certificates and doesn't build chain relationships.|
|A `.txt` file with one certificate|The system treats the certificate as a server certificate and doesn't build chain relationships.|
|A `.txt` file with two certificates|The system treats the first certificate as the server certificate and the second as the root certificate. The chain contains no intermediate certificate.|

**Note:** Certificate chain relationships depend on the most recent URL or IP discovery run. If you import a file that doesn't contain chain relationships, the system removes any existing chain relationships for a certificate with the same certificate fingerprint.

