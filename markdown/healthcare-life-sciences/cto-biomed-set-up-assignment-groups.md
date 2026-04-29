---
title: Set up assignment groups for Care Team Operations for Biomed
description: Associate assignment groups within your healthcare biomed organizations so work orders can be fulfilled.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up work order synchronization, Configure, Care Team Operations for Biomed, Healthcare Operations, Healthcare and Life Sciences]
---

# Set up assignment groups for Care Team Operations for Biomed

Associate assignment groups within your healthcare biomed organizations so work orders can be fulfilled.

## Before you begin

Role required: admin

## About this task

In Care Team Operations for Biomed, assignment groups must be configured so that work orders created from biomed cases can be fulfilled.

**Important:**

The various steps of fulfilling work orders require that assignment groups be created as follows:

-   **Biomed qualifier:**To set up biomed.qualifier roles, users must be assigned the Biomed Qualifier group,which contains the sn\_cto\_biomed.loc\_support\_agent role and the wm\_qualifier roles.
-   **Biomed dispatch:**To set up biomed dispatch roles, users must be assigned the Biomed Dispatcher group, which contains the wm\_dispatcher and sn\_cto\_biomed.loc\_support\_agent roles.

    **Note:** In Agent assignment groups, the Covered by Dispatch Groups tab must be used to indicate which groups can fulfill for them.


For both of the above roles, the **Locations Covered** related list displays all locations these users can qualify or dispatch for.

## Procedure

1.  Navigate to **All** &gt; **Healthcare Operations** &gt; **Healthcare Organizations**.

2.  Select the healthcare organization you want to associate an assignment group with.

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


