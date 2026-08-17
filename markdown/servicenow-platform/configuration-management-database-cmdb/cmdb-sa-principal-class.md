---
title: Principal classes in CMDB success advisor
description: Principal classes are CI classes that your organization treats as business-critical. In CMDB success advisor, the CI classes you select define the Data Foundations advisor scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-principal-class.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-06-24"
reading_time_minutes: 4
keywords: [principal classes, cmdb\_class\_info, principal class filter, task forms]
breadcrumb: [Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Principal classes in CMDB success advisor

Principal classes are CI classes that your organization treats as business-critical. In CMDB success advisor, the CI classes you select define the Data Foundations advisor scope.

Selecting the right principal classes keeps your CMDB focused and accurate.

## Principal class selection

CMDB success advisor processes your instance's history and ranks CI classes by relevance before you set up your Data Foundations advisor scope.

For information about selecting principal classes, see the [Guidance on designating principal classes in the CMDB \[KB2707240\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB2707240) article in the Now Support Knowledge Base.

You can manage the most important CI classes with CMDB success advisor by:

-   Selecting CI classes from the grouped, recommended list in the Data Foundations scope setup. Classes are set as principal automatically when you save.
-   Using intelligent recommendations based on the past incident, problem, and change \(IPC\) activity on your instance.
-   Monitoring data quality continuously through the Data Foundations advisor dashboard.

## Principal class tracking in CMDB success advisor

Use the following system properties to customize how CMDB success advisor recommends and manages principal classes. With the sn\_cmdb\_admin role, you can adjust these properties to control the scope and quality of principal class recommendations.

<table id="table_qky_rf2_k3c"><thead><tr><th>

Property

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

**sn\_cmdb\_advisor.principal\_class\_suggestion\_period**

</td><td>

Number of days of task history CMDB success advisor scans when generating class recommendations.Default value: 180 days

</td></tr><tr><td>

**sn\_cmdb\_advisor.suggested\_principal\_classes\_limit**

</td><td>

Maximum number of recommendations shown in the Recommended group.Default value: 20

</td></tr><tr><td>

**sn\_cmdb\_advisor.principal\_class\_others**

</td><td>

Comma-separated list of custom CI classes to include in the Others group of the Manage principal classes selection.

 **Note:** Use this property when the custom CI classes aren't available in the predefined Data Foundations advisor scope setup list.

</td></tr><tr><td>

**sn\_cmdb\_advisor.principal\_class\_recommendation\_criteria**

</td><td>

Keyword value \(`PREDEFINED`\) that displays a standard set of commonly managed CI classes as recommendations on instances with no prior task activity.This property does not exist by default and must be created manually.

</td></tr></tbody>
</table>The **sn\_cmdb\_advisor.principal\_class\_recommendation\_criteria** property is optional. Create it on instances with no prior task activity where task-based recommendations produce no results. Setting the value to `PREDEFINED` displays a standard set of commonly managed CI classes as recommendations. For instructions, see [Create the principal class recommendation criteria property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-rec-criteria.md).

## Principal class synchronization

The Data Foundations advisor stores its own record of which CI classes are in scope. The advisor does not automatically reflect changes to principal class designations made through CI Class Manager or made directly in the instance. A comparison runs when you open the dashboard to identify any discrepancies.

The following behaviors apply when principal class changes are made outside the advisor:

-   When you set a class as principal outside CMDB success advisor, the class is set as principal on the instance. This applies after the Data Foundations advisor dashboard scope is configured. However, it isn't automatically added to the Data Foundations advisor dashboard scope.
-   When you remove the principal designation from a class outside the advisor, the class remains in the Data Foundations advisor dashboard scope until you remove it manually.

To keep the Data Foundations advisor dashboard scope accurate, make all principal class updates directly in CMDB success advisor by selecting **Manage principal classes** on the Data Foundations advisor dashboard. For more information, see [Managing Data Foundations advisor scope in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-optimize-dashboard.md).

If other tools or processes change principal classes outside the advisor, an out-of-sync notification appears when you open the Data Foundations advisor dashboard. For more information, see [Principal class sync in Data Foundations advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-class-sync.md).

## CI filtering based on principal classes

When you configure a Data Foundations or HAM advisor scope through auto-setup or manual setup, CMDB success advisor automatically sets the selected CI classes as principal class in the platform CMDB Class Information \[cmdb\_class\_info\] table.

If both products are configured on the same instance, HAM scope is applied first, followed by Data Foundations. If principal classes already exist on the instance, CMDB success advisor preserves those principal classes and adds to the existing selection.

Principal classes affect ServiceNow AI Platform behavior beyond CMDB success advisor. After a CI class is set as principal, the platform can filter the **Configuration Item** field on task records so that only CIs that belong to principal classes are available.

**Note:** CMDB success advisor requires principal classes to define advisor scope and function correctly. The system property **com.snc.task.principal\_class\_filter** determines which task types apply the **Configuration Item** filter. If only a limited set of CIs are seen on task forms such as incidents or change requests, remove the affected task table from the **com.snc.task.principal\_class\_filter** system property. Don't clear the **Principal Class** check box on CI classes in the CMDB Class Information \[cmdb\_class\_info\] table to resolve task form filtering issues. This change disables principal class filtering for that task type while allowing CMDB success advisor to continue operating correctly. For more information, see [Principal Class](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/principal-class-filter.md).

