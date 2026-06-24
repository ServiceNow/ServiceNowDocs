---
title: Creator Studio tutorial
description: Use this tutorial to create a Gift Card Request app to streamline the processes of providing recognition to a team.Begin by creating an app from the Creator Studio home page.Adding a form enables people to make a request. Forms contain questions that people respond to when submitting a service desk request.Customize the form for the gift card request app by manually entering questions. When it's done, you can mark the form as ready to be published.Add a playbook that uses the form that you just created to automate approval for the gift card request app.Customize the lists and submitted records in the workspace where fulfillers can process gift card requests from the. In this list customization, you add a column to view the assignment group.Test your app and then request that an admin review and deploy the app to production.Impersonate an admin to deploy the gift card request app that you created.Use the deployed gift card request app that you just created to request a gift card.Verify that your app is working by checking the Request App Workspace to view the gift card request that you submitted.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/creator-studio/creator-studio-tutorial-landing.html
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

    \[Omitted image "crs-all-menu-callouts.png"\] Alt text: Select the All menu and search for Creator Studio

2.  Select the **Create app** button.

    \[Omitted image "crs-tutorial-create-app-button.png"\] Alt text: Select the Create app button

    -   If you're a system administrator, you can read more about this topic in [Application collaboration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/application-collaboration.md).
    -   If you want to know how to request an admin to create the app for you, check out [Ask an admin to create an app for you in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/creator-studio/creator-studio-request-app-added.md).
3.  Select the type of app you want to build, such as **Service Desk**.

    Service Desk apps enable users to submit requests, report issues, and access support related to services within your company.

    **Note:** Your admin may have hidden this page.

    \[Omitted image "crs-interstitial-sd.png"\] Alt text: Within the Creator Studio interface, select the "Service Desk" app option. This type of app is designed to streamline the management of incoming requests or support tickets.

4.  Select the **Continue** button.

5.  Enter the following values on the Create app page.

    |Field|Value|
    |-----|-----|
    |Name|`Gift Card Request`|
    |Description|`Request an internal or third party gift card for employee recognition.`|

    \[Omitted image "crs-tutorial-create-app-nav.png"\] Alt text: Enter app name and description

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

    \[Omitted image "crs-add-form-nav.png"\] Alt text: Select + Add form to start adding a form

2.  Verify on the template page that the **Creator Studio Default Template** is selected.

    \[Omitted image "crs-tutorial-template-select.png"\] Alt text: Select the default template and then select Apply

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

    \[Omitted image "crs-tutorial-add-form-info-nav.png"\] Alt text: Form name, short and long descriptions

    **Note:** This page enables you to specify details for your first form. You can also edit the form details, such as name and description, from inside the app after the form is generated.

3.  Select the **Save and edit form** button.

    Next, we'll work on the contents of the form.

4.  Add an icon to spiff up your form by selecting the icon and uploading an appropriate image.

    You can use any image that you like.

    \[Omitted image "crs-tut-add-image.png"\] Alt text: Select the image icon to upload an image

    1.  Select the add image icon \(\[Omitted image "crs-tut-add-image-icon.png"\] Alt text:\).

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

        \[Omitted image "crs-tut-question1.png"\] Alt text: Specify values to create the first question, and then save

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

        \[Omitted image "crs-tut-question2.png"\] Alt text: Specify values to create the second question, and then save

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

        \[Omitted image "crs-tut-question3.png"\] Alt text: Specify values to create the third question, and then save

    3.  Select the **Save** button.

8.  Add a fourth question so that users can enter a justification for the gift card.

    1.  Drag the **Multi-line text** form element to add it to the form below the third question.

    2.  Enter the following values in the Question details panel that appears:

        |Field|Value|
        |-----|-----|
        |Question label|`Justification`|
        |Content type|Leave as **Multi-line text**|
        |Show question on form|Select this option|

        \[Omitted image "crs-tut-question4.png"\] Alt text: Specify values to create the fourth question, and then save

    3.  Select the **Save** button.

