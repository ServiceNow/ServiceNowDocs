---
title: Proxy server configuration for your Cloud Cost Management MID Server
description: You can configure any MID Server to use a proxy server for Cloud Cost Management operations. Proxy servers support all cloud-based activities such as running Discovery, Billing Download jobs, and Price Sheet Download jobs.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring access to CI data on your account, Configure Cloud Cost Management for AWS, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Proxy server configuration for your Cloud Cost Management MID Server

You can configure any MID Server to use a proxy server for Cloud Cost Management operations. Proxy servers support all cloud-based activities such as running Discovery, Billing Download jobs, and Price Sheet Download jobs.

## Detailed instructions

[Proxy server configuration for MID Servers used for Cloud Discovery and Cloud Provisioning and Governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/mid-server-proxy.md)

## Proxy server limitations

-   Only Windows or Linux platforms are supported.
-   The Google Cloud integration is not supported.
-   The VMware integration is not supported.
-   Remote PowerShell scripts cannot be executed.
-   Custom APIs might not work.

## Supported proxy server authentication for Cloud Cost Management

|Proxy Server type|Authentication type|
|-----------------|-------------------|
|HTTP/HTTPS|No authentication|
|SOCKS5|No authentication|
|HTTP/HTTPS|Basic authentication|
|SOCKS5|Basic authentication|
|HTTP/HTTPS|NTLM|

## Supported Proxy server configurations

|Configuration|Operating system|Proxy server|Authentication mode|
|-------------|----------------|------------|-------------------|
|Configuration 1|Linux|None|Not Applicable|
|Configuration 2|Windows|Squid \(HTTPS\)|None|
|Configuration 3|Linux|Squid \(HTTPS\)|Local|
|Configuration 4|Windows|Squid \(HTTPS\)|Active Directory|

**Related topics**  


[MID Servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerConfiguration.md)

[Install a MID Server on Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-install-prereqs.md)

[Install a MID Server on Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_InstallAMIDServerOnLinux.md)

