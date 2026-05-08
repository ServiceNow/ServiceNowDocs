---
title: Prerequisites for performing top-down discovery using Service Mapping
description: Learn about credentials, users, and user permissions you must configure to let Service Mapping access and discover applications inside your organization private network.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 66
breadcrumb: [Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Prerequisites for performing top-down discovery using Service Mapping

Learn about credentials, users, and user permissions you must configure to let Service Mapping access and discover applications inside your organization private network.

Configure the relevant requirements to enable successful top-down discovery:

-   **Host credentials**

    Service Mapping uses credentials of the hosts to access applications running on this host. Typically, host credentials are enough for top-down discovery. For example, to discover the HP Service Manager Application Server, configure only credentials for accessing the server hosting this application, SSH credentials, or Windows credentials.

-   **Applicative credentials**

    To discover some applications, Service Mapping needs separate credentials from credentials of the host on which such applications run. This type of credentials is referred to in ServiceNow as applicative credentials. For example, to discover the ABAP SAP Central Services \(ASCS\), configure applicative credential in addition to the host credentials.

-   **Elevated rights for Unix-based hosts**

    For Unix-based hosts, configure on MID Servers, you must provide a user with sudo-level credentials on all Unix-based hosts in your organization. For example, if the server hosting ASCS is Unix-based, provide a user with elevated rights to be able to run discovery commands against this Unix-based server.

-   **SNMP community credentials**

    Configure SNMP community credentials to allow Service Mapping and Discovery to query network devices using the SNMP protocol. For example, configure SNMP community credentials for A10 Networks Thunder ADC.

-   **Users or user permissions**

    You may need to provide additional users or user permissions to run certain commands or access certain directories. For example, for ASCS, provide a user with permissions to run SOAP on RFC read table function.


The ServiceNow AI Platform provides a centralized way of configuring credentials for Discovery, Service Mapping, and other applications. It allows you to configure credentials for hosts and applications only once. If you have already configured host-related credentials for another application, you do not need to do it again for Service Mapping.

You can assign credentials to specific MID Servers or keep credential generic so all MID Servers can use them. MID Servers retrieve commands and credentials from the ServiceNow instance and apply them to discover CIs inside organization private network.

![Assigning credentials to the MID Server that uses them to access CIs](../image/CredentialsGeneralDiagram.png "Assigning credentials to the MID Server that uses them to access CIs")

Use the following guidelines to decide for which MID Server to create credentials:

-   If all CIs, belonging to the same CI type, share a credential, you do not need to specify a MID Server for it. In that case, it is used on all MID Servers by default.

    **Note:** Specifying the MID Server when configuring credentials is optional.

-   If CIs of the same type and on the same network have different credentials, configure these credentials and define order in which Service Mapping uses them when trying to connect to these CIs.

In addition to generic credentials, you configure on MID Servers, you must configure sudo-level credentials on all Unix-based hosts in your organization.

If the MID Server does not have sufficient credentials to access a device or application, it can run Network Mapper \(Nmap\) commands to collect basic information without using credentials. Credential-less discovery with Nmap requires additional configuration as described in [Install and uninstall Nmap on a MID Server](https://www.servicenow.com/docs/access?context=install-nmap-on-mid-server&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

Review the list of credentials necessary to discover hosts and applications supported in the base system.

<table id="table_xfr_kpw_dz"><thead><tr><th>

Application

</th><th>

CI type

</th><th>

Configure this

</th></tr></thead><tbody><tr><td>

AIX OS

</td><td>

AIX Server \[cmdb\_ci\_aix\_server\]

</td><td>

Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td rowspan="3">

IBM z/OS

</td><td rowspan="3">

IBM zOS server Server \[cmdb\_ci\_ibm\_zos\_server\]

</td><td>

-   Run the USS service on the port 22 on the z/OS server.
-   On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   Provide the user with the following permissions:
    -   To write into the /tmp directory.
    -   To see all user processes.
    -   To run REXX scripts.

</td></tr><tr><td>

On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Provide the user with the following permissions:-   To write into the /tmp directory.
-   To see all user processes.
-   To run REXX scripts.

</td></tr><tr><td rowspan="2">

HP-UX OS

</td><td rowspan="2">

HPUX Server \[cmdb\_ci\_hpux\_server\]

</td><td>

Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

Linux OS

</td><td rowspan="2">

Linux Server \[cmdb\_ci\_linux\_server\]

</td><td>

Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Solaris OS

</td><td>

Solaris Server \[cmdb\_ci\_solaris\_server\]

</td><td>

Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td rowspan="2">

Windows OS

</td><td rowspan="2">

Windows Server \[cmdb\_ci\_windows\_server\]

</td><td>

On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Provide all necessary credentials and permissions as described in [Credentials required for host discovery](r_Credentials4HostDiscovery.md).

</td></tr><tr><td rowspan="2">

A10 Load Balancing

</td><td rowspan="2">

A10 Load Balancer \[cmdb\_ci\_lb\_A10\]

</td><td>

Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Configure [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

Windows Active Directory Domain Services

</td><td rowspan="2">

Active Directory Domain Controller \[cmdb\_ci\_ad\_controller\]

</td><td>

On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

[AWS DynamoDB](../concept/aws-dynamoDB-discovery.md)

</td><td>

DynamoDB Global Table \[cmdb\_ci\_dynamodb\_global\_table\]

</td><td>

-   On the AWS Console, provide a user with the following permissions: AmazonDynamoDBReadOnly Access and AWSLambdaInvocation-DynamoDB.
-   On the ServiceNow AI Platform®, configure AWS credentials, using a secret key and an access key.

</td></tr><tr><td rowspan="2">

Amazon Web Services \(AWS\) Elastic Load Balancing

</td><td rowspan="2">

Load Balancer Service \[cmdb\_ci\_lb\_service\]

</td><td>

Configure [Amazon Web Services](https://www.servicenow.com/docs/access?context=r_CloudManagementCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) credentials.

</td></tr><tr><td>

On the ServiceNow AI Platform, [create a service account](../../cloud-management-v2-setup/task/aws-first-cld-and-srvc-accts.md). Set the Account ID to the Amazon ELB account ID as it appears in the AWS Management Console.

</td></tr><tr><td rowspan="4">

Amazon Web Services \(AWS\) API Gateway

</td><td rowspan="4">

 

</td><td>

Configure [Amazon Web Services](https://www.servicenow.com/docs/access?context=r_CloudManagementCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) credentials.

</td></tr><tr><td>

On the ServiceNow AI Platform, [create a service account](../../cloud-management-v2-setup/task/aws-first-cld-and-srvc-accts.md). Set the Account ID to the Amazon account ID to which API Gateway belongs. Use the Account ID as it appears in the AWS Management Console.

</td></tr><tr><td>

Provide a user with permissions to run the apigateway:GET function for just the GET action in API Gateway.

</td></tr><tr><td>

Ensure to place the MID Server on the virtual machine that is part of the service account that you are planning to discover.

</td></tr><tr><td rowspan="4">

Amazon Web Services \(AWS\) Elastic Compute Cloud \(EC2\)

</td><td rowspan="4">

Windows Server \[cmdb\_ci\_windows\_server\] or Linux Server \[cmdb\_ci\_linux\_server\]

</td><td>

\(If hosted on a Unix server\), on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

On the ServiceNow AI Platform, [create a service account](../../cloud-management-v2-setup/task/aws-first-cld-and-srvc-accts.md). Set the Account ID to the Amazon account ID to which API Gateway belongs. Use the Account ID as it appears in the AWS Management Console.

</td></tr><tr><td>

Ensure to place the MID Server inside the Amazon cloud.

</td></tr><tr><td rowspan="3">

Amazon Web Services \(AWS\) Relational Database Service \(RDS\)

</td><td rowspan="3">

Cloud DataBase \[cmdb\_ci\_cloud\_database\]

</td><td>

Configure [Amazon Web Services](https://www.servicenow.com/docs/access?context=r_CloudManagementCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) credentials.

</td></tr><tr><td>

On the ServiceNow AI Platform, [create a service account](../../cloud-management-v2-setup/task/aws-first-cld-and-srvc-accts.md). Set the Account ID to the Amazon account ID to which RDS belongs. Use the Account ID as it appears in the AWS Management Console.

</td></tr><tr><td>

Ensure to place the MID Server inside the Amazon cloud.

</td></tr><tr><td rowspan="4">

Amazon Web Services \(AWS\) Lambda

</td><td rowspan="4">

Cloud Function \[cmdb\_ci\_cloud\_function\]

</td><td>

Configure [Amazon Web Services](https://www.servicenow.com/docs/access?context=r_CloudManagementCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) credentials.

</td></tr><tr><td>

On the ServiceNow AI Platform, [create a service account](../../cloud-management-v2-setup/task/aws-first-cld-and-srvc-accts.md). Set the Account ID to the Amazon account IT to which AWS Lambda belongs. Use the Account ID as it appears in the AWS Management Console.

</td></tr><tr><td>

Ensure to place the MID Server on the virtual machine that is part of the service account that you are planning to discover.

</td></tr><tr><td>

Provide a user with permissions to run the ListFunctions API with the Resource: arn:aws:lambda:region:account-id: function:function-name.

Provide a user with permissions to run the GetFunction API with the Resource: ‘\*’.

</td></tr><tr><td rowspan="4">

Apache Tomcat

</td><td rowspan="4">

Tomcat \[cmdb\_ci\_app\_server\_tomcat\]

</td><td>

Give the user elevated rights to execute [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on a Unix server\), on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Apache Tomcat WAR

</td><td rowspan="3">

Tomcat WAR \[cmdb\_ci\_app\_server\_tomcat\_war\]

</td><td>

Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on UNIX\), on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="6">

Apache Web Server

</td><td rowspan="6">

Apache Web Server \[cmdb\_ci\_apache\_web\_server\]

</td><td>

\(If hosted on UNIX\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

On the server hosting the Apache Web Server, give the user permission to execute the following command: `$APACHEHOME/bin/httpd –V`.

</td></tr><tr><td>

On the server hosting the Apache Web Server, verify that the $APACHEHOME/bin/envvar file is configured with the correct native library path.

</td></tr><tr><td>

\(If hosted on UNIX\), on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

App TNS Service

</td><td rowspan="3">

\[cmdb\_ci\_appl\_ora\_tns\]

</td><td>

Give the user elevated rights to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux or UNIX\), on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

F5 BIG-IP Global Traffic Manager \(GTM\) and F5 BIG-IP Local Traffic Manager \(LTM\)

</td><td>

Load Balancer Service \[cmdb\_ci\_lb\_service\]

</td><td>

-   To successfully discover the load balancer pool members, set the **display service names** option \(**bigpipe.displayservicenames**\) of the load balancer to **false** on the F5 load balancer.
-   For F5 Load Balancer pattern:
    -   Configure [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=australia&pubname=australia-platform-security&ft:locale=en-US) on the ServiceNow AI Platform.
    -   \(Optional\) If there are iRules or SNMP community credentials are not enough for discovering outgoing connections, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Note:** If you do not want to use SSH credentials, you can use the REST API to create a connection to F5 BIG-IP devices.

Service Mapping uses the SSH credentials to retrieve connections that are not from CMDB. Discovering connections using the SSH protocol is a failover mechanism for the SNMP-based discovery.

-   For F5 Load Balancer SSH pattern:
    -   Configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).
    -   Verify permissions for the following SSH commands:
        -   `list auth partition all`
        -   `list sys global-settings`
        -   `show sys hardware`
        -   `list sys db failover.state`
        -   `list net self one-line`
        -   `show sys mac-address | grep interface`
        -   `show net interface field-fmt`
        -   `show net self | grep -e 'Mac Address' 'IP:'`
        -   `list ltm pool | grep -e 'pool' 'mode'`
        -   `list ltm pool /<partition_name>/* | grep -e 'pool' 'mode'`
        -   `show ltm pool | grep -e 'Ltm::' 'Total Connections'`
        -   `show ltm pool /<partition_name>/* |grep -e 'Ltm::' 'Total Connections'`
        -   `list sys db bigpipe.displayservicenames | grep value`
        -   `show /net vlan | grep -e 'Interface Name' 'Mac' 'Tag'`
        -   `show ltm virtual detail | grep -e 'Server:' 'State' 'Pool:' 'Destination' 'Total Connections'`
        -   `show ltm virtual detail /<partition_name>/* | grep -e 'Server:' 'State' 'Pool:' 'Destination' 'Total Connections'`
        -   `show gtm wideip | grep -e 'WideIp' 'State'`
        -   `list wideip a /<partition_name>/* | grep -e 'WideIp' 'State'`
        -   `show gtm wideip all | grep -e 'WideIp' 'State'`
        -   `list gtm wideip`
        -   `list gtm wideip all`
-   For F5REST pattern:
    -   For horizontal discovery using Discovery, provide read-only permissions to run the following APIs:

        -   `"https://" + $ipAddress + "/mgmt/tm/ltm/pool"`
        -   `"https://" + $ipAddress + "/mgmt/tm/sys/global-settings"`
        -   `"https://" + $ipAddress + "/mgmt/tm/sys/hardware"`
        -   `"https://" + $ipAddress + "/mgmt/tm/sys/failover"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/self"`
        -   `"https://" + $ipAddress + "/mgmt/tm/ltm/virtual?$select=destination,mask,vlans"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/interface"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/interface/stats"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/trunk"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/vlan"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/vlan/"+<vlan id>+"/interfaces"`
        -   `"https://" + $ipAddress + "/mgmt/tm/gtm/wideip"`
        -   `"https://" + $ipAddress + "/mgmt/tm/cm/traffic-group/"`
        -   `"https://" + $ipAddress + "/mgmt/tm/cm/device"`
    -   Create [basic authentication](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) credentials.
-   For F5 REST OAuth 2.0 authentication pattern:
    -   Verify read-only permission for the following APIs:
        -   `"https://" + $ipAddress + "/mgmt/shared/authn/login"`
        -   `"https://" + $ipAddress + "/mgmt/tm/ltm/pool"`
        -   `"https://" + $ipAddress + "/mgmt/tm/sys/global-settings"`
        -   `"https://" + $ipAddress + "/mgmt/tm/sys/hardware"`
        -   `"https://" + $ipAddress + "/mgmt/tm/sys/failover"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/self"`
        -   `"https://" + $ipAddress + "/mgmt/tm/ltm/virtual?$select=destination,mask,vlans"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/interface"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/interface/stats"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/trunk"`
        -   `"https://" + $ip_address + "/mgmt/tm/net/vlan"`
        -   `"https://" + $ipAddress + "/mgmt/tm/net/vlan/"+<vlan id>+"/interfaces"`
        -   `"https://" + $ipAddress + "/mgmt/tm/gtm/wideip"`
        -   `"https://" + $ipAddress + "/mgmt/tm/cm/traffic-group/"`
        -   `"https://" + $ipAddress + "/mgmt/tm/cm/device"`
    -   Create [basic authentication](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) credentials.
    -   Create [a credential alias](https://www.servicenow.com/docs/access?context=discovery-credential-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US) for the basic authentication credential.
    -   Create a [serverless discovery schedule](../task/create-serverless-sched-f5-rest-oauth.md).
-   For top-down discovery using Service Mapping, provide permissions to run the following APIs:

    -   `https://" get_attr {"managementIP"}"/mgmt/tm/ltm/"get_attr {"irule"}`
    -   `https://" get_attr {"managementIP"}"/mgmt/tm/ltm/virtual/~Common~"get_attr {"vip_name"}`
    -   `https://" get_attr {"computer_system.managementIP"}"/mgmt/tm/ltm/pool/"get_attr {"pool_name"}"/members?`
-   \(Optional\) For top-down discovery with Service Mapping, configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   \(Optional\) For top-down discovery with Service Mapping, provide a user with permissions to run the following commands:
    -   bigpipe commands \(for BIG-IP LTM F5 or BIG-IP GTM F5 version 9\)
    -   bigpipe and Traffic Management Shell \(TMSH\) commands \(for BIG-IP LTM F5 or BIG-IP GTM F5 version 10\)
    -   Traffic Management Shell \(TMSH\) commands \(for BIG-IP LTM F5 or BIG-IP GTM F5 version 11\)
    -   Traffic Management Shell \(TMSH\) advanced commands \(for BIG-IP LTM F5 or BIG-IP GTM F5 version 10, 11, and 12\)
    -   The **show cm traffic-group – get command** for discovering F5 BIG-IP Device Service Clustering
-   \(Optional\) For top-down discovery with Service Mapping, give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td rowspan="3">

BMC CTRL-M Enterprise Manager

</td><td rowspan="3">

Control-M \[cmdb\_ci\_appl\_controlm\]

</td><td>

Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Linux or UNIX server\) \(Optional\) on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

BMC CTRL-M Gateway

</td><td rowspan="3">

Control-M \[cmdb\_ci\_appl\_controlm\]

</td><td>

Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Linux or UNIX server\) \(Optional\) on the ServiceNow AI Platform, configure cc.

</td></tr><tr><td>

BMC IT Asset Management \(ITAM\)

</td><td>

ITAM Asset Center \[cmdb\_ci\_appl\_itam\]

</td><td>

On the ServiceNow AI Platform, configure a Windows OS user with permissions to access the ITAM registry as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

CA Identity Manager Provisioning Server

</td><td rowspan="2">

CA Identity Manager Provisioning Server \[cmdb\_ci\_appl\_ca\_id\_man\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Cadebill Interconnect

</td><td>

inter connect \[cmdb\_ci\_inter\_connect\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Cadebill Interconnect Instance

</td><td>

Interconnect Instance \[cmdb\_ci\_interconnect\_instance\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Cisco Application Control Engine ACE \(on Cisco CSM\)

</td><td rowspan="3">

ACE \[cmdb\_ci\_lb\_ace\]

</td><td>

On the ServiceNow AI Platform, configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

On the ServiceNow AI Platform, configure SNMP community credentials as described in [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

Cisco CallManager

</td><td rowspan="2">

Cisco CallManager \[cmdb\_ci\_appl\_cisco\_call\_man\]

</td><td>

\(If hosted on a Linux or UNIX server\) \(Optional\) on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Cisco Global Site Selector \(GSS\)

</td><td rowspan="3">

Load Balancer Service \[cmdb\_ci\_lb\_service\]

</td><td>

Configure SNMP community credentials as described in [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Provide a user who has permissions to run query on the domain list, DNS rule output, and VIP answer to get the outgoing connections of GSS.

</td></tr><tr><td>

Citrix Delivery Controller

</td><td>

Delivery Controller \[cmdb\_ci\_appl\_delivery\_controler\]

</td><td>

-   Configure [Windows administrative credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) to access the host machine.
-   Make sure that [PowerShell for Discovery](../../discovery/reference/r_PowerShellForDiscovery.md) is installed on your MID Servers. The patterns used for Citrix discovery require the ability to run PowerShell commands.
-   For OS users, make sure you can execute “Get-XDSite.” The Citrix Studio Admin should provide permissions.
-   \(Optional\) For top-down discovery with Service Mapping, on Citrix Delivery Controller, install the Citrix.Broker module.
-   \(Optional\) For top-down discovery with Service Mapping, a user with permission to run PowerShell commands.
-   \(Optional\) \(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Citrix Usage Collector

</td><td>

Citrix Collector \[cmdb\_ci\_appl\_citrix\_collector\]

</td><td>

-   Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   Configure a user with permissions to run PowerShell commands on the Citrix server.
-   \(If hosted on a Windows server\) On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Note:** To use this credential later for XenAPP, set the **Credential alias** attribute to cmdb\_ci\_appl\_citrix\_xenapp. To use this credential later for Citrix, set the **Credential alias** attribute to cmdb\_ci\_appl\_citrix\_collector.

-   To discover Epic, provide permission to run `afarm` command.
-   Provide a user with permissions to read and query the Citrix repository:
    -   For versions 4.5 and later, a PowerShell script from the XenApp server.
    -   For versions earlier than 4.5, a Microsoft Visual Basic Script \(VBScript\) from the Citrix Presentation Server
-   \(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Note:** To use this credential later for XenAPP, set the **Credential alias** attribute to cmdb\_ci\_appl\_citrix\_xenapp. To use this credential later for Citrix, set the **Credential alias** attribute to cmdb\_ci\_appl\_citrix\_collector.


</td></tr><tr><td>

Citrix Presentation Server/Citrix XenApp **Note:** Citrix XenApp is the new name for Presentation Server beginning with the XenApp 5 release.

</td><td>

Citrix XenAPP or Presentation Server \[cmdb\_ci\_appl\_citrix\_xenapp\]

</td><td>

-   On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   \(Optional\) To discover using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

</td></tr><tr><td>

Citrix Netscaler

</td><td>

Citrix Netscaler \[cmdb\_ci\_lb\_netscaler\]

</td><td>

-   Configure [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Note:** You also have the option of using [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US). However, if the payload size of the data that is returned to the instance is large, the discovery process can fail. In this case, use SNMP credentials instead.

-   \(Optional\) Provide a user with the read access to the **NS.conf** configuration file if you do not want to provide SNMP or SSH credentials.
-   Use [basic authentication](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) credentials for discovery via REST.

 Service Mapping uses the SSH credentials to retrieve connections that are not from CMDB. Discovering connections using the SSH protocol is a failover mechanism for the SNMP-based discovery.

</td></tr><tr><td>

Citrix Netscaler Global Server Load Balancer

</td><td>

Load Balancer Service \[cmdb\_ci\_lb\_service\]

</td><td>

-   Configure [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Note:** You also have the option of using [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US). However, if the payload size of the data that is returned to the instance is large, the discovery process can fail. In this case, use SNMP credentials instead.

-   \(Optional\) Provide a user with the read access to the **NS.conf** configuration file if you do not want to provide SNMP or SSH credentials.
-   Use [basic authentication](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) credentials for discovery via REST.

</td></tr><tr><td rowspan="3">

Connect APK

</td><td rowspan="3">

Connect-It Service \[cmdb\_ci\_appl\_connectit\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Linux or Unix server\) on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

EMC Documentum

</td><td rowspan="2">

Documentum DocBase \[cmdb\_ci\_appl\_doc\_docbroker\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Linux or Unix server\) \(Optional\) on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

Epic

</td><td rowspan="2">

epicd app server \[cmdb\_ci\_epicd\_app\_server\]

 epic agent \[cmdb\_ci\_epic\_agent\]

 epic cache \[cmdb\_ci\_epic\_cache\]

 epicd \[cmdb\_ci\_endpoint\_epicd\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Linux or Unix server\) \(Optional\) on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

FormEngine

</td><td rowspan="3">

Oracle Forms Engine \[cmdb\_ci\_appl\_ora\_forms\]

</td><td>

Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Unix server\) on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

[Google Cloud Platform](google-gcp-discovery-pattern.md)

</td><td>

Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

</td><td>

-   Provide a read-only user with permission to use the following API elements.
-   On the ServiceNow AI Platform, configure Google API credentials.

</td></tr><tr><td rowspan="2">

HAProxy

</td><td rowspan="2">

HAProxy Load Balancer \[cmdb\_ci\_lb\_haproxy\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Linux or Unix server\) \(Optional\) on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

HP Operations Manager

</td><td rowspan="2">

HP Operations Manager \[cmdb\_ci\_appl\_hp\_operations\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

HP Service Manager Application Server

</td><td rowspan="3">

HP Service Manager \[cmdb\_ci\_appl\_hp\_service\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Linux or Unix server\) \(Optional\) on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

HP Service Manager Index

</td><td rowspan="2">

HP SM Index Server \[cmdb\_ci\_appl\_hp\_index\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Linux or Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

HP Service Manager Knowledge Base

</td><td rowspan="2">

HP SM KnowledgeBase \[cmdb\_ci\_appl\_hp\_sm\_kb\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

HP Quality Center

</td><td>

HP Quality Center \[cmdb\_ci\_appl\_hp\_qc\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

HP UCMDB

</td><td>

HP uCMDB \[cmdb\_ci\_app\_server\_hp\_ucmdb\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

[IBM Cloud Platform](ibm-cloud-platform-discovery.md)

</td><td>

Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]

</td><td>

On the ServiceNow AI Platform, configure the IBM Credentials for accessing the IBM account.

</td></tr><tr><td rowspan="2">

IBM WebSphere Message Broker

</td><td rowspan="2">

IBM WebSphere Message Broker \[cmdb\_ci\_appl\_ibm\_wmb\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) for a user with permissions to run the following commands: -   "source " + $directory + "/mqsiprofile”
-   "echo $MQSI\_VERSION “
-   $directory + "/mqsireportbroker " + $name
-   $directory + "/mqsibrowse " + $name + " -t BROKERRESOURCES “

 Set the **Credential alias** attribute to \[cmdb\_ci\_appl\_ibm\_wmb\]. Configuring this attribute allows you later to use the credential for this CI in patterns.

</td></tr><tr><td rowspan="2">

IBM CTRL-M Server

</td><td rowspan="2">

Control-M \[cmdb\_ci\_appl\_controlm\]

</td><td>

\(If hosted on Unix\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on Windows\), on the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

IBM CICS Transaction Gateway CTG

</td><td rowspan="2">

IBM CTG \[cmdb\_ci\_appl\_ibm\_ctg\]

</td><td>

Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

IBM Customer Information Control System \(CICS\)

</td><td rowspan="2">

IBM CICS \[cmdb\_ci\_appl\_ibm\_cics\]

</td><td>

\(If hosted on Unix\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

IBM DB2

</td><td>

DB2 Instance \[cmdb\_ci\_db\_db2\_instance\]**Note:** Starting with CMDB CI Class Models version 1.69.0, the label has been renamed to **DB2 Subsystem**.

</td><td>

-   \(If hosted on Linux\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).
-   \(If hosted on Windows\), on the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

Set the tag attribute to \[cmdb\_ci\_db\_db2\_instance\]. Configuring this attribute allows you later to use the credential for this CI in patterns.

\(Optional\) To discover connections to IBM DB2, configure SSH credentials for a user with permissions to run the following commands:

    -   `db2 list tablespaces`
    -   "db2cmd /c /w /i db2 -tvf "+$ script\_name
-   \(If hosted on z/OS\) Provide the user with the following permissions:
    -   To write into the /tmp directory.
    -   To see all user processes.
    -   To run REXX scripts.
    -   To read into the db2 folder.
-   \(If hosted on z/OS\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

IBM J2EE EAR

</td><td rowspan="3">

\[cmdb\_ci\_app\_server\_ws\_ear\]

</td><td>

\(If hosted on Linux only\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Windows\), on the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

[IBM PowerHA SystemMirror for AIX discovery](ibm-powerha-hamcp-discovery.md)

</td><td>

-   Cluster Resource Group \[cmdb\_ci\_cluster\_resource\_group\]
-   UNIX Cluster Resource \[cmdb\_ci\_unix\_cluster\_resource\]
-   UNIX Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]
-   AIX Server \[cmdb\_ci\_aix\_server\]
-   UNIX Cluster \[cmdb\_ci\_unix\_cluster\]
-   Cluster Virtual IP \[cmdb\_ci\_cluster\_vip\]

</td><td>

Configure a UNIX user with permissions to run all commands defined in the official IBM documentation.

</td></tr><tr><td rowspan="5">

IBM Tivoli Access Manager WebSEAL or IBM Security Access Manager \(ISAM\) appliance

</td><td rowspan="5">

Webseal \[cmdb\_ci\_app\_server\_webseal\]

</td><td>

\(For ISAM appliance only\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US) for the user with permissions to run the following REST commands:-   /reverseproxy – for retrieving data about the reverse proxy and instances.
-   /wga/reverseproxy/"+$\{junctionstable\[\].instance\}+"/junctions – for getting junctions per each instance.
-   /wga/reverseproxy/" + $instance\_name + "/junctions?junctions\_id=" + $junction\_name – for getting forwarding URLs for the entry point junction.

</td></tr><tr><td>

\(For ISAM appliance only\) Ensure that the system can use the cURL commands for discovery:-   On the MID Server used for ISAM appliance discovery, define the PATH variable to contain the [cURL package installation](https://curl.haxx.se/download.html) for the relevant MID Server users.
-   Configure permissions to run the `curl.exe` file for the relevant MID Server user.

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Windows\), on the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

[IBM Virtualization and Hardware Management Console \(HMC\)](ibm-hmc-discovery.md)

</td><td>

-   HMC server
-   IBM frame
-   Logical partition \(LPAR\) instance

An LPAR is virtual machine equivalent of IBM.

-   LPAR resource

</td><td>

-   Verify that the following applications are up to date:
    -   Discovery and Service Mapping Patterns
    -   CMDB CI Class Models
-   Verify you have permissions for the following HMC commands:
    -   `lssyscfg`
    -   `lshmc`
    -   `lshwres`
    -   `lssysconn -r all -F type_model_serial_num:ipaddr`
-   Verify you have permissions for the following AIX \(LPAR\) command: `lparstat -i`.

**Note:** The `lparstat -i` command is in addition to the commands required for AIX server discovery. For more information on AIX server discovery, see [AIX server discovery](../../discovery/reference/r_DataCollDiscoAIXComputers.md). For a list of the AIX commands, see [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

-   Configure SSH credentials on the ServiceNow AI Platform. For more information, see [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="6">

IBM WebSphere Application Server

</td><td rowspan="6">

IBM Websphere \[cmdb\_ci\_app\_server\_websphere\]

</td><td>

\(If hosted on Unix only\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Windows\), on the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on z/OS\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on z/OS\) Provide the user with the following permissions:-   To write into the /tmp directory.
-   To see all user processes.
-   To run REXX scripts.
-   To run commands using oeconsol.
-   To run the command that brings info on the WebSphere Application Server task:`"oeconsol 'D OMVS,A=ALL' | grep "+$taskname`.
-   To read content of the WAS installation folder and the permission to read was.env.file where the installation variables are situated.

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

IBM WebSphere DataPower

</td><td>

Data Power \[cmdb\_ci\_app\_server\_datapower\]

</td><td>

-   **[SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

SNMP credentials are necessary for using the following SNMP queries:

    -   For horizontal discovery of the Data Power Hosting Server \[cmdb\_ci\_datapower\_server\]:
        -   1.3.6.1.2.1.1.1
        -   1.3.6.1.2.1.1.5
        -   1.3.6.1.2.1.4.20.1
        -   1.3.6.1.2.1.2.2.1
        -   1.3.6.1.4.1.14685.3.1.196.1
        -   1.3.6.1.4.1.14685.3.1.11.1
        -   1.3.6.1.4.1.14685.3.1.112.1
    -   For top-down discovery of the Data Power \[cmdb\_ci\_datapower\_server\]:
        -   1.3.6.1.2.1.1.1
        -   1.3.6.1.2.1.1.5
        -   1.3.6.1.4.1.14685.3.1.11.1
-   **[Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

Together with SNMP credentials, applicative credentials are required to discover DataPower application domains, otherwise known as logical CIs.

In addition, SNMP and applicative credentials are used for top-down discovery of applicative relationships \(corresponding application DataPower domain\).

-   **User with permissions to run SOAP**

Permissions to run SOAP queries are necessary for top-down discovery of the DataPower Web Service and MQ connection.


</td></tr><tr><td rowspan="4">

IBM WebSphere Message Broker Flow

</td><td rowspan="4">

WMB Flow \[cmdb\_ci\_appl\_wmb\]

</td><td>

\(If hosted on a Unix server\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

Provide an IBM WebSphere Message Broker OS user with permissions to run the WebSphere Message Broker service.

</td></tr><tr><td>

\(If hosted on Windows\), on the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) for a user with permissions to run the following commands: -   "source " + $directory + "/mqsiprofile”
-   "echo $MQSI\_VERSION “
-   $directory + "/mqsireportbroker " + $name
-   $directory + "/mqsibrowse " + $name + " -t BROKERRESOURCES “

 Set the **Credential alias** attribute to \[cmdb\_ci\_appl\_ibm\_wmb\]. Configuring this attribute allows you later to use the credential for this CI in patterns.

</td></tr><tr><td rowspan="4">

IBM WebSphere Message Broker

</td><td rowspan="4">

IBM WebSphere Message Broker \[cmdb\_ci\_appl\_ibm\_wmb\]

</td><td>

\(If hosted on Unix\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US). Set the **Credential alias** attribute to \[cmdb\_ci\_appl\_ibm\_wmb\]. Configuring this attribute allows you later to use the credential for this CI in patterns.

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Provide an IBM WebSphere Message Broker OS user with permissions to run the WebSphere Message Broker service.

</td></tr><tr><td rowspan="6">

IBM MQ \(formerly IBM WebSphere MQ\)

</td><td rowspan="6">

IBM MQ Manager \(formerly IBM WebSphere MQ\) \[cmdb\_ci\_appl\_ibm\_wmq\]

</td><td>

\(If hosted on Unix\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US) for a user with permissions to run the following commands:-   \(If hosted on a Windows server\) "echo display QMSTATUS ALL \| runmqsc -e " + $queue\_manager – for getting the queue manager \(QM\) status.
-   \(If hosted on a Windows server\) "echo display QMGR ALL \| runmqsc -e " + $queue\_manager – for getting the complete information about QM.
-   \(If hosted on a Unix server\) "echo \\" display QMSTATUS ALL \\" \| runmqsc " + $queue\_manager – for getting the QM status.
-   \(If hosted on a Unix server\) "echo \\" display QMGR ALL \\" \| runmqsc " + $queue\_manager – for getting the complete information about QM.
-   \(If hosted on a Unix server\) "echo \\" display queue\(" + $entry\_point.queue + "\) \\" \| runmqsc " + $queue\_manager – for getting the information about the EP queue.

</td></tr><tr><td>

\(If hosted on Windows\), on the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Unix server\) configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).While configuring OS credentials, set the **Credential alias** attribute to cmdb\_ci\_appl\_ibm\_wmq. Configuring this attribute allows you later to use the credential for this CI in patterns.

 \(Optional\) To find IBM MQ connections, configure SSH credentials for a user with permissions to run the following commands:

-   "echo \\" display queue\("+$entry\_point.queue+"\) \\" \| runmqsc "+$queue\_manager
-   "echo \\" display QMSTATUS ALL \\" \| runmqsc "+$queue\_manager
-   echo \\" display QMGR ALL \\" \| runmqsc "+$queue\_manager

</td></tr><tr><td>

\(If hosted on z/OS\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on z/OS\) Provide the user with the following permissions:-   To write into the /tmp directory.
-   To see all user processes.
-   To run REXX scripts.
-   To run commands using oeconsol.
-   To run MQ commands.

</td></tr><tr><td rowspan="5">

IBM MQ Queue \(formerly IBM WebSphere MQ Queue\)

</td><td rowspan="5">

IBM MQ Queue \(formerly IBM WebSphere MQ Queue\) \[cmdb\_ci\_appl\_ibm\_wmq\_queue\]

</td><td>

\(If hosted on a Unix server\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US) for a user with permissions to run the following commands:-   dspmq – for getting information about the queue manager.
-   "echo \\" display queue\(" + $entry\_point.queue + "\) \\" \| runmqsc " + $queue\_manager – for getting the queue information.
-   "echo \\" display clusqmgr\(\*\) conname \\" \| runmqsc " + $queue\_manager – for getting all cluster queue manager \(QM\) lines.
-   "echo \\" display qstatus\(" + $entry\_point.queue + "\) TYPE\(HANDLE\) OPENTYPE\(INPUT\) CONNAME PID \\" \| runmqsc " + $queue\_manager – for getting the queue status information.

</td></tr><tr><td>

\(If hosted on Unix server\) on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) for a user with permissions to run the following commands: -   dspmq

echo \\" display queue\("+$entry\_point.queue+"\) \\" \| runmqsc "+$queue\_manager

-   \(Optional\) "echo \\" display qcluster\("+$rqmname+"\) \\" \| runmqsc "+$queue\_manager
-   \(Optional\) "echo \\" dischl\(\*\) CHLTYPE\(SDR\) CONNAME XMITQ WHERE\(XMITQ EQ "+$xmit\_name+"\)\\" \| runmqsc "+$queue\_manager
-   \(Optional\) "echo \\" display clusqmgr\(\*\) conname \\" \| runmqsc "+$queue\_manager
-   \(Optional\) "echo \\" display qstatus\("+$entry\_point.queue+"\) TYPE\(HANDLE\) OPENTYPE\(INPUT\) CONNAME PID \\" \| runmqsc "+$queue\_manager

 While configuring OS credentials, set the **Credential alias** attribute to cmdb\_ci\_appl\_ibm\_wmq. Configuring this attribute allows you later to use the credential for this CI in patterns.

</td></tr><tr><td>

\(If hosted on Windows\), on the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) for a user with permissions to run the following commands: -   dspmq

echo \\" display queue\("+$entry\_point.queue+"\) \\" \| runmqsc "+$queue\_manager

-   \(Optional\) "echo \\" display qcluster\("+$rqmname+"\) \\" \| runmqsc "+$queue\_manager
-   \(Optional\) "echo \\" dischl\(\*\) CHLTYPE\(SDR\) CONNAME XMITQ WHERE\(XMITQ EQ "+$xmit\_name+"\)\\" \| runmqsc "+$queue\_manager
-   \(Optional\) "echo \\" display clusqmgr\(\*\) conname \\" \| runmqsc "+$queue\_manager
-   \(Optional\) "echo \\" display qstatus\("+$entry\_point.queue+"\) TYPE\(HANDLE\) OPENTYPE\(INPUT\) CONNAME PID \\" \| runmqsc "+$queue\_manager

 While configuring OS credentials, set the **Credential alias** attribute to cmdb\_ci\_appl\_ibm\_wmq. Configuring this attribute allows you later to use the credential for this CI in patterns..

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="4">

IBM WebSphere Portal

</td><td rowspan="4">

Websphere Portal \[cmdb\_ci\_appl\_websphere\_portal\]

</td><td>

\(If hosted on Linux only\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

Interconnect Web Service

</td><td rowspan="2">

Inter connect \[cmdb\_ci\_inter\_connect\]

</td><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="4">

Jboss

</td><td rowspan="4">

JBoss \[cmdb\_ci\_app\_server\_jboss\]

</td><td>

Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Unix server\) on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Jboss Module

</td><td rowspan="3">

Jboss module \[cmdb\_ci\_app\_server\_jb\_module\]

</td><td>

\(If hosted on a Unix server\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="4">

JRun

</td><td rowspan="4">

Jrun \[cmdb\_ci\_app\_server\_jrun\]

</td><td>

\(If hosted on Unix only\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

JRun WAR Inc

</td><td rowspan="3">

Jrun WAR \[cmdb\_ci\_app\_server\_jrun\_war\]

</td><td>

\(If hosted on Unix only\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Microsoft Azure Web Sites

</td><td>

Cloud WebServer \[cmdb\_ci\_cloud\_webserver\]

</td><td>

On the ServiceNow AI Platform, [add an Azure service principal](../../cloud-management-v2-setup/task/azure-service-account-cloud-mgt.md) and [set up a cloud account for Azure](../../cloud-management-v2-setup/task/azure-cloud-accts-cloud-mgt.md). Set the account Id to the Azure Service Principal as it appears at the Microsoft Azure Console.

</td></tr><tr><td>

Microsoft Azure Load Balancer

</td><td>

Load Balancer Service \[cmdb\_ci\_lb\_service\]

</td><td>

On the ServiceNow AI Platform, configure [add an Azure service principal](../../cloud-management-v2-setup/task/azure-service-account-cloud-mgt.md) and [set up a cloud account for Azure](../../cloud-management-v2-setup/task/azure-cloud-accts-cloud-mgt.md). Set the account Id to the Azure Service Principal as it appears at the Microsoft Azure Console.

</td></tr><tr><td>

Microsoft Azure SQL Database

</td><td>

Cloud Database Rule \[cmdb\_ci\_cloud\_database\]

</td><td>

On the ServiceNow AI Platform, [add an Azure service principal](../../cloud-management-v2-setup/task/azure-service-account-cloud-mgt.md) and [set up a cloud account for Azure](../../cloud-management-v2-setup/task/azure-cloud-accts-cloud-mgt.md). Set the account Id to the Azure Service Principal as it appears at the Microsoft Azure Console.

</td></tr><tr><td rowspan="2">

Microsoft Dynamic CRM

</td><td rowspan="2">

Dynamic CRM Component \[cmdb\_ci\_appl\_ms\_dynamic\_crm\]

</td><td>

On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

Microsoft BizTalk Orchestration

</td><td rowspan="2">

BizTalk Orchestration \[cmdb\_ci\_appl\_biztalk\_orch\]

</td><td>

On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Microsoft BizTalk Server

</td><td>

BizTalk \[cmdb\_ci\_appl\_biztalk\]

</td><td>

On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Microsoft Exchange BackEnd Server

</td><td rowspan="3">

ExchangeBackEndServer \[cmdb\_ci\_exchange\_backend\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Configure [credentials required for host discovery](r_Credentials4HostDiscovery.md) for a Windows server.

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Microsoft Exchange FrontEnd Server

</td><td rowspan="3">

ExchangeFrontEndServer \[cmdb\_ci\_exchange\_frontend\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Configure [credentials required for host discovery](r_Credentials4HostDiscovery.md) for a Windows server.

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

Microsoft FAST Search Server

</td><td rowspan="2">

Fast Search \[cmdb\_ci\_appl\_fastsearch\]

</td><td>

Create a user with the permission to read the following files: -   `install_directory+"\etc\VERSION.xml`
-   `and install_directory+"\etc\CSConfig.xml`

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Microsoft Exchange Hub Transport ServerMicrosoft Exchange Mailbox

 Microsoft Exchange CAS

</td><td>

ExchangeHub \[cmdb\_ci\_exchange\_hub\]Exchange MailBox \[cmdb\_ci\_exchange\_mailbox\]

 Exchange Client Access Server \[cmdb\_ci\_exchange\_cas\]

</td><td>

-   On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US). Use the Microsoft Exchange Server administrator's user name and password as Windows credentials. For example, user name: local\\administrator and password: Are1300.

**Note:** If you configure Windows credentials for a user different from the Microsoft Exchange Server administrator, Service Mapping uses traffic-based discovery that results in mapping all Microsoft Exchange clients.

-   \(For Exchange CAS 2010 and 2013, 2016\) On the ServiceNow AI Platform, configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US), setting the CI type to Exchange Mailbox.

**Warning:** Do not confuse the Exchange Mailbox CI type with the Exchange Mailbox Server CI type.

Service Mapping uses these applicative credentials to access the of/Servers/Servers.slab folder on the Key Exchange Admin Center \(EAC\). Service Mapping also uses the applicative credentials to run the following PowerShell commands against the MID Servers:

    -   Get-ExchangeServer
    -   Get-ExchangeServer
    -   Get-MailboxServer
    -   Get-ClusteredMailBoxServerStatus
    -   Get-ExchangeServer
    -   Get-StorageGroup
    -   Get-MailboxDatabase
-   \(For Microsoft Exchange CAS 2010 and 2016\) On the Windows Server hosting Microsoft Exchange CAS, install the Microsoft.Exchange.Management.PowerShell.E2010 module.
-   \(For Microsoft Exchange CAS 2007\) On the Windows Server hosting Microsoft Exchange CAS, install the Microsoft.Exchange.Management.PowerShell.Admin module.
-   \(For Microsoft Exchange CAS 2007, 2010\) On the ServiceNow AI Platform, upload the rctrlx tool for running PowerShell commands as described in [Upload the rctrlx.exe file to MID Servers](../task/upload-rctrlx-file.md).
-   \(For Microsoft Exchange CAS 2007 and 2010\) Provide an Exchange Mailbox OS user with the rights to run Exchange services on Windows and has permission to query Exchange repository:

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) setting the **Credential alias** attribute to \[cmdb\_ci\_exchange\_mailbox\]. Configuring this attribute allows you later to use the credential for this CI in patterns.

-   \(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   Verify that you know the entry point necessary for discovering the Microsoft Exchange Server. Use the URL for the Outlook web access in the following format:

`http(s)://<hostname>:<port>/owa`

For example, `http(s)://myhost:<443>/owa`


</td></tr><tr><td>

Microsoft Identity Integration Server

</td><td>

IIFP \[cmdb\_ci\_directory\_iifp\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

Microsoft Internet Information Services \(IIS\)

</td><td rowspan="2">

Microsoft iis Web Server \[cmdb\_ci\_microsoft\_iis\_web\_server\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Microsoft Internet Information Services \(IIS\) Virtual Directory

</td><td rowspan="3">

IIS Virtual Directory \[cmdb\_ci\_iisdirectory\]

</td><td>

On the ServiceNow AI Platform, configure the following credentials:-   [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US)

</td></tr><tr><td>

Verify read access to the following files:-   `web.config`: Possible locations `$entry_point.path + "Web.config"` or `$entry_point.path + "\Web.config"`
-   `machine.config`: possible location `"dir \"C:\Windows\Microsoft.NET\"`

</td></tr><tr><td>

-   \(Optional\) To find ADO.NET connections, set the **Credential alias** attribute to \[cmdb\_ci\_iisdirectory\]. Configuring this attribute allows you later to use the credential for this CI in patterns.
-   \(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Microsoft Message Queuing \(MSMQ\)

</td><td>

MSMQ \[cmdb\_ci\_appl\_msmq\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="4">

Microsoft .NET Framework

</td><td rowspan="4">

.NET Application \[cmdb\_ci\_appl\_dot\_net\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).\(Optional\) To find ADO.NET connections, set the **Credential alias** attribute to \[cmdb\_ci\_iisdirectory\]. Configuring this attribute allows you later to use the credential for this CI in patterns.

</td></tr><tr><td>

Provide an IIS Virtual Directory OS user with the rights to run the IIS service on Windows.

</td></tr><tr><td>

Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Microsoft SharePoint

</td><td rowspan="3">

SharePoint \[cmdb\_ci\_appl\_sharepoint\]

</td><td>

On the ServiceNow AI Platform, configure the following credentials:-   [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   Set the **Credential alias** attribute to \[cmdb\_ci\_appl\_sharepoint\]. Configuring this attribute allows you later to use the credential for this CI in patterns.
-   Configure WMI Query access to the remote Sharepoint server.
-   \(Optional\) To find Windows SharePoint connections, configure Windows credentials for a user with permissions to run http get request to the SharePoint Central Administration URL.

</td></tr><tr><td>

Provide a SharePoint OS user with permissions:

-   To run SharePoint services on Windows
-   To log into the SharePoint Admin page

</td></tr><tr><td>

To use two separate credentials with different permissions, configure credentials as covered in [Prerequisites for performing top-down discovery / Service Mapping discovery to Sharepoint system \[KB0813083\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0813083) article in the Now Support Knowledge Base.

</td></tr><tr><td rowspan="3">

Microsoft SQL Database

</td><td rowspan="3">

MySQLClusterDataNode \[cmdb\_ci\_db\_mysql\_clusternode\]

</td><td>

Provide the following user or users:-   For discovering Microsoft Biztalk using SQL queries, provide a user and credentials for Microsoft BizTalk.
-   For discovering licensing information on Microsoft SQL Server, provide a user and credentials for accessing Microsoft SQL Database.

 Refer to the product documentation for operational information.

</td></tr><tr><td>

Credentials for host discovery as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

MongoDB

</td><td rowspan="3">

Mongo Config Server \[cmdb\_ci\_appl\_mongo\_config\_serv\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Provide a user with permissions to run Mongo commands described in [Service Mapping commands not requiring a privileged user](r_NonSudoCommands.md).

</td></tr><tr><td rowspan="2">

MySQL Cluster MGM Node

</td><td rowspan="2">

MySQLClusterMGMNode \[cmdb\_ci\_db\_mysql\_clustermgnode\]

</td><td>

\(If hosted on Unix only\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="4">

Nginx

</td><td rowspan="4">

Nginx Web Server \[cmdb\_ci\_nginx\_web\_server\]

</td><td>

\(If hosted on Unix only\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

OpenText Documentum

</td><td rowspan="2">

Documentum DocBase \[cmdb\_ci\_appl\_doc\_docbase\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Oracle Application Server

</td><td rowspan="3">

Oracle iAS \[cmdb\_ci\_app\_server\_ora\_ias\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Oracle Advanced Queue Queue

</td><td rowspan="3">

Advanced Queue Queue \[cmdb\_ci\_appl\_ora\_queue\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials for Service Mapping](r_SupportedApplications.md).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Oracle Clusterware

</td><td>

UNIX Cluster \[cmdb\_ci\_unix\_cluster\], UNIX Cluster Node \[cmdb\_ci\_unix\_cluster\_node\], UNIX Cluster Resource \[cmdb\_ci\_unix\_cluster\_resource\], Cluster Virtual IPs \[cmdb\_ci\_cluster\_vip\]

</td><td>

See [Oracle database discovery](../../discovery/concept/c_OracleDatabaseDiscovery.md).

</td></tr><tr><td rowspan="4">

Oracle Concurrent Server

</td><td rowspan="4">

Oracle Concurrent Server \[cmdb\_ci\_appl\_ora\_conc\]

</td><td>

\(If hosted on Unix only\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="5">

Oracle Database

</td><td rowspan="5">

Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]

</td><td>

\(If hosted on Unix only\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

[Oracle Database 12c](oracle-cdb-pdb-discovery.md)

</td><td>

Oracle PDB Instance \[cmdb\_ci\_db\_ora\_pdb\_instance\]

</td><td>

-   Configure [Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   For Windows, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   For Unix, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   For the Oracle database, configure [Oracle database discovery](../../discovery/concept/c_OracleDatabaseDiscovery.md)
-   Provide a user with permissions to run queries on the following tables:
    -   V$DATAFILE
    -   V$TEMPFILE​
    -   V$LOG
    -   DBA\_FREE\_SPACE
    -   V$DATABASE
    -   V$PDBS
    -   V$PARAMETER

</td></tr><tr><td rowspan="3">

Oracle Database Advanced Queuing

</td><td rowspan="3">

Advanced Queue Queue \[cmdb\_ci\_appl\_ora\_queue\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Provide an Oracle instance user with permission to run the sqlplus command as described in [Service Mapping commands not requiring a privileged user](r_NonSudoCommands.md).

</td></tr><tr><td rowspan="5">

Oracle Discoverer Engine

</td><td rowspan="5">

Oracle Discoverer Engine \[cmdb\_ci\_appl\_ora\_disc\]

</td><td>

\(If hosted on Unix only\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="5">

Oracle Discoverer UI

</td><td rowspan="5">

Oracle Discoverer UI \[cmdb\_ci\_appl\_ora\_disc\_ui\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials for Service Mapping](r_SupportedApplications.md).

</td></tr><tr><td>

On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Unix only\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="4">

Oracle E-Business Suite

</td><td rowspan="4">

Oracle ESB \[cmdb\_ci\_appl\_ora\_ebs\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Oracle Form UI

</td><td rowspan="3">

Oracle Forms UI \[cmdb\_ci\_appl\_ora\_forms\_ui\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure a domain user for accessing the Windows OS as described in [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

Oracle Fulfillment Server

</td><td rowspan="2">

Oracle Fulfillment Server \[cmdb\_ci\_appl\_ora\_fs\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Oracle GlassFish Server

</td><td>

GlassFish \[cmdb\_ci\_appl\_glassfish\] GlassFish WAR \[cmdb\_ci\_appl\_glassfish\_war\]

</td><td>

-   \(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   \(If hosted on a Linux or UNIX server\) \(Optional\) on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   \(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="4">

Oracle HTTP Server

</td><td rowspan="4">

Oracle HTTP Server \[cmdb\_ci\_appl\_ora\_http\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Oracle iAS Web Module

</td><td rowspan="3">

Oracle iAS Web module \[cmdb\_ci\_app\_server\_ora\_ias\_m\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Oracle Metric Client

</td><td rowspan="3">

Oracle Metric Client \[cmdb\_ci\_appl\_ora\_metric\_client\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="4">

Oracle Metric Server

</td><td rowspan="4">

Oracle Metric Server \[cmdb\_ci\_appl\_ora\_metric\_svr\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="6">

Oracle MySQL Server

</td><td rowspan="6">

MySQL Instance \[cmdb\_ci\_db\_mysql\_instance\]

</td><td>

Provide the following user or users:-   For discovering Microsoft Biztalk using SQL queries, provide a user and credentials for Microsoft BizTalk.
-   For discovering licensing information on Microsoft SQL Server, provide a user and credentials for accessing Microsoft SQL Database.

</td></tr><tr><td>

Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) Give the user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(If hosted on a Linux server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Oracle Net Listener

</td><td>

Oracle Database Listener \[cmdb\_ci\_db\_ora\_listener\]

</td><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

Oracle Notification Server

</td><td rowspan="2">

Oracle Notification Server \[cmdb\_ci\_appl\_ora\_notif\_svr\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Oracle OACORE Server

</td><td rowspan="3">

Oracle OACORE Server \[cmdb\_ci\_appl\_ora\_oacore\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Oracle OAFM Server

</td><td rowspan="3">

Oracle OAFM Server \[cmdb\_ci\_appl\_ora\_oafm\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Unix\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Oracle PeopleSoft

</td><td>

Peoplesoft Application Server \[cmdb\_ci\_appl\_peoplesoft\]

</td><td>

\(If hosted on Unix\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

 

</td><td>

 

</td><td>

Provide a user with permissions to run commands described in [Service Mapping commands not requiring a privileged user](r_NonSudoCommands.md).

</td></tr><tr><td rowspan="4">

Oracle Process Manager

</td><td rowspan="4">

Oracle Process Manager \[cmdb\_ci\_appl\_ora\_pm\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="4">

Oracle Report Server

</td><td rowspan="4">

Oracle Report Server \[cmdb\_ci\_appl\_ora\_report\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Oracle Tnslsnr Engine

</td><td rowspan="3">

Oracle TNS Listener Engine \[cmdb\_ci\_appl\_ora\_tnslsnr\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on Linux\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Oracle Tuxedo and Oracle Tuxedo Portal

</td><td>

Tuxedo \[cmdb\_ci\_appl\_tuxedo\] and Tuxedo Portal \[cmdb\_ci\_appl\_tuxedo\_portal\]

</td><td>

-   On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   \(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   \(If hosted on Unix\) Provide a user with the elevated rights for running commands described in [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

Oracle WebLogic Module

</td><td>

Oracle iAS Web module \[cmdb\_ci\_app\_server\_ora\_ias\_m\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="4">

Oracle WebLogic Server \(version 10.3\)

</td><td rowspan="4">

Weblogic \[cmdb\_ci\_app\_server\_weblogic\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Oracle WebLogic On-demand Router Load Balancer

</td><td rowspan="3">

Websphere ODR LB \[cmdb\_ci\_app\_server\_ws\_odr\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials for Service Mapping](r_SupportedApplications.md).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Radware Alteon NG

</td><td>

Alteon Load Balancer \[cmdb\_ci\_lb\_alteon\]

</td><td>

On the ServiceNow AI Platform, configure [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Radware AppDirector

</td><td>

Radware Load Balancer \[cmdb\_ci\_lb\_radware\]

</td><td>

On the ServiceNow AI Platform, configure [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="3">

Red Hat Cluster Suite

</td><td rowspan="3">

Cluster Virtual IPs \[cmdb\_ci\_cluster\_vip\]

 UNIX Cluster \[cmdb\_ci\_unix\_cluster\]

 UNIX Cluster Node \[cmdb\_ci\_unix\_cluster\_node\]

 UNIX Cluster Resource \[cmdb\_ci\_unix\_cluster\_resource\]

</td><td>

On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Provide a user with permissions to read these files:-   `/etc/cluster/cluster.conf`
-   `/etc/hosts`

</td></tr><tr><td>

Provide a user with elevated rights for running this command: `clustat –x`.

</td></tr><tr><td rowspan="5">

PostgreSQL Database

</td><td rowspan="5">

PostgreSQL Instance \[cmdb\_ci\_db\_postgresql\_instance\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(For hosted on Unix only\) Give this user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="4">

Pivotal RabbitMQ

</td><td rowspan="4">

RabbitMQ Cluster \[cmdb\_ci\_appl\_rabbitmq\_cluster\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

SAP Business Object XI Schedule

</td><td rowspan="2">

SAP BO BOXIScheduleRouter \[cmdb\_ci\_appl\_sap\_bo\_scheduler\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, seew [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

SAP Crystal Management Server

</td><td rowspan="2">

SAP Business Objects CMS server \[cmdb\_ci\_appl\_sap\_bo\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

SAP Central Instance/SAP Central Services \(SCS\)/

 SAP Development Infrastructure/

 SAP Evaluated Receipt Settlement \(ERS\)/

 SAP Java Connector/

 SAP NetWeaver Dialog Instance/

 ABAP SAP Central Services \(ASCS\)

</td><td>

SAP CI Application \[cmdb\_ci\_appl\_sap\_ci\]/SAP SCS Application \[cmdb\_ci\_appl\_sap\_scs\]/

 SAP DI Application \[cmdb\_ci\_appl\_sap\_di\]/

 SAP ERS Application \[cmdb\_ci\_appl\_sap\_ers\]/

 SAP JC Application \[cmdb\_ci\_appl\_sap\_jc\]/

 SAP DI Application \[cmdb\_ci\_appl\_sap\_di\]/

 SAP ASCS Application \[cmdb\_ci\_appl\_sap\_ascs\]

</td><td>

-   \(If hosted on a UNIX server\) On the ServiceNow AI Platform, configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US) and [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US). The SSH credentials are used to create connections from SAP Central Instance \(CI\) to other applications and devices. In addition, provide the user elevated rights to be able to run commands requiring a privileged user: [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).
-   \(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) to create connections from SAP CI to other applications and devices.
-   \(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   \(Optional for top-down discovery by Service Mapping\) Provide a user with permissions to run SOAP on RFC read table function.
-   \(Optional for top-down discovery by Service Mapping\) If your organization deploys SAP Digital Business Services using web services and you want to map all connected services, perform the following actions:
    -   Configure applicative credentials for a user with permissions to access the following tables: CVERS, DBCONS, and RFCDES.
    -   Ensure that you have the web service URL. For information on how to create web services, see [https://blogs.sap.com/2012/10/24/how-to-create-web-services-abap-based/](https://blogs.sap.com/2012/10/24/how-to-create-web-services-abap-based/).

</td></tr><tr><td rowspan="3">

SAP HANA Database

</td><td rowspan="3">

SAP Hana Db \[cmdb\_ci\_appl\_sap\_hana\_db\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="5">

SAP Sybase DB

</td><td rowspan="5">

Sybase Instance \[cmdb\_ci\_db\_syb\_instance\]

</td><td>

\(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(For hosted on Unix only\) Give this user elevated rights to be able to run [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

SQL Server Analysis Services \(SSAS\)

</td><td>

SQL Server Analysis Services \[cmdb\_ci\_db\_mssql\_analysis\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

SQL Server Integration Services \(SSIS\) Job

</td><td>

SQL Server Integration Services Job \[cmdb\_ci\_db\_mssql\_int\_job\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

SQL Server Integration Services \(SSIS\)

</td><td rowspan="2">

SQL Server Integration Services \[cmdb\_ci\_db\_mssql\_integration\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="6">

SQL Server Reporting Services \(SSRS\)

</td><td rowspan="6">

SQL Server Reporting Services \[cmdb\_ci\_db\_mssql\_reporting\]

</td><td>

Provide an SSRS OS user with permissions to run the SSRS Service.

</td></tr><tr><td>

Configure credentials for a user with permissions to run http get request to the entry point URL.

</td></tr><tr><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US). Set the **Credential alias** attribute to \[cmdb\_ci\_db\_mssql\_reporting\]. Configuring this attribute allows you later to use the credential for this CI in patterns.

</td></tr><tr><td>

\(Optional\) To discover connections to report datasources, configure credentials for a user with the permission to run http post request to the entry point URL.

</td></tr><tr><td>

Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

Sun iPlanet Web Server

</td><td rowspan="2">

Iplanet Web Server \[cmdb\_ci\_iplanet\_web\_server\]

</td><td>

Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

Sun Directory

</td><td rowspan="2">

Sun LDAP Server \[cmdb\_ci\_sun\_ldap\_dir\_server\]

</td><td>

Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

Sun JES

</td><td rowspan="2">

JES \[cmdb\_ci\_email\_server\_jes\]

</td><td>

Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Symantec Enterprise Vault

</td><td>

Enterprise Vault \[cmdb\_ci\_email\_server\_ent\_vault\]

</td><td>

On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

TIBCO ActiveMatrix BusinessWorks/TIBCO ActiveMatrix BusinessWorks Process/

 TIBCO EMS Queue/

 TIBCO Enterprise Message Service \(EMS\)/

</td><td>

ActiveMatrix Business Works \[cmdb\_ci\_appl\_tibco\_matrix\]/ActiveMatrix Business Works Process \[cmdb\_ci\_appl\_tibco\_matrix\_proc\]/

 EMS Queue \[cmdb\_ci\_appl\_tibco\_queue\]/

 Tibco Enterprise Message Service \[cmdb\_ci\_appl\_tibco\_message\]

</td><td>

-   \(If hosted on Unix\) Configure [applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=australia&pubname=australia-platform-security&ft:locale=en-US) for the Tibco EMS.
-   \(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   \(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   \(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td rowspan="2">

TIBCO ActiveMatrix Adapter

</td><td rowspan="2">

Tibco Adapter \[cmdb\_ci\_appl\_tibco\_adapter\]

</td><td>

\(If hosted on a Unix server\) On the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Veritas Enterprise Vault

</td><td>

Enterprise Vault \[cmdb\_ci\_email\_server\_ent\_vault\]

</td><td>

\(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr></tbody>
</table>## Resolving credential-related issues

If there are discovery issues caused by incorrectly configured or missing credentials, resolve them as explained in the KB article: [Credentials &amp; Permissions troubleshooting on Discovery, Service Mapping, Orchestration](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0657528)

-   **[Credentials required for host discovery](r_Credentials4HostDiscovery.md)**  
There are credentials and permissions that Service Mapping requires for discovering hosts.
-   **[Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md)**  
Service Mapping uses commands requiring elevated rights to discover and map Unix-based hosts in your organization. In addition to configuring necessary credentials, configure servers in your organization to allow Service Mapping to run these commands with elevated rights.
-   **[Service Mapping commands not requiring a privileged user](r_NonSudoCommands.md)**  
Most of commands utilized by Service Mapping for discovery and mapping do not require elevated rights.
-   **[SNMP-based queries](snmp-based-queries.md)**  
Service Mapping accesses network infrastructure devices like load balancers and routers using Simple Network Management Protocol \(SNMP\) v1/v2c/v3. Configure SNMP community credentials to enable this type of access.

**Parent Topic:**[Configuring Service Mapping](../concept/service-mapping-setup.md)

**Related topics**  


[PowerShell for Discovery and Service Mapping](../../discovery/reference/r_PowerShellForDiscovery.md)

