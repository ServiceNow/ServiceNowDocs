---
title: HR criteria
description: HR criteria defines the audience for HR content, services, or cases. You can make information available to or create an HR case for specific groups, individuals, or to all employees using HR criteria.Create or modify HR criteria to define an audience for HR content, services, or cases.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR criteria

HR criteria defines the audience for HR content, services, or cases. You can make information available to or create an HR case for specific groups, individuals, or to all employees using HR criteria.

HR criteria uses the standard platform condition builder to support complex conditions for controlling the Employee Center content that employees see when logged in. For more information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

HR criteria contains a script include that can be called from an advanced User criteria.

**Note:** Complex conditional statements for scripted User criteria applied to a knowledge base with large amounts of documents can cause performance issues. Standard \(non-scripted\) User criteria is recommended for securing knowledge documents.

See [User criteria for Service Portal](https://www.servicenow.com/docs/access?context=user-criteria&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

HR criteria define conditions that are evaluated against HR tables. Once HR criteria is defined, you can filter what is available to those users.

HR criteria helps group people using a condition builder on any table. User criteria is used across the ServiceNow platform to filter catalog items, Service Portal widgets, and knowledge articles. User criteria filters users based on role, department, group, location, or company. User criteria can be created when HR criteria is created. HR criteria:

-   Filters content on the Employee Center.
-   Applies only to **Subject person**. HR criteria filters **HR services** based on the **Subject person** during case creation or transfer.
-   Filters **Lifecycle Event Activities** in the **Human Resources Scoped App: Lifecycle Events \[com.sn\_hr\_lifecycle\_events\]** plugin.
-   Selects document template for HR cases.
-   Selects users when creating bulk HR cases.

For Lifecycle Events, activities have associated HR criteria that determines when to trigger an activity for the subject person selected on the Lifecycle event case. This step helps to personalize the workflow for the subject person.

**Note:** For HR Catalog Items \(record producers\), ensure **Use "User Criteria" to define access to catalog items and categories** is set to **Yes** under **Service Catalog** &gt; **Catalog Administration** &gt; **Properties**. Verify that this field is checked **Yes**.

You can use user criteria for Knowledge and Service catalog access. Add a reference column to the User Criteria \[user\_criteria\) table when columns are required for the criteria query.

If you use HR criteria for Knowledge and Service catalog access, ensure:

-   Referenced columns are correctly indexed.
-   Conditions that can cause performance issues \(starts with\) are not used.
-   Knowledge document searches and use cases are performance tested with instances that are similar to what is used in production.

When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

**Parent Topic:**[HR Administration](c_AdministerHRServiceManagement.md)

## Configure an HR criteria record

Create or modify HR criteria to define an audience for HR content, services, or cases.

### Before you begin

Role required: sn\_hr\_core.admin

HR criteria uses the standard condition builder. For more information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Criteria**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form.

<table id="table_jmv_njg_3hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the HR criteria record.

</td></tr><tr><td>

Description

</td><td>

Description of the HR criteria.

</td></tr><tr><td>

Active

</td><td>

Option to activate the HR criteria for use.

</td></tr><tr><td>

Related user criteria

</td><td>

You can create user criteria from HR criteria. User criteria is used across the ServiceNow platform to filter catalog items, HR Service Portal widgets, and knowledge articles. **Note:** This field remains blank until you create User criteria.

 The **Create User Criteria** link appears after you click **Save**.

</td></tr></tbody>
</table>4.  Click **Save**.

    You can create User criteria based on HR criteria. User criteria is used across the ServiceNow platform to filter catalog items, HR Service Portal widgets, and knowledge articles.

5.  Select the **Create User Criteria** related link.

    1.  Click **New** or **Edit** to open an existing record.

    2.  Fill in the fields on the form.

<table id="table_twh_yjg_3hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the HR condition.

</td></tr><tr><td>

Table

</td><td>

Table that the HR condition is associated with.The table HR criteria conditions are defined from.

 For example, select the **HR Profile \(sn\_hr\_core\_profile\)** table to select a field and define a condition.

</td></tr><tr><td>

Active

</td><td>

Option to activate the HR condition for use.

</td></tr><tr><td>

User column

</td><td>

Together with the **Table** field, filters users when evaluating a condition for a user.To create User criteria, select **User**.

 **Note:** Depending on the table selected, this field can be required to match conditions. When the User \[sys\_user\] table is selected, this field is mandatory otherwise a false positive can occur since the lookup is not associated to an expected user.

</td></tr><tr><td>

Condition

</td><td>

The field from the table selected and a value that defines the condition.Use conditions to define your HR criteria.

 For example, to define a single condition, you can select the following from the **HR Profile \(sn\_hr\_core\_profile\)** table:

-   **Home country**
-   **is**
-   **United States of America**
This condition selects all employees who have a home country of the United States on their HR profile record.

 You can define multiple conditions for an HR criteria using the **And** **Or** condition filters. When using **And** each condition must be met. When using **Or** any condition that is met is used.

 For more information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

 **Note:** When you use multiple conditions, only the records that match all of the conditions are used.

 When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

**Note:** For more information, see [Filters](https://www.servicenow.com/docs/access?context=c_Filters&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>        For example, to create a condition to show the link for new hires and contractors, select:

        -   Table: Client Role Rule \[sn\_hr\_core\_client\_role\_rule\]
        -   Condition: **\[Role\] \[is\] \[sn\_hr\_core.hrsm\_new\_hire\] AND \[Role\] \[is\] \[sn\_hr\_core.hrsm\_contractor\]**
        After creating a condition, a clickable link appears with the number of matching records. Click the link to see if the correct users are being selected based on the condition.

    3.  Click **Submit** or **Update**.

6.  In the **Conditions** section, you can add more conditions to define the HR criteria.


