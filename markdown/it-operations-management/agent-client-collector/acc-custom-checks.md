---
title: Enable checks from the community for Agent Client Collector
description: You can take checks from the github community and customize them for use in the Agent Client Collector \(ACC\), or you can compose your own scripts. Create a plugin with the customized Sensu check and install it on a ServiceNow instance.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Collect data from your system devices, ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Enable checks from the community for Agent Client Collector

You can take checks from the github community and customize them for use in the Agent Client Collector \(ACC\), or you can compose your own scripts. Create a plugin with the customized Sensu check and install it on a ServiceNow instance.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Copy a check from the github community to your local machine.

2.  Create a `tar.gz` file to be appended to your plugin:

    1.  Create a folder on your local machine.

    2.  Create a sub-folder called `bin`.

    3.  Place the checks you want to run \(scripts and executables\) in the `bin` folder.

    4.  In a Linux environment, give executable permissions to the checks by running `chmod +x filename` on each of the checks.

    5.  Navigate to the parent folder \(above the bin folder\).

    6.  In a Linux environment, run the `tar -C <parent_folder_name> --zcvf <my_plugin_name>.tar.gz *` command.

        In a Windows environment, use an archiving utility that supports the `tar.gz` format.

    7.  In a Windows environment, ensure that you include the following scripts in the `bin` folder:

        -   A batch script configured to run on the check command and initiate the run. For example, `powershell <%~dp0>\test.ps1`

            The `<%~dp0>` variable directs to the drive \(**d**\) and path \(**p**\) of the batch file.

        -   The relevant script \(for example, `test.ps1`\) to be executed in the batch script.
3.  Create a new ACC plugin, as described in [Create and edit Agent Client Collector plugins](create-edit-assets.md).

4.  Test the new plugin.

    1.  Create a new check definition for the customized Sensu check.

        For details, see [Create and edit checks](view-checks.md).

    2.  On the **Check Definition** page, navigate to the **Related Links** section and select **Generate allow list content**.

    3.  Copy the entries you want to include in the allow list and add them to the agent's `check-allow-list.json` file, either manually or using an automation tool.

        The location of this file is indicated in the `allow-list` parameter of the agent's `acc.yml` file.

    4.  Create a new policy and add the newly created check definition.

        For details on creating a policy, see [Create a new Agent Client Collector policy](create-edit-policies.md).

    5.  Select the check definition and in the **Related Links** section, select **Test check**.

5.  Enable credentials when testing a check:

    1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Click **New**.

    3.  Select the type of credentials you want to create.

        For details on creating credentials, see [Create a Connection and Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US).

    4.  Enter values in the fields on the page to assign credentials to your selected credential type.

    5.  Click **Submit**.

6.  Create secure parameters for your check, as described in [Create secure parameters for a check](acc-create-secure-params.md).


