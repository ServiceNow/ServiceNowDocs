---
title: Using the Request App Workspace to fulfill requests
description: After users submit a request through an app built in Creator Studio, fulfillers work on the request's submitted record in the Request App Workspace.
locale: en-US
release: australia
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure workspace lists and records, Build apps, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Using the Request App Workspace to fulfill requests

After users submit a request through an app built in Creator Studio, fulfillers work on the request's submitted record in the Request App Workspace.

## The Request App Workspace holds app requests

The Request App Workspace holds form submissions that come in from each of your apps. [Fulfillers](creator-studio-glossary.md#) \(remember, these are the people who work on requests\) can access the workspace through the ServiceNow AI Platform and see submissions for all the apps they're assigned to.

There is only one Request App Workspace per instance. Each app that you build in Creator Studio has its own category in the Request App Workspace, with as many lists as you configure, regardless of how many forms or automations it has.

Fulfillers access the default workspace on the ServiceNow AI Platform by going to **All** &gt; **App Engine** &gt; **Request App Workspace**. The Request App Workspace displays a category for each app with filtered lists of records, both default and any extra that you added. Fulfillers then select a record to view the details of the request and make updates as needed.

**Note:** To access the Request App Workspace, you must have a fulfiller role for the app built in Creator Studio. For example, x\_snc\_it\_req.agent for an app with the scope x\_snc\_it\_req.

Each app has its own section in the workspace, with lists to filter for submitted request records in various states.

## Using lists to find tickets in various states

Each app's section contains lists, such as **Open** requests and any lists the admin or app creator configured. Fulfillers can use the "My Lists" feature in Workspace to create custom lists that fit their needs. Tell them how to by checking out [ServiceNow AI Platform® list administration](https://www.servicenow.com/docs/access?context=p_ListAdministration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

![All Requests list showing open requests with columns for number, priority, state, assigned to, short description, and task type.](../image/crs-form-sub-workspace.png "Request App Workspace")

The Lists view contains two tabs: **Default Lists** and **My Lists**.

## Using dashboards to analyze request fulfillment

The Dashboard overview view contains a dashboard for every app \(that you have access to\) that was made in Creator Studio.

You can select an app's dashboard to see analysis of all active tasks, as well as the number of records in various states configured by your admin. For more information on working with analytics dashboards, see [Dashboards in Platform Analytics](https://www.servicenow.com/docs/access?context=analytics-center-dashboards&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)

## Working on open requests in the workspace

After you find the subset of requests you need, such as open requests assigned to you, you can select the task record **Name** to open the record.After you find the subset of requests you need, such as open requests assigned to you, you can select the record **Name** to open the record.

![Open request record in the workspace](../image/crs-workspace-record.png "Request record in the Request App Workspace")

The submitted request record has various tabs that help you do your work.

**Parent Topic:**[Configuring workspace lists and records for form submissions](creator-studio-form-submissions-workspace-about.md)

