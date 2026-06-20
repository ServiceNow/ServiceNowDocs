---
title: Creator Studio quick start
description: This quick start guides you through the process of building your first app in Creator Studio and requesting its deployment.Create your app’s foundation before building it out.Associate your app with catalogs and topics to determine and categorize their content.Check out how your app will appear and then make adjustments to how it looks.Add questions to the form to gather the information that your fulfiller needs to evaluate the request, and then publish it to make its catalog items available.Add a playbook to create automation for your app, for example, to automatically assign a record to a manager for approval.Add an activity to your playbook to define what the automation does.Now that you've made an app, it's time to submit it for review so admins can approve and deploy it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/creator-studio/creator-studio-quick-start.html
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 16
breadcrumb: [Exploring Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Creator Studio quick start

This quick start guides you through the process of building your first app in Creator Studio and requesting its deployment.

At a minimum, you need to create the foundation of an app and customize its form, which is where users submit their fulfillment requests.

Building your first app is a good way to understand how Creator Studio enables easy app creation.

Your system administrator must add you to the Creator Studio Users group.

## Quick start: Build the foundation of an app

Create your app’s foundation before building it out.

### Before you begin

Your system administrator must add you to the Creator Studio Users group.

### Procedure

1.  Head over to the Creator Studio home page by going to **All** &gt; **App Engine** &gt; **Creator Studio**.

    \[Omitted image "crs-all-menu-gif.gif"\] Alt text: Select the All menu and search for Creator Studio

    The Creator Studio home page appears. To learn more about working in the home page, check out [Find existing apps in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/view-apps-creator-studio-home-page.md).

2.  Select the **Create app** button to start the process of creating an app.

    \[Omitted image "crs-create-app-button.png"\] Alt text: Select the Create app button

    -   If you're a system administrator, you can read more about this topic in [Application collaboration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/building-applications/application-collaboration.md).
    -   If you want to know how to request an admin to create the app for you, check out [Ask an admin to create an app for you in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-request-app-added.md).
3.  On the modal that pops up, enter a **Name** and brief **Description** of the app's purpose.

    \[Omitted image "cs-create-app-modal.png"\] Alt text: Enter details to create the app

4.  Select **Create app** to finish building the foundation of the app.


### Result

Okay, you've created the beginning of your very own application! You've named and described it. A list of catalog templates appears.

## Quick start: Choose catalogs and topics

Associate your app with catalogs and topics to determine and categorize their content.

### Before you begin

Your system administrator must add you to the Creator Studio Users group.

### Procedure

1.  Select a catalog template from the list, which your admin can customize, and then select **Apply this template**.

    You may not see a catalog template that is exactly what you want. So, choose one that's the closest. If none look close, select the **Creator Studio Default Template** option, if your admin hasn't removed it. It's your best bet.

    **Tip:** Feel free to click through the list of catalog templates. Previews will help you pick the one you want.

    Don't worry if you don't see other catalog templates to choose from! Your admins may not have created any custom catalog templates for you yet.

2.  Add a form to a catalog to specify its business area.

    **Note:** You can skip this step for now and revisit it later when you have a better idea of where it fits.

    The available catalogs are configured by your admin, contact them if you don't see the one you want.

    1.  Select the **Edit button** \(\[Omitted image "cs-edit-form-location.png"\]\) for the Catalogs and categories card.

    2.  Select the catalog that represents the business area the app will use.

        For example, choose a service catalog that contains software and laptop cables. Expand the carat for each catalog to see its sub-catalogs.

        \[Omitted image "crs-add-form-to-cat.png"\] Alt text: Select the catalogs your app will use

    3.  Select as many items in the catalogs as you need.

    4.  Select **Apply**.

    You can edit any of the app's basic settings any time after you finish creating the app. For more information, see [Creator Studio form settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-form-settings.md).

3.  Next, choose one or more topics to specify where the form will appear.

    Find out more about topics in , and more about taxonomy, which is a categorization method, in .

    **Note:** You can skip this step for now and revisit it later when you have a better idea of where it fits.

    1.  Select the **Edit button** \(\[Omitted image "cs-edit-form-location.png"\]\) for the Topics card.

    2.  Choose the **Taxonomy** page where you want the form to appear, such as **Employee**.

        Taxonomy is a method of categorization that Employee Center uses.

    3.  Select the topic\(s\) that represent the Employee Center areas where you want the form to appear.

        For example, choose a topic that contains technology services, and expand its carat to see each of its sub-topics.

        \[Omitted image "crs-topic-taxo.png"\] Alt text: Select one or more topics for your form

    4.  Select the topics where you want the form to appear, as many as you need.

    5.  Select the **Apply** button to save your changes.

4.  Select **Save and continue**.


### Result

Great, you've defined where the app will appear! Next, we'll customize how it looks.

## Quick start: Customize your app's look and feel

Check out how your app will appear and then make adjustments to how it looks.

### Before you begin

Your system administrator must add you to the Creator Studio Users group.

### Procedure

1.  Select to **Preview** how different forms appear in various experiences, or select the **View** or **Edit** button to view or edit the application experience.

    Select different previewing options if you want to make sure that you've selected the correct application and see how it will appear in the following formats:

    -   **Portal** \(see a preview of how it'll appear on a desktop website\)
    -   **Now Mobile** \(see a preview of how it'll appear on a mobile phone or device\)
    -   **Virtual agent** \(see a representation of how it'll appear on a chatbot interface\)

        **Note:** Your organization should have the correct plugins installed to see how the form will appear in Virtual Agent. If you're interested, ask your admin and see  for more information on previewing forms and their catalog items in Virtual Agent.

    The **View** button displays forms that have been published and doesn't explicitly create a new draft form for development. The **Edit** button takes you to a development form, for example, a new draft version of a form that's already been published.

    \[Omitted image "cs-portal-preview.png"\] Alt text: Preview how your app will look

    You can also check out a representation of how the form submissions workspace will appear by selecting the **Submissions** preview, as well as the records your app generates for it \(by selecting the **Record** preview\).

2.  Next, you can customize the form's look and feel on the **Request forms** tab by completing one of the following steps.

    1.  Add or modify the image that appears on your form by selecting the add image icon \(\[Omitted image "cs-add-form-image.png"\] Alt text: Select an image to accompany your form\) and then selecting an image.

    2.  Change the form’s title, short description, and other text by selecting those parts of the form and typing in your changes.

        You can enhance how the longer **Description** appears using rich text, such as font changes and sizing.


### Result

Get more details on customizing your form in [Customize your form for an app in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-edit-form.md).

Next, we'll build and publish a form.

## Quick start: Add questions to and publish a form

Add questions to the form to gather the information that your fulfiller needs to evaluate the request, and then publish it to make its catalog items available.

### Before you begin

Your system administrator must add you to the Creator Studio Users group.

### Procedure

1.  In the Form elements panel, drag the type of question you want onto the form and drop it on the canvas where you’d like it. You can also add questions by selecting the add icon \(+\) that appears when you click on an existing question on the form.

    If you're adding a pre-configured **Question set**, you must select the question set from the modal that appears when you drag it onto the form.

    For a description of question types and how they're used, see [Available question types in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-form-elements-ref.md).

2.  Select the question.

    When you select a question, it's highlighted on the form so you know what you're working on.

3.  In the **Configurations** tab of the Question details panel, specify information about the question you added, such as whether a question must be answered for the requester to submit the form.

    The details vary by question type. For example, if you add a **Dropdown** question, you must supply the options to choose from.

    \[Omitted image "crs-form-questions-sets-dynamic.png"\] Alt text: Entering details for a question on a form

4.  Make the form's appearance change based on how users answer questions by adding [dynamic behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-glossary.md) to it on the **Behaviors** tab.

    For example, if a user says they want a T-shirt for an event they're attending, you can make a **T-shirt size** field required. Get the details on adding dynamic in [Make a form change based on responses in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-dynamic-behavior.md).

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

        \[Omitted image "crs-section-edit-hover.png"\] Alt text: Hover over the section name to edit it

        For more information, see [Layout options for forms in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-form-layout-options.md).

    3.  Select **Save** in the Section details/Question details panel when you’re done revising the form’s layout.

8.  Finally, publish the form when it's ready by selecting the **Mark as ready** button.

    Publishing forms makes them available as catalog items in the production instance for published apps.

    \[Omitted image "cs-mark-as-ready.png"\] Alt text: Mark your app as ready


### Result

Now that the form is available as a catalog item, we can use it to create an automated playbook.

## Quick start: Add a playbook

Add a playbook to create automation for your app, for example, to automatically assign a record to a manager for approval.

### Before you begin

Your system administrator must add you to the Creator Studio Users group.

### Procedure

1.  Select the **Automations** tab in the application header.

    \[Omitted image "cs-automations-tab.png"\] Alt text: Select the Automations tab

2.  Select the **Create a playbook** button.

3.  Specify the playbook's General attributes in the Create playbook modal.

    |Field|Description|
    |-----|-----------|
    |Playbook name|Descriptive name for the playbook you're creating.|
    |Description|Brief explanation of what the playbook does, for example, the end goal for the record type.|

    \[Omitted image "cs-create-playbook-modal.png"\] Alt text: Settings for creating a playbook

4.  Specify the Schedule for the playbook.

    1.  Select the **Form** whose catalog item generates the record type that you want the playbook to run on.

        The table for the form you choose is always the app’s task table, which is specified when the app is created.

    2.  Select the type of **Trigger** that initiates the playbook.

        |Trigger|Description|
        |-------|-----------|
        |Form submitted|Start running the playbook when a user submits the form you chose.|
        |Form updated|Start running the playbook when a user updates the form you chose.|
        |Form submitted or updated|Start running the playbook when a user submits or updates the form you chose.|

        **Note:** You can't change an playbook's trigger type after you finish creating the playbook. Instead, create a new playbook with a different trigger.

        However, you can edit the trigger condition, such as making the playbook run conditionally based on a specific answer to a question. For more information, see [Edit the trigger for a playbook in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-add-trigger-automation.md).

    3.  If you chose a trigger that includes a form being updated, specify how often that app should **Run your playbook**.

        The options are:

        -   **Once**
        -   **For each unique change**
        -   **Only if not currently running**
        -   **For every update**
    4.  Specify the conditions that must be met for the playbook to begin running by selecting **Add condition set**.

        -   If you want to trigger the playbook based on the value of a column in a table, select the **[Field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-glossary.md)** that you want to be the trigger, as well as its condition **Operator** and the specific trigger **Value**. For example, when a **Start date** is **after** the **Date** needed.
        -   If you want to trigger the playbook based on the response from a form, select **Questions** as the trigger **Field**. Then select the question you want in the **Question** field, the condition **Operator** and the answer's **Value**.

            \[Omitted image "crs-trigger-question-answer.png"\] Alt text: Use a specific answer to a form's question as trigger

        Add as many conditions as you need. For more information, see .

5.  Select **Save** before moving on to add an activity.


### Result

Next, we'll add an activity to the playbook to define what the automation does.

## Quick start: Add an activity and activate a playbook

Add an activity to your playbook to define what the automation does.

### Before you begin

Your system administrator must add you to the Creator Studio Users group.

### About this task

If you want to include an if/then statement to define circumstances for the [activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-glossary.md), add a decision. See [Add a decision to an app's playbook in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-add-decision-automation.md) for details.

### Procedure

1.  Select the **Automations** tab in the application header.

    \[Omitted image "cs-automations-tab.png"\] Alt text: Select the Automations tab

2.  Select the add icon \[Omitted image "cs-add-icon.png"\] Alt text: on the connector where you want to add an activity and choose the square **Add an activity** icon \(\[Omitted image "cs-add-activity-icon.png"\] Alt text:\) in the menu that pops up.

3.  Choose the type of activity that you want from the Activity library pop-up.

    **Note:** In addition to the following standard activities, you may see some custom activities that your admin created.

<table id="table_gj1_3cg_n1c"><thead><tr><th>

Activity type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Request approval

</td><td>

Ask someone for permission to accomplish a task.

</td></tr><tr><td>

Assign to

</td><td>

Choose a person who should fulfill the task.

</td></tr><tr><td>

Create task

</td><td>

Specify a process that must be done as part of the playbook.

</td></tr><tr><td>

Send an email

</td><td>

Send an email to one or more people. You can specify images and enrich text for the email that gets sent automatically.

</td></tr><tr><td>

Placeholder

</td><td>

Set an undefined activity to be specified later, or a more advanced activity such as an email notification, when an activity is completed.Placeholder activities don't have any logic assigned to them yet, and must be edited in Workflow Studio. Or, you can swap them out later for another type of activity in Creator Studio.

</td></tr></tbody>
</table>    \[Omitted image "cs-add-activity-email.png"\] Alt text: Select which type of activity to add

4.  Enter the basic details for the activity.

    |Field|Description|
    |-----|-----------|
    |Name|Unique, user-facing name for your activity, which appears to agents and fulfillers while the playbook is running.|
    |Description|Optional details about what the activity accomplishes.|

    \[Omitted image "cs-assign-to-properties.png"\] Alt text: Activity details panel

5.  Complete the details for the activity, using [Add activities to an app's playbook in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-add-activities-automation.md) for information on how to finish creating the activity.

6.  Select the **Save and close** button to finish setting up your activity.

7.  Once the automation is done, activate it by selecting the **Activate** button.

    Activating a playbook makes it available to run when its related form is created or updated on your non-production, development instance.

    \[Omitted image "cs-playbook-activate-button.png"\] Alt text: Select the button to activate the playbook


### Result

The app is now ready to be deployed to production! Let's request deployment in the final step of this quick start guide.

## Quick Start: Submit your app for deployment

Now that you've made an app, it's time to submit it for review so admins can approve and deploy it.

### Before you begin

Your system administrator must add you to the Creator Studio Users group.

### Procedure

1.  In the application header, select **Submit for review**.

    \[Omitted image "cs-submit-review-button.png"\] Alt text: Select Submit for review to request deployment

2.  Select **Continue** on the Submit app for review modal.

3.  Now you need to choose which published forms are visible to users in the catalog. In the Ready for review section of the Review request forms modal, select which of the app's published forms that you want to be available after the app is deployed selecting the **Visible to others** option.

    \[Omitted image "cs-submit-request-forms.png"\] Alt text: Select which forms to deploy

4.  Select **Continue** when you're happy with the forms being deployed to production.

5.  Next, you must decide which of the app's activated playbooks will run on production after the app is deployed. In the Review playbooks modal, select the **Run on production** option for each playbook that you want to run on records that the app generates.

    **Note:** If you can't select a playbook, you need to go back to the **Automations** tab of Creator Studio and activate it. If you need a refresher on that, check out [Activate a playbook in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-activate-automation.md).

6.  Select **Continue** when you're happy with the playbooks being deployed to run on production.

7.  Finally, make sure that all the release details for the published app are correct.

<table id="table_a5n_phs_m1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New version

</td><td>

[Version number](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-glossary.md) of the app you're requesting for deployment. Creator Studio automatically generates an updated version number, but you can change it.Follow your organization's versioning guidelines, or use the x.y.z format, where x = major update, y = minor update, and z = patch.

</td></tr><tr><td>

[Release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-glossary.md)

</td><td>

Details on what's changed in this new version of the app, or a general description of what the app does if this is its first version.

</td></tr></tbody>
</table>    Read more about this step of requesting deployment in [App versioning and release notes for Creator Studio apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-app-release-versioning.md).

    \[Omitted image "cs-deploy-versioning.png"\] Alt text: Versioning info on deployment request

8.  Select **Submit for review** when everything is correct and ready for your admin to review and deploy.


### Result

**Congrats:** Hooray! You've created your app, customized the form, added automation, and submitted it for review. After your admin reviews and deploys it, people will use your brand-new app to make requests.

