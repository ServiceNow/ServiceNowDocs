---
title: Forms in the classic environment
description: A form displays information from one record in a data table.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Forms in the classic environment

A form displays information from one record in a data table.

**Note:** This content pertains to the classic environment, which refers to working in lists of records and on record forms directly, not in the [Configurable Workspace interface](../../../administer/configurable-workspace/concept/workspace-landing-page.md). You can work in the classic environment with Next Experience active, or with it inactive, which is referred to as Core UI \(formerly known as UI16\).

The specific information on a form depends on the type of record displayed. Users can view and edit records in forms. Administrators can configure what appears on forms. Watch this ten-minute video for an overview of the features and functions of ServiceNow forms:User Interface \| Forms including fields, related lists, views, personalization, activity stream, attachments, formatters, following records, and other form header options.

![Form elements](../image/FormElementsUI16.png "Form elements")

<table id="tbl_FormElements"><thead><tr><th>

Form element

</th><th>

Function

</th></tr></thead><tbody><tr><td>

Form header

</td><td>

Provides navigation tools and actions related to the record.

</td></tr><tr><td>

Fields

</td><td>

Stores specific data about the record.

</td></tr><tr><td>

Sections

</td><td>

Groups related information on the form. To enable or disable form tabs, click the gear icon in the banner frame \(![Settings icon](../image/Gear_icon_Heisenberg.png)\) and toggle the **Tabbed forms** option.Users can use icons to collapse \(![collapse form section icon](../image/Hide_form_section_UI15.png)\) or expand \(![expand form section icon](../image/Show_form_section_UI15.png)\) form sections when tabbed forms are disabled. When you collapse or expand a form section, your selection is saved as a user preference. The next time you access a record that uses the same form, the same sections are collapsed or expanded.

</td></tr><tr><td>

Related links

</td><td>

Provides access to additional functions based on record type and system setup. Administrators can add related links to forms using UI actions.

</td></tr><tr><td>

Related lists

</td><td>

Displays records in other tables that have relationships to the current record.

</td></tr><tr><td>

Embedded lists

</td><td>

Allows for editing related lists without having to navigate away from the form. Changes are saved when the form is saved.

</td></tr><tr><td>

Response time indicator

</td><td>

Appears at the bottom of some forms to indicate the processing time required to display the form.

</td></tr></tbody>
</table>-   **[Form headers for UI versions](form-header-by-version.md#)**  
Core UI and UI15 each have a different form header that offers different navigation icons.
-   **[Form context menu](c_FormContextMenu.md)**  
The form context menu provides controls based on the table and user access rights. Administrators can customize some of the options available on a context menu using UI actions.
-   **[Form fields](c_FormFields.md#)**  
A field represents an individual item of data on a record.
-   **[Navigate to a record or module using a URL](../../navigation/task/navigate-using-url.md)**  
Users can navigate to a record or module directly by using a URL. This topic explains the URL schema by which the system renders pages.
-   **[Configure the activity filter](../../../administer/form-administration/task/configure-activity-filters.md#)**  
The activity formatter contains a filter that lets users select which of the available fields to show in the activity list.
-   **[Embedded lists or Related lists](c_EmbeddedLists.md)**  
Some forms may show related lists as embedded. Changes to embedded lists are saved when the form is saved.
-   **[Related lists](c_RelatedLists.md)**  
Related lists appear on forms and show records in tables that have relationships to the current record.
-   **[Edit a form](../task/t_EditingInForms.md#)**  
You can edit a record in the form view. You can also insert a record, apply a template, and cancel changes to the record.
-   **[Personalize a form](../task/t_PersonalizeAForm.md)**  
When the form personalization feature is activated, users can personalize fields to appear on a specific form view according to individual preferences. Form personalization is available in Core UI.
-   **[Add and manage attachments](../task/t_AddingAnAttachment.md)**  
You can upload a file as an attachment to an incident, a knowledge article, a change request, or to another type of record.
-   **[Configure the Next Experience email client for the Core UI](../../../administer/workspace/task/enable-next-experience-email-client-core-ui.md)**  
Access email features from the Next Experience in the Core UI.
-   **[Document Viewer](Documentviewer.md)**  
Document Viewer enables you to view documents directly in the ServiceNow AI Platform rather than having to download them.
-   **[Checklists](c_Checklists.md)**  
Checklists provide a simple way to track the progress of tasks without creating additional records. Checklists can be added to the form view of any table that extends Task \[task\].

**Parent Topic:**[Working in the classic environment](../../../get-started/servicenow-overview/concept/working-in-classic-lists-and-forms.md)

