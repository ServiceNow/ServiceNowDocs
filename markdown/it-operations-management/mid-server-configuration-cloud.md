---
title: Install and configure MID Servers to access cloud environments
description: Install and configure the MID Servers correctly to enable ITOM products to access to the cloud resources.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Access to cloud environments for ITOM products, IT Operations Management]
---

# Install and configure MID Servers to access cloud environments

Install and configure the MID Servers correctly to enable ITOM products to access to the cloud resources.

## Before you begin

Role required: discovery\_admin or sn\_cmp.cloud\_admin \(for Cloud Provisioning and Governance\)

## About this task

## Procedure

1.  For IP-based discovery, [Installing the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-installation.md) on a server inside the cloud environment, inside a Virtual Private Cloud \(VPC\).

    For example, if you are configuring access to AWS service accounts using IAM roles, install the MID Server at the Amazon EC2 instance.

    **Important:** If you configure AWS credentials at ServiceNow AI Platform, the location of the MID Server doesn't matter.

    If your organization has multiple VPC segments, deploy the MID Servers in a manage-mentor transit VPC.

2.  Activate IP-based discovery jobs to access the compute layer using agentless credentials.

3.  Configure the MID Server with the capabilities necessary for the cloud environment you are planning to discover.

    You can select the `ALL` capability or configure specific capabilities for tighter security.

    Add Cloud Management in **supported application** in MID Server for Cloud Provisioning and Governance requests to be processed.

    |Cloud environment|MID Server capability required by Cloud Discovery|MID Server capability required by Cloud Provisioning and Governance|
    |-----------------|-------------------------------------------------|-------------------------------------------------------------------|
    |Amazon AWS Cloud|`AWS` or `Cloud Management` or `ALL`|`AWS` or `Cloud Management`|
    |Microsoft Azure Cloud|`Azure` or `Cloud Management` or `ALL`|`Azure` or `Cloud Management`|
    |Google Cloud|`Google` or `Cloud Management` or `ALL`|`Google` or `Cloud Management`|
    |IBM Cloud Platform|`IBM` or `Cloud Management` or `ALL`|N/A|
    |Oracle Cloud Infrastructure \(OCI\)|`OCI` or `Cloud Management` or `ALL`|N/A|
    |OpenStack|`OpenStack` or `Cloud Management` or `ALL`|N/A|
    |Red Hat Virtualization \(RHV\)|`RHV` or `Cloud Management` or `ALL`|N/A|

4.  If the MID Servers must go through an unauthenticated proxy server to access cloud resources, modify the `agent\conf\wrapper-override.conf` file, as follows:

    ```
    wrapper.java.additional.1=-Dhttp.proxySet=true
             wrapper.java.additional.2=-Dhttp.proxyHost=<proxyHost> 
             wrapper.java.additional.3=-Dhttp.proxyPort=<proxyPort> 
             wrapper.java.additional.4=-DuseProxy=true
    ```

5.  If you're using an authenticated proxy server, configure the MID Server parameters in the `config.xml` file.

    For a description of the parameter values, see the **Proxy server parameters** section in [MID Server parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-parameters.md).


**Parent Topic:**[Access to cloud environments for ITOM products](../reference/accessing-cloud-itom.md)

**Related topics**  


[Proxy server configuration for MID Servers used for Cloud Discovery and Cloud Provisioning and Governance](../reference/mid-server-proxy.md)

