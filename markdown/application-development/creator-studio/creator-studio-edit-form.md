---
title: Customize your form for an app in Creator Studio
description: Forms help people ask for things they need, such as a new keyboard or permission to take time off. The default form that's added when you create an app in Creator Studio needs some changes to fit your needs. For example, you must add question labels to gather information about the request.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
keywords: [app form, request app add item]
breadcrumb: [Working with forms in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Customize your form for an app in Creator Studio

Forms help people ask for things they need, such as a new keyboard or permission to take time off. The default form that's added when you create an app in Creator Studio needs some changes to fit your needs. For example, you must add question labels to gather information about the request.

## Before you begin

To customize a form, you must be given permission to work on the app.

## About this task

You can add additional forms to your application if you need them. Additional forms are stored in the app's same table. No need to worry about those tables right now, but if you want to know how to add more forms besides the form that was generated when the app was created, check out [Add more forms to an app in Creator Studio](creator-studio-add-another-form.md).

**Summary:** After finishing the following steps, you’ll know how to:

-   Open the form that was automatically generated when the app was created.
-   Add questions and images to the form.
-   Arrange the questions and images that you added.

Let's open a form and customize it.

**Note:** For example, you can create a form that people use to register for a company event, with questions like dietary preference and accessibility needs.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio**.

    All the apps built in Creator Studio appear on the home page.

2.  Open the application that contains the form you want to customize.

3.  Select to **Preview** how different forms appear in various experiences, or select the **View** or **Edit** button to view or edit the application experience.

    Select different previewing options if you want to make sure that you've selected the correct application and see how it will appear in the following formats:

    -   **Portal** \(see a preview of how it'll appear on a desktop website\)
    -   **Now Mobile** \(see a preview of how it'll appear on a mobile phone or device\)
    -   **Virtual agent** \(see a representation of how it'll appear on a chatbot interface\)

        **Note:** Your organization should have the correct plugins installed to see how the form will appear in Virtual Agent. If you're interested, ask your admin and see [Catalog builder preview topic conversation](https://www.servicenow.com/docs/access?context=catalog-builder-preview-topic&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information on previewing forms and their catalog items in Virtual Agent.

    The **View** button displays forms that have been published and doesn't explicitly create a new draft form for development. The **Edit** button takes you to a development form, for example, a new draft version of a form that's already been published.

    ![Preview how your app will look](../image/crs-portal-preview.png "Preview the app's experience")

    You can also check out a representation of how the form submissions workspace will appear by selecting the **Submissions** preview, as well as the records your app generates for it \(by selecting the **Record** preview\).

4.  Select the **Request forms** tab to make sure you're editing the correct form in your app.

    If you’re not, select the form you want to edit.

    ![Select the appropriate form from the Request forms tab](../image/cs-form-selection.png)

5.  Let’s customize the form by doing one or more of the following optional steps.

    1.  Add or modify the image that appears on your form by selecting the add image icon \(![Select an image to accompany your form](../image/cs-add-form-image.png)\) and then selecting an image.

    2.  Change the form’s title, short description, and other text by selecting those parts of the form and typing in your changes.

        You can enhance how the longer **Description** appears using rich text, such as font changes and sizing.

6.  Next, add questions to the form your fulfiller needs to evaluate the request. To add and customize a question, complete the following steps.

    1.  In the Form elements panel, drag the type of question you want onto the form and drop it on the canvas where you’d like it. You can also add questions by selecting the add icon \(+\) that appears when you click on an existing question on the form.

        If you're adding a pre-configured **Question set**, you must select the question set from the modal that appears when you drag it onto the form.

        For a description of question types and how they're used, see [Available question types in Creator Studio](../reference/creator-studio-form-elements-ref.md).

    2.  Select the question.

        When you select a question, it's highlighted on the form so you know what you're working on.

    3.  In the **Configurations** tab of the Question details panel, specify information about the question you added, such as whether a question must be answered for the requester to submit the form.

        The details vary by question type. For example, if you add a **Dropdown** question, you must supply the options to choose from.

        ![Entering details for a question on a form](../image/crs-form-questions-sets-dynamic.png "Form question details")

    4.  Make the form's appearance change based on how users answer questions by adding [dynamic behavior](../concept/creator-studio-glossary.md#) to it on the **Behaviors** tab.

        For example, if a user says they want a T-shirt for an event they're attending, you can make a **T-shirt size** field required. Get the details on adding dynamic in [Make a form change based on responses in Creator Studio](creator-studio-dynamic-behavior.md).

    5.  Select **Save and close** when you finish modifying the question.

    6.  Revise or add more questions to the form using this procedure. To change a question type, select the question and then select the new question type in the **Content type** field of the Question details panel. Selecting a new type may introduce new values you must supply.

        Keep these specifications in mind as you create your questions:

        -   You can't change an existing question into a question set. To include a question set on a form, you must newly add it to the form.
        -   If you put two checkbox questions side-by-side on a form, they make a section. You can't add other types of questions to that section.
7.  Now, let's arrange the questions and images that you’ve added to the form.

    1.  From the Form elements panel, drag the layout option you like onto the form and drop it where you want it to appear, for example, a **Divider line**.

        Don’t worry if you don’t like the layout, just try another one by dragging it onto the form's canvas.

    2.  Revise the form layout you chose using the Section details or Question details panel \(depending on the layout you're working on\). You can do things like make text bold, add links, and so forth.

        **Note:** To edit or delete a section, you must hover over the section name and then select **Section** to see the section details in the properties panel, as well as the delete icon.

        ![Hover over the section name to edit it](../image/crs-section-edit-hover.png "Selecting a section")

        For more information, see [Layout options for forms in Creator Studio](../reference/creator-studio-form-layout-options.md).

    3.  Select **Save** in the Section details/Question details panel when you’re done revising the form’s layout.


## Result

**Congrats:** Congratulations! You've customized the default form that came with your app.

## What to do next

You must then mark the form as ready to publish it, which makes it available for the app to use. Find out how to publish a form in [Publish a form for your app in Creator Studio](creator-studio-publish-form.md).

You can select the **Undo all changes** option, available in the form header's more options icon \(![Select more options to undo changes](../image/cs-more-actions-icon.png)\), to reset a form to the most recently published version.

**Parent Topic:**[Working with forms in Creator Studio](../concept/creator-studio-work-with-forms.md)

