---
title: Create and edit Agent Client Collector plugins
description: Custom plugins extend Agent Client Collector monitoring capabilities beyond the default plugins. You can create plugins for specific monitoring requirements or modify existing plugins.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/create-edit-assets.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Create and edit Agent Client Collector plugins

Custom plugins extend Agent Client Collector monitoring capabilities beyond the default plugins. You can create plugins for specific monitoring requirements or modify existing plugins.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Put every script or executable the plugin needs inside `bin/` .

    -   For Linux and macOS assets, ensure that the agent can execute these files.
    -   Make each script/executable executable before building the archive:`chmod +x bin/my_script.rb bin/helper.sh`
    -   For Windows plugins that run scripts other than batch files, include a batch file in`bin/` that calls the actual script. For example, a batch file can call a PowerShell script using `powershell %~dp0\test.ps1`.
2.  If the plugin requires ACC command allowlist validation, create `allow_list/allow_list.json` at the top level of the plugin folder.

    The file is a JSON array. Each entry defines an allowed executable and the arguments it may receive.

    ```
    [
      {
        "args": [
          "-d",
          "--parent_cache_dir",
          "/var/cache/servicenow/agent-client-collector/"
        ],
        "exec": "my_script.rb",
        "skip_arguments": false
      },
      {
        "args": [
          "--log-level=(FATAL|ERROR|WARN|INFO|DEBUG)",
          "-l",
          "(FATAL|ERROR|WARN|INFO|DEBUG)"
        ],
        "exec": "helper.sh",
        "skip_arguments": false,
        "use_regex": true
      }
    ```

    Field meanings:

    -   **exec**: the file name inside `bin/` that is allowed to run.
    -   **args**: list of allowed arguments. Set **use\_regex** to `true` when an argument is a regular expression.
    -   **skip\_arguments**: when `true`, the agent allows the command to run but does not validate the argument list.
    You can generate a starting allowlist from the instance using the **Agent Client Collector Command Allow-list Generator** page.

3.  Build the `.tar.gz`.

    -   On Linux or macOS:

        Open a terminal, change to the plugin folder \(the folder that contains `bin/``` and optionally `allow_list/```\), then run:

        ```bash
        tar -C . -zcvf my_custom_plugin.tar.gz *
        ```

        Command options:

        -   `-C .` — uses the current folder as the base, so the archive contents sit at the root level \(`bin/`, `allow_list/`\) instead of being wrapped in an extra parent folder.
        -   `-z` — gzip compression.
        -   `-c` — create the archive.
        -   `-v` — verbose output.
        -   `-f my_custom_plugin.tar.gz` — output file name.
        -   `*` — include all files and folders in the current directory.
    -   On Windows:

        Use any archiving utility that supports the `.tar.gz` format. Ensure the archive contains `bin/` at the root and optionally `allow_list/` at the root. Do not wrap the contents in an extra parent folder.

4.  Before you upload, verify that the archive has the correct top-level structure:

    Run the following command:

    ```bash
    tar -tzf my_custom_plugin.tar.gz
    ```

    Expected output:

    ```text
    bin/
    allow_list/
    bin/my_script.rb
    bin/helper.sh
    allow_list/allow_list.json
    ```

    There must be no extra parent directory such as `my_custom_plugin/bin/`.

5.  Attach the `tar.gz` file to the plugin record, according to the instructions that appear on the UI page.

6.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Configuration** &gt; **ACC Plugins**.

7.  Click **New**.

    The **Agent Client Collector Plugin - New record** page appears.

8.  Enter values in the fields on the page, as described in the following table.

    |Field|Description|
    |-----|-----------|
    |**Name**|Plugin name. This field is populated automatically with the name of the tar.gz file attached to the plugin, and is visible only when selecting an existing record.|
    |**Description**|Description of the plugin.|
    |**Operating System**|Selects the operating system to be monitored by the plugin.|
    |**Platform**|Selects the platform to be monitored by the plugin.|
    |**Active**|Selected to activate the plugin and download it to the MID server.|
    |**Advanced**|Selected to enable selecting the operating system version to be monitored by the plugin.|
    |**OS Version**|Selects the operating system version to be monitored by the plugin. This field appears only when selecting the **Advanced** check box.|


-   **[Secure a custom plugin with a certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-self-sign-certificate.md)**  
When you customize or create an Agent Client Collector plugin, you can secure the plugin with either a third-party certificate or an internal secure certificate in the plugin's script. Official plugins are signed by an external certificate authority.

**Parent Topic:**[Deploying Agent Client Collector on servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-server-deployment.md)

