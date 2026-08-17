---
title: Principal Class
description: A Principal Class is a designation for these CMDB classes that are most critical for foundational data health and governance in the organization. Those designated classes are prioritized for tracking, health, certification, lifecycle management, and class list views.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/principal-class-filter.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-07-06"
reading_time_minutes: 6
breadcrumb: [CMDB classifications and class dependency, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Principal Class

A Principal Class is a designation for these CMDB classes that are most critical for foundational data health and governance in the organization. Those designated classes are prioritized for tracking, health, certification, lifecycle management, and class list views.

Designating certain CMDB classes as principal classes is a strategic way to focus your CMDB and governance on the CIs that matter most to day-to-day operations. Principal classes identify the classes that are in scope for operational processes—such as change, incident, problem, and quality management. Those classes represent the most critical infrastructure components with meaningful service impact. Limiting some CMDB functions to this set of most essential classes can help organizations improve data quality and ownership, reduce noise in reporting and impact analysis, and more consistently measure health, compliance, and operational risk where it counts.

The Principal Class setting applies only to the current class and is not derived by child classes. For details about the CMDB class hierarchy, see [CMDB schema model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_ConfigurationManagementDatabase.md).

## Principal Class filter

To manage Principal Classes in your organization, add those classes that are designated as Principal Class to the Principal Class filter. You can then manage the list by adding or deleting classes from the Principal Class filter as needed. In a base system, the Principal Class filter doesn't contain any classes. For more information, see [Update class list in the Principal Class filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/update-principal-class-filter.md).

## General guidelines for designating a class as principal

Use the following general guidelines for designating a class as principal:

-   Consider stability and business impact: Choose those classes that are stable, well-understood, and have a direct impact on business operations.
-   Prioritize core infrastructure: When in doubt, select those classes that represent the backbone of your IT environment.
-   Consult stakeholders: Engage with infrastructure, application, and security teams to validate your selections.
-   Review regularly: As your environment evolves, periodically review and update principal classes to ensure continued relevance.

For more information, see the [Guidance on designating principal classes in the CMDB \[KB2707240\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB2707240) article in the Now Support Knowledge Base.

## Uses of the Principal Class filter across the CMDB

The Principal Class filter has uses across the CMDB, such as:

-   In CI lists and dashboards: The Principal Class filter restricts CIs to only those in the filter, so you can focus on those CIs that require attention. For more information about list view filters, see [Save and use filters in a list view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/t_SavingFilters.md).
-   Service Graph Workspace and CMDB Workspace: You can apply the Principal Class filter in the Discovery sources card in the CMDB 360 dashboard. For more information, see [CMDB 360 experience in CMDB Workspace and in Service Graph Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb360-exp-cmdb-workspace.md).
-   CMDB success advisor: CMDB success advisor dashboards rely on principal classes to generate recommendations and KPIs. You can set principal classes in CMDB success advisor for Data Foundations to track the foundational data health of your CMDB. This alignment ensures that insights reflect actual business priorities. For more information, see [CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa.md).
-   HAM \(Hardware Asset Management\) integration: When model categories are added to the CMDB success advisor for HAM, they are marked as principal classes if they weren't already and will appear in the CMDB success advisor for Data Foundations if already set up. For more information, see [Using CMDB success advisor for HAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/cmdb-sa-ham-use.md), [Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/ham-landing-page.md), and [CMDB CI Class Models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models.md).
-   Principal CI class agent in ServiceNow Otto for CMDB: This agent suggests classes to be set as principal classes, and then automates setup for consistency across environments. For more information, see [Getting advice from ServiceNow Otto on CMDB governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-governance.md).

## Task types for Principal Class

The **com.snc.task.principal\_class\_filter** system property is a comma-separated list of task types. The system applies principal class filtering only on the **cmdb\_ci** field of CIs that belong to a class of a specified type. The default value for this property is "incident, incident\_task, problem, problem\_task, change\_request, change\_task".

After you designate a CI class as a principal class in the CMDB Class Information \[cmdb\_class\_info\] table, you can use the **com.snc.task.principal\_class\_filter** system property to specify which task types use principal class filtering on a CI **cmdb\_ci** field. When you create or update those task types, the CI lookup field shows only CIs that belong to principal classes.

.

-   **[Update class list in the Principal Class filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/update-principal-class-filter.md)**  
Manage the list of classes in the Principal Class filter so that those classes are prioritized for tracking, health, certification, lifecycle management, and class list views.

**Parent Topic:**[CMDB classifications and class dependency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_CMDBClassifications.md)

**Related topics**  


[Dependent CIs management]()

[CMDB record types]()

[Related Lists of CI components]()

[Create a CI class]()

[Reclassify a CI]()

[Delete CIs]()

[View and edit class definitions and metadata]()

