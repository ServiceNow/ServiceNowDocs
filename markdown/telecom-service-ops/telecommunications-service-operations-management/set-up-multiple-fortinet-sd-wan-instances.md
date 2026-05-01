---
title: Manage multiple Fortinet SD-WAN instances
description: Configure and manage multiple Fortinet instances within a single ServiceNow AI Platform environment. This functionality facilitates the creation of distinct connection aliases and the establishment of independent import schedules that you can customize to accommodate specific data filtering and frequency requirements for administrators and integrators.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 3
breadcrumb: [Configure Fortinet SGC, Set up Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Manage multiple Fortinet SD-WAN instances

Configure and manage multiple Fortinet instances within a single ServiceNow AI Platform® environment. This functionality facilitates the creation of distinct connection aliases and the establishment of independent import schedules that you can customize to accommodate specific data filtering and frequency requirements for administrators and integrators.

## Before you begin

Verify the following:

-   The active application scope is Service Graph Connector \(SGC\) for Fortinet.
-   The SGC for Fortinet has been installed.
-   The initial Fortinet instance has been set up. For more information, see [Set up the Service Graph Connector for Fortinet schedule](set-up-fortinet-sd-wan.md).
-   The associated MID Server has been set up and validated. For more information, see [Configuring MID Server](https://www.servicenow.com/docs/access?context=configure-mid-server&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

Role required: TSOM Visibility admin

## About this task

You can configure additional Fortinet instances or reuse the same Fortinet instance with different connection aliases and import schedules. To add a new Fortinet instance, run the guided setup to configure a new connection alias. All connectivity stages within the setup must be completed for each new alias.

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Fortinet** &gt; **Setup**.

2.  On the Getting Started page, select **Get Started**.

3.  Create and configure aliases for the connections and credentials:

    1.  Select **Configure**.
    2.  In the **Name** field, specify the alias name.
    3.  Retain the default values in the rest of the fields.
    4.  Select **Submit** and then select **Mark as Complete**.
4.  Create the basic credentials to access the FortiManager.

    1.  Select **Configure**.
    2.  In the **API Key** field, enter the API key created in the FortiPortal.

        **Note:** Other authentication fields might be required depending on the authentication methods used in your Fortinet instance. By default, use basic authentication credentials as part of the Guided setup. For more information, see [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    3.  In the **User name** field, specify your FortiManager instance user name.
    4.  Retain the default values in the rest of the fields.
    5.  Select **Submit** and then select **Mark as Complete**.
5.  Create the HTTP Connection.

    1.  Select **Configure**.
    2.  In the **Name** field, specify the connection name.
    3.  In the **Credentials** and **Connection Alias** fields, choose the items created earlier.
    4.  In the **Connection URL** field, select the URL for Fortinet.
    5.  Select the **Use MID Server** check box and indicate how the MID Server should be selected:
        -   Auto-select: Automatically chooses the most appropriate MID Server.
        -   Specific MID Server: Select the name of the MID Server from the **MID Server** field that is displayed.
        -   Specific MID Cluster: Select the name of the MID cluster from the **MID Cluster** field that is displayed.
    6.  Retain the default values in the rest of the fields.
    7.  Select **Submit** and then select **Mark as Complete**.
6.  Configure the connectivity by creating a connection alias, credentials, and HTTP connection.

    1.  In the Configure Connectivity section, select **Get Started**.

    2.  Select **Configure** to create a new connection alias by entering a unique alias name \(for example, `Meraki_Prod_01`\).

    3.  Select **Submit** and then select **Mark as Complete**.

7.  Configure credentials for the new Fortinet instance.

    1.  Specify a user name and password for the Fortinet instance.

    2.  Select **Submit** and then select **Mark as Complete**.

8.  Configure an HTTP connection.

    1.  Provide the connection name.

    2.  Select the newly created credentials and connection alias.

    3.  Enter the connection URL of the Fortinet instance.

    4.  Enable use MID Server and choose the appropriate MID option.

    5.  Select **Submit** and then select **Mark as Complete**.

9.  Schedule data imports using either bulk or filtered discovery by configuring the import schedule.

    1.  Select **Configure** and fill in the fields.

        For more information, see [Set up the Service Graph Connector for Fortinet schedule](set-up-fortinet-sd-wan.md).

    2.  In the **Use connection** field, choose the new Fortinet instance.

10. Select **Submit**.

11. Confirm that your new instance setup is successful by verifying the configuration.

    1.  Navigate to &gt; **All** &gt; **Service Graph Connectors** &gt; **Fortinet** &gt; **Connection &amp; Credential Aliases**.

    2.  Confirm that the new alias is listed.

    You can configure multiple connection aliases over the same Fortinet instance. This flexibility enables you to run imports at different frequencies and apply different filters to each alias.


