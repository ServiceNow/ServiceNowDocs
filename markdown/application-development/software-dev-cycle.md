---
title: Programming basics
description: Software development usually encompasses a standard set of steps. If you're new to developing applications, read on.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Programming basics

Software development usually encompasses a standard set of steps. If you're new to developing applications, read on.

## Your job as a developer

If you're new to developing applications, if you don't even know how to code, ServiceNow has a low-code development platform called [Creator Studio](../../creator-studio/concept/creator-studio-landing.md) that makes creating a basic request-fulfill application possible for you. Development might be new waters for you to swim in but you will find the low-code tools easy to use. So, don't be shy about developing an app!

Software developers do many things but what they have in common is solving problems using computer code. ServiceNow offers coding platforms that require no coding experience, platform development coding experience, and expert coding experience. The less coding required, the more work the coding platform does for you. So, even experienced software developers will appreciate no-, low-, and platform-level coding products, such as [Creator Studio](../../creator-studio/concept/creator-studio-landing.md) and [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

## Software development life cycle

The common stages of developing an application are:

1.  Define the problem.
2.  Plan the solution.
3.  Code the solution.
4.  Test the application.
5.  Deploy the application.
6.  Document the application.

These steps are commonly referred to as the software development life cycle. [ServiceNow developer documentation](build-applications.md) is grouped according to these steps.

## Do you really need to create a new application

Your first step is to determine if creating an application is necessary. Consider:

-   [Can you extend an existing application instead of creating a new one?](modifying-versus-building-an-application.md)
-   How many people will the application serve? If not many, is it worth the effort?
-   Are you willing to maintain the application as things change over time?
-   How often will anyone use this application? If not often, is it worth the effort?

If creating a new application makes sense, then move forward.

## Defining the problem

If you're planning to create an application, you must have some notion of what you want it to do. You might not have a detailed idea of the solution, however. At a minimum, you need to define in detail:

-   Desired application output
-   Data going into the application

The data going in typically comes from a table of data. You need to know the table name and the type of data in it. You can use ServiceNow tools, like [Table Builder](../../../administer/form-builder/concept/tb-landing-page.md), to store and customize your data.

The desired output might be a dashboard, data stored in a table, or a piece of equipment being sent to an employee. Before you decide on the output, show a mockup of your output to a lot of people to see if they can suggest improvements to the output. Do not skip this step.

## Planning the solution

There are various ways to create an algorithm that produces the output you want. The easiest methodology is to use a flowchart that starts with the input data and shows each step in the process that leads to the output. Using a flowchart enables you to focus on the big picture of what you want to do and avoid how to do it. Look at your flowchart critically to optimize the process.

You may need to get permissions to use tables of data or even permission to create an application. For example, citizen developers are granted app development permissions through [App Engine Management Center](../../app-engine-studio/concept/monitor-requests-using-aemc.md).

For more information about ServiceNow planning tools, see [Planning your application](planning-applications.md).

## Coding the application

To code the application, you can use:

-   Low-code ServiceNow tools, such as [App Engine Studio](../../app-engine-studio/concept/aes-overview.md).
-   Platform developer ServiceNow tools, such as [ServiceNow Studio.](../../servicenow-studio/concept/servicenow-studio-landing.md)
-   Pro-dev source code tools, such as [ServiceNow IDE](../../servicenow-ide/concept/servicenow-ide-landing.md) and [ServiceNow SDK](../../servicenow-sdk/concept/servicenow-sdk-landing.md).

For more information about ServiceNow coding platforms, see [Developing your application](developing-applications.md).

## Testing your application

Testing your application requires inputting data to make sure the outcome is accurate. It is important to input a lot of data, even incorrect data, to see how well your application handles correct and incorrect inputs. Put in data that is too large or the wrong type. Put in no data at all. Try to break your application to prevent your users from doing so. Handling error conditions gracefully is critical for a good customer experience.

For more information about ServiceNow testing tools, see [Testing and debugging applications](testing-and-debugging-applications.md).

## Deploying your application

Now that you've tested your application, it's time to deploy it so customers can use it. Application deployment is done by system administrators not developers.

For information about ServiceNow deployment tools, see [Deploying applications](deploying-applications.md).

## Maintaining your application

Maintaining the application deals with issues such as overloading a server, application errors, and feature updates. Accounting for feature updates is a developer's job. Seeing how well an application is working is a system administrator's job.

For more information about ServiceNow tools that help you maintain your application, see [Maintaining your application](maintaining-applications.md).

## Documenting your application

Application development is never complete until the application is documented. There are many reasons to document your application:

-   Internal notes help other developers work on your application. It takes a lot of time to figure out the reasoning behind programming decisions and methodology. Documenting those helps future developers maintain your application.
-   Users need to know how to use your application. As transparent as you believe the application is, you will find many people who get frustrated trying to use it. Do a usability test on your application and documentation to see where users run into problems. The broader the audience, the more important the application, the more important the documentation. Consider using an experienced technical writer to write the documentation.

