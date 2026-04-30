---
title: Use CyberArk as a secure configuration provider
description: You can use a CyberArk vault to secure any sensitive data from the MID Server config.xml file.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [MID Server configuration file security, Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Use CyberArk as a secure configuration provider

You can use a CyberArk vault to secure any sensitive data from the MID Server **config.xml** file.

## Before you begin

Role required: admin

Before configuring CyberArk as secured config provider, make sure that **JavaPasswordSDK.jar** is available in the `<mid_installation_folder>/agent/extlib` folder.

## About this task

CyberArk is commonly used to secure credentials in its external vault. However, a MID Server parameter in the **config.xml** file enables you to store other types of data in CyberArk.

## Procedure

1.  Open the **config.xml** file in a text editor.

    This file is located in the **/agent** folder in your MID Server installation path.

2.  Enable this parameter and value:

    `<parameter name="mid.secure_config.provider" value="com.service_now.mid.services.config.CyberArkSecuredConfigProvider"/>`

3.  Configure specific data to secure in the CyberArk vault.

    Use the following example as a guide.

    1.  Secure the MID Server credentials by setting this parameter to match the **ID** and **Type** for that data in your [CyberArk integration configuration](https://www.servicenow.com/docs/access?context=c_CyberArkIntegrationConfiguration&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

        ```
        <parameter name="mid.instance.username" secure="true" value="cyberark: id=<CyberArk ID>, type=<CyberArk type>"/>
        <parameter name="mid.instance.password" secure="true" value="cyberark: id=<CyberArk ID>, type=<CyberArk type>"/>
        ```

    2.  Secure the URL of the instance by setting this parameter to match the **ID** and **Type** for that data in your CyberArk configuration.

        `<parameter name="url" secure="true" value="cyberark: id=<CyberArk ID>, type=<CyberArk type>"/>`

4.  Save the configuration file.

5.  Restart the MID Server.


**Parent Topic:**[MID Server configuration file security](../reference/mid-server-encrypter-api.md)

