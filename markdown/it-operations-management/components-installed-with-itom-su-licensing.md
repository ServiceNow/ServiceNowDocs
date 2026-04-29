---
title: Components installed with ITOM/OT SU Licensing
description: Several types of components are installed with activation of the ITOM/OT SU Licensing plugin, including tables and scheduled jobs.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ITOM/OT SU Licensing Reference, ITOM/OT SU Licensing and subscriptions, IT Operations Management]
---

# Components installed with ITOM/OT SU Licensing

Several types of components are installed with activation of the ITOM/OT SU Licensing plugin, including tables and scheduled jobs.

## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|ITOM Exclusion Tables Update Store|Updates the exclusion list.|
|ITOM Licensing Aggregator Store|Calculates the average of daily CI counts for the last 90 days.|
|ITOM Licensing Cloud Accelerate CI Listing Store|Creates the list of licensable CIs for ITOM Cloud Accelerate.|
|ITOM Cloud Accelerate Licensing Usage Count Store|Calculates the daily CI counts for ITOM Cloud Accelerate.|
|Event Management - Node Count Store|Calculates the node count used in Event Management.|
|ITOMHealthCIReporterWithOTOMCountITOMStore|Compiles the list of licensable CIs for ITOM.|
|ITOMHealthCIReporterWithOTOMCountOTOMStore|Compiles the list of licensable CIs for Operational Technology Management \(OTM\).|
|ITOM Health Licensing Usage Count Store|Calculates the daily CI count for ITOM AIOps.|
|ITOM Optimization Licensing Usage Count Store|Calculates the daily CI count for ITOM Optimization.|
|ITOM Licensing Optimization CI Listing Store|Compiles the list of licensable CIs for ITOM Optimization.|
|OTOM Licensing Visibility CI Listing Store|Compiles the list of licensable CIs for ITOM Visibility \(OTM\).|
|ITOM Licensing Discovery CI Listing Store|Compiles the list of licensable CIs for Discovery.|
|ITOM Licensing Visibility CI Listing Store|Compiles the list of licensable CIs for ITOM Visibility.|
|ITOM Visibility Licensing Usage Count Store|Calculates the daily CI count for ITOM Visibility.|
|OTOM Licensing Discovery CI Listing Store|Compiles the list of licensable CIs for Discovery \(OTM\).|
|ITOM DEX Licensing Usage Count Store|Calculates the daily CI counts for ITOM DEX.|
|ITOM Licensing DEX CI Listing Store|Creates the list of licensable CIs for ITOM DEX.|
|ITOM Licensing Service Observability CI Listing Store|Creates the list of licensable CIs for ITOMService Observability.|
|ITOMService Observability Licensing Usage Count Store|Calculates the CI counts for ITOMService Observability.|
|ITOM Licensing Historical Table Update Store|Creates a table to store all the licensable CIs daily|

## Tables installed

For information on how ITOM/OT SU Licensing counts licensable CIs for different ITOM products, refer to [ITOM Subscription Unit license calculation logic \(KB0748149\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0748149).

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

</td></tr><tr><td>

ITOM LU DEX CIs\[sn\_itom\_licensing\_itom\_lu\_dex\_ci\]

</td><td>

Contains the list of CIs counted under the DEX license.

</td></tr><tr><td>

Historical Licensable CIs\[sn\_itom\_licensing\_itom\_lu\_historical\_cis\]

</td><td>

Contains the list of Historical Licensable CIs.

</td></tr></tbody>
</table>**Parent Topic:**[ITOM/OT SU Licensing Reference](itom-su-licensing-reference.md)

