---
title: Approvals experience reference
description: Use the following reference information for better approval experience.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Reference, Employee Center, Employee Service Management]
---

# Approvals experience reference

Use the following reference information for better approval experience.

## Default task configurations

Use the following default task configurations available for approvals.

-   Request with **sysapproval** as reference column and **sc\_request** as reference table.
-   Requested item with **sysapproval** as reference column and **sc\_req\_item** as reference table.

You can customize the task configurations to suit your requirements. The data model is an extension to the Employee Center **To-do configuration** as a related list. Follow the instructions [Enable task configuration for approvals](../task/approval-hub-to-dos-page-filters.md) about configuring the approval experience. For more information on how to configure approvals, see [Configurable approvals experience](../concept/approval-hub-intro.md).

**Note:** A user must have the approval\_user or business\_stakeholder role to approve IT requests \(not applicable to other requests such as HR approvals\) on Employee Centre. Role validation has not been implemented in Core UI16 because modifying ACLs in UI16 might have broader implications at the NowPlatform level.

## Unable to see Approval todos

Ensure you have the approver\_user or business\_stakeholder roles to see the approval todos for the **sc\_request** or **sc\_req\_item** items. In the **\_getClosureFunction\(\)** method of Script Include todoPageUtils:

```
if (tableName == 'sysapproval_approver') { 
 if (!(gs.getUser().hasRole('approver_user') || gs.getUser().hasRole('business_stakeholder'))) { 
  var queryString = "sysapproval.sys_class_name!=sc_request^sysapproval.sys_class_name!=sc_req_item^NQsysapprovalISEMPTY"; 
  grTask.addEncodedQuery(queryString); 
 } 
} 
```

## Fallback to parent table configuration

When the child table does not have task configuration, fallback is one level above its hierarchy and picks the task configuration of the parent table. When the task parent is not available, fallback is to the default configuration.

## SAP Concur reference info

Use the following information for SAP Concur integration.

-   All Concur actions are present in **SAP Concur Spoke** \(sn\_sap\_concur\_spok\) plugin.
-   Scheduled job **Pull concur reports** \(sysauto\_script\) is triggered daily. This scheduled job internally calls the **Concur Integration** record from the **Integration Source** table \(sn\_hr\_integr\_fw\_source\) of the ESM framework.
-   Schedule job runs and updates the record in the **Concur Sync Details** table \(sn\_ex\_cnc\_concur\_sync\_details\) with latest timestamp.
-   Concur reports from ServiceNow are synced in the **Concur Expense Report Staging** table \(sn\_ex\_cnc\_concur\_report\_staging\).
-   Reports from the Staging table are transformed in the **Concur Expense Report** table \(sn\_ex\_cnc\_concur\_report\) by the ESM framework. Use the transformation map **Concur Report Transform Map** in the **Table Transform Map** table \(sys\_transform\_map\).
-   Approval record is created in the **Pulled Integration To-do** table \(sn\_hr\_integr\_fw\_todo\_inbound\) based on the Approver field in the **Concur Expense Report** table.

## Workday reference info

Use the following information for Workday integration.

