---
title: Configuring access to CI data on your AWS account
description: To ensure secure and reliable communications, the Discovery process communicates with your cloud provider accounts and cloud resources through one or more MID Servers. You can set up the MID Servers on your network or in one of your cloud networks.
locale: en-US
release: yokohama
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Cloud Cost Management for AWS, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Configuring access to CI data on your AWS account

To ensure secure and reliable communications, the Discovery process communicates with your cloud provider accounts and cloud resources through one or more MID Servers. You can set up the MID Servers on your network or in one of your cloud networks.

**Important:** This information applies to both the Cloud Cost Management and Cloud Insights Billing apps. All references to Cloud Cost Management also apply to Cloud Insights Billing.

## Requirements

**Important:** This configuration process applies only if you use the Discovery application to discover cloud resources. Skip this process if you use a different method for discovering resources.

AWS: There must be an internal network connection between the MID Servers and the AWS Cloud API endpoints: \*.amazonaws.com.

## Detailed instructions

See Amazon AWS Cloud Discovery.

## MID Server settings for Cloud Cost Management

**Note:** MID Server minimum memory size should be 4 GB.

<table id="table_t5k_dvd_1jb"><thead><tr><th>

Setting

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Supported Applications

</td><td>

Cloud Actions

</td></tr><tr><td>

Capabilities

</td><td>

The **ALL** setting includes all required applications and capabilities. Alternatively, you can specify the following settings:

**Note:** You can specify the following settings for any number of MID Servers. If you specify multiple MID Servers, then Discovery, billing data download operations, and actions that are recommended by Cloud Cost Management are assigned to one of the MID Servers at random.

 Option 1: To use this MID Server only for AWS, specify both of the following values:

-   Cloud Actions
-   AWS

 Option 2: To use this MID Server for all providers, specify the following values:

-   Cloud Actions
-   AWS
-   Azure

</td></tr></tbody>
</table>## Using a proxy server

You can use a proxy server for the Cloud Cost Management MID Server. See [Proxy server configuration for your Cloud Cost Management MID Server](aws-mid-proxy-cloudin.md).

**Related topics**  


[MID Servers](https://www.servicenow.com/docs/access?context=c_MIDServerConfiguration&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[Install a MID Server on Windows](https://www.servicenow.com/docs/access?context=mid-server-install-prereqs&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[Install a MID Server on Linux](https://www.servicenow.com/docs/access?context=t_InstallAMIDServerOnLinux&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

