---
title: CMDB Identification and Reconciliation \(IRE\)
description: The Identification and Reconciliation module provides a centralized framework for identifying and reconciling data from different data sources. It helps maintain the integrity of the CMDB and some non-CMDB tables when multiple data sources are used to create and update CI records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/c\_CMDBIdentifyandReconcile.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB Identification and Reconciliation \(IRE\)

The Identification and Reconciliation module provides a centralized framework for identifying and reconciling data from different data sources. It helps maintain the integrity of the CMDB and some non-CMDB tables when multiple data sources are used to create and update CI records.

## Get started

<table id="table_qdl_bqd_1cc" class="nav-card presentation"><tbody><tr><td>

[Explore\[Omitted image "bus-explore.svg"\] Alt text:Learn about benefits and how IRE helps maintain the integrity of the CMDB.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/exploring-ire.md)

</td><td>

[Configure\[Omitted image "bus-sdlc.svg"\] Alt text:Configure identification, reconciliation, and other rules.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/configuring-ire.md)

</td><td>

[IRE and Import Sets\[Omitted image "bus-integration-and-apis.svg"\] Alt text:Apply IRE to Import Sets that are importing CIs into the CMDB.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/identification-import-sets.md)

</td></tr><tr><td>

[Identification rules\[Omitted image "bus-handshake.svg"\] Alt text:Create the rules that uniquely identify CIs based on CI attributes.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_IdentificationRules.md)

</td><td>

[Reconciliation rules\[Omitted image "bus-root-cause-issue-resolution.svg"\] Alt text:Create the rules that manage authorization and update priority between discovery sources.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/r_ReconciliationRulesPrinciples.md)

</td><td>

[IRE and Duplicate CIs\[Omitted image "bus-2-person.svg"\] Alt text:Learn and configure how IRE detects duplicate CIs and how to process de-duplication tasks.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/id-detect-dup-ci.md)

</td></tr><tr><td>

[IRE and non-CMDB tables\[Omitted image "bus-database.svg"\] Alt text:Apply IRE processes to supported non-CMDB tables.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/ire-support-non-cmdb-tables.md)

</td><td>

[Identification Simulator\[Omitted image "bus-actionable-analytics.svg"\] Alt text:Construct a validated payload and simulate running it through IRE processes.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/identification-simulation.md)

</td><td>

[Reference\[Omitted image "bus-learn.svg"\] Alt text:Properties and tables associated with IRE, and how domain separation is supported in IRE functions.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/ire-reference.md)

</td></tr></tbody>
</table>## Troubleshoot and get help

-   [Ask questions and explore other resources for  in the ServiceNow Community](https://www.servicenow.com/community/)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now)

-   **[Exploring CMDB Identification and Reconciliation \(IRE\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/exploring-ire.md)**  
The Identification and Reconciliation \(IRE\) module provides a centralized framework for identifying and reconciling data from different data sources. It helps maintain the integrity of the CMDB and some non-CMDB tables when multiple data sources are used to create and update CI records.
-   **[Configuring CMDB Identification and Reconciliation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/configuring-ire.md)**  
Configure the necessary rules for CMDB Identification and Reconciliation \(IRE\) to function effectively.
-   **[Applying IRE to Import Sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/identification-import-sets.md)**  
You can apply CMDB Identification and Reconciliation Engine \(IRE\) processes when Import Sets are used to import CIs into the CMDB. CI identification can prevent duplicate CIs in the CMDB, which Import Sets might otherwise cause.
-   **[Detecting duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/id-detect-dup-ci.md)**  
When IRE identification process detects duplicate CIs, it groups each set of duplicate CIs into a de-duplication task for review and remediation. A large number of duplicate CIs might be due to weak identification rules. You can configure the identification engine to reconcile duplicate CIs.
-   **[Using identification simulation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/identification-simulation.md)**  
Identification simulation is a central location for automatically constructing a payload that is guaranteed to be complete and valid. You can then simulate the processing of the payload by the Identification and Reconciliation Engine \(IRE\) and examine the results before actually submitting it for execution by IRE.
-   **[View a reclassification task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/t_ViewReclassificationTask.md)**  
Reclassification tasks are created for CIs that couldn't be automatically reclassified during the identification process. Review these tasks to locate the CIs and decide if to reclassify them.
-   **[IRE support for non-CMDB tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/ire-support-non-cmdb-tables.md)**  
Apply Identification and Reconciliation Engine \(IRE\) processes to supported non-CMDB tables to ensure data integrity and health of those tables.
-   **[CMDB IRE reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/ire-reference.md)**  
Reference topics provide property settings, domain separation, and other reference content for the CMDB Identification and Reconciliation Engine \(IRE\).

**Parent Topic:**[Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_ITILConfigurationManagement.md)

