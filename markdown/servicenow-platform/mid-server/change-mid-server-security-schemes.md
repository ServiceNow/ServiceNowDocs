---
title: Change MID Server configuration file security schemes
description: A MID Server security scheme is the method the MID Server uses to protect sensitive values stored in its config.xml file \(for example, the instance password\). The scheme defines how those values are encrypted and where the encryption key is stored.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/change-mid-server-security-schemes.html
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MID Server configuration file security, Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Change MID Server configuration file security schemes

A MID Server security scheme is the method the MID Server uses to protect sensitive values stored in its `config.xml` file \(for example, the instance password\). The scheme defines how those values are encrypted and where the encryption key is stored.

## Before you begin

Role required: admin

## About this task

MID Server supports several schemes for securing sensitive data in the `config.xml` file. You can switch from the current scheme to a different scheme to meet your security requirements.

**Note:** This procedure outlines the general steps for changing security schemes. The specific changes required in the `config.xml` file vary depending on the scheme you select.

## Procedure

1.  Stop the MID Server service.

2.  Open the `config.xml` file in a text editor.

    This file is located in the **/agent** folder in your MID Server installation path.

3.  Replace each encrypted value in the `config.xml` file with its clear-text value.

    A new scheme can't reuse values encrypted by the previous scheme, so you must restore them in clear text first.

4.  Disable the previous security scheme and configure the MID Server to use the new provider.

5.  Restart the MID Server service.

    The data is re-secured or encrypted, based on the security scheme you have selected.


**Parent Topic:**[MID Server configuration file security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-encrypter-api.md)

**Related topics**  


[Encrypt MID Server configuration data with DPAPI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-data-encrypt-with-dpapi.md)

[Use CyberArk as a secure configuration provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/use-cyberark-secure-config-provider.md)

[MID Server ISecuredConfigProvider interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-secured-config-interface.md)

