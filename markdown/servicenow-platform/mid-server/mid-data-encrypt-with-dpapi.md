---
title: Encrypt MID Server configuration data with DPAPI
description: Windows Data Protection API \(DPAPI\) encrypts sensitive data from the config.xml file, based on the MID Server user account.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MID Server configuration file security, Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Encrypt MID Server configuration data with DPAPI

Windows Data Protection API \(DPAPI\) encrypts sensitive data from the **config.xml** file, based on the MID Server user account.

## Before you begin

Role required: admin

## About this task

DPAPI encryption provides another level of security for data such as credentials, IP addresses, and URLs in the MID Server **config.xml** file. The operating system performs the data encryption, rather than the MID Server. DPAPI encryption is based on the logged in user's account. When this scheme is used, the data can only be decrypted by the same user account. If the account changes, the data must be re-encrypted.

## Procedure

1.  Open the **config.xml** file in a text editor.

    This file is located in the **/agent** folder in your MID Server installation path.

2.  Enable this parameter and value:

    `<parameter name="mid.secure_encrypter" value="com.service_now.mid.services.config.WindowsDPAPIEncrypter"/>`

3.  Save the configuration file.

4.  Restart the MID Server.

    Any values in clear text in the **config.xml** file are encrypted by the operating system.

5.  Follow this procedure if you need to change the MID Server user account that is used for encryption.

    1.  Stop the MID Server service.

    2.  Open the **config.xml** file in a text editor.

        This file is located in the **/agent** folder in your MID Server installation path.

    3.  Re-enter all the encrypted values in clear text.

    4.  Make the changes to the MID Server user account in the ServiceNow® instance.

    5.  Restart the MID Server service.

        The data is re-encrypted by the operating system, based the new MID Server user account.


**Parent Topic:**[MID Server configuration file security](../reference/mid-server-encrypter-api.md)

