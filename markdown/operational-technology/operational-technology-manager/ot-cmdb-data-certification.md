---
title: Create CMDB Data Certification Policy for Operational Technology
description: Create a CMDB Data Certification Policy for Operational Technology \(OT\) to validate and maintain accurate configuration item \(CI\) data.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Operational Technology Manager, Operational Technology]
---

# Create CMDB Data Certification Policy for Operational Technology

Create a CMDB Data Certification Policy for Operational Technology \(OT\) to validate and maintain accurate configuration item \(CI\) data.

## Before you begin

Role required: sn\_cmdb\_admin

## About this task

CMDB Data Certification policies help maintain the accuracy and reliability of data in the CMDB. The policies define when and how configuration items \(CIs\) are validated and automatically generate certification tasks for assigned reviewers.

You can use certification policies to:

-   Periodically validate key attributes of CIs.
-   Assign certification tasks to individuals or groups.
-   Track and manage certification progress from a central workspace.

For example, you can create a policy that certifies IP Address, MAC Address, and Serial Number for all Control Systems located in Site A of a manufacturing plant.

## Procedure

1.  Navigate to **Workspaces** &gt; **** &gt; **CMDB Workspace** &gt; **Management**.

2.  From the Management page, navigate to **Management tools** &gt; **Data Manager** &gt; **Policies**.

3.  Select **Create a new policy** and enter the following information for each parameter:

<table id="table_gcf_b51_hhc"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

General Information

</td><td>

Enter the policy name and description, ensure the Policy type is set to Certification, and Select **Continue**.

</td></tr><tr><td>

Data Filter

</td><td>

Define the criteria for the policy, select **Apply filter** to preview the included CIs, and select **Continue**.

 Verify the records and select **Continue**.

</td></tr><tr><td>

Assignment

</td><td>

Select the Assignment type for the tasks that are created based on the policy and select **Continue**. You can choose to:

-   Assign the tasks to a user or a user group mentioned on the CI record.
-   Set static values as well.
 For example, we are assigning the tasks to the user group responsible for managing the Control Systems in the Site 1.

</td></tr><tr><td>

Options

</td><td>

In the Options section:

-   **Display fields** are visible to users in the list view when they click on review the CIs. Choose field values as per your requirement.
-   The **Certification fields** are the fields that are certified by the user.
-   Select the **Allow field updates** checkbox in case you want to allow users to fill in the field value.
-   In the **Days to complete** field, set the number of days to complete the created certification task.
-   In the **Instructions** field, you can provide additional information or instructions for users.
 Select **Continue**.

</td></tr><tr><td>

Schedule

</td><td>

In the **Schedule** page, enter values according to your requirement to configure the frequency of the policy to be triggered.

</td></tr><tr><td>

Review

</td><td>

Review the policy in detail and select **Publish Policy**.

</td></tr></tbody>
</table>
## Result

You can view the policy in the **Published Policies** section on the main page after publishing.

**Parent Topic:**[Using the Operational Technology Manager](../concept/using-operational-technology-manager.md)

