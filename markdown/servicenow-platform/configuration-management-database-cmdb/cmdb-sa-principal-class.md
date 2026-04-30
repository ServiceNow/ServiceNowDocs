---
title: Principal classes in CMDB success advisor
description: In CMDB success advisor, principal classes are the foundation of the Data Foundations product.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-02-24"
reading_time_minutes: 2
breadcrumb: [Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Principal classes in CMDB success advisor

In CMDB success advisor, principal classes are the foundation of the Data Foundations product.

A principal CI class is a CI class that your organization has designated as important. When you set up your Data Foundations scope, the CI classes you select are automatically marked as principal on your ServiceNow instance.

Once a CI class is designated as principal, an automatic filter is applied to the **Configuration Item** field on task records.

## Principal classes benefits

Selecting the right principal classes keeps your CMDB focused and healthy. The CMDB success advisor monitors and improves data quality for the classes that matter most to your business.

## Principal class selection

CMDB success advisor analyzes your instance's history and ranks CI classes by relevance before you set up your advisor scope.

For guidance on choosing the right classes, see the [Guidance on designating principal classes in the CMDB \[KB2707240\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB2707240) article in the Now Support Knowledge Base.

You can manage most important CI classes with CMDB success advisor by:

-   Selecting CI classes from the grouped, recommended list in the Data Foundations scope setup. Classes are marked as principal automatically when you save.
-   Using intelligent recommendations based on the past 180 days of incident, problem, and change activity on your instance.
-   Monitoring data quality continuously through the Data Foundations advisor dashboard.

## Principal class tracking in CMDB success advisor

Use the following system properties to customize how CMDB success advisor recommends and manages principal classes. As a user with the admin role, you can adjust these properties to control the scope and quality of principal class recommendations in CMDB success advisor for Data Foundations.

<table id="table_qky_rf2_k3c"><thead><tr><th>

Property

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

**sn\_cmdb\_advisor.principal\_class\_suggestion\_period**

</td><td>

Number of days of task history CMDB success advisor scans when generating class recommendations.Default value: 180 days

</td></tr><tr><td>

**sn\_cmdb\_advisor.principal\_class\_suggestion\_limit**

</td><td>

Maximum number of recommendations shown in the Recommended group.Default value: 20

</td></tr><tr><td>

**sn\_cmdb\_advisor.cmdb\_advisor\_scope\_limit**

</td><td>

Maximum number of classes allowed in the Data Foundations scope.Default value: 50

</td></tr><tr><td>

**sn\_cmdb\_advisor.other\_principal\_classes**

</td><td>

Comma-separated list of custom CI classes to include in the Data Foundations scope selection that are not in the standard list.

</td></tr></tbody>
</table>## Principal class synchronization

The Data Foundations advisor maintains its own record of which CI classes are in scope and does not automatically synchronize changes made outside CMDB success advisor. Changes to principal class designations made through CI Class Manager or directly on the instance are not reflected automatically in the Data Foundations advisor scope.

Consider the following behavior:

-   When you mark a class as principal without using the CMDB success advisor after the Data Foundations advisor dashboard scope is configured, the class is marked as principal on the instance but is not automatically added to the Data Foundations advisor dashboard scope.
-   When you remove the principal designation from a class outside the advisor, the class remains in the Data Foundations advisor dashboard scope until you remove it manually.

To keep the Data Foundations advisor dashboard scope accurate, make all principal class updates directly in CMDB success advisor by selecting **Edit principal classes** on the CMDB success advisor card. For more information, see [Manage Data Foundations advisor scope in CMDB success advisor](../task/cmdb-sa-df-optimize-dashboard.md).

