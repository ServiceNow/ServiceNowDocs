---
title: Oracle reconciliation
description: Oracle reconciliation keeps your Oracle license positions accurate and up-to-date without requiring manual calculations. Reconciliation runs weekly or on-demand.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software Asset Management publisher pack for Oracle, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Oracle reconciliation

Oracle reconciliation keeps your Oracle license positions accurate and up-to-date without requiring manual calculations. Reconciliation runs weekly or on-demand.

When you run an Oracle reconciliation, Software Asset Management determines the **Rights Used By** and **Rights Needed By** allocations for the named users, physical devices, and physical hosts that are accessing or running an Oracle product. You can use this information to keep your Oracle products in compliance.

**Note:** Any allocations that you make on a physical host are considered valid. Software Asset Management marks these allocations as **Allocated in use** in the license workbench. Any allocations that you make on a virtual host, such as a virtual machine \(VM\), are considered invalid. Software Asset Management marks these allocations as **Allocated not in use**.

For Oracle database and WebLogic server licensing on VMware virtualization technology, you can select the level of aggregation for your reconciliation calculation using the **Select the level of aggregation for reconciling licenses for Oracle databases and WebLogic servers on VMware** property. You can also enable Software Asset Management to account for VM-Host affinity rules during Oracle reconciliation using the **Use host affinity for reconciling licenses for Oracle databases and WebLogic servers on VMware at the vCenter\(s\) aggregation level** property. See [Software Asset Management properties](../reference/sam-properties.md) for information on these properties.

-   **[Set up domain-specific reconciliation properties for Oracle](../task/define-application-properties-oracle.md)**  
Use domain separation application properties for Software Asset Management to set up Oracle reconciliation properties for specific domains.

**Parent Topic:**[Software Asset Management publisher pack for Oracle](oracle-publisher-pack.md)

