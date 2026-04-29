---
title: View software counter details for the legacy Software Asset Management plugin
description: Software counter details provide information about a specific software counter summary for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Software license reconciliation counters for the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# View software counter details for the legacy Software Asset Management plugin

Software counter details provide information about a specific software counter summary for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

## Before you begin

Role required: sam

## Procedure

1.  On the Software Counter Summary form, click a type in the **Software Counter Details** related list.

2.  View the Software Counter Detail form \(see table\).

    All fields on the form are read-only.

    ![Software counter detail form](../image/SoftwareCounterDetailForm.png "Software counter detail form")

    |Field|Description|
    |-----|-----------|
    |Type|Type of the counter detail.|
    |Software install|Name of the related software install record, if applicable. This field is blank if the type is Entitled not in use or Not allocated.|
    |Software usage|Name of the related [software usage record](t_ViewAUsageCounterResult.md), if applicable.|
    |Software counter|Name of the related [software counter](t_CreateASoftwareCounter.md).|
    |Software counter summary|Name of the related [software counter summary](t_ViewASoftwareCounterSummary.md).|
    |Valuation|A valuation of 1 indicates that the license right is being used. A valuation of 0 indicates that the license right is part of a [software suite](../../product-catalog/concept/c_Models.md), or that the license allows more than one installation per right. The 0 indicates that this installation does not count against the license.|
    |Entitlement|Name of the related [software license entitlement](t_CreatSWLicenseEntitlemnt.md), if applicable. This field is blank if the type is Not entitled or Not allocated.|
    |Software license|Name of the related [software license](t_AddANewSoftwareLicense.md), if applicable. This field is blank if the type is Not entitled.|
    |Usage Section|
    |Foreground|Total duration of foreground usage of the software, based on the related software install record.|
    |Background|Total duration of background usage of the software, based on the related software install record.|
    |Times used|Total number of times the software was used, based on the related software usage record.|
    |Duration|Total duration of foreground and background software usage, based the related software usage record.|


**Parent Topic:**[Software license reconciliation counters for the legacy Software Asset Management plugin](../concept/c_UseCountersSWLicenseReconcil.md)

