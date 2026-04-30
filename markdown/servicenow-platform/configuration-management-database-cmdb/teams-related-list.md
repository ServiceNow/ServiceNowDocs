---
title: Teams related list
description: The Teams related list associates a user group to a CI based on group type, providing flexibility in tracking the different types of groups assigned to a CI. The Teams related list appears on CI forms for CIs of the Service \[cmdb\_ci\_service\] class and its descendent classes such as the Application Service \[cmdb\_ci\_service\_auto\] class.The Teams related list lets you add custom group types that are needed in your organization, extending the initial list of supported group types.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Related Lists of CI components, CMDB classifications and class dependency, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Teams related list

The Teams related list associates a user group to a CI based on group type, providing flexibility in tracking the different types of groups assigned to a CI. The Teams related list appears on CI forms for CIs of the Service \[cmdb\_ci\_service\] class and its descendent classes such as the Application Service \[cmdb\_ci\_service\_auto\] class.

Using the Teams related list can be useful if many data sources are used in the organization, and when using the [IntegrationHub ETL](integrationhub-etl.md).

In the base system, the Teams related list contains group types that match the fields:

-   **Approval Group**
-   **Change Group**
-   **Managed by Group**
-   **Support Group**

When you set a group assignment on a CI form of one of those classes, that group assignment is automatically synchronized with the Teams related list. If you set an assignment group for an application service, a relationship record is created to represent the new group assignment for the CI. The Teams related list on such CI forms, always shows the current settings for the various group assignments for the CI.

If there are multiple groups assigned to a CI, then on the **Teams** related list on a CI form, you can designate one of those groups as primary. When an incident involving that CI is created, the incident is assigned to that primary group. Only one group type can be designated as primary for a CI at any given moment.

As an example, use the Teams related list for an application service with the following characteristics:

-   Requires access to a database
-   Runs on Linux servers
-   Has a group assigned to manage the software portion of the actual application

In that example, you can track all of these group assignments by adding the appropriate group types and setting CIs with the new custom group types.

## By-directional synchronization

When you set or modify the value of one of the assignment group fields on a Service CI form, then the Teams related list is updated with that change, adding a Teams related record if a corresponding one doesn't exist. For example, when you set an empty **Support group** field to **Database San Diego** and save the form, then the system adds a Teams record in which **Group type** is **Support Group** and **User group** is **Database San Diego**.

In the opposite direction, any change in a Teams related record, where **Group type** corresponds one of the group assignment fields in the CI, is synchronized to the corresponding field. For example, if you set **User group** to **CAB Approval** in the **Support Group** group type, the **Support group** field on the CI form is updated with the **CAB Approval** value.

Deleting a Teams record doesn't affect the group assignment fields in the CI.

## Add the Teams related list to a Service CI form

By default, the tab for the Teams related list doesn't appear in the Related Lists section on Service CI forms. You can add the Teams related list by selecting the form's Additional actions menu, selecting **Configure** and then **Related Lists**. In the Available list that appears, move **Teams** to the Selected list and then select **Save**.

**Parent Topic:**[Related Lists of CI components](../reference/r_RelatedListsOfCIComponents.md)

## Add a custom group type to the Teams related list

The Teams related list lets you add custom group types that are needed in your organization, extending the initial list of supported group types.

### Before you begin

Role required: itil\_admin, asset, or cmdb\_admin

### About this task

To add a group type, you must modify the dictionary definition of the **group\_type** column in the **cmdb\_rel\_team** table.

### Procedure

1.  On a Service CI form, select the **Teams** related list.

2.  In the **Columns** tab, select the **Group type** column.

3.  On the Dictionary Entry form, in the **Choices** related list tab, insert a new row for a new Teams choice such as **Datacenter Group**.

4.  Save your changes.


