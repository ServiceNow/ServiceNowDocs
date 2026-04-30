---
title: Exploring Data filtration
description: Use Data filtration to control access to tables and records based on subject attributes when performing read queries.
locale: en-US
release: xanadu
product: Data Filtration
classification: data-filtration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Data filtration, Access Management]
---

# Exploring Data filtration

Use Data filtration to control access to tables and records based on subject attributes when performing read queries.

Data filtration is a separate form of access control designed to work along with the existing Access Control rules \(ACLs\) on your instance. Data filtration denies access to tables and records that do not match subject attributes defined by an administrator. Data filtration is designed to make auditing, reporting, and troubleshooting easier.

This is an optional feature that administrators can activate on their instance.

## Data filtration features

-   **Data Filters**

    Use data filters to grant access based on information within a record. Data filters use data in a tables field to determine whether a record is available to your users.

-   **Subject attribute based condition builder**

    Use subject attributes to evaluate user role, group, subject criteria, or IP network address.

-   **Data filtration uses a deny based model**

    Data filtration uses a deny based model to control access to records. With Data filtration, your instance denies access to records unless a record meets the criteria defined by Data filtration.

-   **Data filtration enforcement**

    Data filtration rules run after the database query for read operations and are evaluated before ACLs. A record denied by any Data filtration rule will not proceed and be evaluated by ACL rules. Data filtration rule enforcement is consistent with that of read ACLs.

-   **Data filtration and reporting**

    Data filtration and ACL's are both applied only when creating list view reports. Reporting does not apply access control when collecting aggregated data. In this case, neither Data filtration nor ACLs are checked.

    For aggregated reports, Data filtration works in conjunction with existing **Report\_view access control list** behaviors. See [Report\_view access control](https://www.servicenow.com/docs/access?context=report-view-access-control&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US) for further details on configuring these report controls.

-   **Session debugging**

    Data filtration supports session debugging. Use session debugging to see which Data filtration records apply for a given query. Admins can use this information to troubleshoot user access to records.


## Components of Data filtration

Data filtration works using the following record types:

-   **Data filtration records**

    Create a Data filtration \[sys\_df\_data\_filtration\] record to grant table access on your instance. The Data filtration record contains the **Data filter** and **Subject attribute** conditions described above to limit the scope of the rule and the affected users.

-   **Subject criteria records**

    Subject criteria \[sys\_df\_subject\_criteria\] records represent specific user attributes you can use to determine whether to grant access with a Data filtration rule. These attributes can be a user's groups, roles, or IP address. To create a subject criteria, you must create the subject criteria record, as well as criteria input and criteria conditions records. For details on this process, see [Creating subject criteria](../task/df-create-criteria.md).

    After creating a subject criteria records, you can apply them to a rule. This is done on the **Subject Condition** tab of your Data filtration rule.

-   **Criteria input records examples**

    ![Example criteria input for all roles containing admin](../image/criteria-condition-example2.png "Example criteria input for all roles containing admin")

    Criteria inputs \[sys\_df\_subject\_filter\_criteria\_m2m\] are records that contain criteria to compare with the user. This can be a list of user groups or roles, an IP address range, or an IP address subnet. These records are used along with subject criteria condition records to evaluate against a user's groups, roles, or IP address to determine access to a table or it's records.

-   **Subject criteria condition records**

    ![Example criteria condition using the Admins Only criteria input](../image/criteria-condition-example3.png "Example criteria condition using the Admins Only criteria input")

    Use subject criteria condition \[sys\_df\_subject\_criteria\_condition\] records to define how to compare user attributes with the roles, groups, or IP addresses defined in you criteria inputs. You can use multiple criteria inputs in a single subject criteria condition to further narrow down access to your records.


