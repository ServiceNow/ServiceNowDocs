---
title: Update class list in the Principal Class filter
description: Manage the list of classes in the Principal Class filter so that those classes are prioritized for tracking, health, certification, lifecycle management, and class list views.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/update-principal-class-filter.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Principal Class, CMDB classifications and class dependency, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Update class list in the Principal Class filter

Manage the list of classes in the Principal Class filter so that those classes are prioritized for tracking, health, certification, lifecycle management, and class list views.

## Before you begin

Carefully review the [Principal Class](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/principal-class-filter.md) topic to learn about uses of the Principal Class filter across the CMDB and the general guidelines for designating a class as principal.

Role required: sn\_cmdb\_admin or itil\_admin, and personalize\_dictionary

## About this task

Designating certain CMDB classes as principal classes is a strategic way to focus your CMDB and governance on the CIs that matter most to day-to-day operations. Principal classes identify the classes that are in scope for operational processes—such as change, incident, problem, and quality management. Those classes represent the most critical infrastructure components with meaningful service impact. Limiting some CMDB functions to this set of most essential classes can help organizations improve data quality and ownership, reduce noise in reporting and impact analysis, and more consistently measure health, compliance, and operational risk where it counts.

In a base system, the Principal Class filter doesn't contain any classes.

The Principal Class designation applies only to the current class and is not derived by child classes. For details about the CMDB class hierarchy, see [CMDB schema model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_ConfigurationManagementDatabase.md).

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
    For more information about adding affected CIs to change requests, see [Associated CIs on a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/c_AffectedCIsAndImpactedServices.md).


**Parent Topic:**[Principal Class](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/principal-class-filter.md)

