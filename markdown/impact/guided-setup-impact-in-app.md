---
title: Use Guided Setup to synchronize and migrate data to the Impact Store Application
description: Use Impact Guided Setup to complete the configuration of the Impact Store Application.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-03-05"
reading_time_minutes: 2
breadcrumb: [Configuring the Impact Store Application, Impact Store Application, Impact]
---

# Use Guided Setup to synchronize and migrate data to the Impact Store Application

Use Impact Guided Setup to complete the configuration of the Impact Store Application.

## Before you begin

Guided setup provides a sequence of tasks that help you configure the Impact Store Application on your ServiceNow instance.

For more information, see [Guided Setup](https://www.servicenow.com/docs/access?context=guided-setup&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

There are three main steps in the Impact Guided Setup:

1.  Establish and verify your connection between the Impact Store Application and the Impact Delivery Instance IDI for data synchronization and migration. See [Connect to the provider instance](connect-instance-impact-store-app.md) for details.
2.  Select the data to synchronize and migrate to the Impact Store Application.
3.  Onboard new and existing users to the Impact Store Application.

You may return to the various steps in the configuration, if you don't complete the entire setup at once.

**Note:** Impact user roles do not have the necessary permissions to configure the Impact Store Application.

Role required: Any Impact role

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Guided Setup**.

    The Impact Guided Setup overview page displays with additional information about the setup process.![Guided Setup landing page.](../image/guided-setup-landing.png)

2.  Select **Continue** to move to the next step.

    The pre-checklist displays to summarize the connection steps.

3.  Select **Get started**.

4.  Complete the steps to initiate the connection to the provider instance.

    See [Initiate the connection to the Impact Delivery Instance](../concept/initiate-the-connection-impact-delivery-instance.md) for details.

5.  Verify the tasks are completed:

    1.  **Initiate connection to the Impact Delivery Instance \(provider\)**.

    2.  **Establish your provider connection in the Impact Store Application**

    3.  **Service Bridge registration**

    4.  **Verify the connection**

        **Note:** See [Connect to the provider instance](connect-instance-impact-store-app.md) for additional information.

6.  Select **Get Started**.

    The setup steps are displayed in category sections. You can expand a category to view details and related tasks. After the tasks for each section are completed, proceed to the next section.

7.  In Initiate Sync and Migration, complete the **Data Migration** task.

    |Task|Description|
    |----|-----------|
    |Initiate migration|Migrates data from IDI to the Impact Store Application.|
    |Test sync in sub-production instance|Migrates data from IDI to the Impact Store Application non-production instance.|

8.  In User Management, complete the tasks:

    1.  **Assign roles to users**

    2.  **Assign users to group**

    3.  **Know your Squad**

    **Note:** For information on Impact roles, see [Exploring Impact Store Application](../concept/exploring-impact-platform.md).


## What to do next

[Using Impact Store Application](../concept/impact-in-app.md)

