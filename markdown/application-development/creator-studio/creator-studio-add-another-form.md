---
title: Add more forms to an app in Creator Studio
description: Add as many forms as you need to create catalog items for your app. For example, you could have an office booking app with three different forms: one for requesting parking spaces, one for requesting a desk, and one for reserving conference rooms.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Working with forms in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Add more forms to an app in Creator Studio

Add as many forms as you need to create catalog items for your app. For example, you could have an office booking app with three different forms: one for requesting parking spaces, one for requesting a desk, and one for reserving conference rooms.

## Before you begin

To add forms to an app, you must be given permission to work on the app.

## About this task

**Note:** An IT fulfillment app could already have one form for requesting hardware accessories \(such as a mouse or headphones\), and you can add a second form for requesting software applications.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that you want to add more forms to.

3.  Select to **Preview** how different forms appear in various experiences, or select the **View** or **Edit** button to view or edit the application experience.

    Select different previewing options if you want to make sure that you've selected the correct application and see how it will appear in the following formats:

    -   **Portal** \(see a preview of how it'll appear on a desktop website\)
    -   **Now Mobile** \(see a preview of how it'll appear on a mobile phone or device\)
    -   **Virtual agent** \(see a representation of how it'll appear on a chatbot interface\)

        **Note:** Your organization should have the correct plugins installed to see how the form will appear in Virtual Agent. If you're interested, ask your admin and see [Catalog builder preview topic conversation](https://www.servicenow.com/docs/access?context=catalog-builder-preview-topic&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information on previewing forms and their catalog items in Virtual Agent.

    The **View** button displays forms that have been published and doesn't explicitly create a new draft form for development. The **Edit** button takes you to a development form, for example, a new draft version of a form that's already been published.

    ![Preview how your app will look](../image/crs-portal-preview.png "Preview the app's experience")

    You can also check out a representation of how the form submissions workspace will appear by selecting the **Submissions** preview, as well as the records your app generates for it \(by selecting the **Record** preview\).

4.  Select **Add form** from **Request forms** header tab.

    ![On the Request forms tab, select the Add form button](../image/cs-forms-tab-add-form.png)

5.  Select the catalog template that you want to use to build the form from the list.

6.  Select the **Apply this template** button.

    You can select the **Preview** button to see a quick mockup of what the form will look like without any modifications.

7.  Add a form to a catalog to specify its business area.

    **Note:** You can skip this step for now and revisit it later when you have a better idea of where it fits.

    The available catalogs are configured by your admin, contact them if you don't see the one you want.

    1.  Select the **Edit button** \(![](../image/cs-edit-form-location.png)\) for the Catalogs and categories card.

    2.  Select the catalog that represents the business area the app will use.

        For example, choose a service catalog that contains software and laptop cables. Expand the carat for each catalog to see its sub-catalogs.

        ![Select the catalogs your app will use](../image/crs-add-form-to-cat.png "Select the catalog")

    3.  Select as many items in the catalogs as you need.

    4.  Select **Apply**.

    You can edit any of the app's basic settings any time after you finish creating the app. For more information, see [Creator Studio form settings](../reference/creator-studio-form-settings.md).

8.  Next, choose one or more topics to specify where the form will appear.

    Find out more about topics in [Associate a catalog item with a taxonomy topic in Employee Center](https://www.servicenow.com/docs/access?context=associate-cat-item-taxonomy-ec&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US), and more about taxonomy, which is a categorization method, in [Unified Taxonomy for Employee Center](https://www.servicenow.com/docs/access?context=config-taxonomy&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

    **Note:** You can skip this step for now and revisit it later when you have a better idea of where it fits.

    1.  Select the **Edit button** \(![](../image/cs-edit-form-location.png)\) for the Topics card.

    2.  Choose the **Taxonomy** page where you want the form to appear, such as **Employee**.

        Taxonomy is a method of categorization that Employee Center uses.

    3.  Select the topic\(s\) that represent the Employee Center areas where you want the form to appear.

        For example, choose a topic that contains technology services, and expand its carat to see each of its sub-topics.

        ![Select one or more topics for your form](../image/crs-topic-taxo.png "Select the topics where your form will appear")

    4.  Select the topics where you want the form to appear, as many as you need.

    5.  Select the **Apply** button to save your changes.

9.  Select the **Save and continue** button.


## Result

**Congrats:** Hooray! You've added another form to the app.

## What to do next

Next, you can edit the form to populate its questions and customize its layout. For more information, see [Customize your form for an app in Creator Studio](creator-studio-edit-form.md).

**Parent Topic:**[Working with forms in Creator Studio](../concept/creator-studio-work-with-forms.md)

