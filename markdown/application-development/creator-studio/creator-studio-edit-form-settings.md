---
title: Edit the settings for a form in Creator Studio
description: Edit form settings if you need to change its basic attributes, such as its associated image or attachments are allowed.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Working with forms in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Edit the settings for a form in Creator Studio

Edit form settings if you need to change its basic attributes, such as its associated image or attachments are allowed.

## Before you begin

To edit the settings for a form, you must be given permission to work on the app.

## About this task

**Note:** After you create the app, its **Template** can't be edited. If you want to change it, create a new form using a different catalog template. The **Record submission table** is automatically generated, and can't be changed.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the application that contains the form you want to edit.

3.  Select to **Preview** how different forms appear in various experiences, or select the **View** or **Edit** button to view or edit the application experience.

    Select different previewing options if you want to make sure that you've selected the correct application and see how it will appear in the following formats:

    -   **Portal** \(see a preview of how it'll appear on a desktop website\)
    -   **Now Mobile** \(see a preview of how it'll appear on a mobile phone or device\)
    -   **Virtual agent** \(see a representation of how it'll appear on a chatbot interface\)

        **Note:** Your organization should have the correct plugins installed to see how the form will appear in Virtual Agent. If you're interested, ask your admin and see [Catalog builder preview topic conversation](https://www.servicenow.com/docs/access?context=catalog-builder-preview-topic&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information on previewing forms and their catalog items in Virtual Agent.

    The **View** button displays forms that have been published and doesn't explicitly create a new draft form for development. The **Edit** button takes you to a development form, for example, a new draft version of a form that's already been published.

    ![Preview how your app will look](../image/crs-portal-preview.png "Preview the app's experience")

    You can also check out a representation of how the form submissions workspace will appear by selecting the **Submissions** preview, as well as the records your app generates for it \(by selecting the **Record** preview\).

4.  Check that you're editing the correct form in your app by selecting it from the **Request forms** tab.

    ![Selection from the Request forms tab](../image/cs-request-forms-tab.png)

5.  Select the more actions icon ![](../image/cs-more-actions-icon.png).

6.  Select **Form settings**.

    ![Menu option to edit form settings](../image/cs-form-settings-menu.png "Form settings menu option")

7.  Update settings on the **General** tab.

    For details on specific form settings, see [Creator Studio form settings](../reference/creator-studio-form-settings.md).

    ![Option to hide a form](../image/cs-form-settings-hide.png "Form settings modal")

8.  Select the **Location** tab to update where the form appears in a catalog, how it's categorized, and which topics it appears for.

    1.  Select the edit icon \(![](../image/cs-edit-form-location.png)\) for the **Catalogs and categories** card.

    2.  Select the catalog that represents the business area the app will use.

        For example, you could select a service catalog that contains software and laptop cables for an IT fulfillment app.

    3.  Expand the carat for each catalog to see its sub-catalogs.

    4.  Select items in the catalogs, as many as you need.

    5.  Select the **Apply** button to save your changes.

    6.  Select the edit icon \(![](../image/cs-edit-form-location.png)\) for the **Topics** card.

    7.  Choose the **Taxonomy** page where you want the form to appear, such as **Employee**.

        Taxonomy is a method of categorization that Employee Center uses.

    8.  Select the topic\(s\) that represent the Employee Center areas where you want the form to appear.

        For example, choose a topic that contains technology services, and expand its carat to see each of its sub-topics. Find out more about topics in [Associate a catalog item with a taxonomy topic in Employee Center](https://www.servicenow.com/docs/access?context=associate-cat-item-taxonomy-ec&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US), and more about taxonomy, which is a categorization method, in [Unified Taxonomy for Employee Center](https://www.servicenow.com/docs/access?context=config-taxonomy&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

    9.  Select the topics where you want the form to appear, as many as you need.

    10. Select the **Apply** button to save your changes.

9.  Select the **Access** tab to change which roles and groups can view and submit the form.

    1.  Select the edit icon \(![](../image/cs-edit-form-location.png)\) to edit users that the form should be **Available for**.

    2.  Select the roles and groups that should have access to the form.

    3.  Select the **Apply** button to save your changes.

    4.  Select the edit icon \(![](../image/cs-edit-form-location.png)\) to edit users that the form should be **Not available for**.

    5.  Select the roles and groups that shouldn’t have access to the form.

        Work with your admin to restrict or provide access to the roles and groups for this setting in non-production and production environments. For more information, see [Administering user access for deployed Creator Studio apps](../concept/creator-studio-administering-user-access-apps.md).

    6.  Select the **Apply** button to save your changes.

10. Select **Save all settings**.


**Parent Topic:**[Working with forms in Creator Studio](../concept/creator-studio-work-with-forms.md)

