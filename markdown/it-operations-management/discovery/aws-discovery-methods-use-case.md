---
title: AWS cloud discovery methods and use cases
description: Comparison of use cases and requirements for cloud discovery methods in AWS.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-10-05"
reading_time_minutes: 1
breadcrumb: [Discovery for AWS, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# AWS cloud discovery methods and use cases

Comparison of use cases and requirements for cloud discovery methods in AWS.

ITOM Visibility offers several methods for AWS cloud discovery. Each method supports different use cases and has its own requirements.

## AWS cloud discovery use cases

|Use case|Cloud Discovery \(Pattern-based\)|Horizontal discovery with AWS Systems Manager \(AWS SSM\)|Service Graph Connectors|Agent Client Collector for Visibility - Content \(without MID Server\)|Agent Client Collector for Visibility - Content \(with MID Server\)|IP-based Horizontal Discovery \(Pattern-based\)|
|--------|---------------------------------|---------------------------------------------------------|------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------|-----------------------------------------------|
|IT Service Management \(ITSM\) - basic and generic virtual CI classes|Yes|Yes|Yes|No|No|No|
|ITSM - extended virtual CI classes|Yes|Yes|No|No|No|No|
|ITSM - hardware CI classes|No|Yes|Yes|Yes|Yes|Yes|
|Pattern discovery of applications|No|Yes|No|No|Most|Yes|
|Tag-based service mapping|Yes|Yes|Yes|No|No|No|
|Machine Learning \(ML\)-based service mapping|No|Some|Some|Yes|Yes|Yes|
|Top-down service mapping|No|No|No|No|Most|Yes|
|Software Asset Management \(SAM\) - package manager|No|Yes|Yes|Yes|Yes|Yes|
|SAM - file-based|No|No|No|No|Yes|Yes|
|Oracle Global License Advisory Services \(GLAS\)|No|No|No|No|Yes|Yes|
|Certificate discovery|No|No|No|No|Yes|Yes, without host relationships|

## AWS cloud discovery requirements

<table id="table_pf5_pql_wgc"><thead><tr><th>

Requirement

</th><th>

Cloud Discovery \(Pattern-based\)

</th><th>

Horizontal discovery with AWS SSM

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

No

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

No

</td><td>

Yes

</td><td>

Yes

</td><td>

No

</td></tr><tr><td>

AWS SSM agent - on all virtual machines \(VMs\)

</td><td>

No

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

AWS S3 bucket

</td><td>

No

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

Network Connectivity Target VM to MID Server

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

No

</td><td>

Yes

</td></tr></tbody>
</table>