-   Workday uses RAAS reports to send data to external system. For more information on RAAS and field-level info about leaves, timesheets, compensation, job change, job requisition, or leave of absence, see [Workday HR Spoke](https://www.servicenow.com/docs/access?context=workday-hr-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).
-   Only the open requests are displayed on the approvers **My tasks** page.
-   Approval and rejection actions are performed using an **Integration System User \(ISU\)**. ISU is a virtual user \(and not an actual user\) which helps in the safe-keeping of approver credentials. With the use of ISU, approval and rejection records protect the sensitive data according to your configuration in Workday. For example,
    -   When John Doe, the approver enters time sheet approved as comment, the comment shown as `John Doe(john.doe@acme.com): Time sheet approved`.
    -   When John Doe performs the action `Approve`, a comment is added in Workday as `John Doe (john.doe@acme.com): Action – Approve`.
    -   When John Doe performs the action `Reject`, a comment is added in Workday as `John Doe john.doe@acme.com): Action – Reject`.
    -   When John Doe performs the action `Reject with a comment-Request is not in compliance with company policy`, two comments are added `John Doe (john.doe@acme.com): Action–Reject` `John Doe(john.doe@acme.com): Request is not in compliance with company policy`.
-   Approve or reject actions are shipped out-of-the-box for all use cases.
-   When an approval is delegated from one approver to another in Workday; report data source is not able to handle the delegation change such as delegated task and other delegation details.
-   When a request requires a multi-level approval with level 1 approved in Workday and ServiceNow, you may see two entries for the same approval. This is a limitation with the ISU use.
-   Attachments support a max limit of 12 MB. Ensure the attachment size is below 12 MB.
-   Use the following scripts:
    -   WorkdayApprovalToDosClientUtilSNC: Retrieves records for the purge process in Workday approvals.
    -   WorkdayApprovalToDosHelperSNC: Contains constants related to Workday approvals.
    -   WorkdayApprovalToDosClientUtil: Extends WorkdayApprovalToDosClientUtilSNC and allows users to define custom code.
    -   WorkdayApprovalToDosHelperUtils: Extends WorkdayApprovalToDosHelperUtilsSNC and enables users to define custom code.
    -   WorkdayApprovalToDosHelperUtilsSNC: Provides functions for Workday approvals.
-   Ensure you configure the right user controls and privileges for Compensation Change and Spend Authorization use cases. Only the authorized users can view the sensitive records and data from Workday.
-   For data protection, use the default purge policy to delete data more often. By default, data purge happens after in 30 days.
-   Ensure only the HR administrator \[sn\_hr\_core.admin\] has access to the sensitive information as explained in [Remove HR Administrator role from IT System Administrators](../../human-resources/task/t_HRRemoveAdminRole.md).

For more information on how to configure approvals, see [Configurable approvals experience](../concept/approval-hub-intro.md).

## Approvals on mobile

Only approvals that are in **sysapproval\_approver** table are shown using the generic card in Now Mobile.

To disable the feature change the value of this sys\_property: sn\_me\_todos.all\_approvals\_mobile\_enabled to false​.

## OOTB action group use

Use the out-of-the-box **Approvals action group** to display the actions such as **Approve** and **Reject**. For more information, see [Action framework](../concept/action-group-framework.md).

**Note:** For actions to appear in my items widget, you can add the OOTB **Approvals action group** from **All** &gt; **Employee Center** &gt; **Administration** &gt; **To-dos Configurations**, click an existing to-dos configuration, navigate to the **To-do Configuration Details** record, and use the OOTB action group under **Fields Mapping**.

## Additional information

-   Click the URLs for additional information and context.
-   Allow BUs to add non-task tables easily to the list in the To-dos or Task configuration reference tables by passing non-task tables as an array in the **Scripted Extension Points**. **sn\_hr\_sp.TodoNonTaskTables**, and **sn\_ex\_sp.RefNonTaskTables**.

**Parent Topic:**[Employee Center reference](emp-center-reference.md)

**Related topics**  


[Activity Configuration form](ec-activity-configuration-form.md)

[Activity Configuration Detail form](activity-configuration-detail-form.md)

[Block content form](block-content-form.md)

[Browser Extension for Employee Center forms](../concept/ecbe-forms.md)

[Campaign overview and Campaign analytics dashboards](../concept/ecpro-content-automation-content-pack.md)

[Components installed with Employee Center Pro](components-installed-with-employee-center-pro-1.md)

[Components installed with Content engagement](installed-content-engagement.md)

[Components installed with Content Experiences](installed-with-content-auto.md)

[Components installed with Content Publishing](installed-with-content-delivery-1.md)

[Components installed with Content Governance](ec-installed-content-governance.md)

[Components installed with Content Analytics](ecpro-installed-content-analytics-1.md)

[Connected Content form](connected-content-form.md)

[Content Analytics dashboards](../concept/content-analytics-dashboards.md)

[Content engagement dashboard](../concept/ec-pro-content-engagement-dashboard.md)

[Content Library Overview dashboard](../concept/content-library-overview-dashboard.md)

[Default Employee Profile Header Configuration record](default-profile-header.md)

[Employee Center widgets](../concept/employee-center-widgets-list.md)

[Employee Profile form](employee-profile-fieldconfig.md)

[Employee Profile Header Configuration form](profile-header-config-form.md)

[Employee Profile portal configuration form](profile-portal-config-form.md)

[Employee Profile upgrade scenarios](emp-profile-upgrade.md)

[Enhanced Requests Experience forms](req-concept-ec.md)

[External Link form](external-link-form.md)

[Featured Content form](featured-content-form.md)

[Feedback Analytics dashboard](../concept/ex-fdback-board.md)

[Feedback configuration form](ex-feedback-new-record.md)

[Feedback definition form](fdbck-dfnition-record.md)

[Footer form](ec-footer-form.md)

[Footer Menus form](ec-footer-menus.md)

[Guided Self-Service reference](gss-guided-self-service-reference-info.md)

[Link content form](link-content-form.md)

[Menu Item form](menu-item-form.md)

[Configuring translation for Content Publishing after upgrade](../concept/ec-multiple-language-support.md)

[Notification content form](notification-content-form.md)

[Employee Profile Overview section form](profile-overview-section-form.md)

[Properties installed with Content Experiences](properties-installed-with-content-auto.md)

[Properties installed with Content Governance](properties-installed-content-governance.md)

[Properties installed with Content Publishing](properties-with-content-delivery.md)

[Quick Link form](ec-quick-link-form.md)

[Standard banner and icon sizes](ec-portal-images-size.md)

[Tab widget mapping form](tab-widget-mapping-form.md)

[Taxonomy form](taxonomy-form.md)

[To-do content form](to-do-content-form.md)

[Topic form](topic-form.md)

[User Criteria form](ec-user-criteria-form.md)

[User Criteria output](user-criteria-output.md)

