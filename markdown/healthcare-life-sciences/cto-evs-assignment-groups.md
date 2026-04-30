---
title: Set up assignment groups for Care Team Operations for Environmental Services
description: Associate assignment groups with your healthcare organizations to determine which user groups are associated with specific healthcare organizations.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up work order synchronization, Configure, Care Team Operations for Environmental Services, Healthcare Operations, Healthcare and Life Sciences]
---

# Set up assignment groups for Care Team Operations for Environmental Services

Associate assignment groups with your healthcare organizations to determine which user groups are associated with specific healthcare organizations.

## Before you begin

Role required: admin

## About this task

In Care Team Operations for Environmental Services, assignment groups must be configured so that work orders created from environmental services cases can be fulfilled.

**Important:**

The various steps of fulfilling work orders require that assignment groups be created as follows:

-   **Environmental Services qualifier:**To set up evs.qualifier roles, you must be assigned the Environmental Services Qualifier group, which contains the sn\_cto\_evs.loc\_support\_agent role and the wm\_qualifier roles.
-   **Environmental Services dispatch:**To set up environmental services dispatch roles, you must be assigned the Environmental Services Dispatcher group, which contains the wm\_dispatcher and sn\_cto\_evs.loc\_support\_agent roles.

    **Note:** In Agent assignment groups, the Covered by Dispatch Groups tab must be used to indicate which groups can fulfill for them.


For both of the preceding roles, the **Locations Covered** related list displays all locations you can qualify or dispatch for.

## Procedure

1.  Navigate to **All** &gt; **Healthcare Operations** &gt; **Healthcare Organizations**.

2.  Select the healthcare organization that you want to associate an assignment group with.

3.  In the Assignment Groups related list, select **New**.

4.  On the Service Organization Assignment Group form, fill in the fields.

    Service Organization Assignment Group form:

<table id="table_omf_3mm_c2c"><tbody><tr><td>

**Field**

</td><td>

**Description**

</td></tr><tr><td>

Service organization

</td><td>

Auto-populated with the name of the healthcare organization to which you’re adding an assignment group.

</td></tr><tr><td>

Assignment group

</td><td>

Name of the assignment group that is to be added.

</td></tr></tbody>
</table>5.  Select **Submit**.


