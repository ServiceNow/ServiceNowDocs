---
title: Data classification
description: Group data by type, using pre-defined or user-defined data classifications. If you have an assigned data classification administrator or auditor role, you can administer different data classes or visually analyze the current state of different types of data within the instance.
locale: en-US
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data privacy, Data Privacy, Platform Privacy]
---

# Data classification

Group data by type, using pre-defined or user-defined data classifications. If you have an assigned data classification administrator or auditor role, you can administer different data classes or visually analyze the current state of different types of data within the instance.

Data Classification enables support for:

-   Visibility into the types of data hosted on a ServiceNow AI Platform instances.
-   Compliance with privacy laws, and meeting regulation requirements for industries such as financial services and medical device manufacturing.

## Data classifications

Data classification is a standalone process in which you manually apply data classifications to existing dictionary entries in any table. See Data dictionary tables for additional information.

-   You classify data as you find appropriate for your business and you can alter the available data classes as necessary.
-   When you classify data, you can use the pre-defined data classifications, or create your own. Although use of pre-defined data classifications is optional, it is advisable do so as a starting point. These pre-defined data classifications are included in demo data that you can install in your instance.
-   If you create your own data classifications, you can also design a tiered hierarchical system with parent and child data classifications.

**Note:** Data Classification supports domain separation, and the data\_classification table itself is process separated. See [Domain separation and Data Classification](../../security/concept/domain-separation-data-classification.md) for additional information.

## Use cases

General Data Protection Regulation \(GDPR\) is a European Union regulation whose purpose is to provide individuals with control over their own personal data. You can use data classifications, such as Personally Identifiable Information, to identify where personal data is being stored in your instance. By applying the appropriate security mechanisms to protect that personal data from leaking out, your organization satisfies GDPR requirements.

If you store customer information in the ServiceNow AI Platform, use the Personally Identifiable Information \(PII\) classification code where needed to track data subject to regulation by local privacy laws.

You can apply a Restricted data classification to Employee table columns that store sensitive employee information such as Social Security Numbers \(SSN\). Administrators and auditors can then use the Overview dashboard to confirm that you have assigned data classifications to the correct columns. They can also view the classification details for restricted types of information.

