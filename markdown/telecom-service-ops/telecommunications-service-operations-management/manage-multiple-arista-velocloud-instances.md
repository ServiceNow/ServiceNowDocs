---
title: Manage multiple Arista VeloCloud instances
description: Configure and manage multiple Arista VeloCloud instances within a single ServiceNow AI Platform environment. This functionality facilitates the creation of distinct connection aliases and the establishment of independent import schedules that you can customize to accommodate specific data filtering and frequency requirements for administrators and integrators.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/manage-multiple-arista-velocloud-instances.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 3
breadcrumb: [Configure Arista VeloCloud SGC, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Manage multiple Arista VeloCloud instances

Configure and manage multiple Arista VeloCloud instances within a single ServiceNow AI Platform® environment. This functionality facilitates the creation of distinct connection aliases and the establishment of independent import schedules that you can customize to accommodate specific data filtering and frequency requirements for administrators and integrators.

## Before you begin

Verify the following:

-   The active application scope is Service Graph Connector \(SGC\) for VeloCloud.
-   The SGC for Arista VeloCloud has been installed.
-   The initial Arista VeloCloud instance has been set up. For more information, see [Set up the Service Graph Connector for Arista VeloCloud schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-the-service-graph-connector-for-arista-velocloud-schedule.md).
-   The associated MID Server has been set up and validated. For more information, see [Configuring MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/configure-mid-server.md).

Role required: TSOM Visibility admin

## About this task

You can configure additional VeloCloud instances or reuse the same VeloCloud instance with different connection aliases and import schedules. To add a new VeloCloud instance, run the guided setup to configure a new connection alias. All connectivity stages within the setup must be completed for each new alias.

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **VeloCloud** &gt; **Setup**.

2.  On the Getting Started page, select **Get Started**.

3.  Create and configure aliases for the connections and credentials:

    1.  Select **Configure**.
    2.  In the **Name** field, specify the alias name.
    3.  Retain the default values in the rest of the fields.
    4.  Select **Submit** and then select **Mark as Complete**.
4.  Create the basic credentials to access the VeloCloud Orchestrator.

    1.  Select **Get Started**.
    2.  Select **Configure**.
    3.  In the **API Key** field, enter the API key created in the Orchestrator.

        **Note:** Other authentication fields might be required depending on the authentication methods used in your Arista VeloCloud instance. By default, use basic authentication credentials as part of the Guided setup. For more information, see [Basic authentication credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_BasicAuthCredentialsForm.md).

    4.  In the **User name** field, specify your Arista VeloCloud instance user name.
    5.  Retain the default values in the rest of the fields.
    6.  Select **Submit** and then select **Mark as Complete**.
5.  Create the HTTP Connection.

    1.  Select **Get Started**.
    2.  Select **Configure**.
    3.  In the **Name** field, specify the connection name.
    4.  In the **Credentials** and **Connection Alias** fields, choose the items created earlier.
    5.  In the **Connection URL** field, select the URL for Cisco Meraki.
    6.  Select the **Use MID Server** check box and indicate how the MID Server should be selected:
        -   Auto-select: Automatically chooses the most appropriate MID Server.
        -   Specific MID Server: Select the name of the MID Server from the **MID Server** field that is displayed.
        -   Specific MID Cluster: Select the name of the MID cluster from the **MID Cluster** field that is displayed.
    7.  Retain the default values in the rest of the fields.
    8.  Select **Submit** and then select **Mark as Complete**.
6.  Configure the connectivity by creating a connection alias, credentials, and HTTP connection.

    1.  In the Configure Connectivity section, select **Get Started**.

    2.  Select **Configure** to create a new connection alias by entering a unique alias name \(for example, `Velocloud_Prod_01`\).

    3.  Select **Submit** and then select **Mark as Complete**.

7.  Configure credentials for the new VeloCloud instance.

    1.  Specify a user name and password for the VeloCloud instance.

    2.  Select **Submit** and then select **Mark as Complete**.

8.  Configure an HTTP connection.

    1.  Provide the connection name.

    2.  Select the newly created credentials and connection alias.

    3.  Enter the connection URL of the VeloCloud instance.

    4.  Enable use MID Server and choose the appropriate MID option.

    5.  Select **Submit** and then select **Mark as Complete**.

9.  Schedule data imports using either bulk or filtered discovery by configuring the import schedule.

    1.  Select **Configure** and fill in the fields.

        For more information, see [Set up the Service Graph Connector for Arista VeloCloud schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-the-service-graph-connector-for-arista-velocloud-schedule.md).

    2.  In the **Use connection** field, choose the new VeloCloud instance.

10. Select **Submit**.

11. Confirm that your new instance setup is successful by verifying the configuration.

    1.  Navigate to &gt; **All** &gt; **Service Graph Connectors** &gt; **VeloCloud** &gt; **Connection &amp; Credential Aliases**.

    2.  Confirm that the new alias is listed.

    You can configure multiple connection aliases over the same VeloCloud instance. This flexibility enables you to run imports at different frequencies and apply different filters to each alias.


