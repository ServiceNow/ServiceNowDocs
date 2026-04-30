---
title: Add the data import task
description: Add the data import task that you’ve configured to the Account lifecycle onboarding process defined in the Process Automation Designer.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Data capture and validation, Set up the account onboarding playbook, Configuring account onboarding, Account onboarding, Customer Success Management]
---

# Add the data import task

Add the data import task that you’ve configured to the **Account lifecycle onboarding process** defined in the Process Automation Designer.

1.  Navigate to **All** &gt; **Process Automation Designer**.
2.  Select the **Account lifecycle onboarding process**.
3.  Navigate to the Data Capture &amp; Validation lane and select **Add an activity**.
4.  Select **Account lifecycle events** and select the **Create &amp; View Tech Task Record**.
5.  Select the **Edit** icon on the newly added task to view the properties.
6.  Select **View all properties** and select **Advanced**.
7.  In the General tab, enter the label name and description.
8.  In the When to start field, select **With Previous**. This option enables you to execute all the activities in the task in parallel.
9.  Select the Automation tab and in the Inputs section, enter the following:
    -   Table: The table for which the record is being created. Select **Account Lifecycle Import Task \(sn\_ti\_core\_imp\_task\)**.
    -   Canceled Conditions: Specify the conditions that must be met before the task moves into the canceled state.
    -   Closed Conditions: Specify the conditions that must be met before the task moves into the Closed state.
    -   Onboarding Case: Select the Account Onboarding Case Record trigger to associate this record with the account onboarding case.
    -   Record View: The name of the Form View that is to be displayed in the Customer Success Management playbook. Enter `tech_pad_imp_task_view` here.
    -   Responsibility Name: Select the ServiceNow Developer/Admin user role from the list. This role is assigned to the internal team members \(defined in the Assign internal team responsibilities task of the **Initiate** stage of the playbook. See [Set up the account onboarding playbook](account-lifecycle-use-playbook.md) for details\). Users with this role can perform the data import task.
10. Select **Add Field** and enter data in the following fields from the Customer Success Management Import Task table.

    -   Source Table: Add the internal name of the staging table. For example, `sn_acct_lc_account_onb_import_locations`.
    -   Target Table: Add the internal name of the target table. For example, `cmn_location`.
    -   Data Source: Select the data source. For example, `cmn_location_template.xlsx`.
    -   Data Import State: The default value is set to 1 \(Data not loaded yet\).
    -   State: The default state is set to 1 \(Open\).
    -   Type: `Select data_capture`.
    -   Account: Select the account onboarding case associated with the case task.
    -   Parent: Select the parent record associated with the account onboarding case.
    -   Visible to customer: Set this **False.**
    Enter the Subject and Description as required and select **Done**

11. Ensure that you test the configuration and then select **Activate** to activate the playbook.

After the data import task has been configured, the Customer Success Management playbook can be used to onboard customers. See [Set up the account onboarding playbook](account-lifecycle-use-playbook.md) for details.

