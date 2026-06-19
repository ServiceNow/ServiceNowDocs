---
title: MID Server ECC Queue
description: The External Communication Channel \(ECC\) Queue is a connection point between an instance and the MID Server. Jobs that the MID Server needs to perform are saved in this queue until the MID Server is ready to handle them.The ECC Queue allows you to create ECC Queue messages, access MID Server log entries, and retrieve statistics from an individual MID Server record.The ECC queue is a connection point between an instance and the MID Server. Because the ECC queue processes commands and scripts in managed environments, it is essential to understand the security boundaries and shared responsibilities for secure deployment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/ecc-queue-mid-server.html
release: australia
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
keywords: [ECC queue, MID Server security, security considerations]
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server ECC Queue

The External Communication Channel \(ECC\) Queue is a connection point between an instance and the MID Server. Jobs that the MID Server needs to perform are saved in this queue until the MID Server is ready to handle them.

<table id="table_sf2_dsf_khb"><tbody><tr><td>

![Links to each of the MID Server sections](../image/MIDRefIconBar.png)

</td></tr></tbody>
</table>## Asynchronous Message Bus

The MID Server subscribes to messages published by the Asynchronous Message Bus \(AMB\), which notifies the MID Server that it has pending task records in the ECC Queue. If a task exists in the ECC Queue for that MID Server, the MID Server sets the status to "Processing". When finished working on a requested job, the MID Server reports back to the ECC queue with the results.

The MID Server opens a persistent connection to the instance through the AMB Client and listens on the `/mid/server/<mid_sys_id>` AMB channel. When an output record is inserted into the Queue \[ecc\_queue\] table, an AMB message is sent to the MID Server's channel. The MID Server receives this message and immediately polls the ecc\_queue table for work, unless the MID Server is busy and the message priority level is not Interactive.

The MID Server polls the ECC queue at the maximum regular interval defined in the **mid.poll.time** configuration parameter \(40 seconds by default\), regardless of AMB message activity. If the MID is busy and receeives an AMB message witrh a priority level other than Interactive, the queue poll time changes to **mid.poll.time.standard** \(5 seconds by default\). This polling of the ECC queue at a regular interval is done in case the AMB connection is dropped.

\[Omitted image "MIDServerPollingArchitectureDiagram.png"\] Alt text: MID Server ECC queue polling process

**Note:** The AMB client on the MID Server does not work in all environments and might need to be disabled to avoid performance issues. To disable AMB in your environment, set the **mid.disable\_amb** parameter to **true**. When you disable AMB, the MID Server no longer receives notifications for each new ECC queue output record. See  **mid.poll.time** in  [MID Server parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-parameters.md) for more information.

## ECC Queue information

You can access the ECC Queue by navigating any of these paths:

-   **Discovery** &gt; **Output and Artifacts** &gt; **ECC Queue**
-   **Discovery** &gt; **Discovery Schedules** &gt; **\{schedule name\}** &gt; **\{Discovery status record\}**
-   **ECC** &gt; **Queue**
-   **\{Discovery Status record\}** &gt; **ECC Queue**

An ECC Queue provides the following information:

<table id="table_ecc-queue-fields"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Agent

</td><td>

The name of the external system that this messages is either from or to. If the message is from or to a MID Server, the agent name is in the form `mid.server.xxx`, where xxx is the name of a particular MID Server.

</td></tr><tr><td>

Topic

</td><td>

The name of the probe the MID server ran. If you are using a pattern for discovery, the Horizontal Pattern probe Horizontal Pattern probe appears.

</td></tr><tr><td>

Name

</td><td>

The actual command the probe ran. For example, if **Topic** is SSHCommand, then the **Name** field contains the actual shell command to run. If you are using a pattern for discovery, the following appears: **Pattern Launcher:** followed by the name of the pattern and the multipage number.

</td></tr><tr><td>

Source

</td><td>

The IP address that the discovery is to run against. A few probes run against multiple IP addresses; in those cases, this field contains a human-readable description.

</td></tr><tr><td>

Response to

</td><td>

This optional field contains a reference \(sys\_id\) to the ECC Queue message that this message is in response to. Discovery makes extensive use of this field to track the hierarchy of messages that result from a given scheduled Discovery. Click the record icon for the value in this field to open the ECC Queue record for the activity that spawned the current probe or sensor record.

</td></tr><tr><td>

Queue

</td><td>

An indicator of whether this message was is an input message or an output message.

</td></tr><tr><td>

State

</td><td>

The state of the current ECC queue record. States update automatically.

</td></tr><tr><td>

Processed

</td><td>

The time when this message was processed.

</td></tr><tr><td>

Created

</td><td>

The time when this message was created.

</td></tr><tr><td>

Sequence

</td><td>

The unique sequence number for this message. This value is automatically generated when an ECC Queue record is inserted. Its use is deprecated.

</td></tr><tr><td>

Error string

</td><td>

An error message, if an error occurred during processing. This field is hidden on the standard form unless there was an error.

</td></tr><tr><td>

Payload

</td><td>

The body of the message in XML format. The returned XML has a root tag of `<results>` containing one or more `<result>` tags and a single `<parameters>` tag. The parameters are simply an echo of those sent to the MID server in the probe; they vary from probe to probe, but in general they tell the probe the details of what it is to do and how it should behave. The result tags are the most interesting ones: they contain the actual data generated by the probe.

</td></tr></tbody>
</table>## ECC queue controls

The ECC Queue form contains these related links:

|Related link|Description|
|------------|-----------|
|Run again|Runs the probe again. You can re-run probes when you encounter a failed discovery or other unexpected results.|
|Go to CMDB item|Open the CI record for the CI that was updated during the discovery.|
|Go to Sensor|Open the record for the associated sensor.|

## ECC Queue retry policy

