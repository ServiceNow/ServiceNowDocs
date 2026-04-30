---
title: Configure MID-less Agent Client Collector using a single-line command
description: Use a single-line command to set up a MID-less Agent Client Collector. You can also use the single-line command to migrate agents configured with a MID Server to have a MID-less configuration.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Getting started, Configure, Digital End-User Experience, IT Service Management]
---

# Configure MID-less Agent Client Collector using a single-line command

Use a single-line command to set up a MID-less Agent Client Collector. You can also use the single-line command to migrate agents configured with a MID Server to have a MID-less configuration.

## Before you begin

Role required:

-   In a Linux or macOS environment: root
-   In a Windows environment: agent\_client\_collector\_admin

## About this task

Running the single-line command includes flags, which indicate the options to be added to the `acc.yml` configuration file. These options dictate the configuration of the MID-less Agent Client Collector. If you don’t specify an option in the command, the existing option in the `acc.yml` file is used. If there’s no existing option, an error message indicates that the parameter is required to enable connecting to an endpoint.

Running a command validates that a connection can be made with the specified parameter \(for example, the specified registration-key value\). However, the command doesn’t verify if the value of the parameter is valid.

## Procedure

1.  Run the following command in a terminal window: `acc gateway ics <flags>`.

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

Location of the `acc.yml` being configured. Can also be used to modify and validate parameters if the file is in a different location from the default. Can also be used to modify a different file location to check if the parameters specified are valid.

Optional. If no value is entered, the default location of the `acc.yml` file is used.

</td></tr><tr><td>

-b, &lt;--backend-url&gt;

</td><td>

String

</td><td>

The gRPC URL for the ITOM cloud services \(ICS\) gateway.

</td></tr><tr><td>

-i, &lt;--instance-url&gt;

</td><td>

String

</td><td>

The instance URL.

</td></tr><tr><td>

-r, &lt;registration-key&gt;

</td><td>

String

</td><td>

The registration key for the ITOM cloud services \(ICS\) gateway.

</td></tr><tr><td>

-h, help

</td><td>

N/A

</td><td>

Explains what the specified command does.

</td></tr></tbody>
</table>2.  Restart the agent for the configuration settings to be entered into the `acc.yml` file.


