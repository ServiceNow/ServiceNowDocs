---
title: Vault tools and metrics
description: Learn about the tools and metrics ServiceNow Vault uses to protect and discover sensitive data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/vault-tools.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [ServiceNow Vault console dashboard, ServiceNow Vault]
---

# Vault tools and metrics

Learn about the tools and metrics ServiceNow Vault uses to protect and discover sensitive data.

ServiceNow Vault integrates with several tools to provide a cohesive overview of your sensitive data security. You can hover over a widget to get further insight on the reported data. Select the **Go to** button on any tool to go to its respective page.

## Know your data

ServiceNow Vault uses Data Discovery and Data Classification to help you understand and know your data.

<table id="table_ltz_vcb_1gc"><thead><tr><th>

Tool

</th><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

[Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-discovery/data-discovery-landing.md)Use Data Discovery to run a discovery scan to look for data patterns that might be sensitive data. Once discovered, data can then be reviewed or classified for further protection and management.

</td><td>

Discovered data

</td><td>

Occurrences of sensitive data across tables in your instance, categorized by sensitive data pattern type.

</td></tr><tr><td>

Discovery status

</td><td>

Current state of all discovered sensitive data patterns, including new findings pending review, classified, or marked as ignored.

</td></tr><tr><td>

Discovered attachments

</td><td>

Total sensitive data occurrences in attachments across tables in your instance.

</td></tr><tr><td rowspan="2">

[Classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-classification/data-classification.md)Data Classification create data classes and helps organize your data into data classes for better management. Classified data can be protected at the class level.

</td><td>

Classifiable data

</td><td>

Proportions of classifiable data.

</td></tr><tr><td>

Classified data

</td><td>

Proportions of classified data.

</td></tr></tbody>
</table>## Protect your data

ServiceNow Vault uses data anonymization, cloud encryption, field encryption, and zero trust access to help secure and protect your data.

<table id="table_vdj_n2b_1gc"><thead><tr><th>

Tool

</th><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

[Anonymization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/dps-data-anonymization.md)Anonymize data by data class with different anonymization techniques to preserve data patterns but remove sensitive data. Useful for sanitizing instances for development or removing specific user data because of rights to be forgotten.

</td><td>

Existing data

</td><td>

All classified data per workflow that is anonymized or not.

</td></tr><tr><td>

Real time data

</td><td>

The amount of anonymized real time data.

</td></tr><tr><td>

Anonymization run times

</td><td>

Run times in hours of data anonymized in real time by channel, such as Now Assist or Virtual Agent.

</td></tr><tr><td>

[Cloud Encryption with Key Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/cloud-encryption/dare-overview.md)Securely protect sensitive data in encrypted storage for your data using block encryption, along with enhanced key management.

</td><td>

Active cloud key

</td><td>

Total rotations of the active cloud key.**Note:** To view this data, you need the [Key Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/encryption.md) admin role \(sn\_kmf.admin or sn\_kmf.cryptographic\_manager\).

</td></tr><tr><td>

 

</td><td>

Key rotation

</td><td>

Time elapsed between each rotation of active keys on your instance. Bar height measures how long a key was used before rotation.**Note:** To view this data, you need the [Key Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/encryption.md) admin role \(sn\_kmf.admin or sn\_kmf.cryptographic\_manager\).

</td></tr><tr><td rowspan="3">

[Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/field-encryption.md)Securely protect sensitive data while providing access for authorized users. Useful for increasing protections from bad actors.

</td><td>

Encrypted fields classification status

</td><td>

Classification status of all data protected with Field Encryption.

</td></tr><tr><td>

Classes protected with Field Encryption

</td><td>

The proportion of classified data protected withField Encryption.

</td></tr><tr><td>

Active encryption keys

</td><td>

Number of active Field Encryption keys in your instance. Ideally, the number of active keys matches the number of classifications.**Note:** To view this data, you need the [Key Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/encryption.md) admin role \(sn\_kmf.admin or sn\_kmf.cryptographic\_manager\) and the security\_admin role.

</td></tr><tr><td rowspan="2">

[Zero Trust Access \(ZTA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/session-access.md)Continuous authentication while accessing classified sensitive data in real time.

</td><td>

Continuous Authentication classification status

</td><td>

Number of classifications that are protected due to the continuous authentication policies.

</td></tr><tr><td>

Classes protected with Continuous authentication

</td><td>

Number of classes protected with continuous authentication, categorized by their class.

</td></tr></tbody>
</table>## All ServiceNow Vault tools

<table id="table_ysx_slf_kfc" class="nav-card"><tbody><tr><td>

[Encryption \[Omitted image "bus-security.svg"\] Alt text:](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/encryption.md)

 [Key Management and Field Encryption is a suite of highly configurable encryption modules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/encryption.md)

</td><td>

[Code Signing\[Omitted image "bus-contract.svg"\] Alt text:](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/code-signing-landing.md)

 [Help improve security by validating sensitive application configuration data and scripts before they are used.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/code-signing-landing.md)

</td></tr><tr><td>

[Data Privacy\[Omitted image "bus-password-reset.svg"\] Alt text:](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/data-privacy-landing.md)

 [Use the Data Privacy plugin to remove personally identifiable information \(PII\) from user data when it is migrated from a production instance to a non-production instance.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/data-privacy-landing.md)

</td><td>

[Data Discovery\[Omitted image "bus-find-an-app.svg"\] Alt text:](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-discovery/data-discovery-landing.md)

 [The Data Discovery plugin enables you to find personally identifiable information \(PII\) from user data. The data can then be classified for further security measures.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-discovery/data-discovery-landing.md)

</td></tr><tr><td>

[Log Export Services\[Omitted image "bus-log-store.svg"\] Alt text:](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/les-landing-page.md)

 [Improve security, performance, and user experience by importing ServiceNow log data into enterprise log analytics using the log export service.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/les-landing-page.md)

</td><td>

[Zero Trust Access\[Omitted image "bus-block.svg"\] Alt text:](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/session-access.md)

 [ServiceNow Session Access enables organizations to dynamically reduce user privilege in a web session](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/session-access.md)

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow Vault console dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/vault-dashboard.md)

