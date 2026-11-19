---
title: Risk indicator definitions
description: Risk indicators are used to identify security vulnerabilities and compliance issues in cryptographic assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/itom-visibility/risk-indicator-definitions.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-11-17"
reading_time_minutes: 1
keywords: [risk indicators, security vulnerabilities, compliance, certificates]
breadcrumb: [Reference, Cryptographic Asset Compliance, ITOM Visibility, IT Operations Management]
---

# Risk indicator definitions

Risk indicators are used to identify security vulnerabilities and compliance issues in cryptographic assets.

## Certificate risk indicators

|Risk Indicator|Description|Detection Criteria|
|--------------|-----------|------------------|
|Weak Algorithm|Certificate uses cryptographic algorithms that are deprecated or considered weak by current security standards|MD5, SHA-1, RSA &lt; 2048 bits, DSA &lt; 2048 bits, DES, 3DES, RC4|
|Trusted CA Risk|Certificate is not issued by a trusted certificate authority or has CA-related trust issues|Self-signed certificate, CA not in trusted root store, or CA not in organizational trust policy|
|No Owner|Certificate has no identified owner or responsible party|Owner field is empty or not assigned|
|No Environment|Certificate lacks environment classification|Environment field is empty or not specified|
|No Renewal|Certificate has no defined renewal process or workflow|No renewal process documented or automated workflow configured|

## Key risk indicators

|Risk Indicator|Description|Applies to|
|--------------|-----------|----------|
|Weak Algorithm|Key uses a weak or insufficient algorithm or key size|AWS KMS keys and Azure Key Vault keys|
|Not PQC ready|Key does not use a post-quantum-safe algorithm|AWS KMS keys and Azure Key Vault keys|
|Pending Deletion|Key is scheduled for deletion|AWS KMS keys|
|Expired|Key expiration date has passed|Azure Key Vault keys|
|Key Disabled|Key is disabled. No other risk indicators are shown for a disabled key.|AWS KMS keys and Azure Key Vault keys|
|Expiring Soon|Key expires within 30 days|Azure Key Vault keys|
|No Renewal|AWS KMS key is older than 365 days or has no creation date. Azure Key Vault key has no expiration date.|AWS KMS keys and Azure Key Vault keys|

