---
title: Planning your application
description: Plan out your application before building it to streamline the development process.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [App creation tutorial, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Planning your application

Plan out your application before building it to streamline the development process.

When you want to build an application, the first thing you should do is develop a plan for the app. Planning involves outlining what the application does and identifying who will use the application. By planning your application, you can better understand the purpose of your application and address potential issues before development begins.

This is the first step in the app creation tutorial. Follow along to develop a plan for an application that manages employee travel requests for an organization.

<table id="table_odl_xfd_fdc"><tbody><tr><td>

Step 1

</td><td align="justify">

![In progress icon](../image/app-tutorial-progress-wip.png)

</td><td>

[Planning your application](app-tutorial-introduction.md)

</td></tr><tr><td>

Step 2

</td><td align="justify">

![Not started icon](../image/app-tutorial-progress-not-started.png)

</td><td>

[Create an app](../task/app-tutorial-create-an-app.md)

</td></tr><tr><td>

Step 3

</td><td align="justify">

![Not started icon](../image/app-tutorial-progress-not-started.png)

</td><td>

[Building a data model](app-tutorial-data-model.md)

</td></tr><tr><td>

Step 4

</td><td align="justify">

![Not started icon](../image/app-tutorial-progress-not-started.png)

</td><td>

[Creating user experiences](app-tutorial-experience-layer.md)

</td></tr><tr><td>

Step 5

</td><td align="justify">

![Not started icon](../image/app-tutorial-progress-not-started.png)

</td><td>

[Adding logic and automation](app-tutorial-logic-automation-layer.md)

</td></tr><tr><td>

Step 6

</td><td align="justify">

![Not started icon](../image/app-tutorial-progress-not-started.png)

</td><td>

[Test your application](../task/app-tutorial-test-app.md)

</td></tr></tbody>
</table>Introduction to the app creation tutorial series. Learn how to develop a plan for your application before building it by identifying your application use case, visualizing your app workflow, and outlining your user and data needs. 

|Timestamp|Section|
|---------|-------|
|0:17|Identify the use case for your application.|
|0:21|Visualize the workflow for your application.|
|0:42|Outline the functional requirements for your app.|

## Step 1: Identify the use case for your application

Start by identifying the use case for your application. In our tutorial, we’re creating an application to manage employee travel requests for an organization. The app automates the entire travel request process and involves users such as employees, managers, regional heads, and travel desk agents as needed.

Consider the problem that you aim to solve with your application. To determine if your use case is a good fit for the tools featured in this tutorial, see [Plan your app development](before-you-begin.md).

## Step 2: Visualize the workflow for your application

Once you have identified the use case for your application, visualize the end-to-end workflow for the application. The end-to-end workflow is the sequence of actions an application follows to complete a task or process.

To visualize the end-to-end workflow for your application, map out what your application does from start to finish. Include any loops that lead back to earlier steps in the workflow and any actions that cause you to exit the workflow.

## Step 3: Outline the functional requirements for your app

It's also important to consider the functional requirements of your application. The functional requirements of an application include who uses the application, what tasks they perform in the app, and what data the app must collect to support these tasks.

Use the following prompts to outline the functional requirements for your application:

1.  Identify the personas who use your application and consider what tasks they perform.

    In our tutorial, the personas who use the employee travel request application and their associated tasks are:

    |Persona|Tasks|
    |-------|-----|
    |Employees|Submit travel requests|
    |Managers and regional heads|Approve or deny travel requests|
    |Travel desk agents|Book travel and complete follow-up tasks|

2.  Determine the data that your application must collect.

    For example, the application in our tutorial must collect details about employees' travel requests, including:

    -   Where the employee is traveling to and from
    -   When the travel occurs
    -   How much the travel costs
3.  Choose the process or processes that you want to automate in the workflow for your application using logic and automation.

    Review the following table to see how we plan to use logic and automation in our tutorial application.

    | |What it does|Tutorial application example|
    |---|------------|----------------------------|
    |Logic|Controls how and when certain actions occur in your application workflow.|Verifies that an employee's travel request is only forwarded to the travel desk after it has been approved by both the manager and the regional head.|
    |Automation|Sets up automatic processes based on the logic that you define.|Updates the employee's travel request case status and sends email notifications whenever a travel request is rejected.|

4.  Consider the roles and permissions for your application.

    Roles determine whether users have access to application content. Permissions are the individual abilities that a user has within application content, such as creating, reading, updating, and deleting. You can determine the roles for your application and configure permissions for each role at a later step in the tutorial. For more information about roles in App Engine Studio, see [Configure AES personas and roles](aes-personas-roles.md).

5.  Think about how you want to organize the data collected by your application.

    The data that your application collects is automatically stored in tables. You might want to organize the data across different tables, depending on the processes that your application completes. You can decide how you want to organize the data for your application a later step in the tutorial. For more information about data organization in App Engine Studio, see [Create a data model for your application](add-data.md).


## Next steps

Once you’ve developed a plan for your application, you can begin building the application in App Engine Studio. Proceed to the next step: [Create an app](../task/app-tutorial-create-an-app.md).

