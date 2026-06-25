---
title: Active Directory Domain Controller discovery
description: The Discovery and Service Mapping Patterns application uses the Active Directory Domain Controller On Windows pattern to find Active Directory domain controllers running on a Windows server. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/r-ActiveDirectory.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-05-27"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Active Directory Domain Controller discovery

The Discovery and Service Mapping Patterns application uses the Active Directory Domain Controller On Windows pattern to find Active Directory domain controllers running on a Windows server. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

When discovery runs on a domain controller, the pattern also creates LDAP endpoint connections to child domains in the same forest, triggering discovery of those domain controllers as well.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Prerequisites

-   **Verify that the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
-   **Verify an LDAP or TCP entry point is configured**

    Verify that the relevant port is open and listening on the domain controller.

-   **Create Windows credentials with WMI access**

    Verify that the credentials have permission to run WMI queries on the `\\root\CIMV2` namespace. For more information, see [Windows credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_WindowsCredentialsForm.md).

-   **Schedule a horizontal discovery**

    For more information, see [Schedule a horizontal discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/t_CreateADiscoverySchedule.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Active Directory Domain Controller On Windows pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the domain controller, which is the domain name.|
|Domain name \[domain\_name\]|Name of the Active Directory domain.|
|Domain Controller name \[domain\_controller\_name\]|Name of the domain controller server.|
|Forest name \[forest\_name\]|DNS name of the Active Directory forest.|

## CI relationships

The Active Directory Domain Controller On Windows pattern creates the following relationships to support Active Directory Domain Controller discovery.

|CI|Relationship|CI|
|---|------------|---|
|Active Directory Domain Controller \[cmdb\_ci\_ad\_controller\]|Runs on::Runs|Windows Server \[cmdb\_ci\_win\_server\]|

**Parent Topic:**[Software discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/c_Software.md)

