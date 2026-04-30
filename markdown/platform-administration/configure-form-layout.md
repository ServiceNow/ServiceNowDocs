---
title: Configuring the form layout
description: Administrators or users with the personalize\_form role can configure the form and related list layout.Configure form layout to change what appears on the form. You can perform tasks like changing what fields are visible, embedding lists, and adding sections and annotations.You can configure related lists to appear on forms and in hierarchical lists.Highlight form elements by displaying blocks of colored text or separators between form elements.Users can toggle annotations on a form in Core UI . The glide.ui.show\_annotations user preference controls the visibility of annotations for each user.Create sections on forms to help group related fields together.Change the place where fields split on a form by moving the split section indicators in a slushbucket.Tabbed forms offer a useful way to make forms and related lists take up less space by reducing the scrolling that must be done to navigate the form.You can embed lists within a form. When a list is embedded in a form, any changes made to the contents of the list are saved when the form is saved.You can configure the indicator for customer updates, which are changes that update sets, scripts, service catalog items, and other configuration tables track.Add a chart to a form to show your users graphical data related to the form. For example, you could show an incident SLA-related chart on the Incident form so your users can see how well service level agreements are being met.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Form configuration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring the form layout

Administrators or users with the personalize\_form role can configure the form and related list layout.

**Important:** Try configuring your forms with Form Builder instead. Form Builder has all of the Form Designer and Form Layout options. It also has other robust features that help you configure each aspect of the form. For more information, see [Accessing Form Builder](https://www.servicenow.com/docs/access?context=access-form-builder&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

**Parent Topic:**[Form configuration](basic-form-administration.md)

## Show or hide fields on a form

Configure form layout to change what appears on the form. You can perform tasks like changing what fields are visible, embedding lists, and adding sections and annotations.

### Before you begin

Role required: personalize\_form

### Procedure

1.  Navigate to a form.

2.  Click the form context menu icon \(![Context menu icon](../image/ContextMenu.png)\) and select **Configure** &gt; **Form Layout**.

3.  Using the slushbucket, select the fields and the order in which you want them to appear.

    Available items that appear in green followed by a plus \(+\) sign represent related tables. To access fields on these tables, use dot-walking.

    ![Configure the form](../image/ConfigureFormScreen.png)

    In Core UI, Form Layout is not responsible for the order of the Additional Comments and Work Notes fields. For more information on how to determine the order of these fields, see [Customize activities](c_ActivityFormatter.md#).

4.  Click **Save**.

    **Warning:** Do not add the same field to more than one section of a form unless the field displays read-only data. Having two or more instances of an editable field can cause data loss and prevent the proper functioning of UI and data policies.


### What to do next

Through form configuration, you can also add new fields to the form, which creates columns to the table that underlies the form. See [Add and customize a field in a table](../../field-administration/task/t_CreatingNewFields.md) for more information.

## Add a related list to a form

You can configure related lists to appear on forms and in hierarchical lists.

### Before you begin

Role required: personalize\_form

### About this task

Related lists display records in another table that have a relationship with the current record.

### Procedure

1.  Open the form.

2.  Click the form context menu icon and select **Configure** &gt; **Related Lists**.

3.  Using the slushbucket, select the related list to display on the form.

4.  Click **Save**.

    Related lists appear at the bottom of the form.


## Add an annotation to a form

Highlight form elements by displaying blocks of colored text or separators between form elements.

### Before you begin

Role required: personalize\_form

### Procedure

1.  Navigate to a form.

2.  Click the form context menu icon \(![Context menu icon](../image/ContextMenu.png)\) and select **Configure** &gt; **Form Layout**.

3.  Under **Form view and section**, select a section.

4.  In the Available list, double-click **\* Annotation** to move it to the **Selected** list.

    The Annotation Details section appears.

    ![Annotation details](../image/AnnotationDetails.png)

5.  Place it above the field to annotate.

6.  In Annotation Details, select the type of annotation.

    The available types of annotations include **Info Box Blue**, **Info Box Red**, **Line Separator** \(any text you add appears beneath the line\), **Section Details**, **Section Separator**, and **Text**.

    ![Form annotation types](../../workspace/image/form-annotations.png)

7.  Select either **Plain Text** or **HTML** for the data type and enter the annotation in the text box.

    All valid HTML tags are supported.

    For example, select the **Text** annotation type, the **HTML** data type, and enter `<span style="color:red">Select the primary location:</span>`. The text appears red on the form.

8.  Click **Save**.


## Toggle annotations

Users can toggle annotations on a form in Core UI . The **glide.ui.show\_annotations** user preference controls the visibility of annotations for each user.

### Before you begin

Role required: none

### Procedure

1.  Navigate to a form.

2.  Select the more options icon \(![More options icon](../image/IconUI16MoreOptions.png)\) to see the annotations icon.

    The icon is light gray and cannot be toggled when no annotations are available.


## Create a form section

Create sections on forms to help group related fields together.

### Before you begin

Role required: form\_admin

### About this task

Users can expand or collapse form sections to show or hide the fields they need. If you have tabs enabled, each form section appears on a separate tab. The default Change Request form is an example of a form with multiple sections as shown in the following image.

![Change request form sections listed in tabs](../image/ChangeFormSections.png "Change Request form sections")

### Procedure

1.  Right-click the form header and select **Configure** &gt; **Form Layout**.

2.  In the **Form view and section** area below the slushbucket, click **New** in the **Section** list.

3.  In the **Section caption** field, give the new section a title, then click **OK**.

4.  Select a form section name and click the up or down arrow to change the section order.

    **Note:** The caption for the first section on the form becomes the form title.

5.  Add fields to the new section using the slushbucket.

6.  Click **Save** when you are finished.

    The new section appears on the form with the fields you selected. If you do not add any fields to a section, the section stays empty.

    If you want to delete the form section later, do the following:

    1.  Navigate to **System UI** &gt; **Form Sections**.
    2.  Filter for the table that contains the section you want to delete. For example, the Incident table. The name of the form section to be deleted is displayed in the **Caption** field.
    3.  Select the check box beside the form section to delete, and then select **Delete** from the **Actions on selected rows** menu.
    4.  Click **OK** to confirm the deletion.

## Move form splits

Change the place where fields split on a form by moving the split section indicators in a slushbucket.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to a form.

2.  Click the form context menu icon \(![Form context menu icon](../image/ContextMenu.png)\) and select **Configure** &gt; **Form Layout**.

3.  Move any of the following split section indicators:

    -   \|- begin\_split -\|
    -   \|- split -\|
    -   \|- end\_split -\|
4.  Click **Save**.


## Display tabbed forms

Tabbed forms offer a useful way to make forms and related lists take up less space by reducing the scrolling that must be done to navigate the form.

### Before you begin

Role required: personalize\_form

### About this task

![Change request with tabbed forms](../image/TabbedForms.png "Tabbed forms")

Form sections and related lists are tabbed separately, each with their own tab line. A user always sees the first form section. All sections after that can be tabbed. Tabs are enabled by default for new instances.

Tabbed forms are enabled by default for new instances. A system user preference with the name **tabbed.forms** specifies whether the tabbed UI is used by default for all users. Users can change this preference as described in this procedure.

### Procedure

1.  Click the gear icon in the banner frame.

2.  Enable **Tabbed forms**.


## Embed a list within a form

You can embed lists within a form. When a list is embedded in a form, any changes made to the contents of the list are saved when the form is saved.

### Before you begin

Role required: personalize\_form

### About this task

This allows the embedded list to be treated just like another element on the form. In addition, users can create records in the list view. After a row is added to the list, double-click any cell in the list to edit its value. You can add the same lists to a form as embedded lists or as related lists, depending on the path selected in the form context menu.

You can also modify embedded list controls, such as the name of the related list and the roles required to create records in the embedded list.

### Procedure

1.  Select a record from the list.

2.  Right-click the form header and select **Configure** &gt; **Form Layout**.

    The slushbucket shows the available fields and the lists that can be embedded in the form. Lists appear in red at the bottom of the **Available** list.

3.  Select a list and move it to the **Selected** column.

4.  Use the up and down arrow buttons to position the list in the form.

5.  Click **Save**.

    Lists adjust to fit the frames of the adjacent fields.

    ![An embedded list of approvers on the Change Request form](../image/ListEmbeddedInAForm.png)


## Configure customer updates indicator

You can configure the indicator for customer updates, which are changes that update sets, scripts, service catalog items, and other configuration tables track.

### Before you begin

Role required: admin

### About this task

The customer updates indicator icon \(![Customer updates indicator icon](../image/CustomerUpdateIndicator.png)\) may appear on the header of forms that have customer updates. Clicking the customer updates indicator opens the update set records for the item.

You can configure this indicator to appear for all or for specific administrators using the **owned\_by\_indicator.form** user preference.

### Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **User Preferences**.

2.  Perform one of the following actions.

<table id="choicetable_o2r_v2r_3r"><tbody><tr><td id="d267711e1109">

**Enable the indicator for all administrators**

</td><td>

Set the **owned\_by\_indicator.form** preference to **true**.

</td></tr><tr><td id="d267711e1124">

**Enable the indicator for an individual administrator**

</td><td>

1.  Make sure the **owned\_by\_indicator.form** system user preference is set to **false**.
2.  Create a user preference with the following values:
    -   **Name:** `owned_by_indicator.form`
    -   **User:** Select the administrator for which to enable the preference.
    -   **Value:** `true`


</td></tr></tbody>
</table>
## Add a chart to a form

Add a chart to a form to show your users graphical data related to the form. For example, you could show an incident SLA-related chart on the Incident form so your users can see how well service level agreements are being met.

### Before you begin

Role required: personalize\_form

### About this task

**Note:** The following report types are not supported on forms: List, Pivot, Multilevel Pivot, Calendar, and Single Score.

![Chart on the Incident form](../image/ChartOnAForm.png "Chart on a form")

### Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Forms**.

2.  Select the form you want to configure.

3.  Click the form context menu icon \(![Form context menu icon](../image/ContextMenu.png)\) and select **Configure** &gt; **Form Layout**.

4.  Using the slushbucket, select **\* Chart**.

5.  Enter a **Label** in the chart details.

6.  Click **Save** to return to the form.

7.  Click **Configure chart**.

8.  Select a chart in the **Report** field and configure other options as desired.

9.  Click **Update**.


