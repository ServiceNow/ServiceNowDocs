---
title: Configure Creator Studio using Guided Setup
description: So you've installed Creator Studio on an instance. Now what? You must configure it before users can start building apps.Set up the admin group to enable ServiceNow administrators access to work on and configure Creator Studio.Set up collaboration descriptors to manage what app Owner and Editor collaboration types can do in Creator Studio.Set up who has full access to Creator Studio to decide which users get full access to work on app in Creator Studio, and who has more limited capabilities.Set up limited access for Creator Studio users. People in the Creator Studio Restricted Users Group have limited access to working with apps, and must request that admins create apps for them.Configure customized email notifications that Creator Studio apps send. For example, you can add branding to notification emails that a request was opened.Configure the activities that appear when users build playbooks in Creator Studio.Use Guided Setup to change the table that the app saves its requests to.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Configure, Creator Studio, Building no-code applications, Developing your application, Building applications]
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

    ![Interface showing All, Favorites, and History tabs with a Filter field.](../image/cs-all-menu.png "All tab")

2.  In the white text field, enter `App Engine`.

    The list of apps displayed underneath the text box now pertains only to App Engine.

3.  In the list, select **Guided Setup – Shared**, which starts the configuration process.

    The Guided Setup app opens, where you make some basic configurations.

    ![Guided Setup walks you through Creator Studio configuration tasks](../image/cs-guided-setup.png "Guided Setup")

4.  Start the setup process by selecting the **Get Started** button.

5.  Select the **Welcome to App Engine Guided Setup​** breadcrumb link to return to the main Guided Setup page.


## What to do next

Next, it's time to configure specific Creator Studio features, which include the following:

