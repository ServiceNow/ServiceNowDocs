---
title: MID Server parameters
description: Parameters control the behavior of a particular MID Server and have lower precedence than MID Server properties.Use a MID Server parameter to control the behavior of a particular MID Server.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 39
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server parameters

Parameters control the behavior of a particular MID Server and have lower precedence than MID Server properties.

<table id="table_ibb_fsf_khb"><tbody><tr><td>

![Links to each of the MID Server sections](../image/MIDRefIconBar.png)

</td></tr></tbody>
</table>To add a parameter to a MID Server, see [Add a MID Server parameter](mid-server-parameters.md#).

**Important:** Changes to parameters only take effect when the MID Server is started \(or restarted\).

**Note:** The value of any MID Server parameter in the config.xml file can be encrypted. See [Encrypt or decrypt MID Server configuration file values](../task/mid-server-manual-encryption.md) for more information.

## Required parameters

**Note:** Using special characters in an XML configuration file requires you to encode them.

-   **url**

    Specifies the URL to the associated instance. Normally the URL is similar to https://instance.service-now.com, where you replace instance with the instance name. If you host your own instance, use the URL set by your organization.

    -   Type: string
    -   Default value: none
-   **mid\_sys\_id**

    Records the MID Server record's unique identifier. This parameter should be empty when you initially configure a MID Server. Do not change the value.

    -   Type: string
    -   Default value: automatically set \(GUID\)
-   **name**

    Use this parameter to supply a name that is meaningful for you. If you do not supply this parameter, the MID Server uses the default value. A set of business rules synchronizes the name in the configuration file with the name in the MID Server record. The business rules ensure that changing the name in one location also changes the name in the other location.

    -   Type: string
    -   Default value: YOUR\_MIDSERVER\_NAME\_GOES\_HERE
-   **mid.instance.username or glide.glidesoap.username**

    If the ServiceNow instance has authentication enabled, as it is by default, set this parameter to define the user name the MID Server should use to log in to the instance. This user should have the mid\_server role on the ServiceNow instance in order to access necessary tables and fields. You can use this parameter to define user names with special characters.

    -   Type: string
    -   Default value: none
-   **mid.instance.password or glide.glidesoap.password**

    If your ServiceNow instance has authentication enabled, as it is by default, set this parameter to define the password the MID Server should use to log in to the instance. You can use this parameter to define passwords with special characters.

    -   Type: string
    -   Default value: none

## CIM parameters

-   **mid.cim.batch.size**

    Specifies the maximum number of messages sent at once to a CIM server.

    -   Type: integer
    -   Default value: 1
-   **mid.cim.request.interval**

    Specifies the number of milliseconds to wait between requests to the same Common Information Model Object Manager \(CIMOM\).

    -   Type: integer
    -   Default value: 0
-   **mid.cim.host.connection.limit**

    Specifies the maximum number of simultaneous connections to each CIMOM. A value of zero disables simultaneous connections.

    -   Type: integer
    -   Default value: 0

## Connection parameters

-   **glide.mid.fast.responses**

    Instructs the MID Server to try sending messages to the instance as soon as they are ready. Normally the MID Servers end messages to the ServiceNow instance serially \(that is, one message at a time\). Since many probes can be run in parallel, there can be multiple messages transmitted simultaneously to the instance. Setting this parameter to **true** may decrease the time between a probe's completion and its response arriving at the instance. However, the multiple simultaneous messages consume resources, decreasing the overall instance responsiveness. If there are communications problems, this parameter's value can also cause a logjam on the MID Server, as threads normally used for running probes may become consumed for sending messages. Generally, leave this parameter out of your configuration. Setting it to **true** is meaningful only under very special circumstances.

    -   Type: true \| false
    -   Default value: false
-   **glide.mid.max.sender.queue.size**

    Places an upper limit on how large the queue is allowed to get. The MID Server starts deleting queued messages if this limit is exceeded. When the MID Server generates messages to the ServiceNow instance faster than it can send them, it queues them temporarily on the file system of the MID Server's host. This queue is normally quite small, and is completely emptied as soon as the MID Server processing slows for a short period. However, this queue can grow in size when there are communication problems between the MID Server and the instance, and especially if there is an integration running on the MID Server.

    The parameter is of the form \{number\}\{multiplier\}, where \{number\} is any positive decimal number including non-integers, and the optional multiplier is any spelling of bytes, kilobytes, megabytes, gigabytes, or terabytes \(only the first character is tested, and the test is case-insensitive\). The default multiplier is bytes. White space is liberally tolerated. The following strings all represent valid parameters: "1000000000", "0.5m", "5 GB", "7.67gigas", "145.69392 meg", and "1.1 terra".

    -   Type: string
    -   Default value: 0.5 GB
-   **instance.date.format**

    Specifies the format the instance uses for dates and times. The primary impact of setting this parameter is to allow the MID Server to correctly refresh its start and stop times on the MID Server record in ServiceNow. The format of this date/time string is identical to that used by the Java SimpleDateFormat class.

    -   Type: string \(Date format\)
    -   Default value: yyyy-MM-dd HH:mm:ss
-   **mid.disable\_amb**

    Disables the Asynchronous Message Bus \(AMB\) notifications for new ECC queue output messages. For more information, see the Asynchronous Message Bus section in[Asynchronous Message Bus](../concept/ecc-queue-mid-server.md#section_b5j_ysv_s1b). When AMB is enabled the MID Server uses a different default polling interval than when AMB is disabled. See the **mid.poll.time** parameter for more details. If you set a polling interval with the **mid.poll.time** parameter, the MID Server uses that value whether or not the AMB client is enabled.

    -   Type: true \| false
    -   Default value: false
-   **mid.https.truststore.password**

    Sets the trustStore password that is required for HTTPS connections with the Asynchronous Message Bus \(AMB\) Client.

    -   Type: string
    -   Default value: none
-   **mid.https.truststore.path**

    Path to the trustStore to be used by the MID Server for TLS transactions \(Asynchronous Message Bus \(AMB\) Client\). Add this parameter only if you want to change the default path.

    -   Type: string
    -   Default: Path to the JRE trustStore bundled with the MID Server
-   **mid.instance.skip\_basic\_auth**

    Allows the MID Server to connect to an instance using cookies instead of basic authentication credentials. When set to **true**, it uses cookies first. However, if the connection fails, the MID Server will try to connect again using basic authentication credentials.

    -   Type: true \| false
    -   Default value: true
-   **mid.jmx.enabled**

    Enables a JMX server on the MID Server, which exposes some management information to JMX consoles. Implementing JMX requires additional configuration of the Java runtime environment. Setting this parameter to **true** is only recommended for those with detailed knowledge of the Java security architecture and a specific need for JMX.

    -   Type: true \| false
    -   Default value: false
-   **mid.poll.time**

    Sets the default MID Server polling interval \(in seconds\). The polling interval is the amount of time the MID Server waits before checking the ECC queue for work when the MID Server is not busy. For more information, see the Asynchronous Message Bus section in.

    When **mid.disable.amb** is set to false \(the default setting\), see the Asynchronous Message Bus section in [Asynchronous Message Bus](../concept/ecc-queue-mid-server.md#section_b5j_ysv_s1b) for more information about how **mid.poll.time** is used.

    When **mid.disable.amb** is set to true, polling occurs on a fixed **mid.poll.time** interval, but polling switches to using **mid.poll.time.standard** \(5 seconds by default\) when the MID Server is busy.

    -   Type: integer \(seconds\)
    -   Default value: 40 when **mid.disable.amb** is false, or 5 when **mid.disable.amb** is true.
-   **mid.probe.wait.resources**

    Indicates whether probe execution is delayed until resources are available. Used to enable [MID Server Resource Reservation](../concept/mid_server_resource_reservation.md#).

    **Note:** Requires MID Server restart.

    -   Type: true \| false
    -   Default value: true
-   **mid.property.long\_runner**

    Identifies the name of a script include that manages long running commands.

    **Note:** This property is applicable till the Rome version only. If your instance is of a later version, you must configure the system property, **glide.eccprobe.longrunner.class**.

    -   Type: string
    -   Default value: LongRunner
-   **threads.interactive.max**

    Sets the maximum number of interactive worker threads that can run simultaneously in the interactive thread pool. See [Set MID Server Thread Use](../task/t_SetMIDServerThreadUse.md).

    -   Type: integer
    -   Default value: 10
-   **threads.expedited.max**

    Sets the maximum number of expedited worker threads that can run simultaneously in the expedited thread pool. See [Set MID Server Thread Use](../task/t_SetMIDServerThreadUse.md).

    -   Type: integer
    -   Default value: 20
-   **threads.max**

    Sets the maximum number of standard worker threads that can run simultaneously in the standard thread pool. This parameter provides direct control over what CPU resources the MID Server consumes on the computer that hosts it. See [Set MID Server Thread Use](../task/t_SetMIDServerThreadUse.md).

    -   Type: integer
    -   Default value: 25
    **Important:** You can set threads.max as high as 200, however, this setting may need to be changed depending on the OS. For example, Windows-based MID Servers running Discovery uses Powershell which is resource intensive. In this case, you may exhaust the CPU power of the host machine with just 50 threads count.


## Credentials parameters

-   **mid.aws.instance\_profile\_name**

    Name of the AWS IAM role configured on the EC2 instance. When configured, the MID Server uses the temporary credentials granted to this role by the AWS instance profile to Discover cloud resources.

    -   Type: string
    -   Default value: None \(User must provide a non-blank value\)
-   **mid.credentials.provider**

    Specifies the Java class name of the credentials provider.

    -   Type: string
    -   Default value: com.service\_now.mid.creds.standard.StandardCredentialsProvider
-   **mid.secure\_credentials.key\_pairs.provider**

    Class that the MID Server uses to generate secure key pairs.

    -   Type: string
    -   Default value: com.service\_now.mid.keypairs.provider.standard.StandardKeyPairsProvider

## Debug parameters

-   **debug.logging**

    \[Deprecated\] Specifies whether to enable logging of MID Server events and messages \(both sent and received\). Normally this parameter is only used by developers, but it is occasionally useful when troubleshooting a problem. Be aware that setting this parameter to **true** causes intensive logging on the MID Server, potentially using considerable disk space.

    -   Type: true \| false
    -   Default value: false
    This parameter has been replaced by the **mid.log.level** parameter.

-   **debug**

    \[Deprecated\] Specifies whether to enable debug logging on the MID Server. Normally this parameter is only used by developers, but it is occasionally useful when troubleshooting a problem. Be aware that setting this parameter to **true** causes intensive logging on the MID Server, potentially using considerable disk space.

    -   Type: true \| false
    -   Default value: false
    This parameter has been replaced by the **mid.log.level** parameter.

-   **file.probe.template.debug**

    Specifies whether to debug file probe templates.

    -   Type: true \| false
    -   Default: false
-   **mid.cim.debug**

    Specifies whether to enable debug logging for CIM, WBEM, SLP, or SMI-S.

    -   Type: true \| false
    -   Default value: false
-   **mid.ssh.debug**

    Enables SSH debug information in the log file. The parameter usage depends on whether the ServiceNow SSH client is enabled.

    When the ServiceNow SSH client is enabled, the parameter functions as follows:

    -   Type: string
    -   Default value: false

        The following string values are valid for the ServiceNow SSH client:

        -   true: Enables SSH debug information in the log file.
        -   false: Disables SSH debug information in the log file.
        -   &lt;IP Addresses&gt;: Specify which IP ranges to enable SSH debug information in the log file. You can enter IP addresses in the following formats:
            -   An IP range defined by a slash and the number of bits in the subnetwork. For example, the string 10.10.10.0/24 scans 24 bits of IP addresses from 10.10.10.0 to 10.10.10.254.
            -   An IP range defined by a dash. For example, the string 10.10.11.0-10.10.11.165 scans the IP addresses from 10.10.11.0 to 10.10.11.165.
            -   A comma-separated list of specific IP addresses. For example the string 10.10.11.200,10.10.11.235 scans the IP addresses 10.10.11.200 and 10.10.11.235.
        -   deferred: Logs SSH debug information in memory unless an error or warning occurs. If an error or warning occurs, the platform publishes the debug information to the log file. This ensures that only the part of the log file pertaining to the error or warning is recorded. If no error or warning is detected, the platform deletes the unused log data from memory when the session closes. Each session stores up to 1000 log messages. If the session exceeds 1000 log messages, the deferred log discards the oldest log message to make room for the newest log message.
    When the ServiceNow SSH client is disabled, the parameter enables or disables SSH debug information in the log file:

    -   Type: true \| false
    -   Default value: false
    **Note:** The MID Server parameter **mid.ssh.debug** only affects SNCSSH and J2SSH. To enable Maverick client debug logging, set the MID Server configuration parameter **mid.log.level** to `debug, com.maverick=debug`.

-   **mid.log.level**

    Specifies the logging level for the MID Server. Possible values are:

    -   debug
    -   info
    -   warn
    -   error
    **Note:** Values are case insensitive.

    -   Type: string
    -   Default value: info
-   **mid.http.idle\_connection\_monitor.debug**

    Enables debug logging for the Idle Connection Monitor.

    -   Type: true \| false
    -   Default value: false

## DNS parameters

-   **mid.dns\_scan.regulator.interval\_ms**

    Specifies the interval between DNS scans in milliseconds.

    -   Type: integer
    -   Default value: 10
-   **mid.dns\_scan.regulator.packets\_per\_interval**

    Specifies the number of regulator packets per DNS scan.

    -   Type: integer
    -   Default value: 1
-   **mid.dns\_scan.default\_name\_servers**

    Specifies the host names or IP addresses of the default name servers.

    -   Type: string
    -   Default value: none
-   **mid.dns\_scan.default\_name\_servers**

    Specifies the host names or IP addresses of the default name servers.

    -   Type: string
    -   Default value: none
-   **mid.dns\_scan.additional\_name\_servers**

    Specifies the host names or IP addresses of any additional name servers.

    -   Type: string
    -   Default value: none
-   **mid.dns\_scan.load\_balancing\_enable**

    Specifies whether to enable load balancing of name servers.

    -   Type: true \| false
    -   Default value: false
-   **mid.probe.use\_legacy\_forward\_dns**

    Enables the legacy DNSNameResolver probe and disables the default DNSNameResolver probe. See [Probes used by Orchestration](https://www.servicenow.com/docs/access?context=r_OrchestrationProbes&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) for more information.

    -   Type: true \| false
    -   Default value: false
-   **mid.probe.use\_legacy\_reverse\_dns**

    Enables the legacy DNS probe and disables the default DNS probe. If you experience problems with the features of the default DNS probe, use this parameter to disable those features. The default DNS probe's features include being lightweight and faster due to executing in parallel, while the legacy probe is throttled by the MID Server because it executes in serial. The default probe utilizes DNS lookup by the MID Server host OS to make use of the OS maintained DNS cache, while the legacy probe does not. Consequently, after a DNS lookup by the default probe fails in Windows systems, the OS also tries looking up by NETBIOS name.

    -   Type: true \| false
    -   Default value: false

## Event Management parameters

-   **mid.probe.event.bulk\_size**

    Specifies the maximum size of an event payload, in MB.

    -   Type: integer
    -   Default value: 120
-   **mid.probe.event.wait\_time**

    Waiting period on an empty queue for sending events.

    -   Type: integer
    -   Default value: 1000
-   **mid.probe.event.send.enabled**

    Enables or disables the sending of events.

    -   Type: true \| false
    -   Default value: true
-   **mid.probe.event.queue.max\_size**

    Specifies the maximum size permitted for the event queue before incoming events are rejected.

    -   Type: integer
    -   Default value: 100,000
-   **mid.probe.event.max.retry\_time**

    The maximum number of seconds MID retries sending events.

    -   Type: integer
    -   Default: 1800
-   **mid.probe.event.queue.use\_bulk**

    Specifies whether events are sent to the server singly or in bulk. If this parameter evaluates to **true** then events are sent to the server in bulk.

    -   Type: true \| false
    -   Default value: true
-   **mid.probe.event.suppress.whitespaces**

    Allows line breaks in description fields for multi-line events. Apply this parameter to each MID Server used with event connector instances. Choices are:

    -   **all**

        This setting removes all whitespaces.

    -   **leave\_as\_is**

        This setting keeps all whitespaces.

    -   **keep\_newline**

        This setting keeps only new\_line and removes all other whitespaces.

    -   Type: string
    -   Default: all
-   **mid.em.metric.metric\_to\_ci\_map\_limit**

    Specifies the maximum number of active metrics allowed per CI map.

    -   Type: integer
    -   Default value: 200,000
-   **mid.em.metric\_binding\_timeout\_seconds**

    Specifies the number of seconds to wait before resending unhandled events

    -   Type: integer
    -   Default value: 300
-   **mid.em.metric\_binding\_timeout\_max\_seconds**

    Specifies the maximum number of seconds to wait before resending unhandled events.

    -   Type: integer
    -   Default value: 10800
-   **mid.em.metric\_max\_elapsed\_time\_before\_refresh**

    Specifies the maximum number of seconds before the metric source type cache is refreshed in memory.

    -   Type: integer
    -   Default value: 60
-   **mid.em.matric\_max\_sql\_string\_length\_for\_types**

    Specifies the maximum length of the string \(composed of types\) used for an SQL command

    -   Type: integer
    -   Default value: 30000
-   **mid.em.statistics\_report\_perioon\_sec**

    Specifies the period, in seconds, between statistics reports to the instance. Use **0** to disable reporting. This parameter requires a restart.

    -   Type: integer
    -   Default value: 60
-   **mid.em.metric\_connector\_max\_run\_time\_seconds**

    Specifies the maximum number of seconds to collect metrics in every cycle.

    -   Type: integer
    -   Default value: 300
-   **mid.em.metric\_connector\_history\_min**

    Specifies the number of minutes to go back in history to retrieve metrics.

    -   Type: integer
    -   Default value: 180
-   **mid.em.metric\_event\_logging**

    Specifies the level of metric and event logging. Choices are:

    -   none
    -   all
    -   events
    -   metrics
    -   metrics:&lt;filter&gt;
    -   events:&lt;filter&gt;
    -   Type: string
    -   Default value: none
-   **mid.em.metric\_connector\_late\_arrivals\_delay**

    Specifies the number of seconds to delay when collecting metrics.

    -   Type: integer
    -   Default value: 30

## FTP connection parameters

-   **mid.ftp.max\_pool\_size**

    Specifies the maximum size of the FTP Connection Pool, in megabytes.

    -   Type: integer
    -   Default value: 25
-   **mid.ftp.max\_per\_target**

    Specifies the maximum number of the FTP connections per target.

    -   Type: integer
    -   Default value: 5
-   **mid.ftp.max\_conn\_idle\_time**

    Specifies the maximum amount of time, in milliseconds, that an FTP connection can sit idle in the pool.

    -   Type: integer
    -   Default value: 300000
-   **mid.filesystem.max.ls**

    Specifies the maximum number of files that can be returned in the filesystem list directory command.

    -   Type: integer
    -   Default value: 10000

## Logging parameters

-   **disable\_monitors**

    Specifies whether to disable the MID Server from actively checking for monitors on the instance.

    -   Type: true \| false
    -   Default value: true
-   **mid.show.queries**

    Instructs the MID Server whether to log details about every query it makes to the ServiceNow instance. Typically this parameter is only used by developers, but it is occasionally useful when troubleshooting a problem. Be aware that setting this parameter to **true** causes intensive logging on the MID Server, potentially using considerable disk space.

    -   Type: true \| false
    -   Default value: false
-   **disable.remote.logging**

    Prevents the MID Server from logging any information to the MID Server log on the instance. Relatively little information is logged on the instance in any case, but setting this parameter to **true** eliminates all logging to the instance.

    -   Type: true \| false
    -   Default value: false
-   **disable.status**

    Prevents the MID Server from sending a status report to the instance every 10 minutes.

    -   Type: true \| false
    -   Default value: false
-   **mid.file\_cleaner.disabled**

    Files and empty folders within the following folders may be deleted by this MID File Cleaner. Files last accessed more than 30 days ago are deleted. It runs on start-up, and then every 24 hours after that. You can force the File Cleaner to run by restarting the MID Server service.

    Folders/files cleaned:

    -   `\agent\import`
    -   `\agent\export`- Used by the Export Set feature.
    -   \\`agent\work\monitors\ECCSender\output_error` - Used for ECC input payloads that cannot be inserted for any reason
    -   `\agent\work\monitors\ECCSender\output_oversize` - Used for saving copies of payloads that are not sent to the instance because they are larger than the limit set by **mid.eccq.max\_payload\_size**, which defaults to 20000000 bytes
    -   `\agent\logs`- Specifically JFR Dumps
    -   Type: true \| false
    -   Default value: false

## mTLS protocol parameters

Add these parameters to the `config.xml` file in the `/agent` directory, in the MID Server installation directory.

-   **mid.httpclient.protocol.myprotocol.path**

    Specifies the path to the keystore. The path can be absolute or relative. In the parameter name, make sure you replace **myprotocol** with the name of your protocol.

    Type: String.

-   **mid.httpclient.protocol.myprotocol.port**

    Specifies the port number for the protocol. In the parameter name, make sure you replace **myprotocol** with the name of your protocol.

    Type: String.

-   **mid.httpclient.protocol.myprotocol.password**

    Specifies the mTLS credential password. In the parameter name, make sure you replace **myprotocol** with the name of your protocol. Add the encryption attribute **secure="true"** to encrypt the password using standard MID Server encryption.

    Type: String.


## Pattern parameters

-   **mid.parsing.max\_field\_size**

    Sets the maximum character length of strings stored as temporary variables while patterns are run. Strings longer than this parameter's value are truncated to equal the value. Use the parameter to increase the limit when parsing longer strings.

    **Warning:** Exceeding the max field size limits of the SQL database implementation cause errors.

    -   Type: integer
    -   Default value: 1024
-   **mid.sa.discovery.pattern\_string\_attributes.deduplicate**

    Reduces memory consumption for pattern execution context attributes by eliminating duplicate strings.

    -   Type: true \| false
    -   Default: true

## Proxy server parameters

-   **mid.instance.use\_proxy or mid.proxy.use\_proxy**

    If your MID Server must go through a web proxy to access the ServiceNow instance, set this parameter to **true** to instruct the MID Server to use the proxy. You must also set the proxy server's host and port, and perhaps the user name and password as well.

    -   Type: true \| false
    -   Default value: false
-   **mid.proxy.host**

    If your MID Server must go through a web proxy to access the ServiceNow instance, set this parameter to define the proxy's host.

    -   Type: string
    -   Default value: none
-   **mid.proxy.password**

    If your MID Server must go through a web proxy to access the ServiceNow instance, and your proxy requires a password, set this parameter to define that password.

    -   Type: string
    -   Default value: none
-   **mid.proxy.port**

    If your MID Server must go through a web proxy to access the ServiceNow instance, set this parameter to define the proxy's port.

    -   Type: integer \(0-65535\)
    -   Default value: 80
-   **mid.proxy.username**

    If the MID Server must go through a web proxy to access the ServiceNow instance, and the proxy requires a user name, set this parameter to define that user name.

    -   Type: string
    -   Default value: none

## Request timeout override parameters

-   **mid.sa.cloud.request\_timeout**

    Sets the timeout in milliseconds for cloud requests. This parameter overrides the **glide.http.timeout** system property, which specifies the maximum number of milliseconds to wait before an outbound REST transaction times out.

    -   Type: integer
    -   Default value: 30000
-   **mid.http\_classy.request\_timeout**

    Sets the timeout in milliseconds for HTTP classification requests with the HTTP - Classify probe. This parameter overrides the **glide.http.timeout** system property, which specifies the maximum number of milliseconds to wait before an outbound transaction times out.

    -   Type: integer
    -   Default value: 30000

## Security parameters

-   **mid.windows\_host.file\_permissions.allow\_list**

    Sets an inclusion list for Windows file permissions enforcement to improve security. The parameter takes a string of comma separated group names, user names, and SIDs. Group and user names must follow SAM account naming requirements. Domain accounts can be specified by using the SID.

    -   Type: string \(comma separated group and user names\)
    -   Default value: None
-   **mid.windows\_host.file\_permissions.enforce**

    Enables the MID Server to use Windows file permissions enforcement to improve security. Setting this parameter to **false** will prevent the MID Server from updating the file permissions inclusion list, but will not revert the file permissions.

    -   Type: true \| false
    -   Default value: true

## Shazzam parameters

-   **mid.shazzam.regulator.interval\_ms**

    Sets the interval, in milliseconds, in which Shazzam can launch packets. This parameter works with the **mid.shazzam.regulator.packets\_per\_interval** parameter to set the number of packets allowed in this interval. By default, Shazzam launches one packet each millisecond.

    -   Type: integer
    -   Default value: 1
-   **mid.shazzam.regulator.packets\_per\_interval**

    Sets the number of packets that Shazzam can launch in the configured time interval. This parameter works with the **mid.shazzam.regulator.interval\_ms** parameter, which sets that interval. By default, Shazzam launches one packet each millisecond.

    -   Type: integer
    -   Default value: 1
-   **mid.shazzam.chunk\_size**

    Specifies the maximum number of IP addresses that Shazzam scans in parallel. This parameter primarily controls outbound port consumption.

    -   Type: integer
    -   Default value: 100
-   **mid.shazzam.threads**

    Specifies the number of concurrent threads that Shazzam uses. Setting this or the mid.shazzam.max\_scanners\_per\_thread parameter to 0 disables Shazzam multi-thread optimization.

    -   Type: integer
    -   Default value: 5
-   **mid.shazzam.max\_scanners\_per\_thread**

    Specifies the number of concurrent scanners processed by each Shazzam thread. Setting this or the mid.shazzam.threads parameter to 0 disables Shazzam multi-thread optimization.

    -   Type: integer
    -   Default value: 500

## SNMP configuration parameters

-   **mid.snmp.enable\_auto\_public**

    Specifies whether to use the SNMP public community string automatically if no other SNMP credentials were successful.

    -   Type: true \| false
    -   Default value: true
-   **mid.snmp.request.timeout**

    Specifies the timeout value for the first OID request, in milliseconds. For subsequent requests \(for example, table OIDs\), the **mid.snmp.session.timeout configuration** parameter \(see below\) takes effect.

    **Note:** You can override this parameter with the **timeout** SNMP probe parameter.

    -   Type: integer
    -   Default value: 1500
-   **mid.snmp.session.timeout**

    Specifies the timeout value for subsequent OID request, in milliseconds. SNMP communication is stateless and does not have a session or connection in the normal sense. The system regards a positive response from the first OID request as a sign that it should expect prompt responses to subsequent requests. While the default is short, it may be useful to increase this parameter value to the same value as that used for **mid.snmp.request.timeout**.

    **Note:** You can override this parameter with the **establish\_session\_timeout** SNMP probe parameter.

    -   Type: integer
    -   Default value: 500
-   **mid.snmp.use\_getbulk**

    Specifies whether to use GETBULK to receive a large amount of data in batches. This can be used to configure an individual MID Server.

    -   Type: true \| false
    -   Default value: True
    GETBULK can also be set at the probe level or globally for all MID servers. Settings are listed in the order of precedence:

    -   [SNMP probe parameter](https://www.servicenow.com/docs/access?context=r_SNMPProbeParameters&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)
    -   MID Server configuration parameter
    -   [MID Server properties](r_MIDServerProperties.md#)
-   **mid.snmp.use\_snmp4j**

    Use the Snmp4j library for SNMP communication. This is a strict requirement for SNMPv3. This parameter should only be set to **false** based on advice from Customer Service and Support.

    -   Type: true \| false
    -   Default value: true
-   **mid.snmp.use\_snmp\_v1\_v2c**

    Attempt communication using the SNMPv1 and SNMPv2c protocol versions. It may require configuration of [SNMP community credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=xanadu&pubname=xanadu-platform-security&section=r_SNMPCommunityCredentialsForm&ft:locale=en-US). This parameter is an alternative and**not a strict requirement for SNMPv3.**

    -   Type: true \| false
    -   Default value: true
-   **mid.snmp.use\_snmp\_v3**

    Attempt communication using the SNMPv3 protocol version. Requires configuration of SNMPv3 credentials.

    -   Type: true \| false
    -   Default value: true

## SSH Discovery parameters

By default, the MID Server is configured to search for SSH commands in the following paths and the logged-on user's default paths:

-   /usr/sbin
-   /usr/bin
-   /bin
-   /sbin

-   **mid.connection\_cache**

    Specifies whether to cache connections. Set to **false** to disable connection caching. This parameter applies to SSH connections only.

    -   Type: true \| false
    -   Default value: true
-   **mid.ssh.set\_path**

    Specifies whether to set the PATH environment variable for SSH commands.

    -   Type: true \| false
    -   Default value: true
-   **mid.ssh.local**

    Specifies whether to execute commands for the MID Server host machine \(localhost\) via SSH rather than from a console. This allows long-running commands to execute properly. This parameter applies to the legacy SSH client only.

    -   Type: true \| false
    -   Default value: false
-   **mid.ssh\_connections\_per\_host**

    Controls the number of concurrent probes the MID Server can run against a given host. Lowering the number of concurrent connections can slow Discovery.

    -   Type: integer
    -   Default value:

        7 for the ServiceNow client

        3 for the legacy SSH client.

-   **mid.ssh.sudo\_preserve\_environment**

    Specifies whether to use sudo to preserve the environment for SSH.

    -   Type: true \| false
    -   Default value: false
-   **mid.ssh.terminal.width**

    Controls the maximum characters per line when handling sudo -l in the terminal. If the value is too low, the output can be broken into multiple lines and affect the parser. Set the value to a sufficient size to handle outputs as needed.

    -   Type: int
    -   Default value: 255
-   **mid.ssh.path\_override**

    Overrides the default paths set before executing a command. Enter one or more override paths delimited by a colon \(:\). The default path is /usr/sbin: /usr/bin: /bin: /sbin.

    -   Type: string \(a colon-separated list of directories\)
    -   Default value: None
    The ServiceNow SSH client accepts the following prefixes in front of the path\_overide value.

    -   **append**: Appends the override path to the end of the host’s path. This is the default behavior.
    -   **replace**: Replaces the host path with the path\_overide value.
    -   **prepend**: Appends the override path to the front of the host path.
-   **mid.ssh.use\_snc**

    Enables the ServiceNow SSH client \(SNCSSH\) on individual MID Servers. SNCSSH is a ServiceNow implementation of an SSH client and is active by default for all MID Servers on new instances, via a [MID Server property](r_MIDServerProperties.md#). Enabling the ServiceNow SSH client disables the legacy J2SSH client.

    **Important:** Mixing SSH client types for MID Servers connected to the same instance is not a good practice.

    -   Type: true \| false
    -   Default value: false
-   **mid.ssh.max\_retries**

    Specifies the maximum amount of times to retry an SSH operation after a time-out. The system sleeps two seconds between each connection attempt. By default, the MID Server retries once only. Set the parameter to 0 to disable retries.

    -   Type: integer
    -   Default value: 1
-   **mid.ssh.alt\_rm**

    Sets a different SSH remove file command.

    -   Type: string
    -   Default value: none
-   **mid.ssh.initial\_delay\_ms**

    Delays sending any SSH probe commands to a server after connecting to the target for the time specified, in milliseconds. This parameter applies to the legacy SSH client only.

    -   Type: integer \(milliseconds\)
    -   Default value: 0
-   **mid.ssh.suppress\_history**

    Suppresses the generation of the SSH history file. This parameter applies to the legacy SSH client only.

    -   Type: true \| false
    -   Default value: false
-   **mid.ssh.socket\_timeout**

    Specifies the timeout value for the SSH socket to prevent issues created by a socket timeout. Some devices, such as systems with embedded controllers like UPSs and PDUs, that have SSH enabled require more time to respond to an authentication request. The default value of 2 minutes ensures such requests do not timeout prematurely.

    -   Type: integer \(milliseconds\)
    -   Default value: 120000 \(2 minutes\)
-   **mid.ssh.channel\_timeout**

    Specifies the amount of time that the MID Server waits for activity on the SSH socket before closing the connection. If there has been no activity on the SSH socket for the specified timeout value, the MID Server closes the connection. Some devices, such as systems with embedded controllers like UPSs and PDUs, that have SSH enabled may require more time to respond to an authentication request.

    -   Type: integer \(milliseconds\)
    -   Default value: 120000 \(2 minutes\)
-   **mid.ssh.session\_timeout**

    Specifies the amount of time that a cached session remains in memory after last use. Excessively small values tend to decrease performance. This parameter applies to the ServiceNow SSH client only.

    -   Type: integer \(milliseconds\)
    -   Default value: 300000 \(5 minutes\)
-   **mid.ssh.command\_timeout\_ms**

    The timeout duration, in milliseconds, for the execution of an SSH command.

    -   Type: integer \(milliseconds\)
    -   Default value: 300000 \(5 minutes\)
-   **mid.ssh.use\_keyboard\_interactive**

    Uses the keyboard interactive authentication mode in SSH daemons on which it is activated.

    -   Type: true \| false
    -   Default value: false
    **Warning:** An issue exists in Mac OS X Sierra and later with the authentication order of the **password** and **keyboard-interactive**modes that can cause Discovery to fail. For details about this issue and the configuration required for proper SSH authentication, see [KB0623600](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsys_kb_id%3D66feae3edbf33a805a4af85e0f9619ea%26sysparm_stack%3D%26sysparm_view%3D).

-   **mid.ssh.dh\_group\_length\_min**

    Specifies the minimum group length in bits used for generating a "shared secret" key in Diffie-Hillman key exchange. The larger the key the more secure the SSH connection is but at the cost of performance.

    -   Type: integer \(bits\)
    -   Default value: 1024
-   **mid.ssh.dh\_group\_length\_max**

    Specifies the maximum group length in bits used for generating a "shared secret" key in Diffie-Hillman key exchange. The larger the key the more secure the SSH connection is but at the cost of performance.

    -   Type: integer \(bits\)
    -   Default value: 8192
-   **mid.ssh.shells\_supported**

    Defines the bourne-compatible shells supported by the MID Server. This value is a comma-separated list of supported shells, such as **ksh**, **dsh**, **bash** and **sh**.

    -   Type: string
    -   Default value: ksh,bash,sh
-   **mid.ssh.discard\_lrc\_error**

    Discard long running command error output, emulating legacy behavior.

    -   Type: string
    -   Default value: j2ssh - true, sncssh - false
-   **mid.ssh.pool\_thread\_ratio**

    Ratio of the SSH session pool capacity to the configured MID Server thread number \(threads.max\), expressed as a percentage. The number of permitted pool capacity sessions is set in this parameter. Regardless of the value set in this parameter, the system never permits the pool capacity to fall below 25 sessions.

    -   Type: integer
    -   Default value: 150
-   **mid.ssh.disable\_privilege\_check**

    This parameter has no effect if the target is using a privileged command other than sudo. For more information, see [MID Server privileged commands](../concept/c_PrivilegedCommandsForMIDServer.md#).

    The remainder of this section only applies to targets which run sudo. When this parameter is set to **true**, the MID Server assumes that the user configured in the credential has the privilege to run the given command using sudo. The MID Server assumes the target user can run any command string following sudo on the target. When this parameter is set to **false**, the MID Server runs "sudo -l" on the target to verify the command which follows sudo has permission to run on the target. Regardless of this parameter's value, the MID Server always validates that sudo by itself can be run on the target.

    Some releases do not show this parameter in the MID Configuration Parameters pull down list. In this case, you may optionally add this parameter in MID Properties.

    -   Type: true \| false
    -   Default value: false

## Upgrade parameters

-   **mid.pinned.version**

    Name of the version to which this MID Server is pinned.

    -   Type: string
    -   Default value: MID buildstamp

        **Note:** To see the MID buildstamp for your instance, type **stats.do** in the navigation filter. An example of the buildstamp format is **london-06-27-2018\_\_patch3-10-24-2018\_11-11-2018\_0542**.

-   **mid.upgrade.use\_proxy**

    If your MID Server must go through a web proxy to access the upgrade URL, set this parameter to **true** to instruct the MID Server to use the proxy. You must also set the proxy server's host and port. If the instance proxy user name and password are set, they are used for the upgrade proxy as well.

    **Note:** This parameter is not intended to control proxy details configured with **glide.mid.autoupgrade.proxy\*** parameters.

    -   Type: true \| false
    -   Default value: true
-   **glide.mid.autoupgrade.proxy\_host or glide.glidesoap.proxy\_host**

    If your MID Server must go through a web proxy to access the upgrade URL, define the proxy's host here.

    -   Type: string \(URL\)
    -   Default value: none
-   **glide.mid.autoupgrade.proxy\_port or glide.glidesoap.proxy\_port**

    If your MID Server must go through a web proxy to access the upgrade URL, define the proxy's port here.

    -   Type: integer \(0-65535\)
    -   Default value: 80
-   **glide.mid.autoupgrade.proxy\_user**

    If your MID Server must go through a web proxy to access the upgrade URL, define the proxy's user name here.

    -   Type: string \(URL\)
    -   Default value: none
-   **glide.mid.autoupgrade.proxy\_password**

    If your MID Server must go through a web proxy to access the upgrade URL, define the proxy's password here.

    -   Type: string
    -   Default value: none

## Windows Discovery parameters

-   **mid.powershell\_api.session\_pool.max\_size**

    Specifies the maximum number of sessions allowed in the session pool.

    **Note:** Setting or changing this parameter requires restarting the MID Server.

    -   Type: integer
    -   Default value: 25
-   **mid.powershell\_api.session\_pool.target.max\_size**

    Specifies the maximum number of sessions allowed in the pool per target host.

    **Note:** Setting or changing this parameter requires restarting the MID Server.

    -   Type: integer
    -   Default value: 2
-   **mid.sa.prefer\_powershell**

    Enables MID Server to use PowerShell Remoting.

    -   Type: true \| false
    -   Default value: false
-   **mid.powershell\_api.winrm.use\_ssl**

    Requires the use of SSL certificates for HTTPS connections using WinRM.

    -   Type: true \| false
    -   Default value: false
-   **mid.powershell\_api.winrm.additional\_pssesion\_options**

    Controls advanced options for a PSSession. For more information about advanced PSSession options, see [https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/new-pssessionoption?view=powershell-6](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/new-pssessionoption?view=powershell-6).

-   **mid.powershell\_api.winrm.remote\_https\_port**

    Configures the port for connecting to Windows servers using PowerShell over HTTPS.

    -   Type: integer
    -   Default value: 5986
-   **mid.powershell\_api.winrm.remote\_port**

    Configures the port for connecting to Windows servers using PowerShell over HTTP.

    -   Type: integer
    -   Default value: 5985
-   **mid.powershell\_api.winrm.skip\_ssl\_cert\_check**

    Skips the SSL certificate check when using WinRM for HTTPS connections.

    -   Type: true \| false
    -   Default value: false
-   **mid.powershell\_api.winrm.skip\_ssl\_cert\_check\_options**

    Skips specific SSL certificate checks when using WinRM for HTTPS connections. Configure the MID Server to skip checks for certificates from a Certification Authority \(CA\), from the Common Name \(CN\) that identifies the host associated with the certificate, and for revoked certificates.

    -   Type: string
    -   Default value: -SkipCACheck -SkipCNCheck -SkipRevocationCheck
-   **mid.powershell.use\_credentials**

    Determines the credentials to use for Discovery with PowerShell. A setting of **true** directs the MID Server to run probes with the Windows credentials from the credentials table. To run probes with the credentials of the user for the MID Server service, set this parameter to **false**.

    -   Type: true \| false
    -   Default value: true
-   **mid.powershell.path**

    Enables an administrator to point to a specific PowerShell on a MID Server in cases where more than one PowerShell is installed. Supply the path to the folder containing the PowerShell executable, for example, `C:\mypowershell` or `C:\mypowershell\`. ServiceNow automatically appends the string powershell.exe to the path. Configure this parameter when both a 32-bit and 64-bit PowerShells are active on the same MID Server, and it becomes necessary to launch the correct PowerShell for the context. 64-bit Windows employs file system redirection and the MID Server runs as a 32-bit application. If trying to specify a path in %WinDir%\\System32, Windows automatically redirects to %WinDir%\\SysWOW64. To avoid redirection, specify the path as %WinDir%\\Sysnative. For example, instead of C:\\WINDOWS\\system32\\WindowsPowerShell\\v1.0\\, specify C:\\WINDOWS\\sysnative\\WindowsPowerShell\\v1.0\\.

    **Note:** On a 64-bit version of Windows XP, a Microsoft hotfix may be required to enable this.

    To discover applications running on a 64-bit Windows machine, the MID Server must be running on a 64-bit Windows host machine.

    -   Type: string \(path\)
    -   Default value: none
-   **mid.powershell.enforce\_utf8**

    Enable this parameter to force commands on a target Windows system to return UTF-8 encoded output. Disabling it allows the target system to use its default encoding. This parameter is only valid when PowerShell is enabled.

    Setting this value to **false** may result in incorrect values in the CMDB when non-ASCII characters are returned by a probe.

    -   Type: true \| false
    -   Default value: true
-   **mid.powershell.local\_mid\_service\_credential\_fallback**

    Enables automatically falling back to MID Server service credentials if all other credentials fail.

    -   Type: true \| false
    -   Default value: true
-   **mid.powershell\_api.idle\_session\_timeout**

    Specifies the timeout value of idle PowerShell sessions in seconds.

    **Note:** Setting or changing this parameter requires restarting the MID Server.

    -   Type: integer
    -   Default value: 60
-   **mid.powershell.command.parameter\_passing**

    Enable this parameter to allow passing PowerShell parameters from the command line.

    -   Type: true \| false
    -   Default value: false
-   **mid.powershell.command.script.parameter\_passing**

    Enable this parameter to allow passing PowerShell scripts from the command line.

    -   Type: true \| false
    -   Default value: true
-   **mid.windows.management\_protocol**

    Enables administrators to select the Windows management protocol used for device and process classification. Options include: WMI and WinRM.

    -   Type: string
    -   Default value: WMI
-   **mid.windows.probe\_timeout**

    Sets the timeout interval for all Windows probes on a specific MID Server. This value is overridden by the values configured for individual probes with the wmi\_timeout probe parameter.

    -   Type: integer
    -   Default value: 300
-   **mid.powershell.jea.append\_username**

    Specifies whether user name of the current user will be appended to the JEA endpoint.

    -   Type: true \| false
    -   Default value: False
-   **mid.powershell.jea.endpoint**

    JEA configuration name \(endpoint\) on remote servers that the MID Server will connect to. Set to JEA\_DISCO\_BASIC.

    -   Type: string
    -   Default value: ""

**Parent Topic:**[MID Server reference](../concept/mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements](r_MIDServerSystemRequirements.md)

[MID Server upgrades](../concept/c_UpgradeAndTestMIDServer.md)

[Resolving MID Server issues](r_MIDServerTroubleshooting.md)

[MID Server dashboard](../concept/c_MIDServerDashboard.md)

[MID Server properties](r_MIDServerProperties.md#)

[MID Server Configuration Parameter settings and priority](mid-config-param-priority.md)

[MID Server File Cleaner](../concept/mid_file_cleaner.md)

[MID Server protected records and reserved characters](mid-server-reserved-characters.md)

[MID Server privileged commands](../concept/c_PrivilegedCommandsForMIDServer.md#)

[MIDSystem methods](r_MIDSystemMethods.md)

[Manually start, stop, and restart a MID Server](../task/t_InstallMIDServerAsWinService.md)

[MID Server heartbeat](r_MIDServerHeartbeat.md)

[Set the MID Server JVM memory size](../task/t_MIDServerOptionalConfiguration.md)

[Pause the MID Server](../task/t_PauseTheMIDServer.md#)

## Add a MID Server parameter

Use a MID Server parameter to control the behavior of a particular MID Server.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Servers**.

2.  From the list of MID Servers, select a MID Server to configure.

3.  Select the **Configuration Parameters** related list.

    This shows all the parameters currently in the MID Server's configuration file. If there are any passwords, they are displayed in asterisks for security reasons. See [MID Server parameters](mid-server-parameters.md#) for a list of available parameters.

    ![Defining MID Server configuration parameters](../image/MIDConfig.png "Defining MID Server configuration parameters")

4.  To add parameters, click **New**, and then complete the form.

    After the form is submitted, the configuration file for that MID Server is modified to include the new parameter. Changes to existing parameters are reflected in the MID Server configuration file as well. Changes made to the MID Server configuration file do not take place immediately, but rather the next time the MID Server is restarted. The MID Server form has a related link for restarting the MID Server.

    **Note:** ServiceNow prevents you from saving changes, such as modifying or deleting parameters, that would cause the MID Server to lose communications with the instance. For example, you cannot change the url parameter. Any changes to these protected parameters must be made directly in the `config.xml` file for that MID Server.

5.  Set parameters in the `config.xml` file.

    MID Server configuration is controlled by an XML file called `config.xml`. This file is located in the `/agent` directory, in the MID Server isntallation directory. You can edit this file directly to make any configuration changes to protected parameters. Many configuration changes, such as those that do not disrupt communication between the MID Server and the ServiceNow instance, may also be made from the instance.

    The structure of the `config.xml` file is simply an outer parameters tag and a series of inner parameter tags. Each parameter tag has name and `value` attributes.

    -   To change the value of a parameter, edit the value attribute.
    -   To add a parameter, add another parameter tag with its name and value.
    -   To delete a parameter, delete the entire parameter tag.
    The order of the parameters within the file is not important. Notice the green comment sections in the sample. Use these elements to add useful comments to the configuration file.

    **Note:** When configuring the MID Server for use with a proxy server, be sure to remove the comment tags around the proxy sections that you configure.

    ![MID Server config.xml file](../image/MIDConfigXml.png "MID Server config.xml file")

    **Note:** The sample file here is from a Firefox browser. Conventional text editors, such as Notepad, WordPad, or TextEdit, do not display colors and variable fonts.


