---
title: Configure CyberArk for SNMPv2 credentials
description: If your system uses SNMPv2, you can create a special file to map the attribute in a credential to the community string.
locale: en-US
release: zurich
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CyberArk integration configuration, CyberArk credential storage integration, External credential storage, Get started with credentials, Connections and Credentials, Access Management]
---

# Configure CyberArk for SNMPv2 credentials

If your system uses SNMPv2, you can create a special file to map the attribute in a credential to the community string.

## Before you begin

Role required: admin

Before starting this procedure, configure the MID Server to have access to the CyberArk vault.

## About this task

**Note:** If the community string appears in the password field of the CyberArk credential, it is not necessary to perform this procedure.

SNMPv2 is not natively supported in CyberArk. If your organization has created custom SNMPv2 credentials in which the community string does not appear in the password field of the credential, use this procedure to map the attribute in the credential to the community string.

## Procedure

1.  For CyberArk CCP configurations:

    1.  Open the `config.xml` file.

    2.  Set the property `snmpv2_community_property` to the attribute name.

2.  For CyberArk AIM API configurations:

    1.  In a text editor, create a file called: `CredMap.properties`.

    2.  Add the code: `SNMPv2.Community=attribute_name`

    3.  Save the file to the `/agent` directory of your MID Server installation.


## Result

On credential look-up, the MID Server attempts to find this attribute for the credential. If the attribute is not found, the MID Server then looks in the password field. If the password field is empty, the credential look-up fails.

**Parent Topic:**[CyberArk integration configuration](../concept/c_CyberArkIntegrationConfiguration.md)

