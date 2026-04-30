---
title: Normalization properties
description: On the normalization properties form, you can see and change the configurable properties for the Normalization Data Services plugin.
locale: en-US
release: yokohama
product: User Administration
classification: user-administration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Normalization data services, Creating users, companies, and departments, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Normalization properties

On the normalization properties form, you can see and change the configurable properties for the Normalization Data Services plugin.

|Field|Description|
|-----|-----------|
|Reference qualifiers on all tables that reference the company will be updated to use the Normalized field.|If **Yes**, any reference field for the company – for any table across the platform – uses the Normalized name. This service only works if you have run the Update Reference Qualifiers task in the Guided Setup.|
|Enable a business rule that automatically normalizes manufacturer names for configuration items.|If **Yes**, the system normalizes company names when you add or update configuration items by a mechanism other than Discovery \(such as by manual import sets\).|
|Enable Discovery to use the normalization service for the manufacturer name.|To have Discovery use the normalized company name for the manufacturer name, select **Yes**.|
|This property is to enable or disable the Normalization process.|To enable the Normalization Data Service process, select **Yes**. To disable, select **No**. For details, see [Normalization data services](../concept/c_NormalizationOverview.md).|
|Normalize existing canonical core\_company records.|Select **Yes** to update an existing normalized \(canonical=true\) Companies record to not-normalized \(canonical=false\) if a mapping is present. For details, see [KB0957144](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0957144).|

**Parent Topic:**[Normalization data services](../concept/c_NormalizationOverview.md)

