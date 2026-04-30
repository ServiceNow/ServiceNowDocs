---
title: Deleting forms and questions in Creator Studio
description: Deleting unpublished forms and questions from Creator Studio removes them completely from the ServiceNow AI Platform.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2025-10-07"
reading_time_minutes: 1
breadcrumb: [Forms in apps, Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Deleting forms and questions in Creator Studio

Deleting unpublished forms and questions from Creator Studio removes them completely from the ServiceNow AI Platform.

To delete a form or question, you must have the admin role, or be an owner or editor of the app. For details on owning and editing apps, see [Collaborating with others to build apps in Creator Studio](../reference/creator-studio-collaboration-roles.md).

If a form has been published, you can hide it to make it inactive without deleting it. Check out [Hide a form from use in the ServiceNow AI Platform in Creator Studio](../task/creator-studio-deactivate-form.md) for more information.

## Deleting forms

Deleting a form completely removes the form's record from the ServiceNow AI Platform, including from Catalog Builder.

**Note:** You can't delete the following items:

-   Forms after they’ve been published
-   Drafts of previously published forms

## Deleting questions from forms

Deleting a question from an unpublished form completely removes the record for the question from the ServiceNow AI Platform, including from Catalog Builder.

However, if you delete a question from a form that has already been published, the record for the question remains in Catalog Builder but is marked as inactive.

To delete a question from a form, select the question and the select the delete icon. You must then confirm the deletion in a modal.

![Select the delete icon to delete a question](../image/crs-delete-question.png "Deleting a form question")

-   **[Delete a form in Creator Studio](../task/crs-delete-form.md)**  
Delete an unpublished form from a Creator Studio app to remove it completely from the ServiceNow AI Platform.
-   **[Hide a form from use in the ServiceNow AI Platform in Creator Studio](../task/creator-studio-deactivate-form.md)**  
Hiding a catalog item for your app's form effectively makes the form inactive. Hidden forms are unavailable in both the app and the catalog it belongs to.

**Parent Topic:**[Working with forms in Creator Studio](creator-studio-work-with-forms.md)

