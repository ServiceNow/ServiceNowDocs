---
title: Evidence Management for Employee Relations
description: Use Evidence Management to capture and categorize evidence for Employee Relations or related cases.Set up HR Service Delivery Management so your agents can collect evidence and information related to Employee Relation \(ER\) cases.Create evidence types to catalog and organize employee relation evidence in an efficient and logical way to enhance your business processes.You can create, edit, and categorize evidence related to an employee relations case using the Core UI or HR Service Delivery Agent Workspace.Create evidence records to attach to an Employee Relations case to help with investigations.Create evidence records to attach to an Employee Relations case to help with investigations using HR Service Delivery Agent Workspace.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Setting up Employee Relations, Employee Relations cases, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Evidence Management for Employee Relations

Use Evidence Management to capture and categorize evidence for Employee Relations or related cases.

Evidence is defined as any digital artifacts gathered as part of an investigation, like files that are either uploaded to Evidence Management or reside in another system.

## Setting up Evidence Management

Set up HR Service Delivery Management so your agents can collect evidence and information related to Employee Relation \(ER\) cases.

You can activate Evidence Management \[com.sn\_evidence\_management\] plugin if you have the admin role. This plugin activates when the Human Resources Scoped App: Employee Relations \[com.sn\_hr\_employee\_realtions\] plugin is activated. For more information, see [Activate Employee Relations](../task/activate-hr-employee-relations.md#).

### Roles

The following roles are installed with the Evidence Management \[com.sn\_evidence\_management\] plugin:

<table id="table_v2h_p2t_lbc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Evidence admin \[sn\_em.admin\]

</td><td>

Can access and configure all areas within Evidence Management.

</td><td>

-   sn\_em.evidence\_config\_manager
-   sn\_em.evidence\_reader
-   sn\_em.evidence\_writer

</td></tr><tr><td>

Evidence Configuration manager \[sn\_em.evidence\_config\_manager\]

</td><td>

Can access, create, and manage evidence type records.**Note:** requires the evidence reader and writer roles to manage the evidence type records.

</td><td>

 

</td></tr><tr><td>

Evidence reader \[sn\_em.evidence\_reader\]

</td><td>

Can view evidence if the ER case is accessible.

</td><td>

 

</td></tr><tr><td>

Evidence writer \[sn\_em.evidence\_writer\]

</td><td>

Can create and manage evidence records.

</td><td>

sn\_em.evidence\_reader

</td></tr></tbody>
</table>Employee Relations roles include Evidence Management roles.

Users are unable to read evidence when impersonating.

When an Employee Relations case is restricted, users can only view the evidence record if they can view the ER case.

### Evidence types

Before you can add evidence to an ER case, you must set up evidence types. Evidence types help you categorize and organize the evidence you collect related to ER cases. The base system provides:

-   Audio
-   Chat logs
-   Email
-   Photos
-   Screenshots
-   SMS
-   Video

You can create additional evidence types. For more information, see [Create evidence types](hr-er-evidence-mgmt.md#).

### Create evidence types

Create evidence types to catalog and organize employee relation evidence in an efficient and logical way to enhance your business processes.

#### Before you begin

Role required: sn\_em.evidence\_config\_manager

**Note:** The base system provides preconfigured evidence types.

#### Procedure

1.  Navigate to **All** &gt; **Evidence Management** &gt; **Evidence Types**.

2.  Select **New**.

3.  Fill in the form or edit the fields.

    |Field|Value|
    |-----|-----|
    |**Name**|The name that identifies and describes the evidence type.|
    |**Active**|Indicates if the evidence type is active and available for use.|

4.  Select **Submit**.


## Using Evidence Management

You can create, edit, and categorize evidence related to an employee relations case using the Core UI or HR Service Delivery Agent Workspace.

You can associate evidence to an Employee Relations \(ER\) case. For more information on ER cases, see [Employee Relations cases](hr-case-employee-relations.md).

### Adding evidence to an Employee Relations case in the legacy UI

Create evidence records to attach to an Employee Relations case to help with investigations.

#### Before you begin

Role required: sn\_hr\_er.case\_writer

#### Procedure

1.  Navigate to **All** &gt; **Employee Relations** &gt; **Cases**.

2.  Select a case.

3.  Scroll down to the **Evidence** tab in the related list.

4.  Select **New**.

5.  Fill in the form.

<table id="simpletable_ywj_rhh_ppb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The number that identifies the evidence record. This is automatically generated by the application.

</td></tr><tr><td>

Name

</td><td>

The name that describes the evidence.

</td></tr><tr><td>

Evidence type

</td><td>

The evidence type associated with the evidence. The base system provides the following:

-   Audio
-   Chat logs
-   Email
-   Photos
-   Screenshots
-   SMS
-   Video
 For more information, see [Create evidence types](hr-er-evidence-mgmt.md#).

</td></tr><tr><td>

Created by

</td><td>

Name of the user that created the evidence record.

</td></tr><tr><td>

Submitted by involved party

</td><td>

Name of the person who submitted the evidence.Select the **Lookup using list** icon ![Lookup using list icon](../image/magnifying-glass.png) and search for the person that submitted the evidence.

 If no names appear, you can select **New** and create an involved party. For more information, see [Create an involved parties record](../task/hr-er-involved-parties.md).

</td></tr><tr><td>

Involved parties

</td><td>

Any person involved with the evidence provided in the ER case.Select the **Unlock involved parties** icon \(![Unlock involved parties icon](../image/icon-hr-unlock-add-parties.png)\) and search for people you want to include as involved parties.

 If no names appear, you can select **New** and create an involved party. For more information, see [Create an involved parties record](../task/hr-er-involved-parties.md).

</td></tr><tr><td>

Table

</td><td>

The table evidence is associated with. The default is the Employee Relations Case \[sn\_hr\_er\_case\] table, but you can associate evidence to any table.

</td></tr><tr><td>

Parent

</td><td>

The parent case the evidence is related to.To associate a parent case, select the **Lookup documents using list** icon ![Lookup documents using list icon](../image/magnifying-glass.png) and select the table associated with the parent case. The default is the Employee Relations Case \[sn\_hr\_er\_case\] table.

 Select the table and the associated case that is the parent case.

**Note:** If you have a parent case and evidence is added to it, this field is pre-populated.

</td></tr><tr><td>

Evidence source type

</td><td>

Indicates if the evidence is an attachment or a URL.Select one. If the evidence is an attachment, attach the file using the Manage Attachments icon \(![Manage attachments icon](../image/attach-icon.png)\) at the top, right of the form.

 If the evidence is a URL, enter the URL in the URL source field.

</td></tr><tr><td>

URL source

</td><td>

Select the Edit this URL icon \(![Edit this URL icon](../image/icon-hr-unlock-add-parties.png) and enter the URL.This field displays only when you select **URL** from the Evidence source type field.

</td></tr><tr><td>

Interview

</td><td>

The associated interview number. If you came from the interview record, the number automatically displays.

 For more information, see [Interview Management](hr-er-interview-1.md#).

</td></tr><tr><td>

Description

</td><td>

Description of the evidence.

</td></tr></tbody>
</table>6.  Select **Submit**.


### Add evidence to an Employee Relations case in Agent Workspace for HR Case Management

Create evidence records to attach to an Employee Relations case to help with investigations using HR Service Delivery Agent Workspace.

#### Before you begin

Role required: sn\_hr\_er.case\_writer

#### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Select the **Lists** icon \(![Lists icon](../image/agent-ws-hr-list-icon.png)\).

3.  Select **Other**.

4.  Select **Employee Relations Cases**.

5.  Select an ER case you want to attach evidence to.

6.  Select **more** from the row of tabs below the **Case Timeline**.

7.  Select **Evidence** from the row of tabs below the **Case Timeline**.

8.  Select **New**.

9.  Fill in the form.

<table id="simpletable_qqj_v2h_ppb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The number that identifies the evidence record. This is automatically generated by the application.

</td></tr><tr><td>

Name

</td><td>

The name that describes the evidence.

</td></tr><tr><td>

Evidence type

</td><td>

The evidence type associated with the evidence.The base system provides the following:

-   Audio
-   Chat logs
-   Email
-   Photos
-   Screenshots
-   SMS
-   Video
 For more information, see [Create evidence types](hr-er-evidence-mgmt.md#).

</td></tr><tr><td>

Created by

</td><td>

Name of the user that created the evidence record.

</td></tr><tr><td>

Submitted by involved party

</td><td>

Name of the person who submitted the evidence.Select the **Search for Record** icon ![Search for record icon](../image/magnifying-glass.png) and search for the person that submitted the evidence.

 If no names appear, you can select **New** and create an involved party. For more information, see [Create an involved parties record](../task/hr-er-involved-parties.md).

</td></tr><tr><td>

Involved parties

</td><td>

Any person involved with the evidence provided in the ER case.Click into the field and a list of involved parties appears.

 If no names appear, you have to create an involved party record. For more information, see [Create an involved parties record](../task/hr-er-involved-parties.md).

</td></tr><tr><td>

Table

</td><td>

The table evidence is associated with. The default is the Employee Relations Case \[sn\_hr\_er\_case\] table, but you can associate evidence to any table.

</td></tr><tr><td>

Parent

</td><td>

The parent case the evidence is related to.To associate a parent case, select the **Lookup documents using list** icon ![Lookup documents using list icon](../image/magnifying-glass.png) and select the table associated with the parent case. The default is the Employee Relations Case \[sn\_hr\_er\_case\] table.

 Select the table and the associated case that is the parent case.

**Note:** If you have a parent case and evidence is added to it, this field is pre-populated.

</td></tr><tr><td>

Evidence source type

</td><td>

Indicates if the evidence is an attachment or a URL.Select one of the following:

-   Attachment
-   URL
If the evidence is an attachment, select **Browse** from Attachments on the right and attach the file.

 If the evidence is a URL, enter the URL in the **URL source** field.

</td></tr><tr><td>

URL source

</td><td>

Select the Edit this URL icon \(![Edit this URL icon](../image/icon-hr-unlock-add-parties.png) and enter the URL.This field displays only when you select **URL** from the Evidence source type field.

</td></tr><tr><td>

Interview

</td><td>

The associated interview number. If you came from the interview record, the number automatically displays.

 If no interview number appears, click into the field and you can select one.

 For more information, see [Interview Management](hr-er-interview-1.md#).

</td></tr><tr><td>

Description

</td><td>

Description of the evidence.

</td></tr></tbody>
</table>10. Select **Save**.


