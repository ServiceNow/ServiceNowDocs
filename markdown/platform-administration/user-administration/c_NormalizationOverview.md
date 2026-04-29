---
title: Normalization data services
description: The Normalization Data Services plugin helps maintain consistency for table fields that refer to a company name.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [search optimization, data]
breadcrumb: [Creating users, companies, departments, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Normalization data services

The Normalization Data Services plugin helps maintain consistency for table fields that refer to a company name.

Tables related to configuration items and assets usually contain columns referring to a company name, such as a vendor or manufacturer. Often, these tables refer to the same company by several different names. This situation can happen for many reasons. For example, vendors sometimes use different company names depending on the device. This inconsistency creates problems, especially for reports that rely on these company names.

The Normalization Data Services plugin helps alleviate this problem.

When you enable and configure the Normalization Data Services plugin, the system downloads a list of standard company names that ServiceNow has compiled. It also downloads a list of common variants of that name. Anytime the plugin finds a company-name field with one of those variants, it substitutes the standard name in its place.

**Note:** The Normalization Data Services plugin refers to a standard name as a normalized name and to a variant name as a discovered name.

While the Normalization Data Services plugin provides services similar to the field normalization feature, this plugin doesn’t require you to manually set up the mappings from one name to another. If you like, you can add your own mappings to the set. However, you automatically start with extensive lists of common company names \(normalized names\) and their variants \(discovered names\).

The Normalization Data Services plugin stores data in two tables. The Normalized Company Names table contains the list of normalized company names. The Normalized Mappings table contains the mappings between each discovered name and its normalized name.

**Important:** If you edit a field whose value is a normalized name, you change the normalized name for ALL discovered names that map to it. These types of updates occur regardless of the table in which you edit the field.

The Normalization Data Services plugin adds a unique index or hash on the \[core\_company\] table. You can store only one company record for a company name. The unique hash is the same for two companies with the same name. The uniqueness is required for many features to work correctly. For example, **Discovery**, which creates customer management database \(CMDB\) models and CIs. On a domain separated instance, the unique index is expanded to hash,sys\_scope. This enables each domain to have its own version of a company with the same name.

-   **[Implementing normalization data services using guided setup](implementing-normalization-data-services-using-guided-setup.md)**  
You can implement Normalization Data Services using a guided setup.
-   **[Normalized company names table](../reference/r_NormalizedCompanyNames.md)**  
The Normalization Data Services plugin stores the normalized company names in the Normalized Company Names table.
-   **[Normalized Mappings table](../reference/r_NormalizedMappings.md)**  
The Normalized Mappings table lists all the discovered names and the normalized name to which each maps.
-   **[Normalization properties](../reference/r_NormalizedProperties.md)**  
On the normalization properties form, you can see and change the configurable properties for the Normalization Data Services plugin.
-   **[Changing normalized company names](c_NormalChangingNames.md#)**  
You can change a normalized company name several different ways. In all cases, that change affects all normalized fields referring to that company.
-   **[Enabling duplicate company names in extension tables](enhanced-nds-for-duplicate-records.md#)**  
You can create records with duplicate company names in extension tables, such as Customer Account \[customer\_account\] table, without causing normalization conflicts in Normalization Data Services.

**Parent Topic:**[Creating users, companies, and departments](../../roles/concept/using-user-administration.md)