9.  Select **Mark as ready** to publish the form.

    When you finish editing a form, you mark it as ready, which puts it in the Published state. This version of the form then appears in its specified catalog of items.

    **Note:** The published form appears only on the non-production instance where you're developing your app. You must request that your admin deploy the app to production for the form to appear in the catalog on the production instance.

    \[Omitted image "crs-tut-mark-ready.png"\] Alt text: Select the Mark as ready button

10. Specify where users can access the form in the Service Catalog and Employee Center.

    1.  Select the **Edit location setting** button.

        \[Omitted image "crs-tutorial-location-form1.png"\] Alt text: Warning to edit location

    2.  Select the **Edit** button to add the form to a Service Catalog topic.

        \[Omitted image "crs-tut-catgory-select.png"\] Alt text: Edit the categories

    3.  Select the catalog that represents the business area the app will use.

        For example, you can expand the **Service Catalog** and then select the **Can we help you?** category.

        \[Omitted image "crs-tut-catalog-select-cat.png"\] Alt text: Select where the form will appear

    4.  Select the **Apply** button to save your changes.

    5.  Select the **Edit** button to add the form to an Employee Center topic.

        \[Omitted image "crs-tutorial-location-form2.png"\] Alt text: Select Employee Center topics

    6.  Choose the section of the Employee Center where the form will live.

        \[Omitted image "crs-tutorial-location-form3.png"\] Alt text: Select where the topic will live

11. Select the **Apply** button.

12. Select the **Save all settings** button to save your changes.

    \[Omitted image "crs-tutorial-location-form4.png"\] Alt text: Save all settings on the location

13. See how the form will look by selecting the **Preview** button.

    You can see a preview of the how the current version of the form will appear in various experiences by selecting **Portal** \(such as Employee Portal\), **Now Mobile**, or **Virtual Agent**. You can fill in the form when previewing, but selecting the **Submit** button doesn't generate a task record.

    \[Omitted image "crs-preview-mobile.png"\] Alt text: Preview how a form looks on mobile


## Tutorial part 4:Add an automated playbook

Add a playbook that uses the form that you just created to automate approval for the gift card request app.

### Before you begin

Role required: Creator Studio User

### Procedure

1.  Select **+ Add automation** for the Gift card request form.

    \[Omitted image "crs-tut-add-auto-link.png"\] Alt text: Select + Add automation under the form

2.  Enter the following values in the Create a playbook modal:

    |Field|Value|
    |-----|-----|
    |Playbook name|`Gift card approvals`|
    |Description|`Route approvals when a gift card is requested.`|
    |Form|Make sure the name of the form that you created \(**Gift card request**\) is selected.|
    |Trigger|Leave the trigger as **Form submitted**.|

    \[Omitted image "crs-tut-playbook-details.png"\] Alt text: Enter details for the playbook

3.  Select the **Create** button.

4.  Add the manager approval activity.

    1.  Select the add icon \(\[Omitted image "cs-add-icon.png"\] Alt text:\).

        \[Omitted image "crs-tut-playbook-plus.png"\] Alt text: Select the plus sign to add an activity

    2.  Select the Add an activity icon \(\[Omitted image "cs-add-activity-icon.png"\]\).

        \[Omitted image "crs-tut-playbook-step2.png"\] Alt text: Select the square to add an activity

    3.  Select the **Request approval** activity.

        \[Omitted image "crs-tut-playbook-step3-zs2.png"\] Alt text: Select to add a Request approval activity

        The Request approval properties panel appears, where you can define the activity.

    4.  Enter the following activity details.

        |Field|Value|
        |-----|-----|
        |Label|`Request manager approval`|
        |Requester's manager|Select this option.|
        |Approval type|Leave as **Anyone approves**.|
        |Conditions|Select **When playbook starts**.|

        \[Omitted image "crs-tut-playbook-step4.png"\] Alt text: Enter details to define the activity

    5.  Select **Save and close**.

