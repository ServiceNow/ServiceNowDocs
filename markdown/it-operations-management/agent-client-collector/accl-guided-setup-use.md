---
title: Set up Agent Client Collector Log Analytics using guided setup
description: Configure Agent Client Collector Log Analytics on your ServiceNow instance using guided setup.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector Log Analytics setup, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Set up Agent Client Collector Log Analytics using guided setup

Configure Agent Client Collector Log Analytics on your ServiceNow instance using guided setup.

## Before you begin

-   Agent Client Collector Log Analytics has a dependency on the ServiceNow® Event Management application. Set up Event Management before you configure Agent Client Collector Log Analytics. For more information, see [Event Management setup](../../event-management/concept/c_EMConfiguration.md).
-   ServiceNow Service Operations Workspace ITOM Apps must be installed. If it is not installed already, install it manually. For more information, see [Install Service Operations Workspace for ITOM application](../../service-operations-workspace-itom/task/install-sow-itom-apps.md).

**Note:** Currently, this setup only supports basic authentication with the MID Server. mTLS is not supported.

Role required: agent\_client\_collector\_admin

## About this task

Agent Client Collector Log Analytics guided setup provides a sequence of tasks that help you configure Agent Client Collector Log Analytics. Using guided setup ensures that you have the minimum required setup to use the application.

**Note:** If you are not using guided setup, you must perform several configuration steps manually. For more information, see [Set up Agent Client Collector Log Analytics without using guided setup](acc-enable-hla.md).

## Procedure

1.  Navigate to **All** &gt; **Guided Setup** &gt; **ITOM Guided Setup**.

    The IT Operations Management Guided Setup welcome screen appears.

2.  Select **Get Started**.

3.  In the Agent Client Collector Log Analytics pane, click **Get Started**.

    ![Agent Client Collector Log Analytics guided setup pane.](../image/accl-guided-setup1.png)

4.  In the **MID setup** section, take the appropriate action:

    -   If you have already configured a MID Server, select **Mark as Complete**.
    -   If you have not configured a MID Server, select **Configure** and set up a MID Server, then select **Mark as Complete**. For more information, see Use MID Server guided setup.

        **Note:** To stream data into the system, you must have a MID Server with the Log Ingestion capability enabled.

    When the MID Server is configured, the status indicator for Agent Client Collector Log Analytics guided setup shows that 64% of the configuration is complete. The progress indicator shows the completion percentage for all the IT Operations Management tasks.

    ![MID Server setup task completed.](../image/accl-guided-setup3.png)

5.  Configure Agent Client Collector Log Analytics.

    1.  In the **ACC Configuration** section, select a setup task and read the instructions in the help pane.

        ![Selected setup task and Configure button.](../image/accl-guided-setup2.png)

    2.  Select **Configure** and complete the task.

        For detailed information about each setup task, consult the Agent Client Collector Log Analytics product documentation.

    3.  Complete all required setup tasks in the task list.

    4.  Select **Mark as Complete** to complete the Agent Client Collector Log Analytics configuration.


