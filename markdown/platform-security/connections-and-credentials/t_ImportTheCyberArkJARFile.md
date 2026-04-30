---
title: Import the CyberArk JAR file
description: Import the CyberArk JavaPasswordSDK.jar file into the instance to make it accessible to the MID Server.
locale: en-US
release: yokohama
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [CyberArk integration configuration, CyberArk credential storage integration, External credential storage, Getting started with credentials, Connections and Credentials, Access Management]
---

# Import the CyberArk JAR file

Import the CyberArk JavaPasswordSDK.jar file into the instance to make it accessible to the MID Server.

## Before you begin

Role required: agent\_admin or admin

Before starting this procedure, ensure that CyberArk is configured to allow the MID Server access to credentials. Ensure that the CyberArk AIM API is installed on each server hosting a MID Server that is used to access the vault.

**Note:** Two separate CyberArk integrations are not supported by the MID Server. The same version of the CyberArk AIM API must be installed on all MID Servers connected to the same instance.

## About this task

Use this process even if the JavaPasswordSDK.jar file already exists on the MID Server.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **JAR Files**.

2.  Click **New**.

3.  Complete the form using the fields in the table.

    |Field|Description|
    |-----|-----------|
    |Name|Unique and descriptive name for identifying the file in the instance.|
    |Version|Optional version number for the file, if one is available.|
    |Source|Provider of the JAR file. Source information is not used by the system.|
    |Description|Optional short description of the JAR file and its purpose in the instance.|

4.  Attach the JAR file to this record.

    The AIM `JavaPasswordSDK.jar` file comes with the AIM SDK installation files and is typically located on the MID Server in the AIM installation directory at `<install_dir>/CyberArk/ApplicationPasswordSdk`.

    **Note:** The attached AIM JavaPasswordSDK.jar must match the installed version of the CyberArk AIM API. Any mismatch in JavaPasswordSDK.jar files may lead to unpredictable behavior and potential functionality issues.

5.  Click **Submit**.

6.  Restart the MID Server service.

    The platform makes the JAR file available to any MID Server configured to communicate with the instance.


**Parent Topic:**[CyberArk integration configuration](../concept/c_CyberArkIntegrationConfiguration.md)

