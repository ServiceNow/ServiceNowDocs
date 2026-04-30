---
title: Maintaining Certificate chain relationships via certificate import
description: Maintaining certificate chain relationships via certificate import ensures the integrity and security of digital certificates, validating their authenticity in a system.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Visibility to TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Maintaining Certificate chain relationships via certificate import

Maintaining certificate chain relationships via certificate import ensures the integrity and security of digital certificates, validating their authenticity in a system.

To maintain the certificate chain relationships, the industry standard .txt extension is used. Certificate chain relationships are not maintained with any other file extensions. The expected order of certificates in a .txt certificate chain file is: Server certificate, Intermediate certificate, and Root certificate.

Use cases:

-   If two or more certificates are found in formats like .cert or .pem, only the first certificate is considered. The other certificates are not processed and no certificate chain relationships are maintained.
-   If there is a .txt extension containing only one certificate, it is considered as a server certificate and no certificate relationship are maintained.
-   If there is a .txt extension, containing two certificates, the first certificate is considered as server certificate and the second certificate is considered as root certificate, with no intermediate certificates.

**Note:** The certificate chain relationship is dependent on the latest URL/IP Discovery run. Importing a file without certificate chain relations disrupts any existing chain relationships associated with the same certificate \(fingerprint\).

