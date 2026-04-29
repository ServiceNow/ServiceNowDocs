---
title: Configure the basic authentication method
description: For instances that use the basic authentication method, you must assign users the Integration role, create an authentication record, import both into each instance that will use Scan Engine integrations, then connect your instances.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Register your instance, Scan Engine integrations, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure the basic authentication method

For instances that use the basic authentication method, you must assign users the Integration role, create an authentication record, import both into each instance that will use Scan Engine integrations, then connect your instances.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\).

## Procedure

1.  Create an integration account with the required role \(sn\_se.internal\_rest\_integration\) by navigating to **All** &gt; **System Security** &gt; **Users and Groups** &gt; **Users**. Then select **New**.

    For more information on creating a new user, see [Create new user form](https://www.servicenow.com/docs/access?context=eaw-create-new-user-form&version=australia&pubname=australia-application-portfolio-management&ft:locale=en-US).

    **Note:** You can also use an existing integration user by ensuring they are provisioned for the required role.

2.  To create a basic authentication record, navigate to the `sys_auth_profile_basic` table, and then select **New**.

    Ensure that the record contains the same username and password established for the user in step 1. Also, make sure you set **Application** to **Scan Engine**.

3.  Export the user \(from step 1\) and the basic authentication record \(from step 2\), and then import them to all instances that will use Scan Engine integrations.

    **Note:** Ensure that you assign the integration role to the user account in each instance. After importing, verify that the passwords match, as they may not carry over correctly.

4.  Navigate to **ALL &gt; Impact &gt; Configuration &gt; Scan Engine Properties**, then select the **My SN Instances** tab.

    Make sure you are on the Development instance when performing these steps.

5.  Select **New** to create a new record for each instance that will use Scan Engine integrations.

    1.  Ensure that you set **Authentication type** to **Basic**.

    2.  For **API Credential Config**, enter the basic authentication record you created in step 2.

        **Important:** The instance URL must contain your instance name. For example, if your instance name is `demodev1` then the URL should be `www.demodev1.service-now.com/`.

    3.  Enter an **Instance Name**. For example, if your URL is `https://demodev1.service-now.com/`, then the instance name value should be `demodev1`.

    4.  Enter the full **Instance URL**.

    5.  Select the correct **Environment**, either **Development**, **Production**, or **Test**. Note that only one instance can be listed as **Production**. Otherwise, the integration will fail.

    6.  **Validated** indicates whether the instance has been successfully validated using the **Validate Connection** action available on the instance configuration form. This action attempts a live connection to the target instance using the defined credentials and connection parameters. If successful, the instance is flagged as `Validated = true`, and **Validation** will be enabled on this screen.

    7.  **Connection status** represents the current state of connectivity between local and remote instances. This field is automatically updated based on the results of the validation process. It reflects the outcome of the live connection test and cannot be edited.

    8.  Set the **Authentication Type** to **Basic**.

    9.  For **API Credential Config**, enter the basic authentication record you created in step 2.

6.  Promote or export the list of **My SN Instances** to all instances that will use Scan Engine integrations.

7.  In an instance that will use Scan Engine integrations, navigate to **ALL &gt; Impact &gt; Configuration &gt; Scan Engine Properties**, and then select the **My SN Instances** tab.

8.  Select and view the production records you imported, and then select **Validate Connection**.

    After a few moments, the connection status should update to **Connection Valid** for this sub-production environment.

9.  Select **Update** to save your changes.

    The configuration has now been set up between instances

10. Repeat steps 7 through 9 for each instance that will use Scan Engine integrations.


