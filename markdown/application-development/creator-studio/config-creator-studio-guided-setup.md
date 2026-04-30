---
title: Configure Creator Studio using Guided Setup
description: So you've installed Creator Studio on an instance. Now what? You must configure it before users can start building apps.
locale: en-US
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configuring Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Configure Creator Studio using Guided Setup

So you've installed Creator Studio on an instance. Now what? You must configure it before users can start building apps.

## Before you begin

Creator Studio must be installed on the instance before you can configure it. Find out more about that in [Installing Creator Studio from the ServiceNow Store](../concept/installing-creator-studio-from-the-store.md).

To ensure that forms appear correctly for users, the non-production and production instances must have the same Service Catalog and all of its categories.

Role required: admin

## About this task

Guided Setup streamlines configuring Creator Studio, and keeps track of what you have completed, so you can stop and start again where you left off.

In this Guided Setup, you'll configure user access and collaboration settings to control who can do what in Creator Studio.

## Procedure

1.  Let's open Guided Setup. On your instance, select the **All** tab.

    ![The All menu lets you see all the apps on your instance](../image/cs-all-menu.png "All tab")

    This tab lets you see all the apps installed on your instance.

2.  In the white text field, enter `App Engine`.

    The list of apps displayed underneath the text box now pertains only to App Engine.

3.  In the list, select **Guided Setup – Shared**, which starts the configuration process.

    The Guided Setup app opens, where you make some basic configurations.

    ![Guided Setup walks you through Creator Studio configuration tasks](../image/cs-guided-setup.png "Guided Setup")

4.  Start the setup process by selecting the **Get Started** button.

5.  Configure user access by selecting the **Get Started** button in the Set up user access section.

6.  Set up the admin group to enable ServiceNow administrators access to work on and configure Creator Studio.

    1.  Select the **Configure** button for the Set up the admin group section.

    2.  Make any changes to the App Engine Admins group.

        App Engine Admins approve tasks for app development, such as when restricted users need an app created for them.

    3.  Update the record to save your changes.

    4.  Select the **Mark as complete** button on the Guided Setup page to indicate that you're done with this step.

7.  Set up collaboration descriptors to manage what app Owner and Editor collaboration types can do.

    By default, owners can do anything on an app, while editors are more restricted in what they can do. For more information, see [Collaboration in Creator Studio](../reference/creator-studio-collaboration-roles.md).

    1.  Select the **Configure** button for the Set up collaboration descriptors to manage your user's capabilities section.

    2.  Customize the collaboration roles or add new ones.

        For more information, see [Application collaboration](../../applications/concept/application-collaboration.md).

    3.  Update the record to save your changes.

    4.  Select the **Mark as complete** button on the Guided Setup page to indicate that you're done with this step.

8.  Select the **Welcome to App Engine Guided Setup​** breadcrumb link to return to the main Guided Setup page.

9.  Set up who has full access to Creator Studio by selecting the **Get Started** button in the Set up access to Creator Studio section.

    In this section, you decide which users get full access to work on app in Creator Studio, and who has more limited capabilities. For example, restricted users must request that an admin create a new app for them. For more information, see [Creator Studio roles and personas](../reference/roles-creator-studio.md).

10. Set up full access for users by selecting the **Configure** button for the Grant full Creator Studio access to users section.

    1.  Add users to the Creator Studio Users Group.

        People in the Creator Studio Users Group have full access to working with apps, and can create apps without needing help from an admin.

    2.  Update the record to save your changes.

    3.  Select the **Mark as complete** button on the Guided Setup page to indicate that you're done with this step.

11. Set up limited access for users by selecting the **Configure** button for the Grant Creator Studio Restricted Access section.

    1.  Add users to the Creator Studio Restricted Users Group.

        People in the Creator Studio Restricted Users Group have limited access to working with apps, and must request that admins create apps for them.

    2.  Update the record to save your changes.

    3.  Select the **Mark as complete** button on the Guided Setup page to indicate that you're done with this step.


## What to do next

After you finish configuring Creator Studio, you can configure Pipelines and Deployments to enable apps built in Creator Studio to be deployed to production. For information on how, see [Configure Pipelines and Deployments](../../pipelines-and-deployments/task/config-p-and-d.md).

**Parent Topic:**[Configuring Creator Studio](../concept/configuring-creator-studio.md)

