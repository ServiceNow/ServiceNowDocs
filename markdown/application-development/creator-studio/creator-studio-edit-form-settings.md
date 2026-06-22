---
title: Edit the settings for a form in Creator Studio
description: Edit form settings if you need to change its basic attributes, such as its associated image or attachments are allowed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/creator-studio/creator-studio-edit-form-settings.html
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Forms in apps, Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Edit the settings for a form in Creator Studio

Edit form settings if you need to change its basic attributes, such as its associated image or attachments are allowed.

## Before you begin

To edit the settings for a form, you must be given permission to work on the app.

## About this task

**Note:** After you create the app, its **Template** can't be edited. If you want to change it, create a new form using a different catalog template.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the application that contains the form you want to edit.

3.  Select the form you want to work on in the navigation panel.

    If you have multiple forms, make sure to select the form you want to edit settings for.

    \[Omitted image "crs-forms-select-multi.png"\] Alt text: Select the appropriate form from the navigation panel

4.  Select the more actions icon \[Omitted image "cs-more-actions-icon.png"\] Alt text:.

5.  Select **Form settings**.

    \[Omitted image "crs-form-settings-menu.png"\] Alt text: Menu option to edit form settings

6.  Update settings on the **General** tab.

    For details on specific form settings, see [Creator Studio form settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/creator-studio/creator-studio-form-settings.md).

    \[Omitted image "cs-form-settings-hide.png"\] Alt text: Option to hide a form

7.  Select the **Location** tab to update where the form appears in a catalog, how it's categorized, and which topics it appears for.

    1.  Select the edit icon \(\[Omitted image "cs-edit-form-location.png"\] Alt text:\) for the **Catalogs and categories** card.

    2.  Select the catalog that represents the business area the app will use.

        For example, you could select a service catalog that contains software and laptop cables for an IT fulfillment app.

    3.  Expand the caret for each catalog to see its sub-catalogs.

    4.  Select items in the catalogs, as many as you need.

    5.  Select the **Apply** button to save your changes.

    6.  Select the edit icon \(\[Omitted image "cs-edit-form-location.png"\] Alt text:\) for the **Topics** card.

    7.  Choose the **Taxonomy** page where you want the form to appear, such as **Employee**.

        Taxonomy is a method of categorization that Employee Center uses.

    8.  Select the topic\(s\) that represent the Employee Center areas where you want the form to appear.

        For example, choose a topic that contains technology services, and expand its carat to see each of its sub-topics. Find out more about topics in [Associate a catalog item with a taxonomy topic in Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/service-catalog/associate-cat-item-taxonomy-ec.md), and more about taxonomy, which is a categorization method, in [Unified Taxonomy for Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/employee-experience-foundation/config-taxonomy.md).

    9.  Select the topics where you want the form to appear, as many as you need.

    10. Select the **Apply** button to save your changes.

8.  Select the **Access** tab to change which roles and groups can view and submit the form.

    1.  Select the edit icon \(\[Omitted image "cs-edit-form-location.png"\] Alt text:\) to edit users that the form should be **Available for**.

    2.  Select the roles and groups that should have access to the form.

    3.  Select the **Apply** button to save your changes.

    4.  Select the edit icon \(\[Omitted image "cs-edit-form-location.png"\] Alt text:\) to edit users that the form should be **Not available for**.

    5.  Select the roles and groups that shouldn’t have access to the form.

        Work with your admin to restrict or provide access to the roles and groups for this setting in non-production and production environments. For more information, see [Administering user access for deployed Creator Studio apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/creator-studio/creator-studio-administering-user-access-apps.md).

    6.  Select the **Apply** button to save your changes.

9.  Select **Save all settings**.


## Result

The form's settings are updated. Remember: You just updated the settings for the form you selected, not for all of the app's forms if it has multiple.

**Parent Topic:**[Working with forms in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/creator-studio/creator-studio-work-with-forms.md)

