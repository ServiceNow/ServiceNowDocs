---
title: CSM Configurable Workspace form templates
description: Create and edit form templates for use in CSM Configurable Workspace and then use the templates to automatically populate fields on records.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# CSM Configurable Workspace form templates

Create and edit form templates for use in CSM Configurable Workspace and then use the templates to automatically populate fields on records.

Form templates simplify the process of creating and submitting new records by populating fields with selected values. In CSM Configurable Workspace, form templates are available in the Templates tab in the contextual side panel. From the Templates tab, you can do the following:

-   View template cards that display information including the template name, description, and when the template was last used.
-   View different lists of templates, including Favorites, My Templates, and All.
-   Mark templates as Favorites by selecting the star icon on the template card.
-   Sort the available templates alphabetically or by last used.
-   Create a new template by selecting the Create icon \(**+**\) at the top of the Templates tab.
-   Edit an existing template by selecting the More actions icon on the template card and then selecting **Edit**.

## Templates tab

The Templates tab in the contextual side panel includes form templates that are available to the current user. This tab includes three lists of templates:

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

## Using form templates to create comments and work notes

You can create and use form templates that add content to the **Additional comments** and **Work notes** fields on a case record and then post that content to the activity stream. Selecting a template displays a modeless dialog with the template content. For more information, see [Modeless dialogs](csm-front-line-case-page-modeless-dialogs.md#section_gzj_wlb_s2c).

