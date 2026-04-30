---
title: Validate commands used in pattern-based discovery
description: Validate pattern commands to verify that the MID Server can successfully run them. Typically, commands might fail if you haven't configured the credentials necessary to run these commands on your ServiceNow instance. Another common reason of command failure is that the IP addresses used for discovery aren’t reachable.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Discovery commands for probes and patterns, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Validate commands used in pattern-based discovery

Validate pattern commands to verify that the MID Server can successfully run them. Typically, commands might fail if you haven't configured the credentials necessary to run these commands on your ServiceNow instance. Another common reason of command failure is that the IP addresses used for discovery aren’t reachable.

## Before you begin

-   Verify that you have the following applications:
    -   Pattern Designer Enhancements \(sn\_itom\_pde\)
    -   Discovery and Service Mapping Patterns \(sn\_itom\_pattern\)
-   Check the log for horizontal discovery based on patterns, as described in [Review the logs for horizontal discovery](../../discovery/reference/r_DiscoveryLog.md#).
-   If you are viewing commands for the first time, have upgraded Discovery and Service Mapping Patterns, or have customized any pattern, refresh the command list by navigating to **All** &gt; **Pattern Designer** &gt; **Command Validation Tool** &gt; **Commands List** and selecting **Refresh Command List**.
-   To be able to test credentials on an IP range or IP network, install the ParseIPRanges script include attached to the KB article: [KB1123625: Command Validation Tool](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1123625).

Role required: discovery\_admin

## About this task

Whether you perform discovery using patterns or probes, the MID Server executes commands to access configuration items \(CIs\). Most commands require credentials to run them. In addition, you must assume a role of a user with elevated rights to run some of these commands. If the necessary credentials are missing, discovery fails.

For pattern-based discovery, you can validate all commands used by a certain pattern simultaneously.

You can also validate discovery commands to check that the IP addresses you’re using for discovery are reachable. Sometimes IP addresses are incorrect or the servers using these IP addresses are down.

If you validate commands that contain applicative credentials, the Command Validation Tool checks the Connections and Credentials module and uses relevant applicative credentials configured there.

Starting with Pattern Designer Enhancements version 3.9.0, the new pde\_viewer role can view the command validation task results through the **Command Validation Tasks** and **Command Validation Task Results** modules but can't edit or modify them. For more information, see [View command validation task results in pattern-based discovery](../../discovery/task/view-command-validation-task-results.md).

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Command Validation Tool** &gt; **Create New**.

2.  To validate all commands used by a pattern, select **Validate All Pattern Commands**.

3.  Fill in the fields as described in [Command Validation Tasks form for pattern-based discovery](../reference/command-validation-reference.md).

4.  Select and hold \(or right-click\) the form header and select **Save**.

5.  If the commands you selected contain temporary variables, add the values for these variables before validating such commands.

    1.  Select **Refresh Temporary Variable Mappings** under **Related Links**.

        The tool creates a list of all temporary variables for the chosen commands and IPs.

    2.  Select the **Temporary Variable Mappings** tab and enter the values for the temporary variables.

        ![The value column](../image/pde-command-validation-temporary-variable.png "Temporary Variable Mappings tab")

6.  Select **Run Command Validation**.

7.  Check if **FAILURE** appears in the **Result** column in the **Command Validation Task Results** section.

    ![Validation Task Result section](../image/pde-command-validation-task-result.png)

8.  Select the link in the **Command Validation Test** column.

9.  Review the description in the **Results Details** field.


## What to do next

1.  Select the **Open suggestions to troubleshoot failure** link.

    ![Open suggestions to troubleshoot failure](../image/pde-command-validation-task-result-suggestion.png)

2.  Follow the instructions in the **Steps to Remediate** window.

**Related topics**  


[Discovery commands for probes and patterns](../../discovery/concept/discovery-command-probe-pattern.md)

[Getting started with credentials](https://www.servicenow.com/docs/access?context=credentials-getting-started&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

[Command List form for pattern-based discovery](../reference/commands-list-discovery.md)

[Discovery CLI commands](../../discovery/reference/discovery-cli-commands.md)

