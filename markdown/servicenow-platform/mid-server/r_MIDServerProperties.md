---
title: MID Server properties
description: Properties control the behavior of all MID Servers or a particular MID Server.Use a MID Server property to control either the behavior of all MID Servers or a particular MID Server.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 22
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server properties

Properties control the behavior of all MID Servers or a particular MID Server.

<table id="table_gwj_2sf_khb"><tbody><tr><td>

![Links to each of the MID Server sections](../image/MIDRefIconBar.png)

</td></tr></tbody>
</table>The MID Server properties are in the MID Server Property \[ecc\_agent\_property\] table and can be accessed by navigating to **MID Server** &gt; **Properties**. To set these properties, you must add them, if they are not already present.

## MID Server properties

-   **com.glide.closure\_max\_rows\_per\_table**

    Sets the maximum number of rows allowed in a table. This property is not visible by default and must be added.

    -   Type: integer
    -   Default value: 200000
-   **concurrent.dist.download**

    Sets the number of concurrent MID Server auto-upgrades permitted by the instance. The default value of this property is 2, which allows the MID Server to use 2 of the 4 semaphores available on the instance for upgrading. If your instance has more than 4 INT semaphores, you can increase the value in this property to allow more concurrent upgrades.

    -   Type: integer
    -   Default value: 2
-   **glide.stored\_proc.data\_type.validation**

    Stops validation of data types in stored procedure parameters. Use this property if you use Orchestration to run a stored procedure on MySQL, Oracle DB, and MS-SQL databases and you want to avoid performing data type validation. Restart the MID Server service after you change the value of this property.

    -   Type: true \| false
    -   Default value: false
