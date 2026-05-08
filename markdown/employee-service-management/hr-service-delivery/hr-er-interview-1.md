---
title: Interview Management for Employee Relations
description: Use Interview Management to create templates to capture questions, answers, and notes in a consistent and efficient way, sync scheduling with Microsoft Outlook, and better plan and track your interviews.Set up HR Service Delivery Interview Templates so your agents can quickly, consistently, and accurately capture appropriate information.You can activate the Interview Templates plugin \(com.sn\_interview\_templates\) for the ServiceNow AI Platform if you have the admin role.Interview Question Templates provides your agents with a consistent and efficient way to capture answers from interviews.Create template tags you can use to filter interview question templates on pre-defined attributes. Template tags allow you to find relevant questions easier and faster.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configuring Employee Relations, Employee Relations, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Interview Management for Employee Relations

Use Interview Management to create templates to capture questions, answers, and notes in a consistent and efficient way, sync scheduling with Microsoft Outlook, and better plan and track your interviews.

## Setting up Interview Templates

Set up HR Service Delivery Interview Templates so your agents can quickly, consistently, and accurately capture appropriate information.

Activate the Interview Templates plugin \(com.sn\_interview\_templates\) for the ServiceNow AI Platform if you have the admin role. For more information, see [Activate Interview Templates](hr-er-interview-1.md#).

-   Create interview question templates.
-   Create interview template tags. Tags help you filter your interview question templates so you can easily browse for relevant questions to use in an interview. For example, agents ask different questions depending on who they are talking to and what the specific allegations are. Template tags help agents to find the appropriate interview template.

|Role|Description|Contains roles|
|----|-----------|--------------|
|Interview questions template admin \[sn\_interview\_temp.admin\]|Can access, read, create, and edit interview question templates, template tags, and Employee Relations properties.|sn\_interview\_temp.reader, sn\_interview\_temp.writer|
|Interview questions template writer \[sn\_interview\_temp.writer\]|Can access, read, create, and edit interview question templates and template tags.|sn\_interview\_temp.reader|
|Interview template reader \[sn\_interview\_temp.reader\]|Can access and read interview question templates and template tags.|N/A|

### System properties

The **sn\_interview\_temp.filter\_attr\_allowed\_tables** system property determines the tables you are allowed to create interview template tags for interview question templates.

When entering multiple tables, separate the table names with a comma \(,\) but with no space between each table.

### Template tags

Template tags are a way to organize your interview templates and a way to filter them when looking for the correct template. Template tags allow you to find relevant questions easier and faster.

From the legacy UI, you can select the **Questions** button to show all interview templates. The template tags appear at the bottom of each interview template displayed.

In the HR Service Delivery Agent Workspace, the template tag appears at the bottom.

There are two types of template tags you can create:

-   Referenced: Uses the fields from the following tables to create reference tags:
    -   Allegation Subtype \[sn\_hr\_er\_allegation\_subtype\]
    -   Allegation Type \[sn\_hr\_er\_allegation\_type\]
    -   HR Service \[sn\_hr\_core\_service\]
-   Custom: You create you own interview template organization. For example:

    -   Customer category = Involved party type
    -   Custom tags:
        -   Complainant
        -   Subject of allegation
        -   Witness
    Involved party type becomes the top-level category in the organization with the tags being a way to organize the type of person you are interviewing.


### Activate Interview Templates

You can activate the Interview Templates plugin \(com.sn\_interview\_templates\) for the ServiceNow AI Platform if you have the admin role.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Interview Templates plugin \(com.sn\_interview\_templates\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


### Create an interview question template

Interview Question Templates provides your agents with a consistent and efficient way to capture answers from interviews.

#### Before you begin

Role required: sn\_interview\_temp.admin

#### Procedure

1.  Navigate to **All** &gt; **Employee Relations** &gt; **Interview Question Templates**.

2.  Select **New** or an existing interview question template.

3.  Fill in the form or make edits.

<table id="choicetable_lzw_sjn_r4b"><thead><tr><th align="left" id="d301440e450">

Field

</th><th align="left" id="d301440e453">

Value

</th></tr></thead><tbody><tr><td id="d301440e459">

**Active**

</td><td>

Option for enabling the **Interview Question Template** and make it available.

</td></tr><tr><td id="d301440e471">

**Name**

</td><td>

The name that identifies the interview question template.

</td></tr><tr><td id="d301440e480">

**Application**

</td><td>

The application the interview question template belongs to.**Note:** The application that appears is dependent on your current application scope. For more information, see Application scope.

</td></tr><tr><td id="d301440e496">

**Table**

</td><td>

Name of the table the interview question template is associated with.**Note:** To only show interview question templates for ER interview records, select the Interview \(sn\_er\_interview\) table. If you leave this field blank, the interview template is available globally \(any tables that have been configured to use interview templates also have access\). Currently in the base system, only Employee Relations interviews are set up to access.

</td></tr><tr><td id="d301440e509">

**Question template body**

</td><td>

List of questions related to the type of interview. Interview question templates support rich text.

</td></tr></tbody>
</table>4.  Select **Save**.

    The **Template Tags** related list appears. In order to filter your interview templates, you must associate the interview template with a template tag.

    **Note:** For more information on **Template Tags**, see [Create an interview template tag](hr-er-interview-1.md#).


### Create an interview template tag

Create template tags you can use to filter interview question templates on pre-defined attributes. Template tags allow you to find relevant questions easier and faster.

#### Before you begin

Role required: sn\_interview\_temp.admin

Interview template tags drive the filtering interaction for an agent as a way to browse or search for a template.

#### Procedure

1.  Navigate to **All** &gt; **Interview Templates** &gt; **Template Tags**.

2.  Select **New**.

3.  Fill in the form.

<table id="simpletable_bbn_bps_4pb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tag type

</td><td>

The category of tag you are creating. The choices are:-   Referenced: Select to create tags related to a specific table. The tables that appear depend on the entries in the **sn\_interview\_temp.filter\_attr\_allowed\_tables** system property. For more information, see [Setting up Interview Templates](hr-er-interview-1.md#).

**Note:** When you have multiple applications that use **Interview Question Templates**, using **Referenced**, can keep your interview question templates separate. Associating a tag with a table helps your users filter for interview question templates faster and easier.

-   Custom: Select to create tags that are free-form text and referenced by a custom category.


</td></tr><tr><td>

Table

</td><td>

The table associated with a interview template tag. The tags you select are from the table you select.You can associate one of the following tables:

-   Allegation Subtype \[sn\_hr\_er\_allegation\_subtype\]
-   Allegation Type \[sn\_hr\_er\_allegation\_type\]
-   HR Service \[sn\_hr\_core\_service\]
 This field only appears whe you select **Referenced** from the Tag type field.

</td></tr><tr><td>

Custom category

</td><td>

The category that your custom tag belongs to.Ensure you have mapped out your structure before creating. Having a clear organization of your tags and categories makes searching for specific questions faster.

 This field only appears when you select **Custom** from the **Tag type** list.

</td></tr><tr><td>

Custom tag

</td><td>

The tag you want to associate with a question interview template.Enter a custom tag associated with the Custom category to create a hierarchy with custom category as the top of the hierarchy and tags under it.

 For example:

-   Customer category = Involved party type
-   Custom tags:
    -   Witness
    -   Complainant
    -   Subject of allegation
Involved party type becomes the top-level category in the organization with the tags being a way to organize the type of person you are interviewing.

</td></tr><tr><td>

Application

</td><td>

The application scope you are currently in and associated with the interview template tag.

</td></tr><tr><td>

Domain

</td><td>

The domain your current scope is associated with. This field applies to customers that have multiple domains. For more information, see [Domain Separation and HR Service Delivery](hr-domain-separation.md).

</td></tr></tbody>
</table>4.  Select **Save** or **Submit**.


