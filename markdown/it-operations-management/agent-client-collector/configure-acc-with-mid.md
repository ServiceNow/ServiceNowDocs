---
title: Configure an Agent Client Collector with a MID Server using a single-line command
description: Use a single-line command to set up an Agent Client Collector with a MID Server. You can also use the single-line command to migrate agents with MID-less configuration to be used with a MID Server.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-08"
reading_time_minutes: 1
breadcrumb: [Configuring Agent Client Collector with a MID Server, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Configure an Agent Client Collector with a MID Server using a single-line command

Use a single-line command to set up an Agent Client Collector with a MID Server. You can also use the single-line command to migrate agents with MID-less configuration to be used with a MID Server.

## Before you begin

Role required:

-   In a Linux or macOS environment: root
-   In a Windows environment: agent\_client\_collector\_admin

## About this task

Running the single-line command includes flags, which indicate the options to be added to the `acc.yml` configuration file. These options dictate the configuration of the Agent Client Collector with the MID Server. If you don’t specify an option in the command, the existing option in the `acc.yml` file is used. If there’s no existing option, an error message indicates that the parameter is required to enable connecting to an endpoint.

Running a command validates that a connection can be made with the specified parameter \(for example, the specified api-key value\). However, the command doesn’t verify if the value of the parameter is valid.

## Procedure

1.  Run the following command in a terminal window: `acc gateway mid <flags>`.

    The available flags appear in the following table:

<table id="table_my3_sgn_xfc"><thead><tr><th>

Flag

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

-y, &lt;--acc-yml&gt;

</td><td>

String

</td><td>

Location of the `acc.yml` being configured. Can also be used to modify and validate parameters if the file is in a different location that the default.Optional. If no value is entered, the default location of the `acc.yml` file is used.

</td></tr><tr><td>

-a, &lt;--api-key&gt;

</td><td>

String

</td><td>

The API key to be used by the MID Server.

</td></tr><tr><td>

-b, &lt;--backend-url&gt;

</td><td>

String

</td><td>

One or more backend connection URLs specifying a websocket endpoint to a MID Server. Multiple values are specified using commas between entries with no spaces separating the values; for example, `<url1>,<url2>`.

</td></tr><tr><td>

-h, help

</td><td>

N/A

</td><td>

Explains what the specified command does.

</td></tr></tbody>
</table>2.  Restart the agent for the configuration settings to be entered into the `acc.yml` file.


**Parent Topic:**[Configuring Agent Client Collector with a MID Server](../concept/acc-configuring-with-mid.md)

