---
title: Configuring workspace lists and records for form submissions
description: So, you’ve built your app, and people are submitting requests through it, that’s great! However, you might be wondering where those requests go after they’re submitted. They live in lists in a workspace where fulfillers can work on submitted forms, which you can customize in Creator Studio to suit your needs.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Configuring workspace lists and records for form submissions

So, you’ve built your app, and people are submitting requests through it, that’s great! However, you might be wondering where those requests go after they’re submitted. They live in lists in a workspace where fulfillers can work on submitted forms, which you can customize in Creator Studio to suit your needs.

## A little more about workspaces

The Request App Workspace holds form submissions that come in from each of your apps. [Fulfillers](creator-studio-glossary.md#) \(remember, these are the people who work on requests\) can access the workspace through the ServiceNow AI Platform and see submissions for all the apps they're assigned to.

There is only one Request App Workspace per instance. Each app that you build in Creator Studio has its own category in the Request App Workspace, with as many lists as you configure, regardless of how many forms or automations it has.

As the app owner, you’re responsible for the look and feel of the workspace lists that the app's fulfillers use. Thankfully, the workspace should be ready to use out-of-the-box, but you can also customize it on the **List configurations** section of your app's navigation panel in Creator Studio.

When you open the **List configurations** tab, you’ll see some filtered lists that appear in the default workspace. These filtered lists \(**Open**, **Open – Unassigned**, **Closed**, and **All**\) are intended to give fulfillers a quick view of all the form submissions. You can add more filtered lists as needed, for example, you could add a filtered list for each of the app's forms or for canceled requests.

If it would help your fulfillers to have additional categories, you must ask your admin to add them using the List Category \[sys\_ux\_list\_category\] table on the ServiceNow AI Platform.

![Customize the workspace in the List configurations section](../image/crs-list-configs-whole.png "List configurations section")

## Creating lists to support multiple forms

When fulfillers open the workspace to view an app's form submissions, the default "Open" list displays all open requests made through the app. However, if you have multiple forms in your app, fulfillers might find it easier to have separate "Open" lists for each form in the app. In that case, you should create a different list for each separate form and name each of them after the forms. Find out how in [Add a filtered list to a workspace in Creator Studio](../task/creator-studio-add-filtered-list.md).

Fulfillers can use the "My Lists" feature in Workspace to create custom lists that fit their needs. Tell them how to by checking out [ServiceNow AI Platform® list administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-administration/p_ListAdministration.md).

## How fulfillers access submitted forms

Fulfillers access the default workspace on the ServiceNow AI Platform by going to **All** &gt; **App Engine** &gt; **Request App Workspace**. The Request App Workspace displays a category for each app with filtered lists of records, both default and any extra that you added. Fulfillers then select a record to view the details of the request and make updates as needed.

**Note:** You can't access the Request App Workspace as the owner of an app, though you can access it if you also have an admin or the applicable agent role. The app's agent role is &lt;app scope&gt;.agent, for example, x\_snc\_app\_name.agent.

You can preview and interact with how records appear in the workspace category directly within Creator Studio by navigating to the **List categories** section of the navigation panel and selecting a record.

-   Answers to the form's questions \(which are catalog variables\) appear on the **Details** tab of the submitted record. For more on form questions, see [Working with forms in Creator Studio](creator-studio-work-with-forms.md).
-   Results of any playbooks appear on the **Automations** tab of the submitted record. For more on playbooks, see [Working with automation in Creator Studio](creator-studio-working-with-automations.md).

Edit how the record a form generates will appear by navigating to the **Record details** section of the navigation panel.

![Request App Workspace record preview within Creator Studio](../image/crs-record-preview-nav.png "Editing how a submitted record will appear")

What fulfillers can see in the workspace lists depends on their permissions. For example, admins can see workspace categories for all apps built in Creator Studio. However, most users see only the workspace category for their particular app.

![sc](../image/crs-form-sub-workspace.png "Request app workspace")

When fulfillers view a record for an individual request in the workspace, the **Catalog tasks** tab displays the playbook that you configured in Creator Studio.

Fulfillers or admins may also want to monitor the app’s performance as requests come in. This is where the **Dashboard overview** in the Request App Workspace is helpful! On the **Dashboard overview** tab, each app has its own analytics dashboard that shows applicable data, like how many open requests you have or what tasks are related to the app. There’s a lot of helpful information here. Find out more about working with data in [Platform Analytics overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-center.md).

-   **[Add a filtered list to a workspace in Creator Studio](../task/creator-studio-add-filtered-list.md)**  
Create custom filtered lists in the app submission workspace to view records that meet specific conditions. For example, if your app has multiple forms, you can create a list for each form by filtering on the record type.
-   **[Customize an app's workspace configuration in Creator Studio](../task/creator-studio-edit-workspace.md)**  
Make changes to the app's workspace category where fulfillers review submitted requests from apps built in Creator Studio to adjust how it appears. For example, you can rearrange columns in its lists and customize how the record generated by the request app looks.
-   **[Change the layout of an app's record in Creator Studio](../task/creator-studio-work-with-record-details.md)**  
Adjust how the submitted records that your app generates will look, such as the order in which fields appear.
-   **[Using the Request App Workspace to fulfill requests](creator-studio-request-app-workspace.md)**  
After users submit a request through an app built in Creator Studio, fulfillers work on the request's submitted record in the Request App Workspace.

**Parent Topic:**[Building apps with Creator Studio](building-apps-with-creator-studio.md)

