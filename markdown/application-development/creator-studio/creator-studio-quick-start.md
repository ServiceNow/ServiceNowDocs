---
title: Creator Studio quick start
description: This quick start guides you through the process of building your first app in Creator Studio and requesting its deployment.Create your app first. Later, we'll continue building it out.Let's add a form so people can make a request. Forms contain questions that people respond to when submitting a service desk request.Add questions to the form and define what they are asking to gather the information that your fulfiller needs to evaluate the request. You can then publish it to make its catalog items available.Add a playbook to create automation for your app, for example, to automatically assign a record to a manager for approval.Add an activity to your playbook to define what the automation does.Now that you've made an app, it's time to submit it for review so admins can approve and deploy it.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 17
breadcrumb: [Explore, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Creator Studio quick start

This quick start guides you through the process of building your first app in Creator Studio and requesting its deployment.

At a minimum, you need to create the app, and then add and customize a form, which is where users submit their fulfillment requests.

Building your first app is a good way to understand how Creator Studio enables easy app creation.

For a more thorough tutorial where you build a gift card request app, see [Creator Studio tutorial](../concept/creator-studio-tutorial-landing.md#).

Your system administrator must add you to the Creator Studio Users group.

## Quick start part 1: Create an app

Create your app first. Later, we'll continue building it out.

### Before you begin

Your system administrator must add you to the Creator Studio Users group.

**Note:** If you don't have permission to create apps yourself, you can ask your admin to create one for you. See [Ask an admin to create an app for you in Creator Studio](creator-studio-request-app-added.md) to find out how.

### About this task

You can also watch a short video on how to create an app.

Video on how to create an app 

### Procedure

1.  Head over to the Creator Studio home page by going to **All** &gt; **App Engine** &gt; **Creator Studio**.

    ![Select the All menu and search for Creator Studio](../image/crs-all-menu-callouts.png "Start Creator Studio")

    The Creator Studio home page appears. To learn more about working in the home page, check out [Find existing apps in Creator Studio](view-apps-creator-studio-home-page.md).

2.  Select the **Create app** button to start the process of creating an app.

    ![Select the Create app button](../image/crs-create-app-button-search.png "Create app button")

    -   If you're a system administrator, you can read more about this topic in [Application collaboration](../../applications/concept/application-collaboration.md).
    -   If you want to know how to request an admin to create the app for you, check out [Ask an admin to create an app for you in Creator Studio](creator-studio-request-app-added.md).
3.  Select the type of app you want to build, such as **Service Desk**.

    Service Desk apps enable users to submit requests, report issues, and access support related to services within your company.

    **Note:** Your admin may have hidden this page.

    ![Within the Creator Studio interface, select the "Service Desk" app option. This type of app is designed to streamline the management of incoming requests or support tickets.](../image/crs-interstitial-sd.png "Select the app type")

4.  Select the **Continue** button.

5.  On the page that appears, enter a **Name** and brief **Description** of the app's purpose.

    ![Enter details to create the app](../image/cs-create-app-modal.png "Create an app")

6.  Select **Create app**.


### Result

Okay, you've created the beginning of your very own application! You've named and described it.Now, let's add a form.

## Quick start part 2: Add a form

Let's add a form so people can make a request. Forms contain questions that people respond to when submitting a service desk request.

### Before you begin

Your system administrator must add you to the Creator Studio Users group.

### Procedure

1.  Select **+ Add form** to get started.

    ![Select to Add form](../image/crs-add-form-new-nav.png "Select to add a form")

2.  Select a catalog template from the list, which your admin can customize, and then select **Apply template and continue**.

    You may not see a catalog template that is exactly what you want. So, choose one that's the closest. If none look close, select the **Creator Studio Default Template** option, if your admin hasn't removed it. It's your best bet.

    **Tip:** Feel free to click through the list of catalog templates. Previews will help you pick the one you want.

    Don't worry if you don't see other catalog templates to choose from! Your admins may not have created any custom catalog templates for you yet.

3.  Choose how you want to build the form:

    -   To use Now Assist, stay on the **Build with Now Assist** tab and enter directions for the form you want. To learn more, see [Generating forms with Now Assist](../concept/creator-studio-text-to-form.md).

        **Note:** You can select **Try an example** to see some examples of the available directions. To see a quick mock up of what the form will look like, select the **generate form preview** button. If you want a different form, change the provided direction and select **Regenerate preview** for a quick look.

    -   To manually build the form, select the **Build on your own** tab and enter the information for the form:

        |Field|Description|
        |-----|-----------|
        |Form name|A descriptive name for the form.|
        |Short description|Some information on what the form is used for.|
        |Long description|Additional details for the form. You can include content like images and links to other sources of information \(for example, a knowledge base article\).|

    If you don't see the option to **Build with Now Assist** tab, you need to check with your admin. To install Now Assist for Form generation, see [Configuring form generation in Creator Studio](../concept/creator-studio-configure-now-assist.md).

4.  Select **Save and edit form**.


### What to do next

Now that you've added a form to your app, it's time to customize it! Remember: You can add multiple forms to your app for if you need to.

## Quick start part 3: Add questions to and publish a form

Add questions to the form and define what they are asking to gather the information that your fulfiller needs to evaluate the request. You can then publish it to make its catalog items available.

### Before you begin

Your system administrator must add you to the Creator Studio Users group.

### Procedure

1.  Select the question that you want to customize.

    When you select a question, it's highlighted on the form so you know what you're working on.

    ![Select a question, which highlights it in the canvas](../image/crs-modify-question.png "Select a question to work on it")

2.  In the **Configurations** tab of the Question details panel, specify information about the question you added, such as a label for what the question is asking and whether it must be answered for the requester to submit the form.

    The details vary by question type. For example, if you add a **Dropdown** question, you must supply the options to choose from.

    ![Entering details for a question on a form](../image/crs-form-questions-sets-dynamic-update.png "Form question details")

3.  Make the form's appearance change based on how users answer questions by adding [dynamic behavior](../concept/creator-studio-glossary.md#) to it on the **Behaviors** tab.

    For example, if a user says they want a T-shirt for an event they're attending, you can make a **T-shirt size** field required. Get the details on adding dynamic in [Make a form change based on responses in Creator Studio](creator-studio-dynamic-behavior.md).

4.  Automatically populate a question's answer based on the answer to another question on the form \(record choices questions only\) by selecting the **Add auto-fill** option.

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
</table>5.  Select **Save and close** when you finish modifying the question.

6.  Add another question by dragging the type of question you want from the Form elements panel onto the form, dropping it on the canvas where you’d like it.

    You can also add questions by selecting the add icon \(+\) that appears when you click on an existing question on the form. If you're adding a pre-configured **Question set**, you must select the question set from the modal that appears when you drag it onto the form.

    For a description of question types and how they're used, see [Available question types in Creator Studio](../reference/creator-studio-form-elements-ref.md).

7.  Change a question type by selecting the question and then choosing the new question type in the **Content type** field of the Question details panel.

    Selecting a new type may introduce new values you must supply.

    Keep these specifications in mind as you create your questions:

    -   You can't change an existing question into a question set. To include a question set on a form, you must newly add it to the form.
    -   If you put two checkbox questions side-by-side on a form, they make a section. You can't add other types of questions to that section.
8.  Now, let's arrange the questions and images that you’ve added to the form.

    1.  From the Form elements panel, drag the layout option you like onto the form and drop it where you want it to appear, for example, a **Divider line**.

        Don’t worry if you don’t like the layout, just try another one by dragging it onto the form's canvas.

    2.  Revise the form layout you chose using the Section details or Question details panel \(depending on the layout you're working on\). You can do things like make text bold, add links, and so forth.

        **Note:** To edit or delete a section, you must hover over the section name and then select **Section** to see the section details in the properties panel, as well as the delete icon.

        ![Hover over the section name to edit it](../image/crs-section-edit-hover.png "Selecting a section")

        For more information, see [Layout options for forms in Creator Studio](../reference/creator-studio-form-layout-options.md).

    3.  Select **Save** in the Section details/Question details panel when you’re done revising the form’s layout.

9.  See how your form will look in various experiences by selecting the **Preview** button.

    You can see a preview of the how the current version of the form will appear in various experiences by selecting **Portal** \(such as Employee Portal\), **Now Mobile**, or **Virtual Agent**. You can fill in the form when previewing, but selecting the **Submit** button doesn't generate a task record.

    ![Preview how a form looks on mobile](../image/crs-preview-mobile.png "Preview a form")

10. Publish the form when it's ready by selecting the **Mark as ready** button.

    Publishing forms makes them available as catalog items in the production instance after the associated app has been deployed.

    ![Mark your app as ready](../image/crs-mark-as-ready.png "Mark as ready button")


### Result

Now that the form is available as a catalog item, we can use it to create an automated playbook.

## Quick start part 4: Add a playbook

Add a playbook to create automation for your app, for example, to automatically assign a record to a manager for approval.

### Before you begin

The form that you want to add automation to must already be published.

Your system administrator must add you to the Creator Studio Users group.

### Procedure

1.  Select **+ Add automation** in the navigation panel for the form you want to add a playbook to.

    **Note:** If the form isn't yet published, you must first mark it as ready. For more information, see [Publish a form for your app in Creator Studio](creator-studio-publish-form.md).

    ![Select add automation for the form](../image/crs-add-auto-new.png "Add automation")

2.  Specify the playbook's General attributes in the Create playbook modal.

    |Field|Description|
    |-----|-----------|
    |Playbook name|Descriptive name for the playbook you're creating.|
    |Description|Brief explanation of what the playbook does, for example, the end goal for the record type.|

    ![Settings for creating a playbook](../image/crs-create-playbook-modal.png "Create a playbook")

3.  Specify the Schedule for the playbook.

    1.  Select the type of **Trigger** that initiates the playbook.

        |Trigger|Description|
        |-------|-----------|
        |Form submitted|Start running the playbook when a user submits the form you chose.|
        |Form updated|Start running the playbook when a user updates the form you chose.|
        |Form submitted or updated|Start running the playbook when a user submits or updates the form you chose.|

        **Note:** You can't change an playbook's trigger type after you finish creating the playbook. Instead, create a new playbook with a different trigger.

        However, you can edit the trigger condition, such as making the playbook run conditionally based on a specific answer to a question. For more information, see [Edit the trigger for a playbook in Creator Studio](creator-studio-add-trigger-automation.md).

    2.  If you chose a trigger that includes a form being updated, specify how often that app should **Run your playbook**.

        The options are:

        -   **Once**
        -   **For each unique change**
        -   **Only if not currently running**
        -   **For every update**
    3.  Specify the conditions that must be met for the playbook to begin running by selecting **Add conditions**.

        -   If you want to trigger the playbook based on the value of a column in a table, select the **[Field](../concept/creator-studio-glossary.md#)** that you want to be the trigger, as well as its condition **Operator** and the specific trigger **Value**. For example, when a **Start date** is **after** the **Date** needed.
        -   If you want to trigger the playbook based on the response from a form, select **Questions** as the trigger **Field**. Then select the question you want in the **Question** field, the condition **Operator** and the answer's **Value**.

            ![Use a specific answer to a form's question as trigger](../image/crs-trigger-question-answer.png "Question answer as trigger for an automation")

        Add as many conditions as you need. For more information, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

    4.  Select **Create**.


### Result

Next, we'll add an activity to the playbook to define what the automation does.

## Quick start part 5: Add an activity and activate a playbook

Add an activity to your playbook to define what the automation does.

### Before you begin

Your system administrator must add you to the Creator Studio Users group.

### About this task

If you want to include an if/then statement to define circumstances for the [activity](../concept/creator-studio-glossary.md#), add a decision. See [Add a decision to an app's playbook in Creator Studio](creator-studio-add-decision-automation.md) for details.

### Procedure

1.  Ensure that you're viewing the playbook that you just created.

2.  Select the add icon ![](../image/cs-add-icon.png) on the connector where you want to add an activity and choose the square **Add an activity** icon \(![](../image/cs-add-activity-icon.png)\) in the menu that pops up.

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

</td></tr><tr><td>

Update submission

</td><td>

Update the value of the specified fields on the record that the form generates when a user submits it.

</td></tr></tbody>
</table>    ![Select which type of activity to add](../image/crs-add-activity-more.png "Activity library for a playbook")

4.  Enter the basic details for the activity.

    |Field|Description|
    |-----|-----------|
    |Label|Unique, user-facing name for your activity, which appears to agents and fulfillers while the playbook is running.|
    |Description|Optional details about what the activity accomplishes.|

    ![Activity details panel](../image/cs-assign-to-properties.png "Activity details panel")

5.  Complete the details for the activity, using [Add activities to an app's playbook in Creator Studio](creator-studio-add-activities-automation.md) for information on how to finish creating the activity.

6.  Select the **Save and close** button to finish setting up your activity.

7.  Once the automation is done, activate it by selecting the **Activate** button.

    Activating a playbook makes it available to run when its related form is created or updated on your non-production, development instance.

    ![Select the button to activate the playbook](../image/crs-playbook-activate.png "Activate the playbook")


### Result

The app is now ready to be deployed to production! Let's request deployment in the final step of this quick start guide.

## Quick Start part 6: Submit your app for deployment

Now that you've made an app, it's time to submit it for review so admins can approve and deploy it.

### Before you begin

Your system administrator must add you to the Creator Studio Users group.

### Procedure

1.  Test the form by selecting the **Try it** button.

    You can then enter test values in the fields and select **Submit** to view the record your form submission created.

2.  In the navigation panel, select **Submit for review**.

    ![Select Submit for review to request deployment](../image/crs-submit-review-btn.png "Submit for review")

3.  Select **Continue** on the Submit app for review modal.

4.  Now you need to choose which published forms are visible to users in the catalog. In the Ready for review section of the Review request forms modal, select which of the app's published forms that you want to be available after the app is deployed by selecting the **Visible to others** option.

    ![Select which forms to deploy](../image/cs-submit-request-forms.png "Review request forms for deployment")

5.  Select **Continue** when you're happy with the forms being deployed to production.

6.  Next, you must decide which of the app's activated playbooks will run on production after the app is deployed. In the Review playbooks modal, select the **Run on production** option for each playbook that you want to run on records that the app generates.

    **Note:** If you can't select a playbook, you need to go back to the **Automations** section of Creator Studio and activate it. If you need a refresher on that, check out [Activate a playbook in Creator Studio](creator-studio-activate-automation.md).

7.  Select **Continue** when you're happy with the playbooks being deployed to run on production.

8.  Finally, make sure that all the release details for the published app are correct.

<table id="table_a5n_phs_m1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New version

</td><td>

[Version number](../concept/creator-studio-glossary.md#) of the app you're requesting for deployment. Creator Studio automatically generates an updated version number, but you can change it.Follow your organization's versioning guidelines, or use the x.y.z format, where x = major update, y = minor update, and z = patch.

</td></tr><tr><td>

[Release notes](../concept/creator-studio-glossary.md#)

</td><td>

Details on what's changed in this new version of the app, or a general description of what the app does if this is its first version.

</td></tr></tbody>
</table>    Read more about this step of requesting deployment in [App versioning and release notes for Creator Studio apps](../concept/creator-studio-app-release-versioning.md).

    ![Versioning info on deployment request](../image/cs-deploy-versioning.png "App versioning info")

9.  Select **Submit for review** when everything is correct and ready for your admin to review and deploy.


### Result

**Congrats:** Hooray! You've created your app, customized the form, added automation, and submitted it for review. After your admin reviews and deploys it, people will use your brand-new app to make requests.

