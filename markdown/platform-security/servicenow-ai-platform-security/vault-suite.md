---
title: Vault Suite
description: Vault Suite deploys the complete set of ServiceNow Vault capabilities on your instance automatically, eliminating manual plugin setup.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/servicenow-ai-platform-security/vault-suite.html
release: australia
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: concept
last_updated: "2026-05-25"
reading_time_minutes: 1
keywords: [vault suite, vault, plugins, installation]
breadcrumb: [Exploring ServiceNow Vault, ServiceNow Vault]
---

# Vault Suite

Vault Suite deploys the complete set of ServiceNow Vault capabilities on your instance automatically, eliminating manual plugin setup.

Vault Suite is available on the ServiceNow Store. When you install Vault Suite, all included capabilities are activated on your instance automatically. You don't have to install each capability separately.

Vault Suite includes the following capabilities:

<table id="table-vault-suite-capabilities"><thead><tr><th>

Capability

</th><th>

Plugin ID

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Vault Console

</td><td>

Store app \(Scope:sn\_vault\_console\)

</td><td>

Unified administration dashboard for managing and monitoring all Vault Suite capabilities.

</td></tr><tr><td>

Data Privacy

</td><td>

Store app \(Scope:sn\_dp\_store\_app\)

</td><td>

Discovers, classifies, and anonymizes sensitive data to prevent leakage during clone, fulfill Right to Be Forgotten requests, and mask PII across platform channels.

</td></tr><tr><td>

Code Signing

</td><td>

com.glide.code\_signing\_enterprise

</td><td>

Verifies the integrity of code artifacts on the platform.

</td></tr><tr><td>

Field Encryption

</td><td>

com.glide.field.encryption.enterprise

</td><td>

Provides unlimited field and attachment encryption with customer-managed key support.

</td></tr><tr><td>

Zero Trust Access — Continuous Authentication

</td><td>

com.snc.zero\_trust\_continuous\_authentication

</td><td>

Requires continuous re-authentication when users access sensitive data.

</td></tr><tr><td>

Zero Trust Access — Location

</td><td>

com.snc.zero\_trust\_location\_access

</td><td>

Restricts access to classified data based on user location.

</td></tr><tr><td>

Zero Trust Access — Session Access

</td><td>

com.snc.zero\_trust\_session\_access

</td><td>

Controls access to sensitive operations at the session level.

</td></tr><tr><td>

Log Export Service

</td><td>

com.sn\_logstoanalytics

</td><td>

Forwards instance logs to external analytics platforms.

</td></tr><tr><td>

Cloud Encryption

</td><td>

com.glide.platform.cloud\_encryption

</td><td>

Encrypts data at rest at the cloud platform level.**Note:** Cloud Encryption is not installed automatically with Vault Suite because provisioning requires explicit user consent. To provision Cloud Encryption on your instance, see [KB1117369](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1117369).

</td></tr></tbody>
</table>**Note:** To install Vault Suite, check your entitlements to determine whether you have the ServiceNow Vault subscription, then request it from the ServiceNow Store. For installation steps, see [Install Vault Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/install-vault-suite.md).

**Parent Topic:**[Exploring ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/exploring-servicenow-vault.md)

