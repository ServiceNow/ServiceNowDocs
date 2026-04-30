---
title: Interview Management
description: Use Interview Management to create templates to capture questions, answers, and notes in a consistent and efficient way, sync scheduling with Microsoft Outlook, and better plan and track your interviews.Set up HR Service Delivery Interview Templates so your agents can quickly, consistently, and accurately capture appropriate information.You can activate the Interview Templates plugin \(com.sn\_interview\_templates\) for the ServiceNow AI Platform if you have the admin role.Interview Question Templates provides your agents with a consistent and efficient way to capture answers from interviews.Create template tags you can use to filter interview question templates on pre-defined attributes. Template tags allow you to find relevant questions easier and faster.You can schedule and document interviews and use interview templates using the Core UI or HR Service Delivery Agent Workspace.You can use the default ServiceNow calendar or integrate with Microsoft Exchange to schedule interviews related to Employee Relations \(ER\) cases.Documenting interviews is crucial to ER cases. Use the Interview form to take notes and capture important details of the ER case.Use HR Service Delivery Agent Workspace to capture a record of an interview.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 14
breadcrumb: [Setting up Employee Relations, Employee Relations cases, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Interview Management

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

![Interview Question Template system property](../image/hr-er-sys-property.png)

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
        ![Interview question template tags](../image/agent-ws-hr-template-tag-ex.png)

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

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


### Create an interview question template

Interview Question Templates provides your agents with a consistent and efficient way to capture answers from interviews.

#### Before you begin

Role required: sn\_interview\_temp.admin

#### Procedure

1.  Navigate to **All** &gt; **Employee Relations** &gt; **Interview Question Templates**.

2.  Select **New** or an existing interview question template.

3.  Fill in the form or make edits.

<table id="choicetable_lzw_sjn_r4b"><thead><tr><th align="left" id="d279327e462">

Field

</th><th align="left" id="d279327e465">

Value

</th></tr></thead><tbody><tr><td id="d279327e471">

**Active**

</td><td>

Option for enabling the **Interview Question Template** and make it available.

</td></tr><tr><td id="d279327e483">

**Name**

</td><td>

The name that identifies the interview question template.

</td></tr><tr><td id="d279327e492">

**Application**

</td><td>

The application the interview question template belongs to.**Note:** The application that appears is dependent on your current application scope. For more information, see [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

</td></tr><tr><td id="d279327e508">

**Table**

</td><td>

Name of the table the interview question template is associated with.**Note:** To only show interview question templates for ER interview records, select the Interview \(sn\_er\_interview\) table. If you leave this field blank, the interview template is available globally \(any tables that have been configured to use interview templates also have access\). Currently in the base system, only Employee Relations interviews are set up to access.

</td></tr><tr><td id="d279327e521">

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


## Using Interview Management

You can schedule and document interviews and use interview templates using the Core UI or HR Service Delivery Agent Workspace.

Creating a record of an interview is an important part of an employee relations investigation.

Scheduling an interview: There are two \(2\) methods you can use to schedule an interview:

-   Manual entry: You enter a start and end date/time for the interview and confirm outside the application.

    **Note:** In legacy UI, the manual entry is the only method available for scheduling an interview.

-   Use Microsoft Outlook Calendar to schedule an interview.

    -   To use this feature, you must integrate with Microsoft Exchange. Ensure the **sn\_hr\_er.ex\_online\_notification\_url** system property contains the Callback URL in the **Value** field. For more information, see [Set up Microsoft Exchange Online spoke](https://www.servicenow.com/docs/access?context=setup-ms-exch-ol&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).
    -   The **sn\_hr\_er.exchange\_online\_max\_candidate** system property determines the maximum number of meeting time slots to return when trying to schedule an interview using Microsoft Exchange. The default value is 500 slots.
    **Note:** You can use the manual method of scheduling in HR Service Delivery Agent Workspace. For more information, see [Schedule an interview in HR Service Delivery Employee Relations using the legacy UI](hr-er-interview-1.md#) or [Schedule an interview in HR Service Delivery Employee Relations using Agent Workspace for HR Case Management](hr-er-interview-1.md#).


### Scheduling an interview

You can use the default ServiceNow® calendar or integrate with Microsoft Exchange to schedule interviews related to Employee Relations \(ER\) cases.

### Schedule an interview in HR Service Delivery Employee Relations using the legacy UI

Documenting interviews is crucial to ER cases. Use the Interview form to take notes and capture important details of the ER case.

#### Before you begin

Role required: sn\_hr\_er.case\_writer

#### Procedure

1.  Navigate to **All** &gt; **Employee Relations** &gt; **Cases**.

2.  Select an ER case.

3.  Scroll down and select the **Interviews** tab in the related list.

4.  Select **New**.

5.  Fill in the form.

<table id="table_hbw_4cv_mlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The number identifying the interview record. The application automatically assigns interview numbers.

</td></tr><tr><td>

HR case

</td><td>

The HR ER case number associated with the interview.**Note:** If you access the interview from **Employee Relations**, you have to select an HR case to associate the interview to.

</td></tr><tr><td>

Interviewee

</td><td>

Name of the person who you are interviewing.Select the **Lookup using list** icon ![Lookup using list icon](../image/magnifying-glass.png) and search for the person you are interviewing. If no names appear, you can select **New** and create an involved party. For more information, see [Create an involved parties record](../task/hr-er-involved-parties.md).

</td></tr><tr><td>

Interviewers

</td><td>

Names of the people who conducted the interview.Click the **Unlock Interviewers** icon ![Unlock Interviewers icon](../image/icon-hr-unlock-add-parties.png) and search for the names of the people who conduct the interview.

**Note:** Only members with the sn\_interview\_temp.writer role or belong to a group that has the Employee Relations skill.

 You can optionally enter the email addresses for each interviewer.

</td></tr><tr><td>

External attendees

</td><td>

Indicates people outside of your company attended the interview.

</td></tr><tr><td>

External invite email

</td><td>

The email addresses of the external people that attend the interview.

</td></tr><tr><td>

Scheduling method

</td><td>

The method you are using to schedule the interview. If your company only uses the manual method of scheduling, **Manual entry** appears and cannot be edited.

 If your company uses the integration with Microsoft Outlook Calendar to schedule, **Calendar** appears. For more information, see [Using Interview Management](hr-er-interview-1.md#).

</td></tr><tr><td>

Start date

</td><td>

The date and start time of the interview.

</td></tr><tr><td>

End date

</td><td>

The date and end time of the interview.

</td></tr><tr><td>

Additional parties

</td><td>

Other people you want as part of the interview record.Click the **Add me** icon ![Add me icon](../image/icon-hr-add-me.png) to add yourself or the **Unlock additional parties** icon ![Unlock additional parties icon](../image/icon-hr-unlock-add-parties.png) to add yourself or other people.

 You can optionally enter the email addresses for each interviewer.

</td></tr><tr><td>

External URL

</td><td>

A URL that is relevant to the interview. For example, if your company maintains interview notes in a different or external system from HR Service Delivery, you can enter the URL to maintain a link and consistency.

</td></tr><tr><td>

Interview date

</td><td>

The date the interview took place. Appears after the interview concluded.

</td></tr><tr><td>

Created by

</td><td>

The user that created the interview invite record.

</td></tr><tr><td>

Interview notes

</td><td>

Notes from the interview or you can enter the answers to the questions from the interview question templates.

</td></tr></tbody>
</table>6.  Select the **Questions** button at the top, right corner to view, and select questions from an interview template.

    Interview templates ensure consistency and efficiency when conducting interviews. For more information, see [Create an interview question template](hr-er-interview-1.md#).

7.  If an interview template appears, select it and you can select **Copy to clipboard** or **Insert to notes**.

    **Note:** **Copy to clipboard** copies the questions from the interview template and allows you to paste it to an external document. **Insert to notes** copies all questions to the **Interview notes** field.

8.  Select **Save** or **Submit**.

    If you select **Save**, the Evidence related list appears. For more information, see [Evidence Management for Employee Relations](hr-er-evidence-mgmt.md#).


### Schedule an interview in HR Service Delivery Employee Relations using Agent Workspace for HR Case Management

Use HR Service Delivery Agent Workspace to capture a record of an interview.

#### Before you begin

Role required: sn\_hr\_er.case\_writer

#### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Select the **Lists** icon \(![Lists icon](../image/agent-ws-hr-list-icon.png)\).

3.  Select **Other**.

4.  Select **Employee Relations Cases**.

5.  Select an ER case.

6.  Select **more** from the row of tabs below the **Case Timeline**.

7.  Select **Interviews**.

8.  Select **New**.

9.  Fill in the form.

<table id="simpletable_bhv_s5z_4pb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

he number identifying the interview record. The application automatically assigns interview numbers.

</td></tr><tr><td>

HR case

</td><td>

he HR ER case number associated with the interview.**Note:** If you access the interview from **Employee Relations**, you have to select an HR case to associate the interview to.

</td></tr><tr><td>

Interviewee

</td><td>

Name of the person who you are interviewing.Select the **Lookup using list** icon ![Lookup using list icon](../image/magnifying-glass.png) and search for the person you are interviewing. If no names appear, you can create an involved party. For more information, see [Create an involved parties record](../task/hr-er-involved-parties.md).

</td></tr><tr><td>

Interviewers

</td><td>

Names of the people who conducted the interview.Click inside the field and a list of names appear that you can select.

**Note:** Only members with the sn\_interview\_temp.writer role or belong to a group that has the Employee Relations skill.

</td></tr><tr><td>

External attendees

</td><td>

Indicates you want to add external attendees to the interview record.

</td></tr><tr><td>

External invite email

</td><td>

The email addresses of the external attendees.Only appears when you select the **External attendees** choice.

**Note:** Separate each email address with a comma.

</td></tr><tr><td>

Scheduling method

</td><td>

The method you are using to schedule the interview. Select **Manual entry** to select the Start and End dates and times of the interview.

 If your company uses the integration with Microsoft Outlook Calendar to schedule, select **Calendar**. You can schedule an interview with an interface that syncs with your company's Outlook Calendar. For more information, see [Using Interview Management](hr-er-interview-1.md#).

</td></tr><tr><td>

Start date

</td><td>

The start date and time of the interview.Select the **Show calendar** icon \(![Show calendar icon](../image/hr-ws-show-calendar-icon.png) and select the date and time the interview starts.

</td></tr><tr><td>

End date

</td><td>

The endt date and time of the interview.Select the **Show calendar** icon \(![Show calendar icon](../image/hr-ws-show-calendar-icon.png) and select the date and time the interview ends.

</td></tr><tr><td>

Additional parties

</td><td>

Other people you want as part of the interview record.Click in the field and a list of names appears.

 You can optionally enter the email addresses for each interviewer.

**Note:** These names appear from

</td></tr><tr><td>

External URL

</td><td>

A URL that is relevant to the interview.

</td></tr><tr><td>

Created by

</td><td>

The user name of the person who created the interview record.

</td></tr><tr><td>

Interview notes

</td><td>

Notes from the interview or you can enter the answers to the questions from the interview question templates.In the Contextual Sidebar, select the **Interview Templates** icon \(![Interview template icon](../image/hr-ws-int-temp-icon.png) to search for interview question templates.

 ![HR Agent Workspace - Interview Template](../image/agent-ws-hr-er-int-temp.png)

 Interview templates provide questions you can use in the interview, You can insert the questions from the template into the **Interview notes** field or copy to the clipboard to insert in an outside document.

 ![HR Agent Workspace - Interview templates](../image/agent-ws-hr-er-interview.png)

 Select ![Interview Template icon](../image/hr-ws-int-temp-icon2.png) to see the Insert to notes or Copy to clipboard choices.

 Interview templates ensure consistency and efficiency when conducting interviews. For more information, see [Create an interview question template](hr-er-interview-1.md#).

</td></tr></tbody>
</table>10. Select **Save**.


