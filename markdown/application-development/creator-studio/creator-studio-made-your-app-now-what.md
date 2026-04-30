---
title: I've built my app in Creator Studio, now what?
description: You've added forms and automation to your app, and customized the form submission workspace. Now what?
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [app faq, creator studio faq]
breadcrumb: [Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# I've built my app in Creator Studio, now what?

You've added forms and automation to your app, and customized the form submission workspace. Now what?

## What happens after I submit my app for review?

When you finish creating your app and select to **Submit for review**, your admin gets a deployment request. They then review your app deployment request and move the app to production.

After the app is deployed to production, the forms are available on the ServiceNow AI Platform.

## Where do I find my app after it's deployed?

After deployment, your app lives as forms in the Service Catalog and categories you specified when creating the forms.

Users can access those forms directly in Service Catalog, as well as Service Portal and Employee Center.

If you associate the app's form with one or more topics, the form will appear in the relevant, dynamically created topic pages in Employee Center. Find out more about topics in [Associate a catalog item with a taxonomy topic in Employee Center](https://www.servicenow.com/docs/access?context=associate-cat-item-taxonomy-ec&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US), and more about taxonomy, which is a categorization method, in [Unified Taxonomy for Employee Center](https://www.servicenow.com/docs/access?context=config-taxonomy&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

## Where do fulfillers work on submitted forms?

Fulfillers access the default workspace on the ServiceNow AI Platform by going to **All** &gt; **App Engine** &gt; **Request App Workspace**. The Request App Workspace displays a category for each app with filtered lists of records, both default and any extra that you added. Fulfillers then select a record to view the details of the request and make updates as needed.

**Note:** You can't access the Request App Workspace as the owner of an app, though you can access it if you also have an admin or the applicable agent role. The app's agent role is &lt;app scope&gt;.agent, for example, x\_snc\_app\_name.agent.

![Fulfillers work on requests in the workspace](../image/cs-form-sub-workspace.png "Form submission workspace")

You can also preview and interact with how records will appear in the Request App Workspace directly within Creator Studio.

![Request App Workspace record preview within Creator Studio](../image/crs-wkspce-preview-record.png "Previewing how a record will appear")

## Can I continue developing my app in other ServiceNow AI Platform builders?

You can open Creator Studio apps in other builders. For example, open it in App Engine Studio to add more experiences or complex automations.

## Get help and check out the FAQs

Got more questions? Take a look at the [Creator Studio FAQs on the Community site](https://www.servicenow.com/community/creator-studio-blogs/creator-studio-faqs/ba-p/2947282)!

You can also [watch a quick video on how to contact your admin and check out some helpful resources](creator-studio-get-help-now.md).

-   **[Closing requests and app notifications in Creator Studio](creator-studio-closing-requests-and-notifications.md)**  
The records that your app creates when a form is completed are not automatically closed, and some notifications are not automatic and must be configured.

**Parent Topic:**[Building apps with Creator Studio](building-apps-with-creator-studio.md)

