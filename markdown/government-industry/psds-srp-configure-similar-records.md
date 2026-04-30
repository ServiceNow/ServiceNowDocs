---
title: Configure the Similar Records Activity UI in Service Request Playbook
description: The Similar Records Activity UI uses the name and description of existing cases to display a list of cases associated with the current case, allowing an agent to determine whether the current case is a duplicate of an existing case. Similar records can also provide helpful information about a current case.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Request Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the Similar Records Activity UI in Service Request Playbook

The Similar Records Activity UI uses the name and description of existing cases to display a list of cases associated with the current case, allowing an agent to determine whether the current case is a duplicate of an existing case. Similar records can also provide helpful information about a current case.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Service Request**.

3.  Under Intake, select **Add Activity**.

4.  Select**Playbooks for Customer Service Management** &gt; **Similar Records**

5.  Under When to Start, select **With Previous** from the dropdown.

6.  Select **View all properties**, then **Automation**.

7.  Select the arrow next to Record, and select **Trigger- Service Request** &gt; **Service Request Record**.

8.  Under Conditions, select **Stage** &gt; **is not** &gt; **Intake**.

9.  Toggle **Advanced** in the top right corner of the screen.

10. Select **Experience**, and set the associated table to "Service Request".

11. Set the associated record to **Trigger- Service Request** &gt; **Service Request Record**

12. To set parameters for.

13. Set the title to **This activity** &gt; **Label**.

14. Select **Done**, then select **Activate**.


## Result

The Similar Records UI activity is now configured, and the modal should now display when you open a new or existing Service Request Playbook.

