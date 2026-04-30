---
title: Create an Agent Client Collector log policy
description: Create a new ACC log policy when no default policy exists for the CI that you want Agent Client Collector to monitor.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Agent Client Collector log policies, Agent Client Collector Log Analytics, Agent Client Collector, IT Operations Management]
---

# Create an Agent Client Collector log policy

Create a new ACC log policy when no default policy exists for the CI that you want Agent Client Collector to monitor.

## Before you begin

-   The Agent Client Collector Log Analytics \(ACC-L\) application, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home), must be installed. For more information, see [Agent Client Collector installation](../../agent-client-collector/concept/acc-installation.md).
-   The Agent Client Collector comes with the default **servicenow** user. Ensure that this user has read access to enable Agent Client Collector to view all the configured log paths. For example, the Agent Client Collector **servicenow** user that comes installed with the base system does not have permissions to view the paths to `/var/log/` in Linux and `C:\Windows\System32` in Windows. For information about configuring permissions for the **servicenow** user, see the [ACC-L Permission Denied issues \[KB1117271\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1117271) article in the Now Support Knowledge Base.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **ACC Log Analytics** &gt; **ACC Log Policies**.

    The **Policies** page displays all Log Analytics policies. For a list of the policies that come with the base system, see [Agent Client Collector Log Analytics default policies and checks](../../agent-client-collector/reference/acc-log-analytics-policies-checks.md).

2.  Click **New**.

    **Note:** For general information about creating an ACC policy, see [Create a new Agent Client Collector policy](../../agent-client-collector/task/create-edit-policies.md).

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|A descriptive name for the policy.|
    |Description|Description of the policy.|
    |Publish status|Hard coded as **Draft**, which means that the policy has not yet been published. You cannot edit this field.|
    |Hierarchy|Hard coded as **None**. When a child policy is added to the policy, the value changes to **Parent**. Child policies have a value of **Child**.|

4.  On the **Checks** tab, associate the log policy with the relevant log shipper check.

    -   For Linux and Windows, except for Windows event logs, select the **log shipper** check definition.
    -   For Windows event logs only, select the **log shipper for win events** check definition.
5.  On the **Monitored CIs** tab, specify the CIs to which the policy applies.

    1.  Choose the CI type to be monitored.

        -   **Monitored CI type by filter**: Select the monitored CI type. You can narrow down the CIs that will be monitored by using filter conditions.
        -   **Monitored CI type by script**: Specify the monitored CIs by using a script.
        -   **Monitored CI type by CMDB Group**: Specify the monitored CIs by using CMDB group queries.
        For more information about choosing monitored CI types, see [Create a new Agent Client Collector policy](../../agent-client-collector/task/create-edit-policies.md).

    2.  Monitor only CIs that are associated with an Application Service by selecting **Filter Monitored CIs by Application Service**.

        You can specify the Application Services to be monitored by using filter conditions. Agent Client Collector will only retrieve the logs of CIs that are associated with these Application Services.

6.  Save the log policy.

    In the Check instances related list, a check instance record is created.

7.  Open the relevant check instance record and then select **Edit in Sandbox**.

8.  Select the Log path configurations related list.

9.  Add a log path for the check instance.

    **Note:** A check must have at least one log path configured for it to enable streaming logs. For more information about checks, see [Checks and policies](../../agent-client-collector/concept/checks-policies.md).

    1.  Select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Path|The full path from where the logs are streamed. You can use a wildcard. This field is required.|
        |Component|The device type or stack layer that provides a context for the logs, used for anomaly detection and correlation. For example: Tomcat.|
        |Source Type|Defines how Health Log Analytics handles a specific log type and parses the log data. For example: Tomcat Catalina.|

    3.  For shipping multiline logs using Filebeat, configure the following properties.

        These parameters control how Agent Client Collector Log Analytics \(ACC-L\) handles messages that span multiple lines of text.

        For more information, see [Manage multiline messages](https://www.elastic.co/guide/en/beats/filebeat/current/multiline-examples.html) in the Elastic documentation.

<table id="table_i3n_1v5_rqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

multiline.pattern \(regex\)

</td><td>

The regular expression to match.**Note:** You must define this property before you can configure the multiline.match and multiline.negate properties.

</td></tr><tr><td>

multiline.match

</td><td>

How ACC-L combines matching lines into a single log line.The available options are None, Before, and After. Default is None.

</td></tr><tr><td>

multiline.negate

</td><td>

Option for determining whether the pattern identified in the log lines is negated.The available options are None, True, and False. Default is None.

</td></tr></tbody>
</table>    4.  Define the following properties that control the Filebeat YML configuration.

<table id="table_o1d_stm_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Fields

</td><td>

Field that enables you to include and exclude information in the output. For example, you can add a field for filtering the log data.Add more Field rows by selecting the plus icon next to the Value field: ![Plus icon.](../../agent-client-collector/image/hla-log-path-add-field.png). Remove a Field row by selecting the minus icon: ![Minus icon.](../../agent-client-collector/image/hla-log-path-remove-field.png).

 For more information, see the Log input [Fields](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-input-log.html#filebeat-input-log-fields) description in the Elastic documentation.

</td></tr><tr><td>

Configuration Options

</td><td>

Field that enables you to add configuration options to the log lines. For example, you can add the encoding to use.**Note:** Define only configuration options that are supported by Filebeat.

For more information, see the Log input [Configuration options](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-input-log.html#filebeat-input-log-options) description in the Elastic documentation.

</td></tr></tbody>
</table>    5.  Select **OK**.

        The log path is created.

10. Select **Return to Policy**.

11. On the policy form, select **Publish**.

    The policy's Publish status changes to **Published**.

12. Activate the policy by selecting **Activate**.


## What to do next

[Ensure that the data input is streaming data](../../agent-client-collector/task/accl-verify-log-streaming.md).

