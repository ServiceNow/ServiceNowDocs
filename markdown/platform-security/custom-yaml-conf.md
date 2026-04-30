---
title: Specify custom rules in ECC firewall
description: Configure the External Communication Channel \(ECC\) firewall in your MID Server by specifying the custom rules to selectively allow or reject the incoming message and override the Code Signing configuration.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Code Signing, Platform Security]
---

# Specify custom rules in ECC firewall

Configure the External Communication Channel \(ECC\) firewall in your MID Server by specifying the custom rules to selectively allow or reject the incoming message and override the Code Signing configuration.

Security administrators can use the ECC firewall tags to override the Code Signing configuration and allow or reject specific operations on MID Server. These custom rules must be specified in the YAML file of the located at: `agent/boot-config.yaml`.

These tags are specific to a protocol. The configuration specified for the parent tag is applicable to the child tag. For example, if `Http` protocol is allowed, `rest` and `soap` protocols are also allowed. This table outlines the available parents and child tags.

<table id="table_tcl_p1j_3rb"><thead><tr><th>

Parent tag

</th><th>

Child tag

</th></tr></thead><tbody><tr><td>

DNS

</td><td>

 

</td></tr><tr><td>

HTTP

</td><td>

-   REST
-   SOAP

</td></tr><tr><td>

DIRECTORY\_SERVICES

</td><td>

LDAP

</td></tr><tr><td>

SNMP

</td><td>

 

</td></tr><tr><td>

SSH

</td><td>

-   SCP
-   SFTP

</td></tr><tr><td>

SYSLOG

</td><td>

 

</td></tr><tr><td>

WINDOWS

</td><td>

-   CIM
-   POWERSHELL
-   WMI
-   WINRM

</td></tr><tr><td>

JAVASCRIPT

</td><td>

 

</td></tr><tr><td>

GROOVY

</td><td>

 

</td></tr><tr><td>

VCS

</td><td>

GIT

</td></tr><tr><td>

DATABASES

</td><td>

JDBC

</td></tr><tr><td>

DATA\_SOURCES

</td><td>

 

</td></tr><tr><td>

INTEGRATION\_HUB

</td><td>

 

</td></tr><tr><td>

ITOM

</td><td>

-   CLOUD\_PROVISIONING\_GOVERNANCE
-   DISCOVERY
-   EVENT\_MANAGEMENT
-   HEALTH\_LOG\_ANALYTICS
-   SERVICE\_MAPPING

</td></tr><tr><td>

ORCHESTRATION

</td><td>

 

</td></tr></tbody>
</table>To configure the custom rules:

1.  In the MID Server, identify the file `boot-config-sample.yaml`.
2.  Rename the YAML file to `boot-config.yaml` and move the file to the location: `agent/boot-config.yaml`.
3.  In the YAML file, specify the custom rules and save the changes. An example of the YAML file:

    ```
    security:​
      eccFirewall:​
        mode: enforcing​
        rules:​
          - tags: [rest]​
            action: accept​
          - tags: [soap]​
            action: accept​
          - tags: [jdbc]​
            action: reject​
    ```

4.  Restart the MID Server.

**Parent Topic:**[Configuring Code Signing](../concept/config-code-signing.md)

