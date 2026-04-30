---
title: Change MID Server configuration file security schemes
description: The MID Server provides several schemes for securing sensitive data in the config.xml file and allows you to switch between these options to suit your security requirements.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [MID Server configuration file security, Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Change MID Server configuration file security schemes

The MID Server provides several schemes for securing sensitive data in the **config.xml** file and allows you to switch between these options to suit your security requirements.

## Before you begin

Role required: admin

## Procedure

1.  Stop the MID Server service.

2.  Open the **config.xml** file in a text editor.

    This file is located in the **/agent** folder in your MID Server installation path.

3.  Re-enter all the encrypted values in clear text.

4.  Disable the previous security scheme and configure the MID Server to use the new provider.

5.  Restart the MID Server service.

    The data is re-secured or encrypted, based on the security scheme you have selected.


**Parent Topic:**[MID Server configuration file security](../reference/mid-server-encrypter-api.md)

