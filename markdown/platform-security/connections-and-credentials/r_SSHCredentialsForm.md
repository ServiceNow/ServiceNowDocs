---
title: SSH credentials
description: Discovery, Orchestration, and Integration Hub explore UNIX and Linux devices by using SSH credentials to execute commands over Secure Shell \(SSH\). SSH commands must run with root privileges, either with root credentials or through the use of sudo. SSH private key credentials provide additional security.
locale: en-US
release: zurich
product: Connections and Credentials
classification: connections-and-credentials
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Create and test your credentials, Get started with credentials, Connections and Credentials, Access Management]
---

# SSH credentials

Discovery, Orchestration, and Integration Hub explore UNIX and Linux devices by using SSH credentials to execute commands over Secure Shell \(SSH\). SSH commands must run with root privileges, either with root credentials or through the use of sudo. SSH private key credentials provide additional security.

## Granting root privileges

Before granting root privileges, review your security policy and options with your organization's security team.

Use either of these approaches to allow users to run SSH commands with root privileges:

-   Give other credentials for Discovery, Orchestration, or Integration Hub, but grant the user in those credentials the right to execute certain commands with root privileges, using [sudo](http://www.sudo.ws/sudo/sudo.html). This is a secure way to grant limited privileges. Discovery, Orchestration, or Integration Hub use sudo on any probe that has the `must_sudo`parameter set to **true** \(it defaults to **false**\). However, each system must be configured to allow sudo to work. This is done by editing the **/etc/sudoers** file using the **visudo** command.
-   Give **root** credentials. These are obviously the most powerful credentials, but may not be desirable from a security perspective. If Discovery, Orchestration, or Integration Hub have the root credentials to any UNIX or Linux system, no further configuration is required.

## Privileged commands

The platform provides default privileged commands for the MID Server to use and the ability to add additional commands to the system. For details about using sudo and other privileged commands, see [MID Server privileged commands](https://www.servicenow.com/docs/access?context=c_PrivilegedCommandsForMIDServer&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

## SSH private key credential type

**Note:** SSH private key credentials should be used in most cases. They provide better security than SSH password credentials, including against MitM \(man-in-the-middle\) attacks in which communications between two parties are intercepted.

<table id="table_ncs_m5x_gpb"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and descriptive name for this credential. For example, you might call it **SSH Atlanta**.

</td></tr><tr><td>

Active

</td><td>

Enable or disable these credentials for use.

</td></tr><tr><td>

User name

</td><td>

Enter a UNIX or Linux user name. Avoid leading or trailing spaces in user names. A warning appears if the platform detects leading or trailing spaces in the user name.

</td></tr><tr><td>

Password

</td><td>

Enter the UNIX or Linux password. For **SSH Private Key** type credentials, enter the sudo password if one is required for the user name.

</td></tr><tr><td>

SSH passphrase

</td><td>

Type a secure SSH passphrase. This field is available only for **SSH Private Key** credentials.

</td></tr><tr><td>

SSH private key

</td><td>

Enter a secure, RSA, DSA, ECDSA or ED25519 private key.The private key must be entered in the proper format to ensure it is correctly encrypted. The private key must start with the string `-----BEGIN`.

Here is an example of a correctly formatted RSA private key:

```
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAsEK65scPssPSobpDFMpR+Btv3MS4Q7NP8ERaStRZsh3IWz+x...
...7hrxV2dbSug60FahyupGWBGtPnXm5PaE2X5WPLuUj94ue48i1Fs
-----END RSA PRIVATE KEY-----
```

An example of a DSA key:

```
-----BEGIN DSA PRIVATE KEY-----
MIIEogIBAAKCAQEAsEK65scPssPSobpDFMpR+Btv3MS4Q7NP8ERaStRZsh3IWz+x...
...7hrxV2dbSug60FahyupGWBGtPnXm5PaE2X5WPLuUj94ue48i1Fs
-----END DSA PRIVATE KEY-----
```

An example of a ECDSA key:

```
-----BEGIN EC PRIVATE KEY-----
MIIEogIBAAKCAQEAsEK65scPssPSobpDFMpR+Btv3MS4Q7NP8ERaStRZsh3IWz+x...
...7hrxV2dbSug60FahyupGWBGtPnXm5PaE2X5WPLuUj94ue48i1Fs
-----END EC PRIVATE KEY-----
```

And an example of an ED25519 private key:

```
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACAlYlqhcdwx8VQzZ5XaIC5ltQpjRr3lIlq/aE66mufmiwAAAKDQUtxZ0FLc
WQAAAAtzc2gtZWQyNTUxOQAAACAlYlqhcdwx8VQzZ5XaIC5ltQpjRr3lIlq/aE66mufmiw
AAAECuvsTkFUPdpTh0kw23i8TYx19qsFOZ3TRgowkkHBh6wSViWqFx3DHxVDNnldogLmW1
CmNGveUiWr9oTrqa5+aLAAAAGmFiaGluYXYuc3V0YXJATVJFTUE3OTAzMkI3AQID
-----END OPENSSH PRIVATE KEY-----
```

**Note:** For an ED25519 private key, only the OpenSSH key format is supported, which is generated using OpenSSH SSH-keygen utility.

The ServiceNow AI Platform supports private keys in the PEM format generated by the OpenSSH ssh-keygen utility. To convert PPK keys that were generated by PuTTY:

 -   Open your private key in PuTTYGen.
-   Export it in OpenSSH format from the menu **Conversions** &gt; **Export OpenSSH key**.
-   Save the new OpenSSH key.

</td></tr><tr><td>

SSH Certificate

</td><td>

Enter an RSA or ED25519 based OpenSSH certificate. When the certificate is entered, a private key is used for certificate based authentication. This authentication is supported from OpenSSH 7.8 onwards.

</td></tr><tr><td>

Credential alias

</td><td>

-   Allow flow designers to use aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you do not need to update any actions that use the connection. For more information, see [Connections and Credentials](r-credentials.md).
-   Allow workflow creators to assign individual credentials to any activity in an Orchestration workflow or assign different credentials to each occurrence of the same activity type in an Orchestration workflow.

</td></tr><tr><td>

External credential store

</td><td>

Select this check box to use an external credential storage system. When you select this option the **User name** and **Password** fields are replaced with the **Credential ID** field. Currently, the only supported external storage system is CyberArk.

</td></tr><tr><td>

MID servers

</td><td>

Select one or more MID Servers from the list of available MID Servers. The credentials configured in this record are available to the MID Servers in this list. This field is available only when you select **Specific MID servers** from the **Applies to** field.

</td></tr><tr><td>

Applies to

</td><td>

Select whether to apply these credentials to **All MID servers** in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use these credentials in the **MID servers** field.

</td></tr><tr><td>

Order

</td><td>

The order \(sequence\) in which the platform tries this credential as it attempts to log onto devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), Discovery or Orchestration tries the credentials in a random order.

</td></tr></tbody>
</table>## SSH credential type

These fields are available in the SSH credentials form.

<table id="table_o5n_n5x_gpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique and descriptive name for this credential.

</td></tr><tr><td>

Active

</td><td>

Enable or disable these credentials for use.

</td></tr><tr><td>

User name

</td><td>

Enter the user name to create in the Credentials table. Avoid leading or trailing spaces in user names. A warning appears if the platform detects leading or trailing spaces in the user name. For CIM discovery, the user must have the admin role.

</td></tr><tr><td>

Password

</td><td>

Enter the password.

</td></tr><tr><td>

Credential ID

</td><td>

Enter the unique key configured for external credentials in the JAR file uploaded to the MID Server for an external credential system. The **Credential ID** field has a limit of 40 characters.This field is only visible when the **External credential store** check box is selected.

</td></tr><tr><td>

Credential alias

</td><td>

-   Allow flow designers to use aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you do not need to update any actions that use the connection. For more information, see [Connections and Credentials](r-credentials.md).
-   Allow workflow creators to assign individual credentials to any activity in an Orchestration workflow or assign different credentials to each occurrence of the same activity type in an Orchestration workflow. To use the credential for discovering CIs not belonging to this CI type using Service Mapping and Discovery patterns, enter the table name for the CI type to which the CI belongs, for example cmdb\_ci\_apache\_web\_server.

</td></tr><tr><td>

External credential store

</td><td>

Select this check box to use an external credential storage system. When you select this option the **User name** and **Password** fields are replaced with the **Credential ID** field. [External credential storage](../concept/c_ExternalCredentialStorage.md) is only available when the External Credential Storage plugin in activated. **Note:** Currently, the only supported external storage system is [CyberArk](../concept/c_CyberArkCredStorageIntegrate.md).

</td></tr><tr><td>

Applies to

</td><td>

Select whether to apply these credentials to **All MID servers** in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use these credentials in the **MID servers** field.

</td></tr><tr><td>

MID servers

</td><td>

Select one or more MID Servers from the list of available MID Servers. The credentials configured in this record are available to the MID Servers in this list. This field is available only when you select **Specific MID servers** from the **Applies to** field.

</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr></tbody>
</table>## Commands that require root privileges for Discovery, Orchestration, and Integration Hub

These examples assume that the user name is **Disco**. Substitute the actual user name and ensure that the paths for the commands match the paths on the system.

**Note:** Sudo commands do not work with private key credentials, because there is no password to supply to the sudo command. A solution is to add the NOPASSWD option to the sudo configuration. For example, you might enter: `disco ALL=(root) NOPASSWD:/usr/sbin/dmidecode,/usr/sbin/lsof,/sbin/ifconfig`.

<table id="table_a1w_sdw_ts"><thead><tr><th>

Command

</th><th>

Purpose

</th></tr></thead><tbody><tr><td colspan="2">

**HP-UX**

</td></tr><tr><td>

adb

</td><td>

Gathers CPU speed and memory.-   **/etc/sudoers line example**: Disco ALL=\(root\) /usr/bin/adb
-   **Used by**: Discovery

</td></tr><tr><td colspan="2">

**All Linux and UNIX versions**

</td></tr><tr><td>

chage

</td><td>

Changes the number of days between password changes and the date of the last password change.-   **/etc/sudoers line example**: Disco ALL=\(root\) /usr/bin/chage
-   **Used by**: Orchestration and Integration Hub

</td></tr><tr><td>

chpasswd

</td><td>

Changes user passwords.-   **/etc/sudoers line example**: Disco ALL=\(root\) /etc/chpasswd
-   **Used by**: Orchestration and Integration Hub

</td></tr><tr><td colspan="2">

**All Linux**

</td></tr><tr><td>

dmidecode

</td><td>

Gathers several pieces of information about the hardware, including the serial number embedded within the motherboard.-   **/etc/sudoers line example**: Disco ALL=\(root\) /sbin/dmidecode
-   **Used by**: Discovery

</td></tr><tr><td>

fdisk

</td><td>

Gathers the disks and size information on the system.-   **/etc/sudoers line example**: Disco ALL=\(root\) /usr/bin/fdisk -l
-   **Used by**: Discovery

</td></tr><tr><td>

multipath

</td><td>

Gathers device mappings for MPIO.-   **/etc/sudoers line example**: Disco ALL=\(root\) /usr/bin/multipath -ll
-   **Used by**: Discovery

</td></tr><tr><td>

ls

</td><td>

Gathers the contents of a directory.-   **/etc/sudoers line example**: Disco ALL=\(root\) /usr/bin/ls, /bin/ls
-   **Used by**: Discovery

</td></tr><tr><td colspan="2">

**Linux and Solaris**

</td></tr><tr><td>

dmsetup

</td><td>

Examines a low level volume. -   **/etc/sudoers line example**:
    -   Disco ALL=\(root\) /usr/bin/dmsetup table \*
    -   Disco ALL=\(root\) /usr/bin/dmsetup ls
-   **Used by**: Discovery

</td></tr><tr><td colspan="2">

**All UNIX versions**

</td></tr><tr><td>

lsof

</td><td>

Determines the relationship between processes and the connections being made to the system.-   **/etc/sudoers line example**: Disco ALL=\(root\) /sbin/lsof
-   **Used by**: Discovery

</td></tr><tr><td>

oratab

</td><td>

Grants read access to the oratab file for locating the Oracle Home and pfile.-   **/etc/sudoers line example**: N/A
-   **Used by**: Discovery

</td></tr><tr><td colspan="2">

**Solaris**

</td></tr><tr><td>

iscsiadm

</td><td>

Gets iSCSI IQNs-   **/etc/sudoers line example**: $\{sudo:iscsiadm list target -S\}
-   **Used by**: Discovery

</td></tr><tr><td>

fcinfo

</td><td>

Gets WWPNs for ports.-   **/etc/sudoers line example**: $\{sudo:fcinfo remote-port -sl -p $port\}
-   **Used by**: Discovery

</td></tr><tr><td>

prtvtoc

</td><td>

Reports information about disk partitions.-   **/etc/sudoers line example**: Disco ALL=\(root\) /usr/bin/prtvtoc
-   **Used by**: Discovery

</td></tr><tr><td>

pfiles

</td><td>

Used for gathering TCP connections information.

 -   **/etc/sudoers** line example: Disco ALL=\(root\) /usr/bin/pfiles

-   **Used by**: Discovery


</td></tr><tr><td>

pgrep

</td><td>

Used for listing process IDs of a particular region to run pfiles on.

 -   **/etc/sudoers line** example: Disco ALL=\(root\) /usr/bin/pgrep

-   **Used by**: Discovery


</td></tr><tr><td>

/usr/bin/ps

</td><td>

Lists running process. As an alternative to running with root access, add a proc\_owner role.-   **/etc/sudoers line example**: Disco ALL=\(root\) /usr/bin/ps
-   **Used by**: Discovery

</td></tr><tr><td>

/usr/ucb/ps

</td><td>

Lists running process. As an alternative to running with root access, add a proc\_owner role. The use of the `/usr/ucb/ps` command is deprecated as of Solaris 11. Because Discovery, Orchestration, and Integration Hub require the use of this command for all Solaris versions, you must install the ucb utility manually on Solaris 11 systems. For instructions, see [KB0564262](https://support.servicenow.com/kb_view.do?sysparm_article=KB0564262).

-   **/etc/sudoers line example**: Disco ALL=\(root\) /usr/ucb/ps
-   **Used by**: Discovery

</td></tr></tbody>
</table>For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](https://www.servicenow.com/docs/access?context=r_CommandsnCredentials&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

## Access Requirements for Non-Root Credentials

If you do not provide Discovery with root access credentials, you must provide credentials with the following access requirements.

|Application|File or Directory|Access Required|
|-----------|-----------------|---------------|
|Apache|httpd.conf|Read|
|Hbase|hbase-site.xml|Read|
|JBoss|jboss-service.xml|Read|
|JBoss home directory|Read|
|web.xml|Read|
|MySQL|my.cnf|Read|
|NGINX|nginx.conf|Read|
|Oracle|oratab|Read|
|Associated \(s\) pfiles|Read|
|Oracle Listener|lsnrctl|Execute|
|listener.ora|Read|
|Tomcat|catalina.jar|Read|
|server.xml|Read|
|web.xml|Read|
|Unix|/etc/\*release|Read|
|/etc/bashrc|Read|
|/etc/profile|Read|
|/proc/cpuinfo|Read|
|/proc/vmware/sched/ncpus|Read|
|/var/log/dmesg|Read|
|APD directory|Read|
|WebSphere|cell.xml|Read|
|server.xml|Read|
|serverindex.xml|Read|

