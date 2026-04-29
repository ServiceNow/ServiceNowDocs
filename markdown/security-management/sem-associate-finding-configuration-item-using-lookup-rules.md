---
title: Associating finding with a configuration item using lookup rules
description: Unified Security Exposure Management uses lookup rules to associate imported third-party exposure findings with configuration items \(CIs\) in the Configuration Management Database \(CMDB\). These rules match asset data to existing CIs, enabling accurate remediation.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Associating finding with a configuration item using lookup rules

Unified Security Exposure Management uses lookup rules to associate imported third-party exposure findings with configuration items \(CIs\) in the Configuration Management Database \(CMDB\). These rules match asset data to existing CIs, enabling accurate remediation.

Findings imported from external scanners such as Qualys, Tenable, and Rapid7 often lack direct CI references. Lookup rules bridge this gap by applying matching logic to map findings to CIs in the CMDB.

## Characteristics of lookup rules

-   **Domain separation and source specificity**: Lookup rules can be domain-separated and are specific to each source, enabling multiple deployments according to source.
-   **Shared across deployments**: Rules are shared across all deployments of a scanner source integration. Any changes or deletions affect all deployments.

## How lookup rules work

The lookup rules follow a three-step process.

1.  **Initial lookup**: When assets or findings are imported, the system first checks the **Discovered Items** list using third-party IDs. If an asset ID matches, it populates the **Configuration Item** field in the finding record.
2.  **Matching process**: If no asset ID match exists, the rules use other asset details to identify the correct CI. You can view mappings in the **Discovered Items** list.
3.  **Placeholder CI creation**: If no match is found, a placeholder CI is created and marked as an Unmatched CI.
    -   Matching starts with a vendor ID lookup across source, source\_instance, and vendor ID.
    -   The rules execute in ascending order and stop when a single CI match is found.
    -   If the matched CI is a low-level networking element \(for example, `dscy_switchport`, `cmdb_ci_network_adapter`, `cmdb_ci_nic`, or `cmdb_ci_ip_address`\), the parent CI is returned.
4.  **Rule execution**: Rules run from lowest to highest priority until a single match is found. If multiple matches occur, only the first is used.

## Special considerations

-   **Excluding CI classes**: A system property enables excluding certain CI classes from matching. See [Ignore CI classes](sem-configure-lookup-rules.md#) for upgrade information and instructions on setting the property.
-   **Parent CI return**: To avoid matching low-level networking elements, the parent CI is returned if the matched CI is a network adapter, Network Interface Cards \(NICs\), or IP address.

## Lookup rules for specific integrations

Each integration plugin includes its own set of rules:

-   Qualys: Qualys HOST ID, FQDN, NetBIOS, DNS, IP
-   Rapid7: MacAddress, FQDN, HostName, IP
-   Tenable.io: FQDN, NETBIOS, HOSTNAME, MacAddress, DNS
-   Tenable.sc: MacAddress, FQDN, NETBIOS

    **Note:** Tenable.io lookup rules prioritize and populate the non-empty network interface values \(FQDN, IPV4, and MacAddress\) over the regular FQDN, IPV4, and MacAddress values for a discovered item. When these network interface values are empty, the regular FQDN, IPV4, and MacAddress values are populated for a discovered item.


**Managing Lookup rules**

-   **Test custom rules**: Test custom or modified lookup rules to avoid performance issues.
-   **Deactivate instead of delete**: Deactivate rules rather than deleting them to avoid data loss.

If rules aren’t carefully constructed, importing exposure findings data can be taxing on an instance and performance issues with resources can occur. The logic used to iterate through and perform matching within the CMDB can result in lengthy processing times. To avoid any potential degradation of resources or performance complications, test any custom-written lookup rules or modifications to pre-defined **Lookup Rules**. See [Steps to help prevent duplicate or orphaned records after running lookup rules](sem-ci-identifier-rules-impl-test.md) for more information on helping prevent duplicate orphan records, deleting data, and cleaning up data.

**Note:** For information on CI matching, see [KB0998706](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0998706).

## Reapplying updated lookup rules

After updating rules, use **Reapply** to rerun them on unmatched or previously matched discovered items. This updates CI information in findings and detections. You can also run lookup rules on specific selected discovered items. For more information, see [Reapply lookup rules on selected discovered items](sem-configure-lookup-rules.md#).

## Unmatched CIs and unclassed hardware

-   **Unmatched CIs**: CIs without a match in the CMDB are listed under Discovered Items with Class set to **Unmatched CI**.

    **Note:** Each discovered item includes a **Class** field. If a CI is unmatched, this field is set to **Unmatched CI**.

-   **Unclassed hardware**: Assets that can’t be categorized by lookup rules are referred to as unclassed hardware.

By effectively managing lookup rules, Unified Security Exposure Management can help with identifying accurate ownership and streamlining remediation.

-   **[Managing unmatched configuration items \(CIs\)](sem-unmatchedCIs.md)**  
When assets are imported, they are automatically matched against existing CIs in your Configuration Management Database \(CMDB\). Assets that do not find a match are listed as 'Unmatched CIs' under Discovered Items.
-   **[Managing unclassed hardware](sem-unclassed-hardware.md)**  
An asset is classified as unclassed hardware when it cannot be matched to an existing configuration item \(CI\) in the Configuration Management Database \(CMDB\) using defined lookup rules during import.
-   **[Steps to help prevent duplicate or orphaned records after running lookup rules](sem-ci-identifier-rules-impl-test.md)**  
Take steps to help prevent duplicate or orphan records resulting from matching \(configuration items \(CIs\) within the CMDB.

**Parent Topic:**[Automating prioritization and triaging](sem-automating-prioritization-triaging.md)

**Related topics**  


[Configuring lookup rules](sem-configure-lookup-rules.md#)

