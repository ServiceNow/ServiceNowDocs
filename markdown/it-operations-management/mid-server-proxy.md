---
title: Proxy server configuration for MID Servers used for Cloud Discovery and Cloud Provisioning and Governance
description: You can configure the MID Server for Cloud Provisioning and Governance to use a proxy server. Using a proxy server supports all cloud-based activities such as running Discovery, billing downloads, provisioning virtual machines, and running life-cycle operations on virtual machines.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Install and configure MID Servers to access cloud environments, Access to cloud environments for ITOM products, IT Operations Management]
---

# Proxy server configuration for MID Servers used for Cloud Discovery and Cloud Provisioning and Governance

You can configure the MID Server for Cloud Provisioning and Governance to use a proxy server. Using a proxy server supports all cloud-based activities such as running Discovery, billing downloads, provisioning virtual machines, and running life-cycle operations on virtual machines.

## Proxy server limitations

-   VMware Cloud is not supported.
-   Windows or Linux platforms only are supported.
-   The Google Cloud Console integration does not support downloading billing data.
-   Remote PowerShell scripts cannot be executed.
-   Custom APIs may not work.

**Note:**

SSH calls should not be routed through a proxy server, when using a private cloud environment that is on the same side of the proxy as the MID Server.

Set **mid.capi.skip\_proxy\_for\_ssh** to true to skip it. See [MID Server properties used by Service Mapping](../../service-mapping/reference/mid-server-properties-service-mapping.md) for more information.

**mid.capi.skip\_proxy\_for\_ssh**:

-   Determines whether the MID Server skips the proxy server when routing SSH calls.
-   Type: true \| false
-   Default value: false

## Supported proxy server authentication for Cloud Provisioning and Governance

|Proxy Server type|Authentication type|
|-----------------|-------------------|
|HTTP/HTTPS|No authentication|
|SOCKS5|No authentication|
|HTTP/HTTPS|Basic authentication|
|SOCKS5|Basic authentication|
|HTTP/HTTPS|NTLM|

## Supported proxy server configurations for Cloud Provisioning and Governance

|Configuration|Operating system|Proxy server|Authentication mode|
|-------------|----------------|------------|-------------------|
|Configuration 1|Linux|None|Not Applicable|
|Configuration 2|Windows|Squid \(HTTPS\)|None|
|Configuration 3|Linux|Squid \(HTTPS\)|Local|
|Configuration 4|Windows|Squid \(HTTPS\)|Active Directory|

|Cloud provider|Functionality|Configuration 1|Configuration 2|Configuration 3|Configuration 4|
|--------------|-------------|---------------|---------------|---------------|---------------|
|Amazon AWS Cloud, Microsoft Azure Cloud, and IBM Cloud Platform|Cloud Discovery|Yes|Yes|Yes|Yes|
|VM Provisioning|Yes|Yes|Yes|Yes|
|VM life cycle|Yes|Yes|Yes|Yes|
|CFT provisioning|Yes|Yes|Yes|Yes|
|Billing download|Yes|Yes|Yes|Yes|
|Scripts using SSH|Yes|Yes|Yes|Yes|
|Scripts using PowerShell|Not Applicable|Not Applicable|Not Applicable|Not Applicable|
|Cloud events|Not Applicable|Not Applicable|Not Applicable|Not Applicable|
|Google Cloud Platform|Cloud Discovery|Yes|Yes|Yes|Yes|
|VM Provisioning|Yes|Yes|Yes|Yes|
|VM life cycle|Yes|Yes|Yes|Yes|
|CFT provisioning|Yes|Yes|Yes|Yes|
|Billing download|No|No|No|No|
|Scripts using SSH|Yes|Yes|Yes|Yes|
|Scripts using PowerShell|Not Applicable|Not Applicable|Not Applicable|Not Applicable|
|Cloud events|Not Applicable|Not Applicable|Not Applicable|Not Applicable|
|VMware Cloud|Not Applicable|

**Parent Topic:**[Install and configure MID Servers to access cloud environments](../task/mid-server-configuration-cloud.md)

**Related topics**  


[bundle-platcap.mid-server-install-prereqs]

[bundle-platcap.t_InstallAMIDServerOnLinux]

[bundle-platcap.mid-server-parameters]

