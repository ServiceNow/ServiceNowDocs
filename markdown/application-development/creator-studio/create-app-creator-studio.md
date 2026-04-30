---
title: Create the foundation of an app in Creator Studio
description: Before you can build out an app for people to use, you must create its foundation. Eventually, you'll have to customize the default values, but in the following procedure you'll select a catalog template for your first form and specify basic info for the app you're building in Creator Studio.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [App creation in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Create the foundation of an app in Creator Studio

Before you can build out an app for people to use, you must create its foundation. Eventually, you'll have to customize the default values, but in the following procedure you'll select a catalog template for your first form and specify basic info for the app you're building in Creator Studio.

## Before you begin

If you don't have permission to create an app, you can request that a teammate create one for you. For more information, see [Ask an admin to create an app for you in Creator Studio](creator-studio-request-app-added.md).

Your administrator must add you to the Creator Studio Users group.

## Procedure

1.  Let's open Creator Studio. On your instance, select the **All** tab.

    ![The All menu lets you see all the apps on your instance](../image/cs-all-menu.png "All tab")

    This tab lets you see all the apps installed on your instance.

2.  In the white text field, enter `App Engine`.

    The list of apps displayed underneath the text box now pertains only to App Engine.

3.  In the list, select **Creator Studio**.

    That's how you open Creator Studio! You've landed on its home page. Under **Apps**, you see all the apps that people already created.

4.  Select **Create app** to begin your journey.

    -   If you're a system administrator, you can read more about this topic in [Application collaboration](../../applications/concept/application-collaboration.md).
    -   If you want to know how to request an admin to create the app for you, check out [Ask an admin to create an app for you in Creator Studio](creator-studio-request-app-added.md).
5.  Fill in the fields on the modal that pops up.

    ![Enter details to create the app](../image/cs-create-app-modal.png "Create an app")

    1.  Give your app a **Name**, which should be descriptive and intuitive.

    2.  Describe what your app does in the **Description**.

        For example, `This app enables a person to request office equipment.`

    3.  Select **Advanced settings** and confirm that your app's name and tables are unique by specifying the **Scope**.

        For more advanced information about scopes, see [Application scope](../../applications/concept/c_ApplicationScope.md).

    4.  Select **Create app**.

    Okay, you've created the beginning of your very own application! You've named and described it. A list of catalog templates appears.

6.  Select a catalog template from the list, which your admin can customize.

    You may not see a catalog template that is exactly what you want. So, choose one that's the closest. If none look close, select the **Creator Studio Default Template** option, if your admin hasn't removed it. It's your best bet.

    **Tip:** Feel free to click through the list of catalog templates. Previews will help you pick the one you want.

    Don't worry if you don't see other catalog templates to choose from! Your admins may not have created any custom catalog templates for you yet.

7.  Select **Apply this template**.

8.  Add a form to a catalog to specify its business area.

    **Note:** You can skip this step for now and revisit it later when you have a better idea of where it fits.

    The available catalogs are configured by your admin, contact them if you don't see the one you want.

    1.  Select the **Edit button** \(![](../image/cs-edit-form-location.png)\) for the Catalogs and categories card.

    2.  Select the catalog that represents the business area the app will use.

        For example, choose a service catalog that contains software and laptop cables. Expand the carat for each catalog to see its sub-catalogs.

        ![Select the catalogs your app will use](../image/crs-add-form-to-cat.png "Select the catalog")

    3.  Select as many items in the catalogs as you need.

    4.  Select **Apply**.

    You can edit any of the app's basic settings any time after you finish creating the app. For more information, see [Creator Studio form settings](../reference/creator-studio-form-settings.md).

9.  Next, choose one or more topics to specify where the form will appear.

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

10. Select **Save and continue**.

11. Select to **Preview** how different forms appear in various experiences, or select the **View** or **Edit** button to view or edit the application experience.

    Select different previewing options if you want to make sure that you've selected the correct application and see how it will appear in the following formats:

    -   **Portal** \(see a preview of how it'll appear on a desktop website\)
    -   **Now Mobile** \(see a preview of how it'll appear on a mobile phone or device\)
    -   **Virtual agent** \(see a representation of how it'll appear on a chatbot interface\)

        **Note:** Your organization should have the correct plugins installed to see how the form will appear in Virtual Agent. If you're interested, ask your admin and see [Catalog builder preview topic conversation](https://www.servicenow.com/docs/access?context=catalog-builder-preview-topic&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information on previewing forms and their catalog items in Virtual Agent.

    The **View** button displays forms that have been published and doesn't explicitly create a new draft form for development. The **Edit** button takes you to a development form, for example, a new draft version of a form that's already been published.

    ![Preview how your app will look](../image/cs-portal-preview.png "Preview the app's experience")

    You can also check out a representation of how the form submissions workspace will appear by selecting the **Submissions** preview, as well as the records your app generates for it \(by selecting the **Record** preview\).


## Result

**Congrats:** Hooray! You've named your app and selected a catalog template that provides the basics for how your app's first form will look and work. Next, we will customize the forms people will use to fill out requests in your app in the section [Working with forms in Creator Studio](../concept/creator-studio-work-with-forms.md).

To learn all the things you can do as the app owner when building the app, see [Application collaboration](../../applications/concept/application-collaboration.md).

For sys admin eyes only: Every app built in Creator Studio adds a record in the Request App Config table. The name of the table follows the format of scope\_request, for example, x\_snc\_02\_03\_request.

**Parent Topic:**[App creation in Creator Studio](../concept/creator-studio-creating-apps.md)

