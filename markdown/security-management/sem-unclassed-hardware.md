---
title: Managing unclassed hardware
description: An asset is classified as unclassed hardware when it cannot be matched to an existing configuration item \(CI\) in the Configuration Management Database \(CMDB\) using defined lookup rules during import.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Associating finding with a configuration item using lookup rules, Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Managing unclassed hardware

An asset is classified as unclassed hardware when it cannot be matched to an existing configuration item \(CI\) in the Configuration Management Database \(CMDB\) using defined lookup rules during import.

## How unclassed hardware is created

Unclassed hardware is created during initial import from scanner integrations using the following process:

1.  USEM automatically uses host data to search for matches in the CMDB. The lookup rules are used to identify configuration items \(CIs\) and add them to the finding record to aid in remediation.
2.  If no match is found based on the lookup rules, the Identification and Reconciliation engine \(IRE\) applies its own identification rules defined on the hardware class and all its children.
3.  The IRE then creates a new CI under the `cmdb_ci_unclassed_hardware` class.
4.  When Discovery finds this asset, instead of reclassifying the existing unclassed hardware, it creates a CI. This is because the identification rule relies on the name of the hardware CI.

## The challenge with reclassification and duplication

When Discovery subsequently finds an asset that already exists as unclassed hardware, it often creates a new, classified CI \(e.g., a Windows server CI\) instead of reclassifying the existing unclassed hardware CI. This happens because:

-   **Name Field Discrepancy**: The identification rules heavily rely on the name field of the hardware CI.
-   **Inconsistent Naming**: The name used by Unified Security Exposure Management \(e.g., FQDN or NetBIOS name\) might differ from the name used by Discovery \(e.g., just the hostname\).
-   **Result**: This discrepancy prevents IRE from recognizing the unclassed hardware and the newly discovered asset as the same entity, leading to the creation of a duplicate CI under a new class rather than reclassifying the original.

**Note:** If the Identification and Reconciliation Engine \(IRE\) is activated, the option to reclassify items directly from discovered items is not supported.

The following extracts show the IRE payload for creating CI in Unclassed Hardware via Vulnerability Response and Discovery respectively.

```
"className": "cmdb_ci_unclassed_hardware",

"values": {
        "name": "asset01.company.com",//from NetBios,
        "mac_address": "1a:5e:2c:0e:42:f3",
        "fqdn": "asset01.company.com",
        "ip_address": "133.10.3.123"
    }

"settings": {
        "updateWithoutSwitch": true
    }

```

```
"className": "cmdb_ci_cmdb_ci_win_server"

"values": {
        "name": "asset01",
        "mac_address": "1a:5e:2c:0e:42:f3",
        "fqdn": "asset01.company.com",
        "ip_address": "133.10.3.123",
        "os_domain": "company"
    }

"settings": {
        "updateWithoutSwitch": false
    }

```

In this scenario, the existing Unclassed Hardware CI is not reclassified as a Windows Server. Instead, a new CI is created under Windows Server. This is because the identification rule depends on the Hardware CI’s name. As you can see from the payloads, the name received from Unified Security Exposure Management matches the FQDN/NETBIOS, whereas the Discovery payload provides only the host name.

**Parent Topic:**[Associating finding with a configuration item using lookup rules](sem-associate-finding-configuration-item-using-lookup-rules.md)

**Related topics**  


[Reclassify unclassed hardware](../../security-exposure-management-remediation/task/sem-reclassify-unclassed-hardware.md)

