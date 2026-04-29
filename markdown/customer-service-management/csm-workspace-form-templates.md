---
title: CSM Configurable Workspace form templates
description: Create and edit form templates for use in CSM Configurable Workspace and then use the templates to automatically populate fields on case and interaction records.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM Configurable Workspace form templates

Create and edit form templates for use in CSM Configurable Workspace and then use the templates to automatically populate fields on case and interaction records.

Form templates simplify the process of creating and submitting new records by populating fields with selected values. In CSM Configurable Workspace, form templates are available in the Templates tab in the contextual side panel.

Form templates include advanced capabilities that let you control when and how they work. You can set conditions to show templates only for specific cases, choose which fields to populate based on the situation, insert variables that automatically fill in with customer information, and add pre-written emails. These capabilities help you create one flexible template instead of maintaining multiple similar templates.

**Note:** Form templates are available in two versions: basic and advanced. The advanced version is enabled by default for case and interaction records in CSM Configurable Workspace. The basic version is used in the Core UI and for records other than cases and interactions.

From the **Templates** tab, you can do the following:

-   View template cards that display information including the template name, description, and when the template was last used.
-   View different lists of templates, including **Favorites**, **My Templates**, and **All**.
-   Mark templates as Favorites by selecting the star icon on the template card.
-   Sort the available templates alphabetically or by last used.
-   Create a new template by selecting the Create icon \(**+**\) at the top of the **Templates** tab.
-   Edit an existing template by selecting the More actions icon on the template card and then selecting **Edit**.

## Templates tab

The **Templates** tab in the contextual side panel includes form templates that are available to the current user. This tab includes three lists of templates:

-   **Favorites**: Templates that the user has marked as a favorite by selecting the star icon on the template card. The templates that are added to this list are accessible across different records.
-   **My Templates**: Templates created by the user.
-   **All**: All templates available to the user.

Within each list of templates, users can do the following:

-   Search for templates by entering a keyword in the search box.
-   Sort the available templates, either last used or alphabetically, by making a selection from the drop-down menu.

![CSM Configurable Workspace templates tab in the contextual side panel displays available templates to the user](../image/csm-form-templates-template-tab.png "Templates tab with template cards")

## Template cards

The Templates tab displays a card for each template in a list. These cards provide information about the templates, including:

-   A multi-line description of the template.
-   A timestamp that shows when the template was last used.
-   A star icon that you can use to mark a template as a favorite.
-   A preview icon to review template before applying.
-   An **Apply** button to apply the template to the current record.

## Template form

The template form is used to create and edit templates. This form includes two collapsible form sections:

-   **Details**: Includes information about the template, such as the template name and the table that the template applies to.
-   **Template**: Includes the selected fields and the configured values for those fields which are applied to a record.

![Create New Template form with the Details section collapsed. The Templates section includes a numbered row for each field and value added to the template.](../image/csm-form-templates-create-new.png "Template form")

The Template section includes a row for each field that has been added to the template. These rows are numbered for readability and easy reference. The fields and configured values in each row are also labeled for readability.

-   **Field**: The field to update on the record.
-   **Update to**: The value to use for that field.

The template form is available when creating a new template from a case or interaction or editing an existing template. The template form tab header displays a description of the current action:

-   **Create new template**: The system displays this tab header when you create a template.
-   **Edit template**: The system displays this tab header when you save the changes to a new template or when you edit a template.

## Advanced form template capabilities

Form templates in CSM Configurable Workspace support advanced capabilities that give users more control over when and how templates work. Use these capabilities to create flexible templates that adapt to different situations.

Advanced capabilities include:

-   Template-level conditions
-   Field-level conditions
-   Placeholder variables
-   Email templates

**Note:** When you add any advanced capability \(template-level conditions, field-level conditions, placeholder variables, or email templates\) to a template, that template will not work in Core UI. Advanced capabilities are only available in CSM Configurable Workspace.

## Template-level conditions

Template-level conditions control which cases show your template in the Templates list.

**How to use:** Select **Set conditions** under Template Condition. In the Set conditions dialog, select a field, choose an operator, and enter a value. Add multiple conditions using **AND** or **OR** buttons. For example: **\[Account is XYZ\]** **\[AND\]** **\[State is Open\]**. Select **Set** to save.

