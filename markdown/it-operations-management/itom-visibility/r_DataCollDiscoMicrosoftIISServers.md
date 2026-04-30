---
title: Microsoft IIS server discovery
description: Discovery identifies and classifies information about Microsoft IIS servers.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Microsoft IIS server discovery

Discovery identifies and classifies information about Microsoft IIS servers.

## Prerequisites

Install IIS Management Scripts and Tools on a Microsoft IIS Server.

## Credentials

Configure these credentials:

-   [Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)
-   [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

## Classifier, pattern, and probe

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

Discovery uses these classifiers, probes, and patterns for IIS discovery:

<table id="table_fzd_2yv_jz"><thead><tr><th>

Classifier

</th><th>

Trigger probes

</th><th>

Pattern

</th></tr></thead><tbody><tr><td>

Microsoft IIS Server

</td><td>

-   Horizontal discovery probe: launches patterns
-   Windows - Get IIS Information\*

</td><td>

IIS

</td></tr></tbody>
</table>\*Probes inactive on new instances.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](../concept/c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Data collected by Discovery for IIS Web Server

The following data is collected in the IIS Web Server \[cmdb\_ci\_microsoft\_iis\_web\_server\] table:

|Label|Field name|
|-----|----------|
|Name|name|
|Version|version|
|Type\*|type|
|Running process command|running\_process\_command|
|Running process key parameters|running\_process\_key\_parameters|

\*The Type is always IIS.

The following data is collected in the Web site \[cmdb\_ci\_web\_site\] table:

|Label|Field name|Source|
|-----|----------|------|
|Name|name|wmi|
|TCP Port|tcp\_port|wmi|

**Parent Topic:**[Software discovery](../concept/c_Software.md)

