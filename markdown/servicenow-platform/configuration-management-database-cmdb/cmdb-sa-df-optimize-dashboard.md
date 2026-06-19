---
title: Manage Data Foundations advisor scope in CMDB success advisor
description: After the Data Foundations advisor dashboard is configured, you can update the principal class scope to keep it aligned with your goals, and resolve discrepancies when classes are changed outside the advisor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-optimize-dashboard.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 1
breadcrumb: [Advisor setup, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manage Data Foundations advisor scope in CMDB success advisor

After the Data Foundations advisor dashboard is configured, you can update the principal class scope to keep it aligned with your goals, and resolve discrepancies when classes are changed outside the advisor.

The Data Foundations advisor scope defines which principal classes CMDB success advisor monitors. You can add or remove entire CI class groups or fine-tune the selection by including or excluding specific classes within a group.

For guidance on choosing the right classes, see the [Guidance on designating principal classes in the CMDB \[KB2707240\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB2707240) article in the Now Support Knowledge Base.

**Note:** Principal classes that are currently in use by CMDB success advisor for HAM can't be edited here. To edit those classes in Data Foundations, remove them from the HAM advisor first. See .

## Roles required

Role required: sn\_cmdb\_admin

## Managing principal classes

Use the **Set principal classes** dialog box to add or remove CI classes from the Data Foundations advisor scope. Changes take effect when you select **Done**, and the dashboard updates to reflect the new scope.

For instructions, see [Manage principal classes in the Data Foundations advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-manage-scope.md).

## Out-of-sync principal classes

The Data Foundations advisor stores its own record of which CI classes are in scope. When other tools or processes change principal class designations outside the advisor, the advisor scope and the principal class state in the CMDB can diverge. Each time you open the dashboard, a comparison runs and a notification appears if a discrepancy is detected.

For more information about out-of-sync notifications, see [Principal class sync in Data Foundations advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-class-sync.md).

For instructions on resolving a sync discrepancy, see [Resolve an out-of-sync principal class state in the Data Foundations advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-resolve-class-sync.md).