-   **mid.discovery.max\_ci\_count\_per\_page**

    Defines the maximum CI count per page.

    -   Type: integer \(bytes\)
    -   Default value: 500
    You can also configure this as a [configuration parameter on a individual MID Server](mid-server-parameters.md#).

-   **mid.discovery.max\_related\_count\_per\_page**
    -   Type: integer
    -   Default: 100
-   **mid.discovery.max\_relation\_count\_per\_page**

    Splits the payload based on the number of relations in it.

    -   Type: integer
    -   Default: 10000
-   **mid.discovery.max\_total\_items\_size\_per\_page**

    Splits the payload based on the size of the items.

    -   Type: integer
    -   Default:
-   **mid.aws.sts.assume\_role.disable\_credential\_caching**

    Set this property to **true** to prevent the caching of temporary credentials for Cloud Discovery. For more information, see Access setup for AWS service accounts Access setup for AWS service accounts.

    -   Type: true \| false
    -   Default: false
-   **mid.aws.sts.assume\_role.credential\_ttl\_minutes**

    Set the number of minutes you want to cache temporary credentials for Cloud Discovery. For more information, see Access setup for AWS service accounts Access setup for AWS service accounts.

    -   Type: integer
    -   Default: 60
-   **mid.ca.certificate.api.request.retry.count**

    Indicates how many times the Certificate Import query will retry after the rate limit has occurred.

    -   Type: integer
    -   Default: 3
-   **mid.ca.certificate.api.request.retry.interval**

    Used to delay Certificate import from CAs when the rate limit has occurred.

    -   Type: integer
    -   Default: 30000
-   **mid.cloud.discovery.bypass.proxy**

    This configuration parameter accepts a comma separated list of DNS/IP addresses of proxy servers. The listed proxy servers are bypassed during Cloud Discovery. To bypass proxies on multiple cloud service providers \(such as AWS or Azure\), a separate MID Server must be set up for each provider. Otherwise, the MID Server proxy configuration is followed normally.

    -   Type: string
    -   Default value: none
-   **mid.discovery.file\_transfer\_protocol**

    Used to determine the file transfer method used for probes or patterns.

    -   Type: Choice \(SCP or SFTP\)
    -   Default: SCP
-   **mid.discovery.max\_pattern\_payload\_size**

    Defines the maximum overall payload size for the payload of results that come from patterns.

    -   Type: integer \(bytes\)
    -   Default value: 50000000
    You can also configure this as a [configuration parameter on a individual MID Server](mid-server-parameters.md#).

-   **mid.discovery.max\_payload\_size**

    Specifies the maximum string length of Discovery results that the MID Server sends to the instance. If the Discovery probe results exceed the limit, the MID Server discards them and returns a warning message.

    For probes, this applies only to those probes where the Used by Discovery field is true. For patterns, this applies to the Horizontal Pattern probe.

    Set the value to any negative number to disable the payload limit and allow payloads of any size to be sent to the instance. For example, -1.

    -   Type: integer \(bytes\)
    -   Default value: 5000000
    You can also configure this as a [configuration parameter on a individual MID Server](mid-server-parameters.md#).

-   **mid.discovery.multiprobe.skip\_others\_on\_error**

    Prevents probes in a multi-probe from iterating through available credentials when another member probe has already failed or timed out. If this property is set to **false**, each probe in the multi-probe attempts to connect to the target with the same invalid credentials. This condition results in longer probe execution times on the MID Server.

    This property is not visible by default and must be added to the sys\_properties table to change the value.

    -   Type: true \| false
    -   Default value: true
-   **mid.discovery.aws\_ssm.kms\_key\_name**

    Using a dedicated key enhances security by verifying that applicative credentials are encrypted and securely retrieved at runtime, without being exposed in plain text. This step is optional and only necessary if you plan to use applicative credentials during discovery. To configure the MID Server to support secure credential handling during SSM Agent discovery, set the **mid.discovery.aws\_ssm.kms\_key\_name** property to the name of the AWS KMS key.

    -   Type: string
    -   Default value: none
-   **mid.discovery.aws\_ssm.kms\_key\_region**

    Using a dedicated key enhances security by verifying that applicative credentials are encrypted and securely retrieved at runtime, without being exposed in plain text. This step is optional and only necessary if you plan to use applicative credentials during discovery. To configure the MID Server to support secure credential handling during SSM Agent discovery, set the **mid.discovery.aws\_ssm.kms\_key\_region** property to the region where the key is located.

    -   Type: string
    -   Default value: none
-   **mid.discovery.aws\_ssm.s3\_bucket\_name**

    Because the SSM Run Command console has a 24,000-character limit, results that exceed this limit must be stored in and retrieved from an S3 bucket. For Put File commands, the S3 bucket also serves as a transfer point between the MID Server and the AWS environment, enabling file delivery to target devices via SSM. To configure the MID Server to support these S3-based operations, set the **mid.discovery.aws\_ssm.s3\_bucket\_name** property to the name of the S3 bucket used for SSM Agent discovery.

    -   Type: string
    -   Default value: none
-   **mid.discovery.aws\_ssm.s3\_bucket\_region**

    Because the SSM Run Command console has a 24,000-character limit, results that exceed this limit must be stored in and retrieved from an S3 bucket. For Put File commands, the S3 bucket also serves as a transfer point between the MID Server and the AWS environment, enabling file delivery to target devices via SSM. To configure the MID Server to support these S3-based operations, set the bucket’s region in the **mid.discovery.aws\_ssm.s3\_bucket\_region** property.

    -   Type: string
    -   Default value: none
-   **mid.discovery.aws\_ssm.linux.fallback\_root\_user**

    When the **glide.discovery.enable\_ssm** property is enabled, AWS SSM Discovery on Linux defaults to using the root user for command execution. If you prefer not to configure alternate user credentials on your EC2 instances, you must enable the **mid.discovery.aws\_ssm.linux.fallback\_root\_user** property to allow fallback to root execution. When enabled, it automatically creates a record in the AWS SSM Instance Users \[aws\_ssm\_instance\_user\_credentials\] table with the user name root. However, if you leave this property set to false, you must configure non-root credentials to run Discovery commands.

    -   Type: true \| false
    -   Default value: false
-   **mid.eccq.max\_payload\_size**

    Specifies the maximum string length of a payload that the MID Server sends to the instance. The MID Server verifies the size of the payload before sending it to the instance. If the payload size exceeds the limit, the MID Server discards it and returns an error message in the payload.

    -   Type: integer \(bytes\)
    -   Default value: 20000000
    You can also configure this as a [configuration parameter on a individual MID Server](mid-server-parameters.md#).

-   **mid.http\_classy.allow\_credentials\_over\_http**

    Enables the HTTP Classify probe to send credentials over the HTTP protocol during discovery.

    -   Type: true \| false
    -   Default value: false
    **Warning:** Enabling this setting can expose credentials to security risks, such as man-in-the-middle \(MitM\) attacks. Therefore, it’s strongly recommended to keep this property set to **false** and use HTTPS whenever possible.

-   **mid.install\_server.base\_uri**

    Modifying this system property requires maint privileges. The MID Server uses the value provided as the base URL when making requests for update files.

    -   Type: string
    -   Default value: https://install.service-now.com
-   **mid.jdbc.datastream.max.record.size**

    Specifies the maximum record size in KB.

    -   Type: integer
    -   Default value: 64
    -   Maximum value: 128
-   **mid.jdbc.datastream.fail.when.attachement.limit.exceeded**

    Specifies if the data up to 4GB \(four attachments, each of size 1GB\) can be retrieved from the RDBMS. By default, a flow or action fails with an error, when there is data of more than 4GB to be retrieved. Set value to `false` to retrieve data of size 4GB without an error.

    -   Type: string
    -   Default: true
-   **mid.keystore.max\_backups**

    Specifies the maximum number of backups from manual key store operations through the **manage\_certificate** script. If it is 0 or negative, no backup will be made.

    -   Type: Integer
    -   Default value: 3
-   **mid.keystore.max\_live\_backups**

    Specifies the maximum number of live backups from running MID server. If it is 0 or negative, no backup will be made.

    -   Type: Integer
    -   Default value: 2
-   **mid.keystore.backup\_overwrite\_timespan**

    Specifies the number of seconds from the current backup time to determine if a the most recent backup in that time span should be replaced by the new one instead of creating a new backup and so removing the oldest backup, should the number of backups exceed the maximum limit.

    -   Type: Integer
    -   Default value: 60
-   **mid.log.command\_audit.enable**

    Enables the MID Server command audit log.

    -   Type: string
    -   Default value: false
-   **mid.powershell.target\_base\_dir**

    Specifies the location of the target base folder used for Discovery using WMI. If another network share is mounted on each Window's target, the folder may be changed by updating this property.

    -   Type: string
    -   Default value: admin$\\temp
-   **mid.probe.collect\_debug\_info**

    An optional property to collect debug information. If this property is set to true, the probe collects credential debug information when it runs and puts that information in the payload of ECC input message. It doesn't affect how Discovery works.

    -   Type: true \| false
    -   Default value: false
-   **mid.probe.use\_legacy\_forward\_dns**

    Enables the legacy DNSNameResolver probe and disables the default DNSNameResolver probe. See Probes used by Orchestration for more information.

    -   Type: true \| false
    -   Default value: false
-   **mid.probe.use\_legacy\_reverse\_dns**

    Enables the legacy DNS probe and disables the default DNS probe. If you experience problems with the features of the default DNS probe, use this property to disable those features. The default DNS probe's features include being lightweight and faster due to executing in parallel, while the legacy probe is throttled by the MID Server because it executes in serial. The default probe utilizes DNS lookup by the MID Server host OS to make use of the OS maintained DNS cache, while the legacy probe does not. Consequently, after a DNS lookup by the default probe fails in Windows systems, the OS also tries looking up by NETBIOS name.

    -   Type: true \| false
    -   Default value: false
-   **mid.process\_flow.log\_listener.max\_size**

    Sets the maximum size in bytes of memory available to save log messages for Workflow Studio actions running on a MID Server. The MID Server stores up to the limit in memory and discards additional log messages, then sends the messages back to the instance along with the execution plan.

    -   Type: integer \(bytes\)
    -   Default value: 10485760
-   **mid.property.jdbc\_operations**

    Tells the JDBCOrchestrationProbe what JDBC operations it is allowed to execute. Edit this property value to allow JDBC Orchestration activities to perform more operations. All operations are comma separated. Select a MID Server in the **MID server** field to define specific operations for that MID Server, or leave the field empty to apply the list of operations to all MID Servers. This property requires the Orchestration plugin.

    -   Type: string
    -   Default value: select,update,insert,delete,show,create,describe,begin,if,end,not,exists
-   **mid.property.jms.command.allowed\_factory\_names**

    Comma delimited list of Java Messaging Service \(JMS\) connection factories that the MID Server requires for a custom JMS activity or action. This property requires the Orchestration plugin.

    -   Type: string
    -   Default value: connectionFactory, queueConnectionFactory, topicConnectionFactory
-   **mid.property.ssh.use\_snc**

    Enables the use of the SNCSSH client for Discovery and Orchestration. Change this property to **false** to use J2SSH. This property applies to all MID Servers connected to the instance.

    -   Type: true \| false
    -   Default value: true
-   **mid.property.powershell.use\_base64\_password**

    If the Credential is set to be specific to certain MID Servers, then the property can also be set to those same MID Servers. Leaving the MID Servers field empty will apply to all MID Servers.

    -   Type: true \| false
    -   Default value: false
-   **mid.sa.prefer\_powershell**

    Enables MID Server to use PowerShell Remoting.

    **Note:** It is not recommended to change this property as it is being deprecated.

    -   Type: True \| False
    -   Default value: true
-   **mid.sa.ssh.use\_sncssh**

    Toggles SSH between non-interactive and interactive modes. True corresponds to non-interactive mode and allows probes to open sessions with the device without waiting for a prompt. False corresponds to interactive mode, which requires interactive sessions with the device for network devices and servers.

    -   Type: True \| False
    -   Default value: true
-   **mid.sa.windows.allowable\_failures**

    Specifies the number of allowable failures before the MID Server stops executing the pattern. Once the limit is reached, the next failure will terminate the pattern. A failure occurs when a PowerShell command can't complete successfully due to issues such as authentication failure, command timeout, or command execution exceptions.

    -   Type: integer
    -   Default value: 2
    -   Values:
        -   0: The first failure will terminate the pattern immediately.
        -   1: The first failure is tolerated; the second failure will terminate the pattern.
        -   2: Two failures are tolerated; the third failure will terminate the pattern.
        -   -1: no maximum limit on failures; the pattern continues regardless of the number of failures.
-   **mid.servicewatch.max\_concurrent\_connections**

    Defines the maximum number of concurrent tasks sent to an individual host by a single MID Server.

    -   Type: integer
    -   Default value: 7
-   **mid.shazzam.regulator.interval\_ms**

    Sets the interval, in milliseconds, in which Shazzam can launch packets.

    -   Type: integer
    -   Default value: 1
-   **mid.shazzam.regulator.packets\_per\_interval**

    Sets the number of packets that Shazzam can launch in the time interval specified by the mid.shazzam.regulator.interval\_ms property.

    -   Type: integer
    -   Default value: 1
-   **mid.shazzam.threads**

    Specifies the number of concurrent threads that Shazzam uses. Setting this or the mid.shazzam.max\_scanners\_per\_thread parameter to 0 disables Shazzam multi-thread optimization.

    -   Type: Integer
    -   Default value: 5
-   **mid.shazzam.max\_scanners\_per\_thread**

    Specifies the number of concurrent scanners processed by each Shazzam thread. Setting this or the mid.shazzam.threads parameter to 0 disables Shazzam optimization.

    -   Type: Integer
    -   Default value: 100
-   **mid.sm.discolog.max\_log\_size**

    Limits the length of the log statements in the Horizontal Discovery Log. If the results are truncated, the **Command results** reports, "Result is larger than \[value\] characters and was truncated by the logger."

    -   Type: integer \(characters\)
    -   Default value: 1000
-   **mid.sm.discolog.max\_object\_size**

    Limits the length of the object in the Horizontal Discovery Log. Objects in the log statement are truncated to the number of characters set by this property's value. This property only affects the object character size in the Horizontal Discovery Log. The following message appears if an object is limited by this property "The max object size reached the maximum limit of \[value\]. To adjust this use the mid property mid.sm.discolog.max\_object\_size."

    -   Type: integer \(characters\)
    -   Default value: 5000
-   **mid.snmp.use\_getbulk**

    Specifies whether to use GETBULK to receive a large amount of data in batches. This can be used to globally configure all MID servers.

    -   Type: true \| false
    -   Default value: true
    GETBULK can also be set at the probe level or for an individual MID Server. Settings are listed in the order of precedence:

    -   SNMP probe parameter
    -   [MID Server configuration parameter](mid-server-parameters.md#)
    -   MID Server properties
-   **mid.ssh.algorithms.kex**

    Modifies the Key Exchange SSH algorithm priority list. The property accepts a comma separated lists with operators. The first name in the list is highest priority, last name in list is lowest priority. Adding a comma separated list without any operators replaces the default algorithm list. For more information, see [MID Server SSH cryptographic algorithms](mid-ssh-algorithms.md).

    -   Type: string
    -   Default value: ecdh-sha2-nistp256,ecdh-sha2-nistp384,ecdh-sha2-nistp521,diffie-hellman-group-exchange-sha256,diffie-hellman-group14-sha256,diffie-hellman-group16-sha512,diffie-hellman-group14-sha1,diffie-hellman-group1-sha1,diffie-hellman-group-exchange-sha1
-   **mid.ssh.algorithms.host\_key​**

    Modifies the Host Key SSH algorithm priority list. The properties accept comma separated lists with operators. The first name in the list is highest priority, last name in list is lowest priority. Adding a comma separated list without any operators replaces the default algorithm list. For more information, see [MID Server SSH cryptographic algorithms](mid-ssh-algorithms.md).

    -   Type: string
    -   Default value: ecdsa-sha2-nistp256,ecdsa-sha2-nistp384,ecdsa-sha2-nistp521,rsa-sha2-256,rsa-sha2-512,ssh-rsa,ssh-dss
-   **mid.ssh.algorithms.cipher**

    Modifies the Cipher SSH algorithm priority list. The properties accept comma separated lists with operators. The first name in the list is highest priority, last name in list is lowest priority. Adding a comma separated list without any operators replaces the default algorithm list. For more information, see [MID Server SSH cryptographic algorithms](mid-ssh-algorithms.md).

    -   Type: string
    -   Default value: aes128-ctr,aes192-ctr,aes256-ctr,3des-ctr,aes128-cbc,aes192-cbc,aes256-cbc,3des-cbc
-   **mid.ssh.algorithms.mac**

    Modifies the MAC SSH algorithm priority list. The properties accept comma separated lists with operators. The first name in the list is highest priority, last name in list is lowest priority. Adding a comma separated list without any operators replaces the default algorithm list. For more information, see [MID Server SSH cryptographic algorithms](mid-ssh-algorithms.md).

    -   Type: string
    -   Default value: hmac-sha2-256,hmac-sha1,hmac-sha2-512,hmac-sha1-96,mac-md5-96,hmac-md5
-   **shazzam.chunk\_size**

    Maximum number of IP addresses Shazzam can scan in parallel. This property primarily controls outbound port consumption.

    -   Type: integer
    -   Default value: 100
-   **mid.use\_net\_tools**

    Enables or disables the use of net-tools commands during discovery of devices running on the Linux operating system. Starting from Quebec, ITOM Visibility supports the iproute2 commands for discovery. By default, ITOM Visibility and discovery patterns first use net-tools commands, and only then, as a fallback, may use iproute2 commands. If all Linux-based devices and applications in your IT network use iproute2 commands, disable net-tools commands to make the discovery process more efficient.

    -   Type: true \| false
    -   Default value: true
-   **mid.servicewatch.use\_full\_linux\_netstat\_path**

    Controls if the **netstat** command is executed with its full installation path. This command lists open ports on Linux servers during the process detection phase of the top-down discovery.

    -   Type: true \| false
    -   Default value: true
-   **mid.servicewatch.num\_paths\_linux\_netstat\_to\_check**

    Define the maximum number of installation paths to use during discovery of Linux servers. This property is relevant when you run the top-down discovery on Linux servers with several netstat installation paths, and the **mid.servicewatch.use\_full\_linux\_netstat\_path** property is set to true.

    The top-down discovery attempts to execute the **netstat** command using each of these installation paths. The result of the first successful execution is used to determine the list of open ports.

    -   Type: true \| integer
    -   Default value: 5
-   **mid.servicewatch.use\_full\_linux\_ss\_path**

    Controls if the **ss** command is executed with its full installation path. This command lists open ports on Linux servers during the process detection phase of the top-down discovery.

    -   Type: true \| false
    -   Default value: false
-   **mid.servicewatch.num\_paths\_linux\_ss\_to\_check**

    Define the maximum number of installation paths to use during discovery of Linux servers. This property is relevant when you run the top-down discovery on Linux servers with several ss installation paths, and the **mid.servicewatch.use\_full\_linux\_netstat\_path** property is set to true.

    The top-down discovery attempts to execute the **ss** command using each of these installation paths. The result of the first successful execution is used to determine the list of open ports.

    -   Type: true \| integer
    -   Default value: 5

**Parent Topic:**[MID Server reference](../concept/mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements](r_MIDServerSystemRequirements.md)

[MID Server upgrades](../concept/c_UpgradeAndTestMIDServer.md)

[Resolving MID Server issues](r_MIDServerTroubleshooting.md)

[MID Server dashboard](../concept/c_MIDServerDashboard.md)

[MID Server parameters](mid-server-parameters.md#)

[MID Server Configuration Parameter settings and priority](mid-config-param-priority.md)

[MID Server File Cleaner](../concept/mid_file_cleaner.md)

[MID Server protected records and reserved characters](mid-server-reserved-characters.md)

[MID Server privileged commands](../concept/c_PrivilegedCommandsForMIDServer.md#)

[MIDSystem methods](r_MIDSystemMethods.md)

[Manually start, stop, and restart a MID Server](../task/t_InstallMIDServerAsWinService.md)

[MID Server heartbeat](r_MIDServerHeartbeat.md)

[Set the MID Server JVM memory size](../task/t_MIDServerOptionalConfiguration.md)

[Pause the MID Server](../task/t_PauseTheMIDServer.md#)

## Create a MID Server property

Use a MID Server property to control either the behavior of all MID Servers or a particular MID Server.

### Before you begin

Role required: admin

### About this task

You set MID Server properties to override MID Server parameters. Configure MID Server properties in the MID Server plugin. Do not configure MID Server properties in the **glide.properties** file that is located in the properties folder of the agent. The **glide.properties** file gets overwritten during the upgrade process.

### Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  Click **New**.

3.  Fill in the fields, as appropriate \(see table\).

<table id="table_ngk_tld_xp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the property name.

</td></tr><tr><td>

Value

</td><td>

You can enter the value you want the property to have. **Note:** If you are amending JDBC operations through the mid.property.jdbc\_operations properties, you can enter verbs like BEGIN, END, IF, or common PL/SQL block statements. This will assist in being able to run CREATE or ALTER statements. You might have to restart the MID server before running some of the statements.

</td></tr><tr><td>

MID Server

</td><td>

Leave this field blank to set a MID Server property that affects all MID Servers. To set a MID Server property for a particular MID Server , select the MID Server.

</td></tr></tbody>
</table>4.  After setting any MID Server properties, restart the MID Server to ensure the properties sync with the instance.


