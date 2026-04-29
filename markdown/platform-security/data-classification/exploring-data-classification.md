---
title: Exploring Data Classification
description: Explore about data classification.
locale: en-US
release: australia
product: Data Classification
classification: data-classification
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Data Classification, Platform Privacy]
---

# Exploring Data Classification

Explore about data classification.

Data Classification enables support for:

-   Visibility into the types of data hosted on a ServiceNow AI Platform instances.
-   Compliance with privacy laws, and meeting regulation requirements for industries such as financial services and medical device manufacturing.

## Data classifications

Data classification is a standalone process in which you manually apply data classifications to existing dictionary entries in any table. See [Data dictionary tables](https://www.servicenow.com/docs/access?context=c_DataDictionaryTables&version=australia&pubname=australia-platform-administration&ft:locale=en-US) for additional information.

-   You classify data as you find appropriate for your business and you can alter the available data classes as necessary.
-   When you classify data, you can use the pre-defined data classifications, or create your own. Although use of pre-defined data classifications is optional, it is advisable do so as a starting point. These pre-defined data classifications are included in demo data that you can install in your instance. To learn more, see [Installing Data Classification plugin demo data](../task/install-data-classification-plugin-demo-data.md#) and [Components installed with Data Classification demo data](../task/install-data-classification-plugin-demo-data.md#).
-   If you create your own data classifications, you can also design a tiered hierarchical system with parent and child data classifications.
-   When creating manual data classifications on an extended or child table, base fields inherited from the parent table are not available for selection.

    Classification is supported only for dictionary entries. You can't assign different classifications to inherited columns because they share the same dictionary entry. For example, you can't classify task.description as PII while classifying incident.description as Public, as the incident table is a child of the task table.


## Overview dashboard

Use the Overview dashboard to understand how your current data tables map to different data classifications. You can also analyze how your global, regional, international users may require different approaches to data classification, regarding the use or access to data. You can also customize the Overview dashboard content and layout to fit your needs.

To learn how to use the available scripted and REST APIs to apply the classification metadata within existing processes, workflows, and applications, see the following:

-   [Data Classification - REST API](https://www.servicenow.com/docs/access?context=data-classification-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   [DCManager - Global](https://www.servicenow.com/docs/access?context=DCManagerAPIGlobal&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   [ScopedDCManager - Scoped](https://www.servicenow.com/docs/access?context=DCManagerAPIScoped&version=australia&pubname=australia-api-reference&ft:locale=en-US)

**Note:** Data Classification supports domain separation, and the data\_classification table itself is process separated.

## Use cases

General Data Protection Regulation \(GDPR\) is a European Union regulation whose purpose is to provide individuals with control over their own personal data. You can use data classifications, such as Personally Identifiable Information, to identify where personal data is being stored in your instance. By applying the appropriate security mechanisms to protect that personal data from leaking out, your organization satisfies GDPR requirements.

If you store customer information in the ServiceNow AI Platform, use the Personally Identifiable Information \(PII\) classification code where needed to track data subject to regulation by local privacy laws. When you install demo data, it automatically applies this classification code to certain security-sensitive fields in the User \[sys\_user\] table. To learn more, see:

-   [Components installed with Data Classification demo data](../task/install-data-classification-plugin-demo-data.md#)
-   [Assigning data classifications to dictionary entries](../task/apply-data-classification-codes-dictionary-entries.md)

You can apply a Restricted data classification to Employee table columns that store sensitive employee information such as Social Security Numbers \(SSN\). Administrators and auditors can then use the Overview dashboard to confirm that you have assigned data classifications to the correct columns. They can also view the classification details for restricted types of information.

