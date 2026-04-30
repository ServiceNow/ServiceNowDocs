---
title: Assessment task form in Configurable Workspace
description: The form for creating or modifying a Cloud Migration Assessment assessment task displays detailed information about the assessment.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Cloud Migration Assessment reference, Cloud Migration Assessment, ITOM Cloud Accelerate, IT Operations Management]
---

# Assessment task form in Configurable Workspace

The form for creating or modifying a Cloud Migration Assessment assessment task displays detailed information about the assessment.

## Details tab

Enter the information on the Details tab to create or modify an assessment task.

<table id="id_bsx_yjt_csb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Assessment section

</td></tr><tr><td>

Number

</td><td>

The unique name of the assessment task.

</td></tr><tr><td>

Assigned to

</td><td>

The user who is directly responsible for migrating resources associated with this task.

</td></tr><tr><td>

Assignment group

</td><td>

The user group to which this assessment task is assigned.

</td></tr><tr><td>

Created by

</td><td>

The user who created this assessment task.

</td></tr><tr><td>

List of Contacts

</td><td>

The people inside and outside your organization who need to be notified. The system sends automatic notifications when this task is created or updated.

</td></tr><tr><td>

Migration Start Date

</td><td>

Date to start migrating the resources assigned to this assessment task.

</td></tr><tr><td>

Migration Completion Date

</td><td>

The date to finish migrating the resources assigned to this assessment task.

</td></tr><tr><td>

Created

</td><td>

The creation date of the assessment task.

</td></tr><tr><td>

Updated

</td><td>

The modification date of the assessment task.

</td></tr><tr><td>

State

</td><td>

The assessment task state: -   New
-   In Review
-   Approved
-   Exception
-   Migration in Progress
-   Migration Completed

</td></tr><tr><td>

Target Cloud Provider

</td><td>

The cloud provider that hosts resources assigned to this assessment task after the migration is completed.

</td></tr><tr><td>

Target Architecture

</td><td>

The cloud service models used for migrating resources assigned to this assessment task: IaaS, PaaS, Hybrid \(IaaS and PaaS\), Containers, and SaaS.

</td></tr><tr><td>

Urgency

</td><td>

The urgency level: high, medium, or low.

</td></tr><tr><td>

R-Disposition

</td><td>

The migration type:

-   **Rehosting — "Lift-and-shift"**

You rehost your application using a different hardware environment without changing the application architecture. Typically, this strategy suits large legacy applications, or scenarios where the migration must be done quickly and effectively.

-   **Replatforming — “Lift-tinker-and-shift"**

You keep the original architecture of the application, while making just a few optimizations to enjoy the benefits of the cloud infrastructure. Re-platforming may take longer than rehosting, but it is perfect for cases where you must have a degree of cost-effectiveness, functionality and time-savings without the significant resource requirements of refactoring.

-   **Retiring**

You stop using some appliances or products in your current infrastructure. For example, you may decide not to migrate aging servers or applications with few users.

-   **Retaining — "Revisit"**

Migration strategy decisions take a lot of consideration and research. In some cases, you may want to put it on hold and revisit the most crucial or problematic aspects of your infrastructure later.

-   **Refactoring — "Rearchitecturing"**

You review and redesign the architecture of the current infrastructure to leverage cloud features and flexibility. Refactor your infrastructure or its components to achieve scale, performance or agility that the application cannot meet with its existing architecture. This strategy may be the most expensive, but it may also be the perfect solution, especially if you are moving towards a service-oriented infrastructure.

-   **Repurchasing — "Drop and shop"**

You switch from your current application into a service or appliance that the cloud provider offers. In some cases, it is easier and more profitable to start using a new cloud product rather than investing into migrating an old one. If your organization has some home-grown products or an industry specific application not suitable for cloud infrastructures.


</td></tr><tr><td>

Migration wave

</td><td>

The migration wave that contains this assessment task. Migration waves come preconfigured with Cloud Migration Assessment.

</td></tr><tr><td>

Short description

</td><td>

The short description of this assessment task.

</td></tr><tr><td>

Description

</td><td>

The description of this assessment task.

</td></tr><tr><td class="sub-head" colspan="2">

Notes section

</td></tr><tr><td>

Watch list

</td><td>

The watch list for this assessment task.

</td></tr><tr><td>

Work notes list

</td><td>

The comments in free text.

</td></tr><tr><td>

Additional comments \(Customer visible\)

</td><td>

The comments related to this assessment task.

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

The related work notes that are not visible to customers.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Migration Assessment reference](cloud-migration-reference.md)