The ECC Queue Retry Policy plugin \(com.glideapp.ecc\_retry\_policy\) needs to be activated to be able to view the ECC Queue Retry Policy and Queue Retry Activity modules.

## Manage ECC Queue content for a MID Server

The ECC Queue allows you to create ECC Queue messages, access MID Server log entries, and retrieve statistics from an individual MID Server record.

### Before you begin

Role required: admin, mid\_server

### Procedure

1.  Send remote commands through a MID Server to a hosting device directly from the ECC Queue without running Discovery.

    1.  Navigate to the ECC Queue and click **New**.

    2.  Create a message with these settings:

        -   **Agent**: The name of the MID Server that executes the command.
        -   **Topic**: Command
        -   **Name**: The actual command that you want to process. For Windows, this is expressed in a DOS command line structure. For Linux, the structure could be a bash command line entry.
        -   **Queue**: Output
        -   **Payload**: With proper XML tags, you can specify the command here instead of in the **Name** field. The advantage to this is that the command is not restricted by the **Name** field length of 120 characters. Use the following XML format for the command:
        ```
        <parameters>
           <parameter name="name" value="ACTUAL_COMMAND_LINE"/>
        </parameters>
        ```

2.  Access entries in the ECC Queue that show **agent0.log.0** logs and **wrapper.log** logs for an individual MID Server.

    1.  Open a MID Server record.

    2.  Under **Related Links**, click **Grab MID logs, files and thread dump**.

        ECC queue records appear in the list using the following filter:

        -   \[Topic\] \[is\] \[SystemCommand\]
        -   \[Source\] \[is\] \[grabLog\]
        -   \[Agent\] \[is\] \[your MID Server\]
        Only **agent0.log.0** and **wrapper.log** entries appear. These logs are also accessible in the `~\agent\logs\` file path.

    3.  To open a log entry, click the link under the **Created** column.

3.  Access the **queue.stats** topic for useful information about individual MID Servers, such as memory and CPU usage data.

    1.  Open a MID Server record.

    2.  Under **Related Links**, click **MID Statistics**.

        ECC queue records appear in the list using the following filter:

        -   \[Topic\] \[is\] \[queue.stats\]
        -   \[Agent\] \[is\] \[your MID Server\]

## ECC queue security considerations

The ECC queue is a connection point between an instance and the MID Server. Because the ECC queue processes commands and scripts in managed environments, it is essential to understand the security boundaries and shared responsibilities for secure deployment.

### JavaScript sandbox bypass

The MID Server does not implement a full JavaScript sandbox. The credential access protection feature enables only digitally signed MID Script Includes to access the restricted Java packages used for credential retrieval. This feature runs in audit mode by default and protects discovery credentials, not all script execution.

Harden the environment where the MID Server is deployed. Hardening measures include:

-   Containerization: Run the MID Server in a container to isolate it from the host system.
-   OS-level controls: On Linux, use kernel security modules such as seccomp or AppArmor to restrict what resources the MID Server can access locally and remotely.
-   Network controls: Limit the outbound network access of the MID Server to only what its discovery and integration workflows require.

For more information, see Operating system security and Virtual infrastructure security.

### Server-side request forgery via HTTP probe

The ServiceNow platform addresses identified input validation gaps for allowed characters in HTTP probe URLs. The platform does not define which internal endpoints are sensitive within your environment.

Plan and restrict which network destinations the MID Server host can reach. Enforce these restrictions at the host or network level based on your environment and use cases:

-   On Windows: Use Windows Firewall to define outbound rules that permit only approved domains and IP addresses. Set a default deny policy for all other traffic.
-   On Linux: Use iptables or nftables to create an outbound allowlist for the MID Server host, dropping all traffic not explicitly permitted.

### OS command injection via WMI Runner source parameter

The WMI Runner component executes WMI queries against Windows targets as part of the MID Server discovery process. Commands pass to the WMI Runner through the ECC queue. Input validation gaps can allow malformed input, such as command concatenation or injection, to pass through the ECC queue and reach the WMI Runner.

The ServiceNow platform identifies and resolves input validation gaps in the MID Server that permit unauthorized characters or command injection through the ECC queue.

Hardening measures include:

-   WMI access permissions: Configure WMI namespace and access permissions so the MID Server service account can execute only the specific queries required for discovery.
-   Windows Group Policy or local security policy: Restrict the system calls, privileged commands, and executable files available to the MID Server service account at the OS level.
-   Host-based firewall rules: Control which Windows target the MID Server can reach via WMI, limiting lateral reach if a command injection attempt succeeds.

### ECC firewall security control bypass via default accept policy

The ServiceNow platform provides two layers of control that work together to govern ECC message handling:

-   ECC firewall: An opt-in, rule-based mechanism configured in `boot-config.yaml`. If no rules match an incoming message and Code Signing is not enabled, the message is accepted for execution by default. MID Server administrators can also configure an explicit accept rule to bypass validation for specific message types.
-   Code Signing: When enabled, Code Signing adds a second layer of enforcement. If no firewall rules match an incoming message, the message proceeds to digital signature verification before execution rather than being accepted automatically.

Used together, these features give you control over what executes on the MID Server.

Review and configure `boot-config.yaml` to verify that the default accept behavior aligns with your security requirements:

-   Review your ECC firewall rules: Verify your rule set covers the message types relevant to your environment so that unintended messages are not silently accepted by default.
-   Enable Code Signing for stricter environments: If your environment requires that all ECC messages be validated before execution, enable Code Signing alongside your ECC firewall rules. This removes the default accept fallback and replaces it with signature verification.
-   Configure accept rules: If you configure explicit accept rules to bypass validation for certain message types, verify those exceptions are intentional and documented.

For more information, see `boot-config-reference.yaml`.

