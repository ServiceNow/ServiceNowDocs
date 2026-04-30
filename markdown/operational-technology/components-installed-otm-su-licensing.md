---
title: Components installed with ITOM SU Licensing for OTM
description: Several types of components are installed with activation of the OTM SU Licensing plugin, including scheduled jobs and tables.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [OTM SU Licensing References, Operational Technology Management licensing and subscriptions, Operational Technology]
---

# Components installed with ITOM SU Licensing for OTM

Several types of components are installed with activation of the OTM SU Licensing plugin, including scheduled jobs and tables.

## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|ITOM Exclusion Tables Update Store|Updates the exclusion list.|
|ITOM Licensing Aggregator Store|Calculates the average of daily CI counts for the last 90 days.|
|ITOMHealthCIReporterWithOTOMCountOTOMStore|Compiles the list of licensable CIs for OTM Health.|
|ITOM Health Licensing Usage Count Store|Calculates the daily CI count for OTM Health.|
|OTOM Licensing Visibility CI Listing Store|Compiles the list of licensable CIs for OTM Visibility.|
|OTM Foundation Licensing CI Listing Store|Compiles the list of licensable CIs for OTM Foundation.|
|OTM Foundation Licensing Usage Count Store|Calculates the daily licensable CI counts for OT Foundation.|

## Tables installed

<table id="table_uxv_bs1_gtb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ITOM LU Discovery Source Mapping\[itom\_lu\_discovery\_source\_mapping\]

</td><td>

Contains the list of licensable discovery source for each category.

</td></tr><tr><td>

ITOM LU Governance App Mapping\[itom\_lu\_governance\_app\_mapping\]

</td><td>

List of records that contain the mapping of governance applications to their respective licensable CIs.

</td></tr><tr><td>

ITOM LU Governance CIs \[itom\_lu\_governance\_ci\]

</td><td>

Contains the list of CIs counted under the Governance license.

</td></tr><tr><td>

ITOM License Exclusion Metadata\[itom\_license\_exclusion\_metadata\]

</td><td>

Contains the list of exclusion rules applicable to different license.

</td></tr><tr><td>

License Exclusions \[license\_exclusion\_list\]

</td><td>

Contains the list of CIs that need to be excluded from the license count based on the exclusion rule.

</td></tr><tr><td>

Visibility LU Temporary \[visibility\_lu\_temp\]

</td><td>

Contains the list of CIs counted under the Discovery license.

</td></tr><tr><td>

ITOM Licensing Category MetaData \[itom\_lu\_category\_metadata\]

</td><td>

Contains licensing metadata.

</td></tr><tr><td>

ITOM Licensing Discovery Sources\[itom\_lu\_discovery\_sources\]

</td><td>

Contains the categories for all discovery sources.

</td></tr></tbody>
</table>**Parent Topic:**[OTM SU Licensing References](../../operational-technology-management/reference/otm-su-licensing-references.md)

