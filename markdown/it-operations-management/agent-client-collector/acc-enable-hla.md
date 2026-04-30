---
title: Set up Agent Client Collector Log Analytics without using guided setup
description: Configure the Agent Client Collector to stream log data from Linux and Windows hosts to a ServiceNow instance without using guided setup.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Agent Client Collector Log Analytics setup, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Set up Agent Client Collector Log Analytics without using guided setup

Configure the Agent Client Collector to stream log data from Linux and Windows hosts to a ServiceNow instance without using guided setup.

## Before you begin

**Note:** You can configure Agent Client Collector Log Analytics using guided setup. The guided setup ensures that you have the minimum required setup for using the application. For more information, see [Set up Agent Client Collector Log Analytics using guided setup](accl-guided-setup-use.md).

-   The Agent Client Collector Log Analytics \(ACC-L\) plugin must be installed. The plugin comes with the Agent Client Collector Framework \(ACC-F\) and Agent Client Collector Monitoring \(ACC-M\) plugins. For more information, see [Agent Client Collector installation](../concept/acc-installation.md).
-   ServiceNow Service Operations Workspace ITOM Apps must be installed. If it is not installed already, install it manually. For more information, see [Install Service Operations Workspace for ITOM application](../../service-operations-workspace-itom/task/install-sow-itom-apps.md).
-   Agent Client Collector Log Analytics has a dependency on the Health Log Analytics application, Version 22.0.12 - December 2021 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). Streaming log data from Windows hosts is supported in Agent Client Collector Log Analytics Version 3.1.0 and later.

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   The Agent Client Collector comes with the default **servicenow** user. Ensure that this user has read access to enable Agent Client Collector to view all the configured log paths. For example, the Agent Client Collector **servicenow** user that comes installed with the base system does not have permissions to view the paths to `/var/log/` in Linux and `C:\Windows\System32` in Windows. For information about configuring permissions for the **servicenow** user, see the [ACC-L Permission Denied issues \[KB1117271\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1117271) article in the Now Support Knowledge Base.

**Note:** Currently, this setup only supports basic authentication with the MID Server. mTLS is not supported.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **MID Servers**.

2.  On the MID Server page, select a MID Server that is validated and has a Status value of **Up**.

3.  On the MID Server page for the selected server, select **Setup ACC Log Analytics** in the related links section.

    Agent Client Collector Log Analytics setup starts.

    In addition, the system automatically creates an ACC data input. When it has been created, the data input record is added to the ACC data inputs table and the data input is ready to stream logs.

    **Note:** It is important to configure an ACC data input for every MID Server to which Agent Client Collectors can connect. For more information, see [Set up additional ACC data inputs](accl-data-input-setup.md).

    The system also prompts you to set up the MID Web Server. For more information, see [MID Web Server](../../event-management/concept/mid-web-server.md).

4.  In the ACC Log Analytics Setup dialog box, configure the ports.

    1.  In the **MID Web Server Port** and **ACC data input Port** fields, enter the appropriate port numbers.

    2.  Select **OK**.

        The URL with the configured endpoint appears in the dialog box.

    3.  Copy and save the endpoint URL for use when installing the ACC agent on the endpoint machine.

5.  Navigate to **All** &gt; **Agent Client Collector** &gt; **MID Web Server API Key** and copy and save the MID Web Server API key for use when installing the ACC agent on the endpoint machine.

6.  Install the ACC agent on the endpoint machine.

    **Note:** If you have already installed the ACC agent, proceed to [Agent Client Collector log policies](../../health-log-analytics-admin/concept/hla-acc-data-input-log-policies.md).

    1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Downloads**.

    2.  Download the ACC agent for the appropriate operating system.

        For detailed instructions, select the documentation link for the operating system. For example:

        ![ACC agent installation documentation example.](../image/accl-agent-install-documentation-ex.png)


## Result

Agent Client Collector Log Analytics and the ACC agent are installed. You can start using the application.

## What to do next

Review the [Agent Client Collector log policies](../../health-log-analytics-admin/concept/hla-acc-data-input-log-policies.md).

