---
title: HR service categorization
description: HR services are categorized under one of the HR Centers of Excellence \(COEs\), which are part of a data model that organizes HR data, services, and processes by functional discipline.Enable or disable an HR Center of Excellence \(COE\) for use. COEs are tables that extend the HR Case \[sn\_hr\_core\_case\] table and part of a functional discipline, such as total rewards or talent management. COEs are also part of HR services that contain topic category and detail.Create or modify an HR topic category to define the first-level of categorization for HR services. Each topic category is associated with a single HR Center of Excellence \(COE\).Create or modify an HR topic detail to define the second-level of categorization for HR services. Each topic detail is associated with a single topic category and HR Center of Excellence \(COE\).Use COE Access Control List \(ACLs\) Configuration to allow specific groups read or write access to HR cases under a specific COE.Place security on a COE to prevent a group from accessing another group's cases.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [HR Centers of Excellence data model, HR services, HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR service categorization

HR services are categorized under one of the HR Centers of Excellence \(COEs\), which are part of a data model that organizes HR data, services, and processes by functional discipline.

Each COE is an extension of the HR Case \[sn\_hr\_core\_case\] table, and each COE is further organized by HR topic category and detail. Before you begin configuring the individual HR services, determine which COEs you want to use, and then create or modify the appropriate HR topic categories and details for each COE.

**Parent Topic:**[HR Centers of Excellence data model](hr-centers-of-excellence-coes.md)

## Enable or disable an HR Center of Excellence \(COE\)

Enable or disable an HR Center of Excellence \(COE\) for use. COEs are tables that extend the HR Case \[sn\_hr\_core\_case\] table and part of a functional discipline, such as total rewards or talent management. COEs are also part of HR services that contain topic category and detail.

### Before you begin

Role required: sn\_hr\_core.admin

Deactivate COEs manually on all your environments, if your company:

-   Does not use COEs.
-   Wants to deactivate COEs.
-   Has multiple environments and you're using system update sets to update changes.

    **Note:** System update sets capture deactivation in one environment, but after a patch or upgrade, COEs are active in your other environments. See [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).


### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **COE Configuration**.

2.  Enable or disable the applicable HR Center of Excellence \(COE\).

    **Note:** The COEs available to you may differ depending on the HR package you have.

    -   The categorization of HR catalog items are employee-facing only, and have no relation to the categorization of HR services under the HR Centers of Excellence \(COEs\) data model.
    -   If you are creating a new HR service and plan to make it available for employee self-service, see [HR catalog item configuration](hr-catalog-item-configuration.md). Creating a new HR catalog item automatically creates a corresponding HR service, and you can avoid creating duplicate services.
    -   If you have an existing HR service that you want to make available for employee self-service, do not create an HR catalog item. \(Creating a HR catalog item automatically creates a corresponding HR service.\) Instead, see [Configure a record producer for an HR service](../task/configure-hr-record-producer.md) to add the existing service as an HR catalog item in the HR service catalog.
    -   The Agent Workspace for HR Case Management is highly configurable for HR agents. It supports the same functionality in the Classic HR Service Delivery Agent Workspace.
    ![COE Configuration page displaying a list of HR cases like "Employee Relations," "HR Benefits," and "HR Payroll," each with an adjacent toggle switch for enabling or disabling.](../image/coe-enable-disable.png)

    COEs that are not associated with any HR services, topic details, categories, or record producers are automatically disabled.

    When you disable a COE, all associated HR services are also disabled. However, the extended tables linked to that COE remain accessible and are not disabled. Any active cases under the deactivated COE will continue to remain active; only the COE itself is deactivated.

3.  Click **Save**.


## Configure an HR topic category

Create or modify an HR topic category to define the first-level of categorization for HR services. Each topic category is associated with a single HR Center of Excellence \(COE\).

### Before you begin

Role required: sn\_hr\_core.admin

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **Topic Categories**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Active|Check box to activate the HR topic category for use.|
    |COE|Name of the HR Center of Excellence \(COE\) that the HR topic category is categorized under. Each HR topic category is associated with a single COE.|
    |Name|Name of the HR topic category.|

4.  Click **Submit** or **Update**.


## Configure an HR topic detail

Create or modify an HR topic detail to define the second-level of categorization for HR services. Each topic detail is associated with a single topic category and HR Center of Excellence \(COE\).

### Before you begin

Role required: sn\_hr\_core.admin

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **Topic Details**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Active|Check box to activate the HR topic detail for use.|
    |Name|Name of the HR topic detail.|
    |Topic category|Name of the HR topic category that the HR topic detail is categorized under. Each HR topic detail is associated with a single HR topic category.|