Templates that do not meet the conditions do not appear in Templates list. The template only appears for records matching these conditions. Start with template-level conditions before adding field-level conditions, and document complex conditions in the template description.

![set conditions dialog](../image/csm-form-templates-set-conditions.png "Set conditions dialog box")

## Field-level conditions

Field-level conditions control which fields populate when a template is applied, creating one flexible template instead of multiple similar ones.

**How to use:** When adding fields to a template, click the filter icon next to a field. In the Set Conditions dialog, select a field, operator, and value. Use **AND** or **OR** for multiple conditions. Select **Set** to save. Fields without conditions populate every time. Fields with conditions populate only when the condition is met. The conditions appear as pills in the Details section with an **Edit conditions** link.

Example: A template has 10 fields. The **Assigned Team** is set to populate only when **Category** = **Technical**. For billing cases, 9 fields populate \(Assigned Team doesn't\). For technical cases, all 10 fields populate.

## Placeholder variables

Placeholder variables are special codes that the system automatically replaces with real information when you apply a template.

**How to use:** When creating a template, click in a text field and select the variable picker icon. Browse available variables \(all start with $ like *$customer.name*, *$case.number*, *$case.short\_description*\). Select a variable to insert it. When you apply the template, the system replaces variables with actual data from the case or interaction. Use variables for repetitive personalization, but avoid overuse that makes content feel generic. Test variable output to verify correct display.

Example: Template text "Hi *$customer.name*, thank you for contacting us about case *$case.number* regarding *$case.short\_description*" becomes "Hi Sarah Johnson, thank you for contacting us about case CS0012345 regarding login problems."

## Email templates

Email templates let users add pre-written email content to a template. When the template is applied to a case or interaction, a formatted email draft appears in the **Email** tab.

**How to use:** In the Email \(optional\) section, type your message in the Rich Text Editor \(use toolbar for formatting\). Select the variable picker to insert variables. Use **Content Placement** to choose how content is inserted:

-   **None**
-   **Replace existing text**
-   **Insert before existing text**
-   **Insert after existing text**
-   **Insert at cursor**

Save the template. When you apply the template, the email draft appears with variables resolved. The system creates the email as a draft only and does not automatically send. If you reapply the template, the system replaces the existing email draft. When previewing a template, you can view both dynamic placeholders \(*$variable*\) and their resolved values. Review the email, make any necessary edits, and select **Send**.

![email variable picker](../image/csm-form-template-email-variable-picker.png "Email variable picker")

Example: A "Password Reset" template with email content displays as "Dear Sarah Johnson, we received your password reset request for case CS0012345.

## Applying templates

Templates appear in the Templates list when you open a case or interaction that matches the template conditions. For example, a template with conditions "Account is XYZ AND State is Open" only appears when a record has those values.

To apply a template:

1.  **Select a template:** Choose a template from the Templates list.
2.  **Preview \(optional\):** Select the preview icon on the template card to review template details.
3.  **Apply:** Select **Apply**. Fields populate with template values. If you attempt to reapply a template to the same record, the system displays an alert warning that existing values may be overwritten.
4.  **Verify:** Updated fields show a black dot \(●\) next to their labels. The form displays "Unsaved" at the top.
5.  **Save:** Review the changes and select **Save** to save the record.

**To undo:** Select **Undo** in the Templates panel before saving.

Example: A case has **Account = XYZ** **and** **State = Open**. The template "State is Open and Account is XYZ - More info Needed" appears in the Templates list. After applying **Channel**, **Priority**, and **Assignment group** fields show dots \(●\) indicating updates. The changes are reviewed and saved.

## Adding comments, work notes, and email with templates

You can create and use form templates that add content to the **Additional comments** and **Work notes** fields on a case or interaction and then post that content to the activity stream. Selecting a template displays a modeless dialog with the template content. For more information, see [Modeless dialogs](csm-front-line-case-page-modeless-dialogs.md#section_gzj_wlb_s2c).

**Using template email content:** When a template is applied that includes email content, an email draft appears in the Email tab. Select the **Email** tab to view the draft. The **To**, **Cc**, and **Subject** fields are populated based on case information. Review the email, make any edits if needed, and select **Send**.

