---
title: Adding logic and automation
description: Add logic and automation to your application. Learn about logic and automation in App Engine Studio and how we automate the employee travel request application.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [App creation tutorial, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Adding logic and automation

Add logic and automation to your application. Learn about logic and automation in App Engine Studio and how we automate the employee travel request application.

We continue building the employee travel request application by adding logic and automation.

This is the fifth step in the app creation tutorial. In this step, you learn about logic and automation in App Engine Studio. You build a decision table and create a flow for the employee travel request application.

<table id="table_odl_xfd_fdc"><tbody><tr><td>

Step 1

</td><td align="justify">

![Completed icon](../image/app-tutorial-progress-complete2.png)

</td><td>

[Planning your application](app-tutorial-introduction.md)

</td></tr><tr><td>

Step 2

</td><td align="justify">

![Completed icon](../image/app-tutorial-progress-complete2.png)

</td><td>

[Create an app](../task/app-tutorial-create-an-app.md)

</td></tr><tr><td>

Step 3

</td><td align="justify">

![Completed icon](../image/app-tutorial-progress-complete2.png)

</td><td>

[Building a data model](app-tutorial-data-model.md)

</td></tr><tr><td>

Step 4

</td><td align="justify">

![Completed icon](../image/app-tutorial-progress-complete2.png)

</td><td>

[Creating user experiences](app-tutorial-experience-layer.md)

</td></tr><tr><td>

Step 5

</td><td align="justify">

![In progress icon](../image/app-tutorial-progress-wip.png)

</td><td>

[Adding logic and automation](app-tutorial-logic-automation-layer.md)

</td></tr><tr><td>

Step 6

</td><td align="justify">

![Not started icon](../image/app-tutorial-progress-not-started.png)

</td><td>

[Test your application](../task/app-tutorial-test-app.md)

</td></tr></tbody>
</table>## Overview of logic and automation

Logic and automation enable you to define the actions that your application performs and the conditions that trigger those actions. Logic helps you define when certain actions should occur. For example, your application logic can determine whether support tickets are marked as "critical." Automation then defines the actions that the application performs. For example, if support tickets are marked as "critical", your application automation can move those tickets to the top of the queue.

There are several ways to implement logic and automation in App Engine Studio. Our tutorial focuses on decision tables and flows. To learn about the full range of logic and automation capabilities in App Engine Studio, see [Add logic and automation](add-automation.md).

## Tutorial logic and automation

In our tutorial, we create a decision table and a flow to store the logic and automation for the employee travel request application. Decision tables enable you to set and manage business logic in your application separate from your code. The decision table in our tutorial determines which regional heads receive travel requests based on employees' geographic location.

Flows are automated processes that use a trigger, actions, and logic to define the behavior of an application. The flow in our tutorial defines the sequence of actions that the employee travel request application completes once a travel request is created.

We add logic and automation to our application in two phases:

<table id="table_c53_qvw_2dc"><tbody><tr><td>

Phase 1

</td><td>

[Build a decision table](../task/app-tutorial-create-decision-table.md)

</td></tr><tr><td>

Phase 2

</td><td>

[Create a flow](../task/app-tutorial-create-a-flow.md#)

</td></tr></tbody>
</table>## Next steps

Start adding logic and automation to the employee travel request application: [Build a decision table](../task/app-tutorial-create-decision-table.md).

