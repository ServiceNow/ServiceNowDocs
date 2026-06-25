---
title: Translating Service Catalog cart labels
description: You can specify language-specific labels in these Service Catalog screens: Cart, Edit Cart, and Check Out \(including workflows and approvals\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/system-localization/r\_ServiceCatalogButtons.html
release: australia
product: System Localization
classification: system-localization
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring System Localization, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translating Service Catalog cart labels

You can specify language-specific labels in these Service Catalog screens: Cart, Edit Cart, and Check Out \(including workflows and approvals\).

The text for the labels is stored on the Messages \[sys\_ui\_message\] table. Localized Message records for these labels are included in the I18N Internationalization language plugins. The application is Global. You can add a record for an unsupported language, or edit an existing record. If you edit an existing record, export the record to another application, edit it in that application, and re-import it. Otherwise, your edits may be overwritten when your instance is zbooted or updated. For more information about exporting translation records, see [Export and edit translation records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/t_TranslateTheInterface.md).

\[Omitted image "ServiceCatalogButtons.png"\] Alt text: English and Dutch versions of the Service Catalog Shopping Cart.

**Related topics**  


[Message table]()