-   [Set up the Creator Studio admin group](config-creator-studio-guided-setup.md#)
-   [Set up Creator Studio collaboration descriptors](config-creator-studio-guided-setup.md#)
-   [Set up Creator Studio full access users](config-creator-studio-guided-setup.md#)
-   [Set up Creator Studio restricted access users](config-creator-studio-guided-setup.md#)
-   [Set up Creator Studio playbook activities](config-creator-studio-guided-setup.md#)
-   [Configure the table for Creator Studio apps](config-creator-studio-guided-setup.md#)
-   [Set up Creator Studio custom notification emails](config-creator-studio-guided-setup.md#)

## What to do next

After you finish configuring Creator Studio, you can configure Pipelines and Deployments to enable apps built in Creator Studio to be deployed to production. For information on how, see [Configure Pipelines and Deployments](../../pipelines-and-deployments/task/config-p-and-d.md).

**Parent Topic:**[Configuring Creator Studio](../concept/configuring-creator-studio.md)

## Set up the Creator Studio admin group

Set up the admin group to enable ServiceNow administrators access to work on and configure Creator Studio.

### Before you begin

Initiate the Guided Setup as described in [Configure Creator Studio using Guided Setup](config-creator-studio-guided-setup.md#).

### Before you begin

Role required: admin

### Procedure

1.  Select the **Get Started** button in the Set up user access section.

2.  Select the **Configure** button for the Set up the admin group section.

3.  Make any changes to the App Engine Admins group.

    App Engine Admins approve tasks for app development, such as when restricted users need an app created for them.

4.  Update the record to save your changes.

5.  Select the **Mark as complete** button on the Guided Setup page to indicate that you're done with this step.


### What to do next

Next, [Set up Creator Studio collaboration descriptors](config-creator-studio-guided-setup.md#).

## Set up Creator Studio collaboration descriptors

Set up collaboration descriptors to manage what app Owner and Editor collaboration types can do in Creator Studio.

### Before you begin

Initiate the Guided Setup as described in [Configure Creator Studio using Guided Setup](config-creator-studio-guided-setup.md#).

Role required: admin

### Procedure

1.  Select the **Configure** button for the Set up collaboration descriptors to manage your user's capabilities section.

    By default, owners can do anything on an app, while editors are more restricted in what they can do. For more information, see [Collaborating with others to build apps in Creator Studio](../reference/creator-studio-collaboration-roles.md).

2.  Customize the collaboration roles or add new ones.

    For more information, see [Application collaboration](../../applications/concept/application-collaboration.md).

3.  Update the record to save your changes.

4.  Select the **Mark as complete** button on the Guided Setup page to indicate that you're done with this step.


### What to do next

Next, [Set up Creator Studio full access users](config-creator-studio-guided-setup.md#).

## Set up Creator Studio full access users

Set up who has full access to Creator Studio to decide which users get full access to work on app in Creator Studio, and who has more limited capabilities.

### About this task

For example, restricted users must request that an admin create a new app for them. For more information, see [Creator Studio roles and personas](../reference/roles-creator-studio.md).

### Before you begin

Initiate the Guided Setup as described in [Configure Creator Studio using Guided Setup](config-creator-studio-guided-setup.md#).

Role required: admin

### Procedure

1.  Select the **Get Started** button in the Set up access to Creator Studio section.

2.  Set up full access for users by selecting the **Configure** button for the Grant full Creator Studio access to users section.

3.  Add users to the Creator Studio Users Group.

    People in the Creator Studio Users Group have full access to working with apps, and can create apps without needing help from an admin.

4.  Update the record to save your changes.

5.  Select the **Mark as complete** button on the Guided Setup page to indicate that you're done with this step.


### What to do next

Next, [Set up Creator Studio restricted access users](config-creator-studio-guided-setup.md#).

## Set up Creator Studio restricted access users

Set up limited access for Creator Studio users. People in the Creator Studio Restricted Users Group have limited access to working with apps, and must request that admins create apps for them.

### Before you begin

Initiate the Guided Setup as described in [Configure Creator Studio using Guided Setup](config-creator-studio-guided-setup.md#).

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **** &gt; ****.

2.  Select the **Configure** button for the Grant Creator Studio Restricted access to users section.

3.  Add users to the Creator Studio Restricted Users Group.

4.  Update the record to save your changes.

5.  Select the **Mark as complete** button on the Guided Setup page to indicate that you're done with this step.


## Set up Creator Studio custom notification emails

Configure customized email notifications that Creator Studio apps send. For example, you can add branding to notification emails that a request was opened.

### About this task

Customized email templates can be applied to notifications that are sent when users request something from an app, or the request was changed or closed.

### Before you begin

Initiate the Guided Setup as described in [Configure Creator Studio using Guided Setup](config-creator-studio-guided-setup.md#).

Role required: admin

### Procedure

1.  Select the **Configure** button for the Configure Email Notifications Creator Studio Requests section.

2.  Add users to the Creator Studio Restricted Users Group.

    A table displays all email notifications for Creator Studio.

3.  Select the **Name** of the email that you want to customize.

    For example, **Request opened**.

    **Note:** Depending on your scope, you may need to switch to the Creator Studio Configurations scope to make changes.

4.  Make any updates and customizations to the content of the email.

    You can select into any of the following tabs to edit their details:

    1.  **When to send**
    2.  **Who will receive**
    3.  **What it will contain**
    For more information on editing notifications on the ServiceNow AI Platform, see [Create an email notification](https://www.servicenow.com/docs/access?context=t_CreateANotification&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

5.  Update the record to save your changes.

6.  Select the **Mark as complete** button on the Guided Setup page to indicate that you're done with this step.


## Set up Creator Studio playbook activities

Configure the activities that appear when users build playbooks in Creator Studio.

### Before you begin

Initiate the Guided Setup as described in [Configure Creator Studio using Guided Setup](config-creator-studio-guided-setup.md#).

Role required: admin

### Procedure

1.  Select the **Configure** button for the Configure Playbook activities for Creator Studio section.

    All of the default Creator Studio playbook activities appear.

    ![List of playbook activities](../image/crs-setup-activities-list.png "Creator Studio activities in Guided Setup")

2.  Rearrange the order activities appear in the selection list.

    Order numbers are relative to the other activities, which you can view on the Configure Playbook activities for Creator Studio landing page in Guided Setup.

    1.  Select into the **Order** column for the activity you want to renumber.

    2.  Enter a new order number for the activity.

        ![Enter a new order number for the activity](../image/crs-setup-reorder.png "Reorder an activity")

    3.  Select the Save icon ![](../image/crs-save-check.png) or press Enter.

3.  Add a new activity.

    **Note:** The activity must already be configured in the activities table for you to add it to the Creator Studio playbook list.

    1.  Select the **New** button.

    2.  Search for the activity you want to add in the **Activity** field.

    3.  Enter the **Order** it appears in.

    4.  Enter a **Short Description**, which will appear in the activity picker under the activity name.

    5.  Leave the **Active** check box selected to make the activity visible immediately.

    6.  Select the **Submit** button.


### What to do next

Users who are actively working in Creator Studio must refresh their browser to see the changes you just made.

## Configure the table for Creator Studio apps

Use Guided Setup to change the table that the app saves its requests to.

### About this task

Some general guidelines for changing the table are:

-   If you change an app's table to one that doesn't extend a Request Task-extended table, it could affect automations.
-   If the new table doesn't have the **request\_type** field, the app's automations won't be correctly triggered.

    **Note:** You can change the **Request type** field, which specifies the form, on the Request Task table or a table that extends Request Task. To do so, you must be an admin or have the sn\_creatorstudio.configuration\_admin or sn\_creatorstudio.task\_admin role.

-   The request\_type field for the new table should have the label **Request type**, and it should be a reference to the Record Producer table.
-   If the new table isn’t in the same scope as the app, the scope of the table must allow updates from other scopes.

### Before you begin

Initiate the Guided Setup as described in [Configure Creator Studio using Guided Setup](config-creator-studio-guided-setup.md#).

The app must already be created before you can change the table for it.

### Before you begin

For more information on changing an app's table, see [Changing the table for an app](../concept/creator-studio-admin-app-table-about.md).

Role required: admin, app configurator \(sn\_creatorstudio.app\_configurator\), or Creator Studio configuration admin \(sn\_creatorstudio.configuration\_admin\). For more information on working with granular roles, see [Granular admin roles required to secure your instance](https://www.servicenow.com/docs/access?context=roles-within-platform-security&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

### Procedure

1.  Select the **Configure** button for the Configure the associated table for Creator Studio Service Desk apps section.

    All of the apps built on the instance in Creator Studio appear.

    ![List of apps in Guided Setup](../image/crs-setup-table-list.png "Guided Setup to configure the associated table")

2.  Select the app that you want to change the table for.

    **Note:** You may need to change the scope that you're in.

3.  Change the table.

    1.  Select into the **Request table** field.

    2.  Search for and select the table that you want to associate the app with.

        ![Search for and select the table to change to](../image/crs-setup-table-change.png "Change the table")

4.  Select the **Update** button.


### Result

The associated table for an app changes to the new table. Any users currently in Creator Studio may need to refresh their browser to see the change.

