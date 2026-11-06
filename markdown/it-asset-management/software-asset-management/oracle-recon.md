---
title: Oracle reconciliation
description: Oracle reconciliation keeps your Oracle license positions accurate and up-to-date without requiring manual calculations. Reconciliation runs weekly or on-demand.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/oracle-recon.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Software Asset Management publisher pack for Oracle, Supported software publisher licenses, Software Asset Management, IT Asset Management, Asset Management]
---

# Oracle reconciliation

Oracle reconciliation keeps your Oracle license positions accurate and up-to-date without requiring manual calculations. Reconciliation runs weekly or on-demand.

When you run an Oracle reconciliation, Software Asset Management determines the **Rights Used By** and **Rights Needed By** allocations for the named users, physical devices, and physical hosts that are accessing or running an Oracle product. You can use this information to keep your Oracle products in conformance.

**Note:** Any allocations that you make on a physical host are considered valid. Software Asset Management marks these allocations as **Allocated in use** in the license workbench. Any allocations that you make on a virtual host, such as a virtual machine \(VM\), are considered invalid. Software Asset Management marks these allocations as **Allocated not in use**.

During reconciliation, records from the Oracle Options \[samp\_oracle\_options\] table are included only if they meet the following conditions:

-   The **Considered for licensing** field is set to **Yes**.
-   The given Oracle Database option is associated with an Oracle Database instance that is running on one of the following devices:
    -   Physical server
    -   Virtual server that has a relationship with a physical server
    -   End user device, such as a computer

For Oracle database and WebLogic server licensing on VMware virtualization technology, you can select the level of aggregation for your reconciliation calculation using the **Select the level of aggregation for reconciling licenses for Oracle databases and WebLogic servers on VMware** property. You can also enable Software Asset Management to account for VM-Host affinity rules during Oracle reconciliation using the **Use host affinity for reconciling licenses for Oracle databases and WebLogic servers on VMware at the vCenter\(s\) aggregation level** property. See [Software Asset Management properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/sam-properties.md) for information on these properties.

-   **[Set up domain-specific reconciliation properties for Oracle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/define-application-properties-oracle.md)**  
Use domain separation application properties for Software Asset Management to set up Oracle reconciliation properties for specific domains.

**Parent Topic:**[Software Asset Management publisher pack for Oracle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/oracle-publisher-pack.md)

