---
title: Cryptographic Asset Compliance policies
description: Cryptographic Asset Compliance uses policies to evaluate cryptographic assets and flag risk. The policies are available on the Settings page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/policies.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-07-25"
reading_time_minutes: 1
breadcrumb: [Reference, Cryptographic Asset Compliance, ITOM Visibility, IT Operations Management]
---

# Cryptographic Asset Compliance policies

Cryptographic Asset Compliance uses policies to evaluate cryptographic assets and flag risk. The policies are available on the Settings page.

|Policy name|Description|
|-----------|-----------|
|AWS KMS cumulative risk level calculation|Calculates the risk level for AWS KMS keys based on all risk indicators.|
|AWS KMS key rotation check|Checks whether AWS KMS keys have been rotated within the recommended period.|
|AWS KMS PQC readiness|Checks whether an AWS KMS key uses post-quantum-safe algorithms.|
|AWS KMS weak algorithm detection|Identifies AWS KMS keys that use weak or insufficient key algorithms.|
|Azure Key Vault cumulative risk level calculation|Calculates the risk level for Azure Key Vault keys based on all risk indicators.|
|Azure Key Vault key expiration check|Checks whether Azure Key Vault keys have proper expiration dates and are not expired.|
|Azure Key Vault PQC readiness|Checks whether an Azure Key Vault key uses post-quantum-safe algorithms.|
|Azure Key Vault weak algorithm detection|Identifies Azure Key Vault keys that use weak or insufficient key algorithms and sizes.|
|Certificate authority trust|Verifies that certificates are issued by trusted, PQC-capable authorities. For more information, see [Configure trusted certificate authorities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/add-trusted-certificate-authorities.md).|
|Cryptographic inventory &amp; Ownership policy|Identifies unknown or unmanaged certificates.|
|Cumulative risk level calculation|Calculates the risk level for certificates based on all risk indicators.|
|PQC readiness|Checks whether a certificate is PQC compliant.|
|Quantum-vulnerable algorithm detection|Identifies certificates that use cryptographic algorithms that are potentially breakable by quantum computers.|

