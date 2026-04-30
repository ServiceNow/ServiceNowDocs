---
title: Install the application and configure a source for the integration
description: Install and configure the application from ServiceNow Store on your ServiceNow AI Platform instance.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [FireEye Endpoint Security integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install the application and configure a source for the integration

Install and configure the application from ServiceNow Store on your ServiceNow AI Platform instance.

## Before you begin

Role required: NowPlatform administrator \(admin\)

**Note:** An active MID Server is mandatory to configure a source.

Download the Security Incident Response integration with FireEye HX application from the ServiceNow Store and install.

After you have successfully installed the application, follow the below steps to configure it:

## Procedure

1.  Navigate to **Integrations** &gt; **Integration Configurations**.

2.  Select the **Integration Configurations** module to display the available integrations, and locate the **FireEye** tile.

    ![FireEye HX Integration tile highlighted](../image/fireeye-tile.png)

3.  Click **Configure** on the FireEye tile.

4.  Provide the following details to set up the FireEye integration:

    |Field|Description|
    |-----|-----------|
    |Name|Name of the FireEye configuration. This name is used to identify the source and the associated credentials and configuration. This name help you distinguish the credentials and accounts and identify each source to avoid conflicts with profiles.|
    |API URL|Base URL hosting the FireEye API.|
    |User Name|Enter the username of the FireEye account.|
    |Password|Enter the password of the FireEye account.|
    |Mid Application|MID Application that is set up in your environment. Mid server is required to process zip files for some of the enrichment capabilities. By default, it will be ALL. Users should provide valid application name manually.|
    |On Premises Deployment|Default is disabled. If you are using the cloud-based version of FireEye, verify that the check box is cleared.|

    ![FireEye HX Integration Configuration](../image/fireeye-configuration.png)

5.  Click **Submit**.

    The FireEye Configurations list is displayed with your new configuration record. You have completed the configuration for a FireEye server. If you cannot connect to the FireEye, or your credentials are incorrect, a validation error message is displayed as shown in the following figure. Verify that your credentials are correct and try again.

    ![FireEye configuration validation resulted in an error](../image/fireeye-validation.png)


