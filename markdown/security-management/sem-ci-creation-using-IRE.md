---
title: Creating CIs using the Identification and Reconciliation engine
description: You can create configuration items \(CIs\) in the Configuration Management Database \(CMDB\) using the Identification and Reconciliation engine \(IRE\) API. By using the IRE API to create CIs, you can prevent duplicate CIs from being created and you can reconcile CI attributes by allowing only authoritative data sources to write to CMDB.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Creating CIs using the Identification and Reconciliation engine

You can create configuration items \(CIs\) in the Configuration Management Database \(CMDB\) using the Identification and Reconciliation engine \(IRE\) API. By using the IRE API to create CIs, you can prevent duplicate CIs from being created and you can reconcile CI attributes by allowing only authoritative data sources to write to CMDB.

A CI class \(table\) is the original table name in the instance database. CMDB contains base system classes that store data about CIs.

## Using IRE for CI creation

If a matched CI isn’t found either in the Discovered Items list or CMDB, a CI is created in the Unmatched CI class \(`sn_sec_cmn_unmatched_ci`\).

Starting with v24.0.6 of Vulnerability Response, if IRE encounters exceptions that prevent the creation of CIs, the specifics of these exceptions are recorded in the Additional Information field. By examining the details in this field, you can determine the root cause and implement the necessary corrections to ensure the CI is successfully created.

Starting with Vulnerability Response v12.2 to v18.0, if no match is found when the CI lookup rules are applied, the asset information is sent to IRE and a CI is created in one of the Unclassed Hardware and Incomplete IP Identified Device classes. Starting from Vulnerability Response v18.0, a new class, Cloud Resource is also included. For more information on how to configure the categorization of unmatched cloud resources into your preferred CI class, see [Updating CI class for unmatched cloud assets](sem-updating-class-cloud-resource-hybrid-assets.md).

## CMDB CI classes

**Note:** To use the new classes, activate the CMDB CI Class Models plugin. Otherwise, CIs are created in the Unmatched CI class.

If the host that you imported from a third-party scanner can't be found in the Discovered Items list or CMDB, it’s created in one of the following new CMDB CI classes.

<table id="table_nxb_kyt_knb"><thead><tr><th>

CMDB CI Class

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Incomplete IP Identified Device \(cmdb\_ci\_incomplete\_ip\)

</td><td>

CI is created in this table if only the IP address is available in the host information that is received from the scanner.

</td></tr><tr><td>

Unclassed Hardware \(cmdb\_ci\_unclassed\_hardware\)

</td><td>

CI is created in this table if any of the following information is available in the host information that is received from the scanner:-   Host name
-   IP address
-   DNS
-   NETBIOS
-   MAC address

 **Note:** If the MAC address is available, the network adapter entry is created and related to the unclassed hardware CI. If both the IP and MAC addresses are available, the IP address CI is also created and related to the unclassed hardware CI.

</td></tr><tr><td>

Cloud Resource \(cmdb\_ci\_cmp\_resource\)

</td><td>

CI is created in this table if **Cloud Resource ID** is available in the host information that is received from the scanner.**Note:** If the Asset Type of a scanner integration is Hybrid and the **sn\_sec\_cmn.unmatched\_cloud\_resource\_enabled** system property is false, the CIs are created in the Unclassed Hardware class but not in the Cloud Resource class.

</td></tr></tbody>
</table>If the Identification and Reconciliation engine \(IRE\) is activated, the reclassify option from discovered items is not supported.

The system automatically uses an Unmatched CI class if one of the following occurs:

-   The CMDB CI Class plugin is not activated.
-   IRE raises an exception while creating a CI.

-   **[Updating CI class for unmatched cloud assets](sem-updating-class-cloud-resource-hybrid-assets.md)**  
Starting with Vulnerability Response v20.0, you can categorize the unmatched cloud assets from Qualys, Rapid7 and Tenable scanners into Unclassed Hardware by using the **sn\_sec\_cmn.unmatched\_cloud\_resource\_enabled** system property.

**Parent Topic:**[Automating prioritization and triaging](sem-automating-prioritization-triaging.md)

**Related topics**  


[bundle-platcap.cmdb-ci-class-models]

[bundle-platcap.ire]

