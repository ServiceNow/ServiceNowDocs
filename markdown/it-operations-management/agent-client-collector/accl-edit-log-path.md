---
title: Edit log path configurations
description: Modify a log path configuration in the log shipper check instance.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector log policies, Agent Client Collector Log Analytics, Agent Client Collector, IT Operations Management]
---

# Edit log path configurations

Modify a log path configuration in the log shipper check instance.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **ACC Log Analytics** &gt; **ACC Log Policies**.

2.  Select a policy record.

3.  In the Check instances related list, select the log shipper check instance record.

4.  Select **Edit in Sandbox** to enable editing the record.

5.  On the Log path configuration related list, edit a log path configuration.

    1.  Select the log path configuration that you want to edit.

    2.  Edit the configuration.

        -   You can add custom fields, allowing you to include additional information in the output.
        -   You can add extra configuration options, such as `encoding`, `include_lines`, and `exclude_lines`, to filter your log data. For information about discovering file encoding, see the [How to Detect File Encoding on Windows, Linux and Mac \[KB1702770\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1702770) article in the Now Support Knowledge Base.

            These configuration options impact all the files that the data input streams to your instance.

            **Note:** Define only configuration options that are supported by Filebeat. For more information, see the Log input [Configuration options](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-input-log.html#filebeat-input-log-options) description in the Elastic documentation.

    3.  Select **Update** to save your edits.

6.  Add an environment variable or edit an existing one in the **Path** field.

    Use the relevant format for its name:

    -   On Linux, capitalize the name and precede it with a dollar sign: $. For example: `$HOME`. The name is case sensitive.
    -   On Windows, surround the name with percentage signs: %. For example: `%HOMEPATH%`. The name is not case sensitive.
    **Important:** The servicenow user and ACC agent must have access to the environment variable. On Linux systems, only environment variables that reside in the `/etc/environment` file are accessible. Add the environment variable to this file using the format **&lt;NAME&gt;='&lt;VALUE&gt;'**.

7.  Delete a log path.

    1.  Check the box next to the log path configuration that you want to delete.

        **Note:** You can select multiple log path configurations, but a check must have at least one log path configured for it to enable streaming logs. For more information about checks, see [Checks and policies](../concept/checks-policies.md).

    2.  Select **Delete**.

8.  Select **Return to policy** to go back to the log policy record.

9.  Select **Republish** and then confirm to publish the policy again with the updated log path configurations.

    The changes take effect in a few minutes.


