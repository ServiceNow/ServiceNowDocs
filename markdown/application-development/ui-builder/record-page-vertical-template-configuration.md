---
title: Record page vertical template setup
description: Efficiently organize related lists and UI pages on a record page within groups to simplify configuration. Users have the flexibility to create groups, incorporate related lists or UI pages during configuration, and specify the order in which items appear on the page.Configure the properties of the record page vertical template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/record-page-vertical-template-configuration.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Record page vertical template setup

Efficiently organize related lists and UI pages on a record page within groups to simplify configuration. Users have the flexibility to create groups, incorporate related lists or UI pages during configuration, and specify the order in which items appear on the page.

## Before you begin

Ensure that you have the Record page-vertical \(sn\_rec\_pg\_vertical\) pluign installed and activated.

Role required: admin

## About this task

Within a form, multiple related lists may lead to a cluttered appearance. To optimize the display, you can choose and customize the related lists you wish to view on the form, arranging them vertically instead of the default horizontal layout. While you can select any table and configure the related lists for that table, as an example, this procedure uses the example of Operational Sustainability Management and describes how you can create groupings for the Goal configuration table. Apart from the related lists, you can also specify a UX page that you want to display under a group.

## Procedure

1.  Navigate to **All** &gt; **Tables** &gt; **Record View Configurations**.

2.  Select **ESG workspace configuration**.

3.  In the Table configurations related list, select **Goal configuration**.

4.  In the Group configurations related list, select **New**.

5.  On the form, fill in the fields.

<table id="table_bwh_s1s_zxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table configuration

</td><td>

Name of the table for which you're configuring the related list. This field is automatically set.

</td></tr><tr><td>

Name

</td><td>

Name of the group that will be displayed on the related list of the form. For example, you can provide a name such as `Program set up`.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the configuration is active.

</td></tr><tr><td>

Order

</td><td>

Order number of the group on the form. **Note:** If you want to display the order before the Details tab, then the order number must be less than or equal to `100`.

</td></tr><tr><td>

Condition

</td><td>

Conditions that must be met in order to be displayed on the form. For example, you can specify that if a goal is of type Environmental, only then it must be displayed on the form.

</td></tr></tbody>
</table>6.  Select **Submit**.

7.  In the Group configurations related list, select the entry you created.

    1.  In the Group entries related list, select **New**.

    2.  On the form, fill in the fields.

<table id="table_kfn_scs_zxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group configuration

</td><td>

Group for which the related list is being created. For example, in this procedure, the group for which you're configuring the entry is **Program setup**.

</td></tr><tr><td>

Order

</td><td>

Order of the entry on the UI page.

</td></tr><tr><td>

Application

</td><td>

Application for which the related list is being created. This field is automatically set to **Environmental, Social, Governance Management**.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the entry is active.

</td></tr><tr><td>

Type

</td><td>

Choice to indicate the type of item the group will contain. The choices are as follows:-   **UX page**
-   **Related list**


</td></tr><tr><td>

Related list

</td><td>

Related list that you want must appear under the group. This option appears only when the **Type** field contains **Related list**.

</td></tr><tr><td>

Screen

</td><td>

Specific variation or version of a page. This option appears only when the **Type** field contains **UX page**.

</td></tr><tr><td>

Route

</td><td>

Path of the UX screen. This option appears only when the **Type** field contains **UX page**.

</td></tr></tbody>
</table>    3.  Select **Submit**.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Record page vertical template properties

Configure the properties of the record page vertical template.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table name for which the template needs to render.Data type - String

</td></tr><tr><td>

SysId

</td><td>

SysId of the record for which the template needs to render. For new record sysId should be -1.Data type - String

</td></tr><tr><td>

Query

</td><td>

Encoded query to set some default values.Data type-String

</td></tr><tr><td>

View

</td><td>

Name of the view \(sys\_ui\_view\) in which to display forms, like workspace. Use this property to set the UI View record for the workspace.Data type - String

</td></tr></tbody>
</table>