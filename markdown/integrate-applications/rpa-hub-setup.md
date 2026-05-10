---
title: Configuring RPA Hub
description: You can plan and configure an RPA Hub implementation in your organization.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [RPA Hub, Workflow Data Fabric]
---

# Configuring RPA Hub

You can plan and configure an RPA Hub implementation in your organization.

## Configuration overview

Perform the following tasks for configuring RPA Hub:

1.  [Install Robotic Process Automation \(RPA\) Hub](../../rpa-core/task/install-rpa.md).

    Install the Robotic Process Automation \(RPA\) Hub application \(sn\_rpa\_fdn\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

2.  \(Optional\) [Restructure RPA Hub tables](restructured-rpa-hub-tables-utah.md).

    Restructure the Robotic Process Automation \(RPA\) tables to an application file, so that changes that you make to these tables are captured in the update sets and can be moved seamlessly across environments. With this process, you don't have to re-create the data records in the targeted environment.

3.  \(Optional\) [Migrating your data from a lower environment to a higher environment in RPA Hub](migrate-data-rpa-hub.md).

    Use the update set capability to migrate your data from a lower \(non-production\) environment to a higher \(production\) environment for real-time use.

4.  [Set up client authentication and code signing certificates](../../rpa-core/concept/code-signing-certificate-rpa.md).

    You can generate a client authentication and a code signing certificate in two ways. You can either generate and install user certificates or export active directory certificates.

    -   [Generate and install user certificate from KeyStore Explorer](../../rpa-core/concept/use-user-certificates-rpa.md#).

        Generate a client authentication certificate for authentication purposes in the Unattended Robot application. Generate a code signing certificate for publishing an automation project from RPA Desktop Design Studio.

    -   [Export Active Directory certificates](../../rpa-core/concept/export-certificates-rpa.md#).

        You can export Microsoft Active Directory certificates, such as root, intermediate, and a client authentication certificate, for authentication purposes. You can then register the exported root and intermediate certificate in the ServiceNow instance and map the exported client authentication certificate to the user.

5.  [Applying the CSDM guidelines to RPA Hub](../../rpa-core/concept/rpa-hub-apply-csdm.md).

    Apply Common Service Data Model \(CSDM\) guidelines to define configuration items \(CIs\) and relationships between CIs in the CMDB. This process ensures that your data resides in the appropriate CMDB tables for maximum value from your ServiceNow AI Platform applications.

6.  [Create a robot license distribution record in RPA Hub](../task/create-lua-record.md).

    In the classic environment, define the consumption and distribution of licenses for parent and child domains, or global domain by creating a robot license distribution record in RPA Hub.

7.  [Configure RPA Hub properties](../reference/rpahub-sys-properties.md).

    In the classic environment, configure RPA Hub properties, such as auto assignment of robots or defining the authentication mechanism to customize the experience.


## Using Guided Setup to implement RPA Hub

Guided Setup provides a sequence of tasks that help you configure RPA Hub on your ServiceNow® instance. With Guided Setup, keep track of what you have completed, so you can stop and start again where you left off. To open Guided Setup for RPA Hub, navigate to **All** &gt; **Robotic Process Automation** &gt; **Administration** &gt; **Guided Setup**.

For more information about using the guided setup interface, see [Using guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/guided-setup.md).

## Using Guided Tours to get help related to a configuration task

Guided Tours provide step-by-step instructions on your ServiceNow® instance to help you complete a task. For more information about using guided tours, see [Use Guided Tours in RPA Hub](../task/use-guided-tour-rpa-hub.md).

**Related topics**  


[Configuring Unattended Robot](../../rpa-runtime/concept/rpa-runtime-setup.md)

[Configuring Attended Robot](../../rda-runtime/concept/rda-runtime-setup.md)

[Configure Now Assist for RPA Hub](../../rpa-studio/task/configure-now-assist-rpa-hub.md)

[Configuring RPA Desktop Design Studio](../../rpa-studio/concept/rpa-studio-configure.md)

