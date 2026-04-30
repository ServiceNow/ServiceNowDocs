---
title: Legacy - Auto recovery properties
description: Administrators can configure how Studio handles the recovery of draft records by navigating to Auto Recovery Properties .
locale: en-US
release: yokohama
product: ServiceNow Studio
classification: servicenow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Legacy - Automatic recovery of draft records, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Auto recovery properties

Administrators can configure how Studio handles the recovery of draft records by navigating to **Auto Recovery** &gt; **Properties**.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

<table id="table_gwz_ncy_ds"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Enable Auto Recovery**

 **glide.ui.auto.recovery**

</td><td>

By default, automatic recovery is enabled for all Application File \[sys\_metadata\] tables while working from Studio. Set this property to disable automatic recovery of records.

</td></tr><tr><td>

**Comma separated list of tables not supported for auto recovery**

 **glide.ui.auto.recovery.unsupported.tables**

</td><td>

By default, automatic recovery is enabled for all Application File \[sys\_metadata\] tables while working from Studio. Set this property to exclude specific tables from automatic recovery.

</td></tr><tr><td>

**Comma separated list of field types not supported for auto recovery**

 **glide.ui.auto.recovery.unsupported.field.types**

</td><td>

By default, automatic recovery supports all field types. Set this property to exclude certain field types from automatic recovery.

</td></tr><tr><td>

**Comma separated list of field types to exclude from auto recovery**

 **glide.ui.auto.recovery.exclude.field.types**

</td><td>

By default, automatic recovery is enabled for all field types. Set this property to exclude certain field types from automatic recovery.

</td></tr></tbody>
</table>**Parent Topic:**[Legacy - Automatic recovery of draft records](../concept/c_AutomaticRecoveryOfDraftRecords.md)

