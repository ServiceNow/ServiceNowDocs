---
title: Add the data import task
description: Add the data import task that you’ve configured to the Account lifecycle onboarding process defined in the Process Automation Designer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/customer-success-management/account-lifecycle-add-data-import.html
release: australia
product: Customer Success Management
classification: customer-success-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Account onboarding playbook, Configure, Customer Success Management]
---

# Add the data import task

Add the data import task that you’ve configured to the **Account lifecycle onboarding process** defined in the Process Automation Designer.

1.  Navigate to **All** &gt; **Process Automation&gt; Playbook Designer**.
2.  Select the **Account lifecycle onboarding process**.
3.  Navigate to the Data Capture &amp; Validation lane and select **Add an activity**.
4.  Select **Customer Success Management** and select the **Create &amp; View ALE Record**.
5.  Select **Show additional options** and select **Advanced**.
6.  In the Details tab, enter the label name and description.
7.  In the **Start rule when stage starts** field, select **With Previous**. This option enables you to execute all the activities in the task in parallel.
8.  Select the **Automation** tab. In the Inputs section, enter the following:
    -   Table: The table for which the record is being created. Select **Data Import Task \(sn\_ti\_core\_imp\_task\)**.
    -   Canceled Conditions: Specify the conditions that must be met before the task moves into the canceled state.
    -   Closed Conditions: Specify the conditions that must be met before the task moves into the Closed state.
    -   Onboarding Case: Select the Account Onboarding Case Record trigger to associate this record with the account onboarding case.
    -   Record View: The name of the Form View that is to be displayed in the Customer Success Management playbook. Enter `tech_pad_imp_task_view` here.
    -   Responsibility Name: Select the ServiceNow Developer/Admin user role from the list. This role is assigned to the internal team members \(defined in the Assign internal team responsibilities task of the **Initiate** stage of the playbook. See [Initial setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-use-playbook-initiate.md) for details\). Users with this role can perform the data import task.
9.  Select **Add Field** and enter data in the following fields from the Customer Success Management Import Task table.

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

10. Test the configuration and then select **Activate** to activate the playbook.

After the data import task has been configured, the Customer Success Management playbook can be used to onboard customers. See [Account onboarding playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-account-onboard-playbook.md) for details.

**Parent Topic:**[Configure the account onboarding playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-configure.md)