5.  Add the finance approval activity.

    1.  Select the add icon \(\[Omitted image "cs-add-icon.png"\]\).

        \[Omitted image "crs-tut-playbook-step5.png"\] Alt text: Select the plus sign to add an activity

    2.  Select the add an activity icon \(\[Omitted image "cs-add-activity-icon.png"\]\).

        \[Omitted image "crs-tut-playbook-step6.png"\] Alt text: Select the square to add an activity

    3.  Select the **Request approval** activity.

        \[Omitted image "crs-tut-playbook-step7.png"\] Alt text: Select to add a Request approval activity

        The Request approval properties panel appears, where you can define the activity.

    4.  Enter the following activity details.

        |Field|Value|
        |-----|-----|
        |Label|Enter `Request finance approval`.|
        |Group|Select this option.|
        |Group|Enter `Finance group`.|
        |Approval type|Leave as **Anyone approves**.|
        |Conditions|Leave as **After specific activity** with **Request manager approval** selected.|

        \[Omitted image "crs-tut-playbook-step8.png"\] Alt text: Enter details to define the activity

    5.  Select **Save and close**.

6.  Activate the playbook so that it can run when the form is submitted by selecting the **Activate** button.

    \[Omitted image "crs-tut-playbook-step9.png"\] Alt text: Select the Activate button


### Result

Great! You've finished adding a playbook. Next, you can customize the workspace configuration where fulfillers work on submitted requests.

## Tutorial part 5: Customize the fulfillment workspace configuration

Customize the lists and submitted records in the workspace where fulfillers can process gift card requests from the. In this list customization, you add a column to view the assignment group.

### Before you begin

Role required: Creator Studio User

### Procedure

1.  Select the **List configurations** section in the navigation panel.

    \[Omitted image "crs-tut-lists-step1.png"\] Alt text: Select List configurations

2.  Add the assignment group to the workspace.

    1.  Select the **Manage columns** link in the Filtered list details panel.

        \[Omitted image "crs-tut-lists-step2.png"\] Alt text: Select to manage columns

    2.  Search for `Assignment group` in the Available columns.

    3.  Select the **Assignment group**.

        \[Omitted image "crs-tutorial-form-sub-select-col.png"\] Alt text: Add a column and select Apply

    4.  Select the **Apply** button.

    5.  Select the **Save** button in the Filtered list details panel.

        \[Omitted image "crs-tut-lists-step3.png"\] Alt text: Select Save to save changes


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

        \[Omitted image "crs-tut-submit-step1.png"\] Alt text: Select Gift card request form in navigation panel

    2.  Select the **Try it** button.

        \[Omitted image "crs-tut-submit-step2.png"\] Alt text: Select Try it

    3.  Complete the form by entering the following values for each field.

        |Field|Value|
        |-----|-----|
        |Company gift store card?|`Yes`|
        |Amount|`20.00`|
        |Recipient|Choose a recipient from the list of people.|
        |Justification|`Onboarding a cool new person for our team!`|

        \[Omitted image "crs-tut-submit-step3.png"\] Alt text: Enter responses onto the form

    4.  Select the **Submit** button when you're done.

    After you submit your responses, the ServiceNow AI Platform runs any playbooks associated with the form.

    The record that your submitted form creates appears in Creator Studio. You can view the results of the playbooks and interact with the record to see how it appears in the Request App Workspace.

    \[Omitted image "crs-tut-submit-step4.png"\] Alt text: Submitted record in Creator Studio

2.  Select the **Submit for review** button.

    \[Omitted image "crs-tut-submit-step5.png"\] Alt text: Select the submit for review button

3.  Select **Continue** on the Submit app for review modal.

    \[Omitted image "crs-tutorial-sub-review1.png"\] Alt text: Initial submit for review modal

