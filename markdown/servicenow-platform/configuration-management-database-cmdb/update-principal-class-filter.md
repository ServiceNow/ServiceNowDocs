---
title: Update the list of classes in the Principal Class filter
description: Manage the list of classes that are included in the Principal Class filter to restrict the CIs that appear in CIs list views to only specific classes that you need. You can add or remove CMDB classes from the Principal Class filter.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [CMDB classifications and class dependency, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Update the list of classes in the Principal Class filter

Manage the list of classes that are included in the Principal Class filter to restrict the CIs that appear in CIs list views to only specific classes that you need. You can add or remove CMDB classes from the Principal Class filter.

## Before you begin

Role required: itil\_admin and personalize\_dictionary

## About this task

Apply the CMDB Principal Class filter in list views of CMDB CIs so that only CIs that belong to the classes in the filter, appear. In a base system, the Principal Class filter doesn't contain any classes. The principal class setting applies only to the current class and is not derived by child classes. For more information about list view filters, see [Save and use filters in a list view](https://www.servicenow.com/docs/access?context=t_SavingFilters&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

You can also use the Principal Class filter in the Discovery sources card in the CMDB 360 dashboard in CMDB Workspace. For more information about using the Principal Class filter, see [CMDB 360 experience in CMDB Workspace](../concept/cmdb360-exp-cmdb-workspace.md).

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to expand the CI Classes list and then select a class to add or remove from the Principal Class filter.

3.  On the class navigation bar, navigate to **Class Info** &gt; **Basic Info**.

4.  On the Basic Info form, select or clear **Principal Class**.

5.  Select **Save**.


## Result

The Principal Class filter is updated with the addition or the removal of the class from the list of classes in the filter. When you apply the Principal Class filter to a Configuration Items list view, only CIs from classes included in the filter, appear.

## What to do next

In both of the following scenarios, the list of CIs refreshes to show only CIs whose class is included in the Principal Class filter:

-   1.  In the **Filter navigator**, type `cmdb_ci.list` and then press the Enter key.
2.  In the Configuration Items list view, select the **List controls** menu icon, select **Filters** and then select **Principal Class**.
-   1.  Open a Change Request form.
2.  Scroll down and select the **Affected CIs** tab. Select **Add**.
3.  In the **Add Affected CIs** form, select the **List controls** menu icon, select **Filters** and then select **Principal Class**.
    For more information about adding affected CIs to change requests, see [Associated CIs on a change request](https://www.servicenow.com/docs/access?context=c_AffectedCIsAndImpactedServices&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).


**Parent Topic:**[CMDB classifications and class dependency](../concept/c_CMDBClassifications.md)

**Related topics**  


[Dependent CIs management](../concept/manage-dependent-ci.md)

[CMDB record types](../reference/r_CMDBRecordTypes.md)

[Related Lists of CI components](../reference/r_RelatedListsOfCIComponents.md)

[Create a CI class](t_CreateCIType.md)

[Reclassify a CI](t_ManuallyReclassifyCI.md)

[Delete CIs](delete-class-records-ci-class-mgr.md)

[View and edit class definitions and metadata](t_ViewTableDefinitions.md)

