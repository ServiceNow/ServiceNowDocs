---
title: Set up Telecom Visibility
description: Telecom Visibility provides foundational capabilities that support both Telecom Discovery and Telecom Discrepancy Identification &amp; Reconciliation. It includes shared logic, enhanced CI class models, and Identification and Reconciliation Engine \(IRE\) updates tailored for telecom network elements.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Telecommunications Service Operations Management]
---

# Set up Telecom Visibility

Telecom Visibility provides foundational capabilities that support both Telecom Discovery and Telecom Discrepancy Identification &amp; Reconciliation. It includes shared logic, enhanced CI class models, and Identification and Reconciliation Engine \(IRE\) updates tailored for telecom network elements.

## Before you begin

Role required: tsom\_visibility\_admin

Confirm that:

-   Your ServiceNow AI Platform instance is licensed for Telecommunications Service Operations Management.
-   You review any custom IRE rules applied to telecom CIs to help prevent overrides during upgrade.

## About this task

To configure Telecom Visibility, you must install the required plugins and update the CMDB CI Class Models to version 1.82 or later, which introduces telecom-specific IRE identification rules. This ensures accurate CI identification and reconciliation across telecom domains.

**Note:** If you have customized IRE identification rules for any of the affected telecom CIs, upgrading to version 1.82 or later may override or impact those rules.

The following capabilities are included with the Telecom Visibility subscription:

|Plugin Name|Plugin ID|Plugin Description|Store App|
|-----------|---------|------------------|---------|
|Service Graph Connector for Nokia Altiplano|sn\_tsom\_altiplano\_connector|Service Graph Connector for Nokia Altiplano|Yes|
|Service Graph Connector for Cisco Meraki|sn\_tsom\_meraki\_connector|Service Graph Connector for Cisco Meraki|Yes|
|Service Graph Connector for Fortinet|sn\_tsom\_fortinet\_connector|Service Graph Connector for Fortinet|Yes|
|Service Graph Connector for Arista VeloCloud|sn\_tsom\_vcloud\_connector|Service Graph Connector for Arista VeloCloud|Yes|
|Telecommunications Discovery Patterns|sn\_tsom\_patterns|Telecommunication Discovery Patterns|Yes|
|Telecom Visibility Plugin \(Core logic\)|sn\_tsom\_core|Core logic for Telecom Visibility and Discrepancy Reconciliation|No|

## Procedure

1.  Navigate to **All** &gt; **Plugins**.

2.  Search for and install the following:

    1.  Telecommunication Discovery Patterns \( sn\_tsom\_patterns\)

    2.  Telecom Visibility \( sn\_tsom\_core\)

    3.  Service Graph Connector for your vendor.

3.  Update the CMDB CI Class Models.

    1.  Navigate to **All** &gt; **Applications** list in the ServiceNow Store.

    2.  Search for CMDB CI Class Models \(sn\_cmdb\_ci\_class\).

    3.  Install or upgrade to version 1.82 or later.

    **Note:** Installing any of the TSOM plugins listed above will automatically update or install version 1.82 or later of the CMDB CI Class Models app. If your instance doesn’t include TSOM plugins or you're on a pre-Yokohama release \(for example, Washington DC or Xanadu\), you can manually install or upgrade the store app.

4.  Navigate to **CMDB** &gt; **Identification Rules**.

    1.  Review rules related to:

        -   `cmdb_ci_interface_card`
        -   `cmdb_ci_slot`
        -   `cmdb_ci_subslot`
        -   `cmdb_ci_network_adapter`
    2.  Validate that your custom logic remains functional.

    3.  Update or merge custom rules as needed.


## Result

Confirm that the following are listed as active:

-   Telecom Visibility \(sn\_tsom\_core\)
-   Telecommunication Discovery Patterns \(sn\_tsom\_patterns\)
-   Service Graph Connector for your vendor
-   CMDB CI Class Models version 1.82 or later

**Related topics**  


[Telecom Visibility](../concept/tsom-visibility.md)

