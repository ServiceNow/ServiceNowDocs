---
title: Enable log monitoring in a Linux environment
description: To enable monitoring logs in a Linux environment, select the relevant policy and assign specific check parameters to the policy. When log monitoring is enabled and a specified string is discovered in the log being monitored, the system creates an event.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Enable log monitoring in a Linux environment

To enable monitoring logs in a Linux environment, select the relevant policy and assign specific check parameters to the policy. When log monitoring is enabled and a specified string is discovered in the log being monitored, the system creates an event.

## Before you begin

Ensure that the servicenow user has access to the log file being monitored, or that the specified user can run the `sudo` command.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Policies**.

2.  Select the **Linux log monitoring** policy.

3.  On the **Check Instances** tab, select **util.check-logs** to enable monitoring log files not owned by the **root** user.

    Ensure that the Agent Client Collector **servicenow** user has read permissions for the log file being monitored.

4.  Specify the log file to be searched by the check:

    1.  In the **Check Parameter Definitions** tab at the bottom of the page, select the **file** entry in the **Name** column.
    2.  In the **Default value** field, enter the path of the log file you want to search.
5.  Specify the string you want to locate in the log:

    1.  In the **Check Parameter Definitions** tab at the bottom of the page, select the **pattern** entry in the **Name** column.
    2.  In the **Default value** field, enter the search pattern strings that you want to search for in the log file, such as `404`, `Error`, and so forth. The default values are `SEVERE` and `Exception`.

        Ensure that you separate multiple patterns with a pipe \(\|\) and pass it as a parameter inside quotes. For example: `"SEVERE|404"`.

6.  Click **Update** to save your check instance and return to the **Policy - Linux Log Monitoring** page.

7.  Select the **util.check-logs-sudo** check to monitor logs owned by the root user.

8.  Repeat steps [4](acc-enable-log-monitoring-linux.md#log-file) and [5](acc-enable-log-monitoring-linux.md#string) to monitor logs owned by the root user.

9.  For the **util.check-logs-sudo** check, modify the `/etc/sudoers` file on the host or Linux virtual machine, as follows:

    When the agent is installed on the host's default location \(`/usr/share/servicenow/agent-client-collector`\) or on a Linux virtual machine, add the following string to the `/etc/sudoers` file:

    ```
    servicenow ALL= SETENV: /var/cache/servicenow/agent-client-collector/monitoring-plugin-linux/bin/check-log.rb *
    Defaults:servicenow !requiretty
    Defaults exempt_group += servicenow
    
    ```

10. On the **Policy** page, click **Save** and then click **Publish** to activate the policy to monitor the log file.


