---
title: Customize your form for an app in Creator Studio
description: Forms help people ask for things they need, such as a new keyboard or permission to take time off. The default form that's added when you create an app in Creator Studio needs some changes to fit your needs. For example, you must add question labels to gather information about the request.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
keywords: [app form, request app add item]
breadcrumb: [Forms in apps, Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
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

1.  Let's head over to **All** &gt; **App Engine** &gt; **Creator Studio**.

    All the apps built in Creator Studio appear on the home page.

2.  Open the application that contains the form you want to customize.

3.  Select the form you want to customize in the navigation panel.

    **Note:** If your app has a lot of forms, you can use the search box in the navigation panel to search for a specific form.

    ![Select the appropriate form from the navigation panel](../image/crs-form-selection.png "Select the form")

4.  Select the **Edit** button if you want to work on a form that's already been published.

    ![Select Edit to work on a published form](../image/crs-form-edit.png "Edit button")

5.  Let’s customize the form by doing one or more of the following optional steps.

    1.  Add or modify the image that appears on your form by selecting the add image icon \(![Select an image to accompany your form](../image/cs-add-form-image.png)\) and then selecting an image.

    2.  Change the form’s title, short description, and other text by selecting those parts of the form and typing in your changes.

        You can enhance how the longer **Description** appears using rich text, such as font changes and sizing.

6.  Next, add questions to the form your fulfiller needs to evaluate the request. To add and customize a question, complete the following steps.

    1.  Add another question by dragging the type of question you want from the Form elements panel onto the form, dropping it on the canvas where you’d like it.

        You can also add questions by selecting the add icon \(+\) that appears when you click on an existing question on the form. If you're adding a pre-configured **Question set**, you must select the question set from the modal that appears when you drag it onto the form.

        For a description of question types and how they're used, see [Available question types in Creator Studio](../reference/creator-studio-form-elements-ref.md).

    2.  Select the question.

        When you select a question, it's highlighted on the form so you know what you're working on.

    3.  In the **Configurations** tab of the Question details panel, specify information about the question you added, such as a label for what the question is asking and whether it must be answered for the requester to submit the form.

        The details vary by question type. For example, if you add a **Dropdown** question, you must supply the options to choose from.

        ![Entering details for a question on a form](../image/crs-form-questions-sets-dynamic-update.png "Form question details")

    4.  Make the form's appearance change based on how users answer questions by adding [dynamic behavior](../concept/creator-studio-glossary.md#) to it on the **Behaviors** tab.

        For example, if a user says they want a T-shirt for an event they're attending, you can make a **T-shirt size** field required. Get the details on adding dynamic in [Make a form change based on responses in Creator Studio](creator-studio-dynamic-behavior.md).

    5.  Automatically populate a question's answer based on the answer to another question on the form \(record choices questions only\) by selecting the **Add auto-fill** option.

        For example, a form can enable someone to select a user for the **Choose the gift box recipient** field, which retrieves its values from the User table. An additional **Preferred name** field can be automatically populated from the **First name** field of the User table selection, but then edited if someone prefers a nickname.

        The **Add auto-fill** option is available only if the form has a record choices question on it. You must also complete the following fields:

<table id="table_hfg_tk4_sdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select the dependent question

</td><td>

Question whose answer makes the current question automatically populate.

</td></tr><tr><td>

Select the value field

</td><td>

Field in the source table for the record choices question that contains the value you want to use as the answer to the current question.You must select the edit icon \(![](../image/crs-edit-pencil-icon-purple.png)\), navigate to the field in the source table that contains the auto-populated answer, and select to **Apply** it. For more info on selecting fields in a table, see [Dot-walking to data in related tables](https://www.servicenow.com/docs/access?context=c_DotWalking&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>    6.  Select **Save and close** when you finish modifying the question.

    7.  Revise or add more questions to the form using this procedure. To change a question type, select the question and then select the new question type in the **Content type** field of the Question details panel. Selecting a new type may introduce new values you must supply.

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

8.  See how your form will look in various experiences by selecting the **Preview** button.

    You can see a preview of the how the current version of the form will appear in various experiences by selecting **Portal** \(such as Employee Portal\), **Now Mobile**, or **Virtual Agent**. You can fill in the form when previewing, but selecting the **Submit** button doesn't generate a task record.

    ![Preview how a form looks on mobile](../image/crs-preview-mobile.png "Preview a form")

9.  Test using the form and the record it generates by selecting the **Try it** button.

    As you test the form, note any updates you'd like to make and then make those changes on the form before you publish it. For details, see [Test one of your forms for an app](creator-studio-try-it.md).


## Result

**Congrats:** Congratulations! You've customized the default form that came with your app.

## What to do next

You must then mark the form as ready to publish it, which makes it available for the app to use. Find out how to publish a form in [Publish a form for your app in Creator Studio](creator-studio-publish-form.md).

You can select the **Undo all changes** option, available in the form header's more options icon \(![Select more options to undo changes](../image/cs-more-actions-icon.png)\), to reset a form to the most recently published version.

**Parent Topic:**[Working with forms in Creator Studio](../concept/creator-studio-work-with-forms.md)

