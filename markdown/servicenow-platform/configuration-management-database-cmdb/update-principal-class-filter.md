---
title: Update class list in the Principal Class filter
description: A Principal Class is a designation for those CMDB classes that are most important or critical for foundational data health and governance in the organization. Manage the list of classes in the Principal Class filter so that those classes are prioritized for tracking, health, certification, lifecycle management, and class list views.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [CMDB classifications and class dependency, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Update class list in the Principal Class filter

A Principal Class is a designation for those CMDB classes that are most important or critical for foundational data health and governance in the organization. Manage the list of classes in the Principal Class filter so that those classes are prioritized for tracking, health, certification, lifecycle management, and class list views.

## About this task

In a base system, the Principal Class filter doesn't contain any classes.

Designating certain CMDB classes as principal classes is a strategic way to focus your CMDB and governance on the CIs that matter most to day-to-day operations. Principal classes identify the classes that are in scope for operational processes—such as change, incident, problem, and quality management. Those classes represent the most critical infrastructure components with meaningful service impact. Limiting some CMDB functions to this set of most essential classes can help organizations improve data quality and ownership, reduce noise in reporting and impact analysis, and more consistently measure health, compliance, and operational risk where it counts.

General guidelines for designating a class as principal:

-   Consider stability and business impact: Choose those classes that are stable, well-understood, and have a direct impact on business operations.
-   Prioritize core infrastructure: When in doubt, select those classes that represent the backbone of your IT environment.
-   Consult stakeholders: Engage with infrastructure, application, and security teams to validate your selections.
-   Review regularly: As your environment evolves, periodically review and update principal classes to ensure continued relevance.

The Principal Class filter has uses across the CMDB, such as:

-   In CI lists and dashboards: The Principal Class filter restricts CIs to only those in the filter, so you can focus on those CIs that require attention. For more information about list view filters, see [Save and use filters in a list view](https://www.servicenow.com/docs/access?context=t_SavingFilters&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).
-   CMDB Workspace: You can apply the Principal Class filter in the Discovery sources card in the CMDB 360 dashboard. For more information, see [CMDB 360 experience in CMDB Workspace and in Service Graph Workspace](../concept/cmdb360-exp-cmdb-workspace.md).
-   CMDB success advisor: CMDB success advisor dashboards rely on principal classes to generate recommendations and KPIs. You can set principal classes in CMDB success advisor for Data Foundations to track the foundational data health of your CMDB. This alignment ensures that insights reflect actual business priorities. For more information, see [CMDB success advisor](../../cmdb-success-advisor/reference/cmdb-sa.md).
-   HAM \(Hardware Asset Management\) integration: When model categories are added to the CMDB success advisor for HAM, they are marked as principal classes if they weren't already and will appear in the CMDB success advisor for Data Foundations if already set up. For more information, see [Using CMDB success advisor for HAM](../../cmdb-success-advisor/concept/cmdb-sa-ham-use.md), [Hardware Asset Management](https://www.servicenow.com/docs/access?context=ham-landing-page&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US), and [CMDB CI Class Models](../concept/cmdb-ci-class-models.md).
-   Principal CI class agent in Now Assist for CMDB: This agent suggests classes to be set as principal classes, and then automates setup for consistency across environments. For more information, see [Getting advice from Now Assist on CMDB governance](../../now-assist-cmdb/concept/na-cmdb-awf-governance.md).

The Principal Class setting applies only to the current class and is not derived by child classes. For details about the CMDB class hierarchy, see [CMDB schema model](../concept/c_ConfigurationManagementDatabase.md).

## Before you begin

Role required: sn\_cmdb\_admin or itil\_admin, and personalize\_dictionary

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to expand the CI Classes list and then select a class to add or remove from the Principal Class filter.

3.  On the class navigation bar, navigate to **Class Info** &gt; **Basic Info**.

4.  On the Basic Info form, select or clear **Principal Class**.

5.  Select **Save**.


## Result

The Principal Class filter is updated with the addition or the removal of the class from the list of classes in the filter. When you apply the Principal Class filter to a Configuration Items list view, only CIs from classes included in the filter, appear.

## What to do next

In both of the following scenarios, the list of CIs refreshes to show only CIs whose class is included in the Principal Class filter.

-   Scenario 1:
    1.  In the **Filter navigator**, type `cmdb_ci.list` and then press the Enter key.
    2.  In the Configuration Items list view, select the **List controls** menu icon, select **Filters** and then select **Principal Class**.
-   Scenario 2:

    1.  Open a Change Request form.
    2.  Scroll down and select the **Affected CIs** tab. Select **Add**.
    3.  In the **Add Affected CIs** form, select the **List controls** menu icon, select **Filters** and then select **Principal Class**.
    For more information about adding affected CIs to change requests, see [Associated CIs on a change request](https://www.servicenow.com/docs/access?context=c_AffectedCIsAndImpactedServices&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).


**Parent Topic:**[CMDB classifications and class dependency](../concept/c_CMDBClassifications.md)

**Related topics**  


[Dependent CIs management](../concept/manage-dependent-ci.md)

[CMDB record types](../reference/r_CMDBRecordTypes.md)

[Related Lists of CI components](../reference/r_RelatedListsOfCIComponents.md)

[Create a CI class](t_CreateCIType.md)

[Reclassify a CI](t_ManuallyReclassifyCI.md)

[Delete CIs](delete-class-records-ci-class-mgr.md)

[View and edit class definitions and metadata](t_ViewTableDefinitions.md)

