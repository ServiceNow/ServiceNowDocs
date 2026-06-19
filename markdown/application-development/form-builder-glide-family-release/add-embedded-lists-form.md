---
title: Add embedded lists in Table Builder
description: Add an embedded list using Table Builder to display data for a selected related list on your form. A related list shows the records in the tables that have relationships to the current record. For example, for a form view that references a Problem table, you might want to display a list of locations that are impacted by a selected problem.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/form-builder-glide-family-release/add-embedded-lists-form.html
release: zurich
product: Form Builder \(Glide Family Release\)
classification: form-builder-glide-family-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Forms in Table Builder, Using Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Add embedded lists in Table Builder

Add an embedded list using Table Builder to display data for a selected related list on your form. A related list shows the records in the tables that have relationships to the current record. For example, for a form view that references a Problem table, you might want to display a list of locations that are impacted by a selected problem.

## Before you begin

**Note:** Embedded lists are only supported in Core UI and earlier.

-   Launch Table Builder. For more information, see [Accessing Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/form-builder-glide-family-release/accessing-form-builder.md).
-   \(Optional\) Choose a domain to work within \(if not global\). For more information, see [Domain separation and Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/form-builder-glide-family-release/form-builder-domain-separation.md).
-   \(Optional\) Choose an application scope to work within \(if not global\). For more information, see [Using an application scope with Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/form-builder-glide-family-release/fb-application-scope.md).

**Note:** To understand how to approach customizing your forms, review [Table Builder workflow and navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/form-builder-glide-family-release/form-builder-workflow.md).

Role required: personalize\_form or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-studio/aes-app-dev-workflow.md).

## Procedure

1.  Navigate to the **Forms** tab in Table Builder.

2.  Choose a view to work with.

    For detailed information on how to choose a view for a form, see [Choose a form view in Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/form-builder-glide-family-release/manage-form-views.md).

3.  To display a list of the embedded lists that you can add to your form view, in the Add form elements panel, select **Embedded lists**.

    **Note:** You can also launch the Add form elements panel by clicking the Add \(\[Omitted image "fb-add-icon.png"\] Alt text: Add icon.\) icon above an existing element in the form editor.

4.  Select an embedded list, and then drag it to the location in the form editor where you'd like to place it.

    **Note:** Embedded lists in forms are only supported in Core UI and earlier interfaces.

    For information on how you can add an embedded list to a form, see Embed a list within a form.

5.  Select **Save**.


**Parent Topic:**[Forms in Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/form-builder-glide-family-release/form-view-configuration.md)

