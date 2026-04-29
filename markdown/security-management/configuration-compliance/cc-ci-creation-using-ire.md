---
title: Creating CIs for Configuration Compliance using the Identification and Reconciliation Engine
description: Starting with Configuration Compliance 11.1, you can create configuration items \(CIs\) in the Configuration Management Database \(CMDB\) using the Identification and Reconciliation engine \(IRE\) API. By using the IRE API to create CIs, you can prevent duplicate CIs from being created and you can reconcile CI attributes by allowing only authoritative data sources to write to CMDB.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-04-03"
reading_time_minutes: 2
breadcrumb: [Explore, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Creating CIs for Configuration Compliance using the Identification and Reconciliation Engine

Starting with Configuration Compliance 11.1, you can create configuration items \(CIs\) in the Configuration Management Database \(CMDB\) using the Identification and Reconciliation engine \(IRE\) API. By using the IRE API to create CIs, you can prevent duplicate CIs from being created and you can reconcile CI attributes by allowing only authoritative data sources to write to CMDB.

A CI class \(table\) is the original table name in the instance database. CMDB contains base system classes that store data about CIs.

## Using IRE for CI creation

Prior to version 11.1, if a matched CI was not found either in the Discovered Items list or CMDB, a CI was created in the Unmatched CI class \(`sn_sec_cmn_unmatched_ci`\).

For more information, see [Reconcile unmatched discovered items for Configuration Compliance](../task/reapply-reconcile-unmatched-discovered-items-cc.md).

Starting with version 11.1, you can use the IRE API to create CIs in CMDB. Instead of using the Unmatched CI class, a CI is created in the Unclassed Hardware or Incomplete IP Identified Device class.

## CMDB CI classes

**Note:** To use the new classes, activate the CMDB CI Class Models plugin. Otherwise, CIs are created in the Unmatched CI class.

Starting with version 11.1, if the host that you imported from a third-party scanner can't be found in the Discovered Items list or CMDB, it is stored in one of the following new CMDB CI classes.

<table id="table_nxb_kyt_knb"><thead><tr><th>

CMDB CI Class

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Incomplete IP Identified Device \(`cmdb_ci_incomplete_ip`\)

</td><td>

CI is created in this table if only the IP address is available in the host information that is received from the scanner.

</td></tr><tr><td>

Unclassed Hardware \(`cmdb_unclassed_hardware_ci`\)

</td><td>

CI is created in this table if any of the following information is available in the host information that is received from the scanner:-   Host name
-   IP address
-   DNS
-   NETBIOS
-   MAC address

 **Note:** If the MAC address is available, the network adapter entry is created and related to the unclassed hardware CI. If both the IP and MAC addresses are available, the IP address CI is also created and related to the unclassed hardware CI.

</td></tr></tbody>
</table>The system automatically uses an Unmatched CI class if one of the following occurs:

-   The CMDB CI Class plugin is not activated.
-   IRE raises an exception while creating a new CI.

**Related topics**  


[CMDB CI Class Models store app](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Identification and Reconciliation engine \(IRE\)](https://www.servicenow.com/docs/access?context=ire&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

