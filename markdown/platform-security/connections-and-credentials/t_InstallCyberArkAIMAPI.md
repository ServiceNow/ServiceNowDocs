---
title: Configure the CyberArk vault and install the AIM API
description: Configure the CyberArk vault to allow MID Server access and install the CyberArk AIM API on the MID Server machine.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CyberArk integration configuration, CyberArk credential storage integration, External credential storage, Get started with credentials, Connections and Credentials, Access Management]
---

# Configure the CyberArk vault and install the AIM API

Configure the CyberArk vault to allow MID Server access and install the CyberArk AIM API on the MID Server machine.

## Before you begin

Role required: admin

Before starting this procedure, ensure that the [External Credential Storage plugin](t_ActivateExtrnlCredStoragePlugIn.md) is activated. CyberArk Application Access Manager \(AAM\) Credential Providers version 12.0.1 and later is supported.

## Procedure

1.  Configure the CyberArk vault with the application ID and authentication details that all MID Servers requesting credentials will use.

    For details, refer to the CyberArk Credential Provider and ASCP Implementation Guide.

    1.  Ensure that CyberArk is configured to allow the MID Server to access the vault by creating an App-ID in CyberArk called **ServiceNow\_MID\_Server**.

    2.  Make sure that every credential the MID Server needs is granted access to the **ServiceNow\_MID\_Server** App-ID.

        **Note:** You can override the default **ServiceNow\_MID\_Server** App-ID in the MID Server `config.xml` file using the [ext.cred.app\_id](t_ConfigureTheMIDServerForCyberArk.md) parameter. If you change the value in this parameter, make sure to configure a matching value in the vault.

2.  Install the CyberArk Credential Provider, including the AIM API, on each machine that hosts a MID Server service that is used to access the credential store.

3.  Provision CyberArk accounts and set permissions for application access.

    For details, refer to the CyberArk Privileged Account Security Implementation Guide.

    1.  In the CyberArk Password Safe, create the privileged accounts required by Discovery, Orchestration, or Service Mapping to access different devices and ensure that these accounts are members of the safes in which the necessary credentials are stored.

    2.  Add the Credential Provider and application users as members of the Password Safes where the application passwords are stored.


**Parent Topic:**[CyberArk integration configuration](../concept/c_CyberArkIntegrationConfiguration.md)

