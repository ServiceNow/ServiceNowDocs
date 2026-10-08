---
title: Urban Planning &amp; Permitting Administration Data Model
description: The Urban Planning &amp; Permitting Administration provides the data model foundation for ServiceNow developers and administrators to develop integrations with License and Permit Playbook to modernize property administration, streamline permitting workflows, and enable evidence-based urban planning decisions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-uppa-data-model.html
release: brazil
topic_type: reference
last_updated: "2026-10-02"
reading_time_minutes: 1
breadcrumb: [Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Urban Planning &amp; Permitting Administration Data Model

The Urban Planning &amp; Permitting Administration provides the data model foundation for ServiceNow developers and administrators to develop integrations with License and Permit Playbook to modernize property administration, streamline permitting workflows, and enable evidence-based urban planning decisions.

## Plugins installed with Urban Planning &amp; Permitting Administration

|App|Plugin \(scope\) ID|Depends on|
|---|-------------------|----------|
|Urban Planning Core|`com.sn_up_core`|None. Foundation app.|
|CSM Urban Planning|`com.sn_csm_up`|Installation of `com.sn_up_core` is required for use.|
|License &amp; Permit|`com.sn_gsm_lic_prmt` \(base personas from com.sn\_gsm\)|Installation of `com.sn_csm_up` is optional; License &amp; Permit will work normally **without** Urban Planning access.|

## Tables installed with Urban Planning &amp; Permitting Administration

|Table \(exact name\)|Label|
|--------------------|-----|
|sn\_up\_core\_jurisdiction|Jurisdiction|
|sn\_up\_core\_parcel|Parcel|
|sn\_up\_core\_parcel\_lineage|Parcel Lineage|
|sn\_up\_core\_planning\_area|Planning Area|
|sn\_up\_core\_planning\_area\_parcel|Planning Area Parcel|
|sn\_up\_core\_planning\_regulation|Planning Regulation|
|sn\_up\_core\_property\_address|Property Address|
|sn\_up\_core\_property\_record|Property Record|
|sn\_up\_core\_property\_record\_lineage|Property Record Lineage|
|sn\_up\_core\_property\_interest\_base|Property Interest Base \(ownership record\)|
|sn\_up\_core\_property\_interest\_document|Property Interest Document|
|sn\_up\_core\_regulatory\_applicability|Regulatory Applicability|
|sn\_up\_core\_structure|Structure|
|sn\_up\_core\_structure\_parcel|Structure Parcel|
|sn\_up\_core\_structure\_unit|Structure Unit|

**Parent Topic:**[Public Sector Digital Services Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/public-sector-digital-services-data-model.md)

