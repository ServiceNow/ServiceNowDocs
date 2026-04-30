---
title: Create a certification policy
description: Creating a data certification policy serves as a governance mechanism to ensure that the data used in enterprise architecture models and visualizations is accurate, complete, and trustworthy.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-11-22"
reading_time_minutes: 4
breadcrumb: [Data certification in the Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Create a certification policy

Creating a data certification policy serves as a governance mechanism to ensure that the data used in enterprise architecture models and visualizations is accurate, complete, and trustworthy.

## Before you begin

Role required: System admin, cmdb admin + analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Data certification page by selecting the Data certification icon \(![data certification icon](../image/eaw-image/icon-data-cert.png)\).

3.  Select **New policy**.

4.  On the Create policy modal, enter details, then select **Next**.

    The details are saved as General Information in the workflow. For field information, see [General information form](../reference/eaw-reference/eaw-data-cert-gen-info-form.md).

5.  Enter details in the **Data Filter** form.

    For field information, see [Data filter form](../reference/eaw-reference/eaw-data-filter-form.md).

    -   Select **Apply filters** and then review the results of the impact analysis.
    -   Review the lists in the following tabs:
        -   **Included records:** You can select records to be excluded from the policy and select **Exclude records**.
        -   **Excluded records:** Select records to be included in the policy, and select **Include records**.
    -   Select **Continue**.
6.  Enter details in the **Assignment** form and then select **Continue**.

    -   Set the **Assignment type** and then the **Task assignment** field that appears, to specify the type of assignment and the table columns to use for assigning the policy tasks. The drop-down list in **Task assignment** is dynamically populated with columns in the table that the policy is created for, and that reference **Assignment type** tables, as follows:

        -   **User Field**: Assigns policy tasks to a user in the user field specified in **Task assignment**. The drop-down list in **Task assignment** contains fields in the table set by the data filter, that references the User \[sys\_user\] table \(such as **Attested by** and **Assigned to**\).

            During assignment, records are grouped based on the selected column, allocated to tasks, and then the tasks are assigned to the resulting users.

        -   **User Group Field**: Assigns policy tasks to the user group in the user group field specified in **Task assignment**. The drop-down list in **Task assignment** contains fields from the table set in the data filter, that references the Groups \[sys\_user\_group\] table \(such as **Change Group** and **Support Group**\).

            During assignment, records are grouped based on the selected column, allocated to tasks, and then the tasks will be assigned to the resulting user group.

        -   **Specific User**: Assigns policy tasks to the user specified in **Task assignment**. The drop-down list in **Task assignment** contains users with the **data\_manager\_user** role.
        -   **Specific User Group**: Assigns policy tasks to the user group specified in **Task assignment**. The drop-down list in **Task assignment** contains user groups that are either directly associated with the **data\_manager\_user** role, or contain at least one user with the **data\_manager\_user** role.
        In the **User Group Field** and **User Field** you can use dot-walking by selecting the search icon. In the selection dialog box, drill down lists by expanding or selecting list items that are links \(usually appear in a unique text color\).

    -   For certification and attestation tasks, set the **If task assignment field is empty** field to create assigned or unassigned tasks in cases where the specified task assignment field is empty. If you select to create an assigned task, then depending on the **Assignment type** setting, select the user or user group to assign a task to in that situation. Unassigned tasks are later reviewed by an administrator for assignment.
7.  Enter details in the **Options** form.

    For field information, see [Options form](../reference/eaw-reference/eaw-data-cert-options-form.md).

8.  Enter details in the **Schedule** form and then select **Continue**.

    For field information, see [Schedule form](../reference/eaw-reference/eaw-data-cert-schedule-form.md).

9.  Review the policy details on the Review form, and then select **Publish policy** to activate the policy or **Save &amp; Exit** to save the policy as a draft.

    You can later continue to configure a draft policy, and then publish it when it's ready.


**Parent Topic:**[Data certification in the Enterprise Architecture Workspace](../concept/eaw-concept/eaw-explore-data-cert.md)

**Related topics**  


[Edit a certification policy](eaw-task/eaw-data-cert-edit-policy.md)

[Run certification for a policy](eaw-task/eaw-data-cert-run-certification.md)

[Track progress of a certification policy](eaw-task/eaw-data-cert-track-progress.md)

[Activate a certification policy](eaw-task/eaw-data-cert-activate.md)

[Delete a certification policy](eaw-task/eaw-delete-data-cert.md)

[Deactivate a certification policy](eaw-task/eaw-data-cert-deactivate.md)

