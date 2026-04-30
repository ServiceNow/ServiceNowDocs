---
title: Creator Studio tutorial
description: Use this tutorial to create a Gift Card Request app to streamline the processes of providing recognition to a team.Begin by creating an app from the Creator Studio home page.Adding a form enables people to make a request. Forms contain questions that people respond to when submitting a service desk request.Customize the form for the gift card request app by manually entering questions. When it's done, you can mark the form as ready to be published.Add a playbook that uses the form that you just created to automate approval for the gift card request app.Customize the lists and submitted records in the workspace where fulfillers can process gift card requests from the. In this list customization, you add a column to view the assignment group.Test your app and then request that an admin review and deploy the app to production.Impersonate an admin to deploy the gift card request app that you created.Use the deployed gift card request app that you just created to request a gift card.Verify that your app is working by checking the Request App Workspace to view the gift card request that you submitted.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 14
keywords: [creator studio, servicenow creator studio, creator studio srvicenow, creatorstudio, creator studio app, creater studio, cretor studio, creter studio, servicenow customization, studio creator, no code, no-code, request app, citizen development, delegated development, delegate development, request app, request fulfill app, fulfllment app, fulfillment, visual development]
breadcrumb: [Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Creator Studio tutorial

Use this tutorial to create a Gift Card Request app to streamline the processes of providing recognition to a team.

## Tutorial objectives

In this tutorial, you'll assume the following roles to create and deploy the app:

-   As a marketing manager who is looking to streamline the processes of providing recognition to their team, you'll create the Gift Card Request app.
-   As an application development administrator, approve and deploy the new app to a production environment.
-   As a marketing manager, use your live app to submit a recognition request.

## Tutorial scenario

You're a manager with a rapidly expanding team. To date, the team has exceeded its goals every quarter. You want to reward them and provide gift cards as part of that recognition. However, securing approval for monetary awards is an intricate process that can span hours and involve repetitive interaction with many systems and upper management.

To tackle this issue, you check in with the IT admin and confirm that you can create an app to request gift cards. The admin is happy to help you make a new end-to-end app that draws on existing business process knowledge. To enable this, the admin adds you to the Creator Studio Users group in their non-production instance.

**Note:** To complete this tutorial, you must log in to Creator Studio as two different users or impersonate two users: one in the Creator Studio Users group and one admin.

It's time for you to get started on creating a simple app.

## Tutorial part 1: Create the app

Begin by creating an app from the Creator Studio home page.

### Before you begin

Role required: Creator Studio User

### About this task

You can also watch a short video on how to create an app.

Video on how to create an app 

### Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio**.

    ![Select the All menu and search for Creator Studio](../image/crs-all-menu-callouts.png "Start Creator Studio")

2.  Select the **Create app** button.

    ![Select the Create app button](../image/crs-tutorial-create-app-button.png "Create app button")

    -   If you're a system administrator, you can read more about this topic in [Application collaboration](../../applications/concept/application-collaboration.md).
    -   If you want to know how to request an admin to create the app for you, check out [Ask an admin to create an app for you in Creator Studio](../task/creator-studio-request-app-added.md).
3.  Select the type of app you want to build, such as **Service Desk**.

    Service Desk apps enable users to submit requests, report issues, and access support related to services within your company.

    **Note:** Your admin may have hidden this page.

    ![Within the Creator Studio interface, select the "Service Desk" app option. This type of app is designed to streamline the management of incoming requests or support tickets.](../image/crs-interstitial-sd.png "Select the app type")

4.  Select the **Continue** button.

5.  Enter the following values on the Create app page.

    |Field|Value|
    |-----|-----|
    |Name|`Gift Card Request`|
    |Description|`Request an internal or third party gift card for employee recognition.`|

    ![Enter app name and description](../image/crs-tutorial-create-app-nav.png "Add Gift card request app basic details")

6.  Select the **Create app** button.


### What to do next

Next, let's add a form to your app.

## Tutorial part 2: Add a form

Adding a form enables people to make a request. Forms contain questions that people respond to when submitting a service desk request.

### Before you begin

Role required: Creator Studio User

### Procedure

1.  Select **+Add form** within the app.

    You can select **+Add form** in either the navigation panel or the app canvas.

    ![Select + Add form to start adding a form](../image/crs-add-form-nav.png "Start adding a form")

2.  Verify on the template page that the **Creator Studio Default Template** is selected.

    ![Select the default template and then select Apply](../image/crs-tutorial-template-select.png "Select the template")

3.  Select the **Apply template and continue** button.

    Next, let's customize the form by adding questions.


## Tutorial part 3: Customize the form

Customize the form for the gift card request app by manually entering questions. When it's done, you can mark the form as ready to be published.

### Before you begin

Role required: Creator Studio User

### About this task

You can also use Now Assist for Creator on the **Build with Now Assist** tab to customize a form. But for this tutorial, you will manually enter questions.

### Procedure

1.  Select the **Build on your own** tab.

2.  Enter the following information for the form:

    |Field|Value|
    |-----|-----|
    |Form name|`Gift card request`|
    |Short description|`Request an internal or third party gift card for employee recognition.`|
    |Long description|`Looking for a great way to recognize your colleagues? Use this form to request a gift card to our internal company store or to a third party store of your choice!`|

    ![Form name, short and long descriptions](../image/crs-tutorial-add-form-info-nav.png "Enter form details")

    **Note:** This page enables you to specify details for your first form. You can also edit the form details, such as name and description, from inside the app after the form is generated.

3.  Select the **Save and edit form** button.

    Next, we'll work on the contents of the form.

4.  Add an icon to spiff up your form by selecting the icon and uploading an appropriate image.

    You can use any image that you like.

    ![Select the image icon to upload an image](../image/crs-tut-add-image.png "Add an image")

    1.  Select the add image icon \(![](../image/crs-tut-add-image-icon.png)\).

    2.  Search for and choose your image to add to the form.

5.  Create your first question that enables users to order the gift card.

    1.  Select **Question 1**.

    2.  Enter the following values in the Question details panel that appears:

        |Field|Value|
        |-----|-----|
        |Question label|`Company store gift card?`|
        |Content type|**Yes or no**|
        |Show question on form|Select this option|
        |Mark as required|Select this option|

        ![Specify values to create the first question, and then save](../image/crs-tut-question1.png "Add the first question")

    3.  Select the **Save** button.

6.  Create the second question to specify the amount of the gift card.

    1.  Select **Question 2**.

    2.  Enter the following values in the Question details panel that appears:

        |Field|Value|
        |-----|-----|
        |Question label|`Amount`|
        |Content type|Leave selected as **Single-line text**|
        |Show question on form|Select this option|
        |Mark as required|Select this option|

        ![Specify values to create the second question, and then save](../image/crs-tut-question2.png "Add the second question")

    3.  Select the **Save** button.

7.  Create the third question that defines who the gift card recipient will be.

    1.  Select **Question 3**.

    2.  Enter the following values in the Question details panel that appears:

        |Field|Value|
        |-----|-----|
        |Question label|`Recipient`|
        |Content type|**Record choices**|
        |Show question on form|Select this option|
        |Source table|`User (sys_user)`|

        ![Specify values to create the third question, and then save](../image/crs-tut-question3.png "Add the third question")

    3.  Select the **Save** button.

8.  Add a fourth question so that users can enter a justification for the gift card.

    1.  Drag the **Multi-line text** form element to add it to the form below the third question.

    2.  Enter the following values in the Question details panel that appears:

        |Field|Value|
        |-----|-----|
        |Question label|`Justification`|
        |Content type|Leave as **Multi-line text**|
        |Show question on form|Select this option|

        ![Specify values to create the fourth question, and then save](../image/crs-tut-question4.png "Add the fourth question")

    3.  Select the **Save** button.

9.  Select **Mark as ready** to publish the form.

    When you finish editing a form, you mark it as ready, which puts it in the Published state. This version of the form then appears in its specified catalog of items.

    **Note:** The published form appears only on the non-production instance where you're developing your app. You must request that your admin deploy the app to production for the form to appear in the catalog on the production instance.

    ![Select the Mark as ready button](../image/crs-tut-mark-ready.png "Mark a form as ready")

10. Specify where users can access the form in the Service Catalog and Employee Center.

    1.  Select the **Edit location setting** button.

        ![Warning to edit location](../image/crs-tutorial-location-form1.png "Edit location settings warning")

    2.  Select the **Edit** button to add the form to a Service Catalog topic.

        ![Edit the categories](../image/crs-tut-catgory-select.png "Form settings modal")

    3.  Select the catalog that represents the business area the app will use.

        For example, you can expand the **Service Catalog** and then select the **Can we help you?** category.

        ![Select where the form will appear](../image/crs-tut-catalog-select-cat.png "Form settings modal catalogs")

    4.  Select the **Apply** button to save your changes.

    5.  Select the **Edit** button to add the form to an Employee Center topic.

        ![Select Employee Center topics](../image/crs-tutorial-location-form2.png "Select topics in the Employee Center topic")

    6.  Choose the section of the Employee Center where the form will live.

        ![Select where the topic will live](../image/crs-tutorial-location-form3.png "Select the Employee Center topic")

11. Select the **Apply** button.

12. Select the **Save all settings** button to save your changes.

    ![Save all settings on the location](../image/crs-tutorial-location-form4.png "Save all location settings")

13. See how the form will look by selecting the **Preview** button.

    You can see a preview of the how the current version of the form will appear in various experiences by selecting **Portal** \(such as Employee Portal\), **Now Mobile**, or **Virtual Agent**. You can fill in the form when previewing, but selecting the **Submit** button doesn't generate a task record.

    ![Preview how a form looks on mobile](../image/crs-preview-mobile.png "Preview a form")


## Tutorial part 4:Add an automated playbook

Add a playbook that uses the form that you just created to automate approval for the gift card request app.

### Before you begin

Role required: Creator Studio User

### Procedure

1.  Select **+ Add automation** for the Gift card request form.

    ![Select + Add automation under the form](../image/crs-tut-add-auto-link.png "Select to add an automation")

2.  Enter the following values in the Create a playbook modal:

    |Field|Value|
    |-----|-----|
    |Playbook name|`Gift card approvals`|
    |Description|`Route approvals when a gift card is requested.`|
    |Form|Make sure the name of the form that you created \(**Gift card request**\) is selected.|
    |Trigger|Leave the trigger as **Form submitted**.|

    ![Enter details for the playbook](../image/crs-tut-playbook-details.png "Enter playbook details")

3.  Select the **Create** button.

4.  Add the manager approval activity.

    1.  Select the add icon \(![](../image/cs-add-icon.png)\).

        ![Select the plus sign to add an activity](../image/crs-tut-playbook-plus.png "Add manager approval activity: Step 1")

    2.  Select the Add an activity icon \(![](../image/cs-add-activity-icon.png)\).

        ![Select the square to add an activity](../image/crs-tut-playbook-step2.png "Add manager approval activity: Step 2")

    3.  Select the **Request approval** activity.

        ![Select to add a Request approval activity](../image/crs-tut-playbook-step3-zs2.png "Add manager approval activity: Step 3")

        The Request approval properties panel appears, where you can define the activity.

    4.  Enter the following activity details.

        |Field|Value|
        |-----|-----|
        |Label|`Request manager approval`|
        |Requester's manager|Select this option.|
        |Approval type|Leave as **Anyone approves**.|
        |Conditions|Select **When playbook starts**.|

        ![Enter details to define the activity](../image/crs-tut-playbook-step4.png "Request manager approval details")

    5.  Select **Save and close**.

5.  Add the finance approval activity.

    1.  Select the add icon \(![](../image/cs-add-icon.png)\).

        ![Select the plus sign to add an activity](../image/crs-tut-playbook-step5.png "Add finance approval activity: Step 1")

    2.  Select the add an activity icon \(![](../image/cs-add-activity-icon.png)\).

        ![Select the square to add an activity](../image/crs-tut-playbook-step6.png "Add finance approval activity: Step 2")

    3.  Select the **Request approval** activity.

        ![Select to add a Request approval activity](../image/crs-tut-playbook-step7.png "Add finance approval activity: Step 3")

        The Request approval properties panel appears, where you can define the activity.

    4.  Enter the following activity details.

        |Field|Value|
        |-----|-----|
        |Label|Enter `Request finance approval`.|
        |Group|Select this option.|
        |Group|Enter `Finance group`.|
        |Approval type|Leave as **Anyone approves**.|
        |Conditions|Leave as **After specific activity** with **Request manager approval** selected.|

        ![Enter details to define the activity](../image/crs-tut-playbook-step8.png "Request finance approval details")

    5.  Select **Save and close**.

6.  Activate the playbook so that it can run when the form is submitted by selecting the **Activate** button.

    ![Select the Activate button](../image/crs-tut-playbook-step9.png "Activate the playbook")


### Result

Great! You've finished adding a playbook. Next, you can customize the workspace configuration where fulfillers work on submitted requests.

## Tutorial part 5: Customize the fulfillment workspace configuration

Customize the lists and submitted records in the workspace where fulfillers can process gift card requests from the. In this list customization, you add a column to view the assignment group.

### Before you begin

Role required: Creator Studio User

### Procedure

1.  Select the **List configurations** section in the navigation panel.

    ![Select List configurations](../image/crs-tut-lists-step1.png "List configurations in the navigation panel")

2.  Add the assignment group to the workspace.

    1.  Select the **Manage columns** link in the Filtered list details panel.

        ![Select to manage columns](../image/crs-tut-lists-step2.png "Manage columns link")

    2.  Search for `Assignment group` in the Available columns.

    3.  Select the **Assignment group**.

        ![Add a column and select Apply](../image/crs-tutorial-form-sub-select-col.png "Manage the columns to add a column")

    4.  Select the **Apply** button.

    5.  Select the **Save** button in the Filtered list details panel.

        ![Select Save to save changes](../image/crs-tut-lists-step3.png "Save changes to workspace configuration")


### Result

That's it, you've built an app! Now it's time to submit it for review and deployment.

## Tutorial part 6:Test and submit the app for review

Test your app and then request that an admin review and deploy the app to production.

### Before you begin

A pipeline for deployment must be configured before you can submit the gift card app for review.

Role required: Creator Studio User

### Procedure

1.  Test how the app works to make sure that it's ready by selecting the **Try it** button.

    1.  Select the **Gift card request** form from the navigation panel.

        ![Select Gift card request form in navigation panel](../image/crs-tut-submit-step1.png "Select the form to test it")

    2.  Select the **Try it** button.

        ![Select Try it](../image/crs-tut-submit-step2.png "Try it button")

    3.  Complete the form by entering the following values for each field.

        |Field|Value|
        |-----|-----|
        |Company gift store card?|`Yes`|
        |Amount|`20.00`|
        |Recipient|Choose a recipient from the list of people.|
        |Justification|`Onboarding a cool new person for our team!`|

        ![Enter responses onto the form](../image/crs-tut-submit-step3.png "Test the form")

    4.  Select the **Submit** button when you're done.

    After you submit your responses, the ServiceNow AI Platform runs any playbooks associated with the form.

    The record that your submitted form creates appears in Creator Studio. You can view the results of the playbooks and interact with the record to see how it appears in the Request App Workspace.

    ![Submitted record in Creator Studio](../image/crs-tut-submit-step4.png "View the submitted record")

2.  Select the **Submit for review** button.

    ![Select the submit for review button](../image/crs-tut-submit-step5.png "Submit an app for review")

3.  Select **Continue** on the Submit app for review modal.

    ![Initial submit for review modal](../image/crs-tutorial-sub-review1.png "Start the submit for review process")

4.  Check the form to be reviewed for deployment in the Review request forms modal.

    1.  Expand the **Ready for review** section.

    2.  Ensure that the **Visible to others** option is selected for the **Gift Card Request** form.

    3.  Select **Continue**.

    ![Review the form to be deployed with the app](../image/crs-tutorial-sub-review2.png "Check the form to be deployed")

5.  Check the form to be reviewed for deployment in the Review playbooks modal.

    1.  Expand the **Playbooks** section.

    2.  Ensure that the **Run on production** option is selected for the **Gift card approvals** form.

    3.  Select **Continue**.

    ![Review the playbook to be deployed with the app](../image/crs-tutorial-sub-review3.png "Check the playbook to be deployed")

6.  Confirm that the information in the Review versioning modal is correct, and add the **Release notes**.

    ![Add release notes and submit for review](../image/crs-tutorial-sub-review-4.png "Check and update release version and submit for review")

7.  Select **Submit for review**.


### Result

Congratulations, you have created your gift card request app! Now your admin must review and deploy it.

![Confirmation message modal](../image/crs-tutorial-sub-review-5.png "Confirmation of review submission")

## Tutorial part 7:Admin deploys the app

Impersonate an admin to deploy the gift card request app that you created.

### Before you begin

If you can't impersonate an admin, ask your local admin to deploy the app for you.

Role required: admin

### Procedure

1.  In the ServiceNow AI Platform application banner, select your profile icon and impersonate an admin.

2.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Management Center**.

3.  Select the number **1** in the Pending requests to complete section.

    ![Select the 1](../image/crs-tutorial-deploy1.png "Apps ready for deployment")

4.  Open the deployment record by selecting its **Number**.

    ![Select the Number](../image/crs-tutorial-deploy2.png "List of apps to deploy")

5.  Select the **Approve** button.

    ![Select Approve](../image/crs-tutorial-deploy4.png "Approve button for deployment")

6.  Select **Save**.

7.  Reload the page.

8.  Select the **Approve and deploy app** button.

    ![Select Approve and deploy](../image/crs-tutorial-deploy5.png "Approve and deploy button for deployment")

9.  Select the **Deploy** button.

    ![Select Deploy](../image/crs-tutorial-deploy6.png "Deploy the app")


### Result

The app has been deployed to production. Select **Show more** in the activity section if you want to view details for the app.

![Select Show more](../image/crs-tutorial-deploy7.png "Verify the deployment details")

You can end the admin impersonation now.

## Tutorial part 8:Use the app to request a gift card

Use the deployed gift card request app that you just created to request a gift card.

### Before you begin

Role required: ServiceNow AI Platform user

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

    ![Use the All menu to open Employee Center](../image/crs-tutorial-view-app1.png "Open Employee Center")

2.  Search for `Gift card request` in the search bar.

    ![Enter "gift card request" in the search bar](../image/crs-tutorial-view-app2.png "Search for the Gift card request app")

3.  Select the **Gift card request** app that appears in the search results.

    ![Select the app to open it](../image/crs-tutorial-view-app3.png "Open the app")

4.  Fill out the gift card request form to request a gift card.

    ![Fill out the app's form](../image/crs-tutorial-view-app4.png "Request a gift card")

5.  Select the **Submit** button.


## Tutorial part 9:Verify the gift card request

Verify that your app is working by checking the Request App Workspace to view the gift card request that you submitted.

### Before you begin

Role required: admin or the app's agent role, for example, x\_snc\_app\_name.agent

### Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Request App Workspace**.

    ![Use the All menu to open the workspace](../image/crs-tutorial-workspace1.png "Open the Request App Workspace")

2.  Find the gift card request that you submitted and select its **Number** to open it.

3.  View the gift card request details.

    ![Gift card request details](../image/crs-tut-workspace2.png "Gift card request details")


### Result

Hooray! You have completed the gift card request app tutorial.

