---
title: Using CSM Data Classification
description: The CRM Data Classification \(sn\_csm\_dataprivacy\) store application provides base system classifications for customer relationship management \(CRM\) data. It categorizes data as internal, personally identifiable information \(PII\), confidential, and more. The solution leverages the ServiceNow AI Platform data privacy capabilities to apply appropriate protection measures and enhance data security.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/using-csm-data-classification.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Customer management, Use, Customer Service Management]
---

# Using CSM Data Classification

The CRM Data Classification \(sn\_csm\_dataprivacy\) store application provides base system classifications for customer relationship management \(CRM\) data. It categorizes data as internal, personally identifiable information \(PII\), confidential, and more. The solution leverages the ServiceNow AI Platform data privacy capabilities to apply appropriate protection measures and enhance data security.

## Data Classification

As your organization imports and generates significant amounts of sensitive data, including PIIs, it's essential to conform with various privacy laws and security regulations for data protection. With CRM Data Classification, you can identify, categorize, and secure sensitive CRM data.

As an administrator, you can classify sensitive data based on predefined criteria that reflect the sensitivity levels of different data types within your instance. The CRM Data Classification application includes out of the baseline templates for several key plugins​. For more details on creating custom templates, see [Data classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/dps-data-classification.md).

## Data Protection

Once data is classified, you can apply appropriate security controls and policies based on classification levels. These templates help administrators review classifications and apply appropriate data protection measures. These data protection measures might include techniques such as anonymization, encryption, or implementing a zero trust architecture.

The solution leverages Data Classification capabilities to automate data handling policies at the ServiceNow AI Platform level through ServiceNow Vault.​ For detailed guidance on applying data protection measures, see [ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/servicenow-vault-landing.md).

