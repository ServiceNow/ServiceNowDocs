---
title: Principal class sync in Data Foundations advisor
description: When other tools or processes add or remove principal classes outside the advisor scope, the Data Foundations advisor displays a notification prompting you to review and update the scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-class-sync.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-05-19"
reading_time_minutes: 1
breadcrumb: [Manage advisor scope, Advisor setup, Use Data Foundations advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Principal class sync in Data Foundations advisor

When other tools or processes add or remove principal classes outside the advisor scope, the Data Foundations advisor displays a notification prompting you to review and update the scope.

## About principal class sync

The principal classes you select in the advisor define the Data Foundations advisor scope. The CMDB also stores principal class status at the class level, and other tools and processes, such as the CI Class Manager or the principal class recommendations agent, can change it. When tools or processes change principal class designations outside the advisor, the advisor scope and the principal class state in the CMDB can diverge.

Examples of changes that can cause an out-of-sync state:

-   The CI Class Manager marks a CI class as principal, but the Data Foundations advisor scope does not include it.
-   The principal class recommendations agent marks a CI class as principal outside the advisor scope.
-   A direct edit on the instance removes a CI class from the principal class list, but the class remains tracked in the advisor scope.
-   A tool or process outside the advisor removes a CI class from the principal class list, but the class remains tracked in the advisor scope.

Each time you open the Data Foundations advisor dashboard, a comparison runs between the advisor scope and the current principal class state in the CMDB. If a discrepancy exists, notifications appear to alert you.

## Out-of-sync notifications

If a discrepancy exists, the Data Foundations advisor displays two types of notifications.

-   **Dashboard notification**

    An info notification banner appears on the Data Foundations advisor dashboard. Select **Manage principal classes** to open the **Set principal classes** dialog box.

-   **Inline alert in the Set principal classes dialog box**

    When you open the **Set principal classes** dialog box from the advisor, an inline info alert appears at the top of the dialog box with the message about principal classes being out of sync. Select **Show more** to expand the alert and see the list of classes that other tools added or removed outside the advisor. Select **Show less** to collapse the list.


## Resolving an out-of-sync state

To resolve a principal class sync discrepancy, see [Resolve an out-of-sync principal class state in the Data Foundations advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-df-resolve-class-sync.md).

