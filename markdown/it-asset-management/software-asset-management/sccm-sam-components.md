---
title: Components installed with the Microsoft SCCM software usage plugin
description: Several types of components are installed with activation of the Microsoft SCCM software usage plugin.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Microsoft SCCM software usage, Software reclamation rules, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Components installed with the Microsoft SCCM software usage plugin

Several types of components are installed with activation of the Microsoft SCCM software usage plugin.

<table id="table_rw2_45g_1kb"><thead><tr><th>

 

</th><th>

SCCM 2012 v2

</th><th>

SCCM 2016

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

-   SAMP Usage \(Total usage\)
-   SCCM 2012 v2 Software Last Used \(Last used\)

</td><td>

-   SAMP Usage 2016 \(Total usage\)
-   SCCM 2016 Software Last Used \(Last used\)

</td></tr><tr><td>

Scheduled imports

</td><td>

-   SAMP Usage Import
-   SCCM 2012 v2 Software Last Used

</td><td>

-   SAMP Usage 2016 Import
-   SCCM 2016 Software Last Used

</td></tr><tr><td>

Transform map

</td><td>

-   SAMP usage import \(Total usage\)
-   SAMP last used data import \(Last used\)

 \(An onComplete transform script is associated with the transform map\)

</td><td>

-   SAMP usage import 2016 \(Total usage\)
-   SAMP last used data 2016 import \(Last used\)

 \(An onComplete transform script is associated with the transform map\)

</td></tr><tr><td>

Script include

</td><td>

SAMPUsageUtil

</td><td>

SAMPUsage2016Util

</td></tr></tbody>
</table>If you've activated the Integration — Microsoft SCCM 2012 v2 Software Usage \(com.snc.samp\_usage\_sccm\) plugin, navigate to **Integration — Microsoft SCCM 2012 v2** &gt; **Scheduled Import**.

| |SCCM table|Staging table|Target table|
|---|----------|-------------|------------|
|Total usage|v\_MonthlyUsageSummary|Software usage import \[imp\_samp\_usage\_import\]|Software Usage \[samp\_sw\_usage\]|
|Last used|v\_GS\_CCM\_RECENTLY\_USED\_APPS|SCCM 2012 v2 Software Last Used \[imp\_sccm2012v2\_software\_last\_used\]|Software Usage \[samp\_sw\_usage\]|

If you've activated the Integration — Microsoft SCCM 2016 Software Usage \(com.snc.samp.usage\_sccm\_2016\) plugin, navigate to **Integration — Microsoft SCCM 2016** &gt; **Scheduled Import**.

| |SCCM table|Staging table|Target table|
|---|----------|-------------|------------|
|Total usage|v\_MonthlyUsageSummary|Software usage 2016 import \[imp\_samp\_usage\_2016\_import\]|Software Usage \[samp\_sw\_usage\]|
|Last used|v\_GS\_CCM\_RECENTLY\_USED\_APPS|SCCM 2016 Software Last Used \[imp\_sccm2016\_software\_last\_used\]|Software Usage \[samp\_sw\_usage\]|

**Parent Topic:**[Microsoft SCCM software usage](../concept/sccm-software-usage.md)