4.  Check the form to be reviewed for deployment in the Review request forms modal.

    1.  Expand the **Ready for review** section.

    2.  Ensure that the **Visible to others** option is selected for the **Gift Card Request** form.

    3.  Select **Continue**.

    \[Omitted image "crs-tutorial-sub-review2.png"\] Alt text: Review the form to be deployed with the app

5.  Check the form to be reviewed for deployment in the Review playbooks modal.

    1.  Expand the **Playbooks** section.

    2.  Ensure that the **Run on production** option is selected for the **Gift card approvals** form.

    3.  Select **Continue**.

    \[Omitted image "crs-tutorial-sub-review3.png"\] Alt text: Review the playbook to be deployed with the app

6.  Confirm that the information in the Review versioning modal is correct, and add the **Release notes**.

    \[Omitted image "crs-tutorial-sub-review-4.png"\] Alt text: Add release notes and submit for review

7.  Select **Submit for review**.


### Result

Congratulations, you have created your gift card request app! Now your admin must review and deploy it.

\[Omitted image "crs-tutorial-sub-review-5.png"\] Alt text: Confirmation message modal

## Tutorial part 7:Admin deploys the app

Impersonate an admin to deploy the gift card request app that you created.

### Before you begin

If you can't impersonate an admin, ask your local admin to deploy the app for you.

Role required: admin

### Procedure

1.  In the ServiceNow AI Platform application banner, select your profile icon and impersonate an admin.

2.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Management Center**.

3.  Select the number **1** in the Pending requests to complete section.

    \[Omitted image "crs-tutorial-deploy1.png"\] Alt text: Select the 1

4.  Open the deployment record by selecting its **Number**.

    \[Omitted image "crs-tutorial-deploy2.png"\] Alt text: Select the Number

5.  Select the **Approve** button.

    \[Omitted image "crs-tutorial-deploy4.png"\] Alt text: Select Approve

6.  Select **Save**.

7.  Reload the page.

8.  Select the **Approve and deploy app** button.

    \[Omitted image "crs-tutorial-deploy5.png"\] Alt text: Select Approve and deploy

9.  Select the **Deploy** button.

    \[Omitted image "crs-tutorial-deploy6.png"\] Alt text: Select Deploy


### Result

The app has been deployed to production. Select **Show more** in the activity section if you want to view details for the app.

\[Omitted image "crs-tutorial-deploy7.png"\] Alt text: Select Show more

You can end the admin impersonation now.

## Tutorial part 8:Use the app to request a gift card

Use the deployed gift card request app that you just created to request a gift card.

### Before you begin

Role required: ServiceNow AI Platform user

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

    \[Omitted image "crs-tutorial-view-app1.png"\] Alt text: Use the All menu to open Employee Center

2.  Search for `Gift card request` in the search bar.

    \[Omitted image "crs-tutorial-view-app2.png"\] Alt text: Enter "gift card request" in the search bar

3.  Select the **Gift card request** app that appears in the search results.

    \[Omitted image "crs-tutorial-view-app3.png"\] Alt text: Select the app to open it

4.  Fill out the gift card request form to request a gift card.

    \[Omitted image "crs-tutorial-view-app4.png"\] Alt text: Fill out the app's form

5.  Select the **Submit** button.


## Tutorial part 9:Verify the gift card request

Verify that your app is working by checking the Request App Workspace to view the gift card request that you submitted.

### Before you begin

Role required: admin or the app's agent role, for example, x\_snc\_app\_name.agent

### Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Request App Workspace**.

    \[Omitted image "crs-tutorial-workspace1.png"\] Alt text: Use the All menu to open the workspace

2.  Find the gift card request that you submitted and select its **Number** to open it.

3.  View the gift card request details.

    \[Omitted image "crs-tut-workspace2.png"\] Alt text: Gift card request details


### Result

Hooray! You have completed the gift card request app tutorial.

