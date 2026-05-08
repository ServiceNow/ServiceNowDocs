---
title: Modify a data input configuration in Health Log Analytics
description: Change the configuration of a data input for Health Log Analytics by adding a new path to an existing data input configuration or modifying the data input's MID Server destination and port.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [ServiceNow, Health Log Analytics, HLA, data input, configuration, change MID Server port, add new path]
breadcrumb: [Additional data input setup tasks, Set up data inputs manually, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Modify a data input configuration in Health Log Analytics

Change the configuration of a data input for Health Log Analytics by adding a new path to an existing data input configuration or modifying the data input's MID Server destination and port.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  Open a record from the Data Inputs table.

3.  Modify the data input configuration.

<table id="table_mcn_jdb_n4b"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the data input.

</td></tr><tr><td>

Description

</td><td>

Description of the data input.

</td></tr><tr><td>

Port

</td><td>

The port on the MID Server.

**Note:** The port must not be occupied by another process. Make sure that your organization’s security team opens the selected port.

</td></tr><tr><td>

MID

</td><td>

The MID Server to which the logs stream.**Note:**

-   You can select only MID Servers with log ingestion capability that support basic authentication. MID Servers that support mTLS are not listed.
-   The default maximum number of data inputs streaming logs to a single MID Server is 10. You can modify this number in the MID Server properties.


</td></tr></tbody>
</table><table id="table_xxt_k53_n4b"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Path

</td><td>

The full path from which to stream logs. You can use a wildcard.**Note:** This column is not available on Windows systems using Winlogbeat.

</td></tr><tr><td>

Service instance

</td><td>

The service instance to which to bind the log data.**Note:** If no relevant service instance exists, Create an service instance and add CIs to it. Set the status of the new service instance to Operational.

</td></tr><tr><td>

Component

</td><td>

The device type or stack layer as context for the logs that is used for anomaly detection and correlation. For example, Tomcat.Components typically represent CIs in the CMDB. Several components are often clustered together in a single service instance.

</td></tr><tr><td>

Source Type

</td><td>

The source type that defines how Health Log Analytics handles a specific application and parses the log data. For example: Tomcat Catalina.Each data input can have multiple source types depending on the diversity of its log formats. Service instances and components can have any number of source types.

</td></tr><tr><td colspan="2">

For handling multiline messages on Linux / Windows systems using Filebeat only:

</td></tr><tr><td>

Match

</td><td>

Specifies how Filebeat combines matching lines into an event, either **after** or **before**.

</td></tr><tr><td>

Negate

</td><td>

Boolean that defines whether the pattern identified in the log lines is negated. The default is **false**.

</td></tr><tr><td>

Regex

</td><td>

The regular expression to match.

</td></tr></tbody>
</table>    **Note:** You can modify the Rsyslog configuration file to make the agent ship system logs in addition to application logs. For more information, see the [Shipping system logs using Rsyslog \[KB0954507\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0954507) article in the Now Support Knowledge Base.

4.  Select **Update**.

5.  For data inputs that use Rsyslog or Beats agents only, rebuild the server-side configuration file and install it on the endpoint device.

    1.  Select **Rebuild configuration file**.

        Health Log Analytics rebuilds the file and saves it in the Manage Attachments section. Depending on the agent used, the rebuilt file is saved as either `rsyslog.yml`, `filebeat.yml`, or `winlogbeat.yml`.

        The system automatically renames the previous configuration file by adding a suffix with the date and time the file was rebuilt to the file name.

    2.  Install the rebuilt configuration file on the endpoint according to your data input type.

<table id="table_sw2_2y5_s4b"><thead><tr><th>

Data input type

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Rsyslog

</td><td>

1.  Download the file and install it on the endpoint device in the `/etc/rsyslog.d/rsyslog.conf` directory.
2.  Validate the configuration by running the `rsyslogd -N1` command.
3.  Verify the output. If it contains errors, check the `/var/log/messages` system log file for error messages and fix the errors.
4.  Restart Rsyslog by running the `sudo systemctl restart rsyslog` command.


</td></tr><tr><td>

Linux

</td><td>

1.  Download the file and install it on the endpoint device in the `/etc/filebeat/` directory.
2.  Restart the agent service by running the `sudo service filebeat restart` command.
 **Note:** The generated configuration ignores files that were last changed more than six hours ago. If needed, you can change this setting in the configuration file.

</td></tr><tr><td>

Windows using Beats \(Filebeat or Winlogbeat\):

</td><td>

1.  Download the file and install it on the endpoint device in the `C:\Program Files\` directory.
2.  Restart the agent service by running the appropriate command in PowerShell:
    -   Filebeat: `PS > Restart-Service filebeat`
    -   Winlogbeat: `PS > Restart-Service winlogbeat`
 **Note:** The generated configuration ignores files that were last changed more than six hours ago. If needed, you can change this setting in the configuration file.

</td></tr></tbody>
</table>
**Parent Topic:**[Additional data input setup tasks in Health Log Analytics](../concept/hla-data-input-setup-extra.md)

**Related topics**  


[Configure advanced settings for Rsyslog, Splunk, or TCP data inputs in Health Log Analytics manually](hla-data-input-adv-rsyslog-splunk.md)

[Configure advanced settings for Beats data inputs in Health Log Analytics manually](hla-data-input-adv-beats.md)