4.  Click **Submit** or **Update**.


## Configuring HR Service Delivery Center of Excellence \(COE\) security policies

Use COE Access Control List \(ACLs\) Configuration to allow specific groups read or write access to HR cases under a specific COE.

For example, you don't want the Benefits group to view the cases created by the Compensation group. You create a COE security policy that allows the Compensation group access. Groups that aren't included on the policy cannot access the cases.

Use this feature as an alternative to using ACLs rules. For more information on ACLs, see [Access control list rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

COE security policies don't affect case creation. COE security policies affect what cases you can view or modify after creation.

You can still reclassify \(transfer\) HR cases from one HR service to another. Depending on the security policy, you might not be able to view the case after reclassification.

COE ACL Configuration uses the COE Security Policy \[sn\_hr\_core\_coe\_security\_policy\] table to determine access to the extended HR case tables \(COEs\).

The \* next to a table indicates it was deprecated for customers taking the Rome release to support a new data model. Existing customers using the legacy COEs and tables are not affected. These tables have been replaced by the Employee Relations feature. For more information, see [Employee Relations cases](hr-case-employee-relations.md).

The tables you can provide security for are:

|Label|Name|
|-----|----|
|HR Benefits Case|sn\_hr\_core\_case\_benefits|
|HR Compensation Case|sn\_hr\_core\_case\_compensation|
|HR Corporate Communications Case|sn\_hr\_core\_case\_corporate\_communcations|
|\*HR Employee Relations Case|sn\_hr\_core\_case\_relations|
|\*HR Ethics Case|sn\_hr\_core\_case\_ethics|
|HR Global Mobility Case|sn\_hr\_core\_case\_global\_mobility|
|HR Payroll Case|sn\_hr\_core\_case\_payroll|
|\*HR Performance Case|sn\_hr\_core\_case\_performance|
|HR Talent Management Case|sn\_hr\_core\_case\_talent\_management|
|HR Total Rewards Case|sn\_hr\_core\_case\_total\_rewards|
|HR Workforce Administration Case|sn\_hr\_core\_case\_workforce\_admin|
|HRIT Operations Case|sn\_hr\_core\_case\_operations|
|HR Lifecycle Events Case|sn\_hr\_le\_case|

**Note:** You can also provide security to any case table you extend.

To define security for a COE:

-   Choose all or specific HR services that fall under a COE.

    **Note:** When you select specific HR services for a COE, the unselected HR services are accessible by the case reader.

-   Determine what groups have read or write access to HR services under a COE.
-   Create conditions to filter the records that apply to your security policy.

    **Note:** Condition builder is a powerful tool that filters specific actions on the COE. Use caution when using conditions on your security policy. It may also affect system performance.


## Create COE security

Place security on a COE to prevent a group from accessing another group's cases.

### Before you begin

Role required: admin, sn\_hr\_core.admin, sn\_hr\_le.admin

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **COE Security Configuration**.

2.  Select the COE \(table that extends the HR case table\) you want specified groups to have access to.

3.  Check **Applies to all services** if you want all the HR services under the selected COE to be included in the security policy.

4.  Leave this field blank to select specific HR services under a COE.

5.  If you leave this field blank, the **Services** field appears and you can select specific HR services.

6.  Ensure that the **Application** field displays the scope correctly.

    For more information, see [System settings for the user interface \(UI\)](https://www.servicenow.com/docs/access?context=r_UI16BannerFrame&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

7.  Check **Active** to enable security on the COE.

8.  From the **Type** field, select how the policy you are defining controls security for the COE.

    Your choices are:

    -   Read
    -   Write
    -   Case Restriction
    **Note:** The Case restriction option is only displayed when Employee Relations is installed.

    Selecting Case Locking displays the following fields:

    -   Able to lock cases: Users that belong to the associated group can lock cases under the COE.
    -   Able to view locked cases: Users that belong to the associated group can view locked cases.
9.  Select the filter condition \(if configured\) the security policy must pass for the COE to be in effect.

    **Warning:** Selecting the filter condition might impact the security policy and affect all cases under a COE, including the non-active cases. Be sure you understand the full impact of the condition.

10. Select **Save** to remain on the security policy you are working on or **Submit** to return to the list of COE Security Policies.

    If you select **Save**, the Groups related list appears.

11. Select **Edit** to associate groups to the COE security policy.

    For more information on Groups, see [Manage HR Groups](../task/t_ManageHRGroups.md).

12. Move the groups you want associated with the COE security policy you are defining from the Collection column to the Groups List column.

13. Select **Save**.

    The COE Security Policy returns.

14. Select **Update**.


