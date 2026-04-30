---
title: CMDB Identification and Reconciliation \(IRE\)
description: The Identification and Reconciliation module provides a centralized framework for identifying and reconciling data from different data sources. It helps maintain the integrity of the CMDB and some non-CMDB tables when multiple data sources are used to create and update CI records.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB Identification and Reconciliation \(IRE\)

The Identification and Reconciliation module provides a centralized framework for identifying and reconciling data from different data sources. It helps maintain the integrity of the CMDB and some non-CMDB tables when multiple data sources are used to create and update CI records.

## Get started

<table id="table_qdl_bqd_1cc" class="nav-card presentation"><tbody><tr><td>

[Explore![](../../../reuse/icons/brand-icons/bus-explore.svg)Learn about benefits and how IRE helps maintain the integrity of the CMDB.](exploring-ire.md)

</td><td>

[Configure![](../../../reuse/icons/brand-icons/bus-sdlc.svg)Configure identification, reconciliation, and other rules.](configuring-ire.md)

</td><td>

[IRE and Import Sets![](../../../reuse/icons/brand-icons/bus-integration-and-apis.svg)Apply IRE to Import Sets that are importing CIs into the CMDB.](identification-import-sets.md)

</td></tr><tr><td>

[Identification rules![](../../../reuse/icons/brand-icons/bus-handshake.svg)Create the rules that uniquely identify CIs based on CI attributes.](c_IdentificationRules.md)

</td><td>

[Reconciliation rules![](../../../reuse/icons/brand-icons/bus-root-cause-issue-resolution.svg)Create the rules that manage authorization and update priority between discovery sources.](../reference/r_ReconciliationRulesPrinciples.md)

</td><td>

[IRE and Duplicate CIs![](../../../reuse/icons/brand-icons/bus-2-person.svg)Learn and configure how IRE detects duplicate CIs and how to process de-duplication tasks.](id-detect-dup-ci.md)

</td></tr><tr><td>

[IRE and non-CMDB tables![](../../../reuse/icons/brand-icons/bus-database.svg)Apply IRE processes to supported non-CMDB tables.](ire-support-non-cmdb-tables.md)

</td><td>

[Identification Simulator![](../../../reuse/icons/brand-icons/bus-actionable-analytics.svg)Construct a validated payload and simulate running it through IRE processes.](identification-simulation.md#)

</td><td>

[Reference![](../../../reuse/icons/brand-icons/bus-learn.svg)Properties and tables associated with IRE, and how domain separation is supported in IRE functions.](ire-reference.md)

</td></tr></tbody>
</table>## Troubleshoot and get help

-   [Ask questions and explore other resources for  in the ServiceNow Community](https://www.servicenow.com/community/)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now)

-   **[Exploring CMDB Identification and Reconciliation \(IRE\)](exploring-ire.md)**  
The Identification and Reconciliation \(IRE\) module provides a centralized framework for identifying and reconciling data from different data sources. It helps maintain the integrity of the CMDB and some non-CMDB tables when multiple data sources are used to create and update CI records.
-   **[Configuring CMDB Identification and Reconciliation](configuring-ire.md)**  
Configure the necessary rules for CMDB Identification and Reconciliation \(IRE\) to function effectively.
-   **[Applying IRE to Import Sets](identification-import-sets.md)**  
You can apply CMDB Identification and Reconciliation Engine \(IRE\) processes when Import Sets are used to import CIs into the CMDB. CI identification can prevent duplicate CIs in the CMDB, which Import Sets might otherwise cause.
-   **[Detecting duplicate CIs](id-detect-dup-ci.md)**  
When IRE identification process detects duplicate CIs, it groups each set of duplicate CIs into a de-duplication task for review and remediation. A large number of duplicate CIs might be due to weak identification rules. You can configure the identification engine to reconcile duplicate CIs.
-   **[Using identification simulation](identification-simulation.md#)**  
Identification simulation is a central location for automatically constructing a payload that is guaranteed to be complete and valid. You can then simulate the processing of the payload by the Identification and Reconciliation Engine \(IRE\) and examine the results before actually submitting it for execution by IRE.
-   **[View a reclassification task](../task/t_ViewReclassificationTask.md)**  
Reclassification tasks are created for CIs that couldn't be automatically reclassified during the identification process. Review these tasks to locate the CIs and decide if to reclassify them.
-   **[IRE support for non-CMDB tables](ire-support-non-cmdb-tables.md)**  
Apply Identification and Reconciliation Engine \(IRE\) processes to supported non-CMDB tables to ensure data integrity and health of those tables.
-   **[CMDB IRE reference](ire-reference.md)**  
Reference topics provide property settings, domain separation, and other reference content for the CMDB Identification and Reconciliation Engine \(IRE\).

**Parent Topic:**[Configuration Management Database \(CMDB\)](c_ITILConfigurationManagement.md)

