---
title: Configure budget categories in Grants Management
description: Configure the budget categories that appear in the Program budget activity of the playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-gmp-budget-cat.html
release: australia
topic_type: task
last_updated: "2026-03-31"
reading_time_minutes: 1
breadcrumb: [Set up a grant program, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure budget categories in Grants Management

Configure the budget categories that appear in the Program budget activity of the playbook.

## About this task

By default, the Grants Management contains the following required budget categories:

-   Administration: Costs related to project management, administrative support, and general operating expenses directly attributable to the project.
-   Award: Total award amount requested, including all direct and indirect costs for the entire project period.
-   Contractual: Costs for services to be provided by external organizations or consultants, including subcontracts, licensing costs, consulting agreements.
-   Equipment: Total cost for all equipment necessary for project execution.

## Before you begin

Role required: admin

Confirm the application scope is set to **Service Applicant Program Management**.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  In the column name field, search for , and select the entry that has Grant Program as the table.

3.  Select the choices tab.

4.  Select the category you want to modify.

5.  Identify the numeric value of the categories corresponding to each label.

6.  Navigate to **All** &gt; **Process Automation** &gt; **Playbook Designer**.

7.  From the new tab, under the Playbooks tab, identify the Grant Program Setup playbook, and open it.

    The default playbook is “Program setup”, but you should refer to your cloned version.

8.  Select the Program budget activity, then select **Show additional options**.

9.  Select **UI layout**, then the **Required categories** field.

10. Populate the field with the values corresponding to the category you want to add.

    If there are multiple categories, separate the value with comma.

11. Select **Save and close**, then select **Activate**.


## Result

The new configuration should appear in the **Program budget** activity of the grants setup playbook.

**Parent Topic:**[Set up a grant program in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gmp-grant-pgr.md)

**Previous topic:**[Configure a merit review scoring rubric for a grants proposal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gmp-create-rubric.md)

**Next topic:**[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gmp-calendar-period.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gmp-calendar-period.md)

