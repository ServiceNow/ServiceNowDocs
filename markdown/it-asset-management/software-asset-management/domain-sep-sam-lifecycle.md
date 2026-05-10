---
title: Domain separation and lifecycle reports
description: There are certain domain separation aspects to consider when running software lifecycle reports.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Domain separation and Software Asset Management, Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Domain separation and lifecycle reports

There are certain domain separation aspects to consider when running software lifecycle reports.

## Software Asset Management overview

In a domain-separated environment, the software lifecycle report is generated at the level at which the Service Provider \(SP\) is managing compliance for their customers’ environment. Typically, the level at which reconciliation is run indicates such compliance, and the software lifecycle report is generated at the same level.

The following table shows how the reconciliation should behave. In this example:

-   The SP is managing Cisco's software asset management \(SAM\) program at the Cisco corporate level. That means the lifecycle report must run at the Cisco corporate level.
-   The SP is managing Walmart's SAM program for each Walmart division \(US and Mexico\). That means the lifecycle report must run at the Walmart division level.

Here is the SP hierarchy:

-   Cisco Corporate
    -   Cisco USA
    -   Cisco Mexico
-   Walmart Corporate
    -   Walmart USA
    -   Walmart Mexico

|Domain settings \(reconciliation/ normalization\)|Compliance reporting|Lifecycle report level|
|-------------------------------------------------|--------------------|----------------------|
|TOP/Cisco|True|Yes|
|TOP/Cisco/US|False| |
|TOP/Cisco/Mexico|False| |
|TOP/Cisco/Germany|False| |
|TOP/Walmart|False| |
|TOP/Walmart/US|True|Yes|
|TOP/Walmart/Mexico|True|Yes|

If the SP sets up software models for Cisco corporate as well as Cisco Mexico, even though their intent is to manage compliance for Cisco at the Cisco Corporate level, the lifecycle report may show duplicate lifecycle records with the same install count.

|Model domain| |Date| |Software Model|Domain|
|------------|---|----|---|--------------|------|
|Cisco|SQL Server 2012|2014|10|SQL Server 2012|Cisco|
|Cisco Mexico|SQL Server 2012|2014|10|SQL Server 2012|Cisco|
|Walmart USA|SQL Server 2012|2014|5| | |
|Walmart Mexico|SQL Server 2012|2014|20| | |

To learn more about software lifecycles, see [Create software models in Software Asset Management classic](../task/record-terms-software-licenses.md). To learn about domain separation path setup, see [Domain separation setup and administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_DomainSeparationSetup.md)

**Parent Topic:**[Domain separation and Software Asset Management](domain-separation-software-asset-management.md)

