---
title: Proxy server configuration for your Cloud Cost Management MID Server
description: You can configure any MID Server to use a proxy server for Cloud Cost Management operations. Proxy servers support all cloud-based activities such as running Discovery, Billing Download jobs, and Price Sheet Download jobs.
locale: en-US
release: yokohama
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring access to CI data on your AWS account, Configure Cloud Cost Management for AWS, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Proxy server configuration for your Cloud Cost Management MID Server

You can configure any MID Server to use a proxy server for Cloud Cost Management operations. Proxy servers support all cloud-based activities such as running Discovery, Billing Download jobs, and Price Sheet Download jobs.

**Important:** This information applies to both the Cloud Cost Management and Cloud Insights Billing apps. All references to Cloud Cost Management also apply to Cloud Insights Billing.

## Detailed instructions

[Proxy server configuration for MID Servers used for Cloud Discovery and Cloud Provisioning and Governance](https://www.servicenow.com/docs/access?context=mid-server-proxy&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)

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


[MID Servers](https://www.servicenow.com/docs/access?context=c_MIDServerConfiguration&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[Install a MID Server on Windows](https://www.servicenow.com/docs/access?context=mid-server-install-prereqs&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[Install a MID Server on Linux](https://www.servicenow.com/docs/access?context=t_InstallAMIDServerOnLinux&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

