---
title: Azure cloud discovery methods and use cases
description: Comparison of use cases and requirements for cloud discovery methods in Azure.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Discovery for Microsoft Azure, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Azure cloud discovery methods and use cases

Comparison of use cases and requirements for cloud discovery methods in Azure.

ITOM Visibility offers several methods for Azure cloud discovery. Each method supports different use cases and has its own requirements.

## Azure cloud discovery use cases

|Use case|Cloud Discovery \(Pattern-based\)|Service Graph Connectors|Agent Client Collector for Visibility - Content \(without MID Server\)|Agent Client Collector for Visibility - Content \(with MID Server\)|IP-based Horizontal Discovery \(Pattern-based\)|
|--------|---------------------------------|------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------|-----------------------------------------------|
|IT Service Management \(ITSM\) - basic and generic virtual CI classes|Yes|Yes|No|No|No|
|ITSM - extended virtual CI classes|Yes|No|No|No|No|
|ITSM - hardware CI classes|No|Yes|Yes|Yes|Yes|
|Pattern discovery of applications|No|No|No|Most|Yes|
|Tag-based service mapping|Yes|Yes|No|No|No|
|Machine Learning \(ML\)-based service mapping|No|Some|Yes|Yes|Yes|
|Top-down service mapping|No|No|No|Most|Yes|
|Software Asset Management \(SAM\) - package manager|No|Yes|Yes|Yes|Yes|
|SAM - file-based|No|No|No|Yes|Yes|
|Oracle Global License Advisory Services \(GLAS\)|No|No|No|Yes|Yes|
|Certificate discovery|No|No|No|Yes|Yes, without host relationships|

## Azure cloud discovery requirements

<table id="table_mnd_cwl_wgc"><thead><tr><th>

Requirement

</th><th>

Cloud Discovery \(Pattern-based\)

</th><th>

Service Graph Connectors

</th><th>

Agent Client Collector for Visibility - Content \(without MID Server\)

</th><th>

Agent Client Collector for Visibility - Content \(with MID Server\)

</th><th>

IP-based Horizontal Discovery \(Pattern-based\)

</th></tr></thead><tbody><tr><td>

MID Server

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Cloud credential

</td><td>

Yes

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

No

</td></tr><tr><td>

OS credential

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

Yes

</td></tr><tr><td>

ServiceNow agent

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

Yes

</td><td>

No

</td></tr><tr><td>

Azure Monitor Agent/change tracking - on all virtual machines \(VMs\)

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

No

</td></tr><tr><td>

Azure Log Analytics workspace

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

No

</td></tr><tr><td>

Azure storage account

</td><td>

No

</td><td>

Yes

</td><td>

No

</td><td>

No

</td><td>

No

</td></tr><tr><td>

Network Connectivity Target VM to MID Server

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

Yes

</td><td>

No

</td></tr><tr><td>

Network Connectivity MID Server to Target VM

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

No

</td><td>

Yes

</td></tr></tbody>
</table>