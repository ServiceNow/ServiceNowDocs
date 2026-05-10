---
title: Configure the OAuth authentication method
description: To configure the OAuth authentication method, you need create an OAuth authentication record, producer and consumer application registries for each instance that will send data, and then import the user, OAuth authentication record, and consumer application registries to the instances that will use the Scan Engine.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Register your instance, Scan Engine integrations, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure the OAuth authentication method

To configure the OAuth authentication method, you need create an OAuth authentication record, producer and consumer application registries for each instance that will send data, and then import the user, OAuth authentication record, and consumer application registries to the instances that will use the Scan Engine.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\).

## Procedure

1.  To assign a user or users the Integration role \(sn\_se.internal\_rest\_integration\), navigate to **ALL** &gt; **System Security** &gt; **Users and Groups** &gt; **Users**, and then select **New**.

    For more information on creating a new user, see [Create new user form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-new-user-form.md).

2.  To create an OAuth authentication record, navigate to `sys_auth_profile_oauth2.list`, and then select **New**.

    Ensure that the record:

    -   Is created in the Scan Engine scope
    -   Contains the same username and password established for the user in step 1
3.  Export the user \(from step 1\) and the OAuth authentication record \(from step 2\), and then import them to all instances that will use Scan Engine integrations.

    Once the user is exported, you must reassign it the Integration role, as roles do not transfer during the export process. In addition, password fields may become corrupted during the import/export process, so ensure that they are still accurate.

4.  To establish a successful connection between instances, you must create a minimum of one provider and two consumer application registries.

    The provider serves as the endpoint. To create a connection that flows from the Development to the Production instance, you must create a provider on the Production instance.

    By contrast, to create a connection that flows from the Production to the Development instance, you must create a provider in the Development instance. These providers will have corresponding consumer application registries in all instances they communicate with, including themselves. The same logic applies for any other environments \(for example, Test or Q&amp;A\).

5.  To configure the provider application registry:

    1.  On a Production instance, navigate to **All** &gt; **System OAuth** &gt; **Application Registry**, and then select **New**.

    2.  Select **Create an OAuth API endpoint for external clients**.

    3.  To configure the new application registry record form, set the **Name** to `[Instance Name] – Provider`, then set the **Client Secret**.

    4.  Make note of the Client ID and Client Secret entries as you will need them to populate the consumer OAuth application registry.

    5.  Save the record.

6.  Set up the consumer application registry.

    1.  On the Development instance, navigate to **ALL** &gt; **System OAuth** &gt; **Application Registry**, and then select **New**.

    2.  Select **Connect to a third-party OAuth Provider**.

    3.  Configure the new application registry record form.

        1.  Enter the Client ID and Client Secret for the provider application registry.
        2.  Set the **OAuth API Script** to **OAuthUtil**.
        3.  Verify that **Default Grant Type** is **Resource Owner Password Credentials**.
        4.  Set the **Token URL** to `[provider instance url]/oauth_token.do`.
    4.  Save the record.

7.  Initiate the connection between the provider and consumer instances.

    1.  Export the consumer application registry record to the consumer instance.

        The consumer record must exist in both the provider and consumer instances. Initiate this step on the provider \(Production\) instance, and then complete the step in the consumer \(Development\) instance.

        **Important:** Once you import the record into the consumer instance, verify that the **Client Secret** matches the one you created previously.

    2.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**, and then open the **My SN Instances** related list.

    3.  Populate the following fields with the information from the provider instance:

        -   **Instance Name**: The provider instance name \(derived from the provider instance URL\).
        -   **Instance URL**: The provider instance URL.
        -   **Environment**: The provider environment type.
        -   **Authentication Type**: OAuth.
        -   **OAuth Application Registry**: “`[Provider instance] – Consumer`.
        -   **OAuth User Profile**: The OAuth authentication record you created previously.
    4.  Save the record, and then **Validate Connection**.

        **Connection Status** should update to **Connection valid**.

8.  Export the My SN record to the provider instance.

    **Note:** You should export the My SN record rather than individually create it as the system IDs must match for a proper configuration.

9.  Repeat steps 6 and 7 in [Configure the OAuth authentication method](configure-oauth-auth-method.md) for all additional instances that you want to configure with bidirectional communication, but designate a sub-production instance as the Provider, and the Production instance as the Consumer.

    Information such as name and URL will be taken from the sub-production instance.

    In the Development instance, the status field should now display **Connection Valid**. This indicates that setup is complete and the integration now moves bi-laterally.

    **Note:** When setting up instances on the **My SN instances** related list, verify that each instance is connected to their respective OAuth application registry. Developer instances should be connected to `[Developer Instance] – Consumer`. Provider instances should be connected to `[Production Instance] – Consumer`.


