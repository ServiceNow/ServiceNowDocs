---
title: Check role access for an encrypted column with Now Assist for Vault
description: Use the check role access for encrypted column skill to identify user roles that have access to encryption and decryption keys in your instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-12-03"
reading_time_minutes: 1
breadcrumb: [Using Now Assist for Vault, Now Assist for Vault]
---

# Check role access for an encrypted column with Now Assist for Vault

Use the check role access for encrypted column skill to identify user roles that have access to encryption and decryption keys in your instance.

## Before you begin

-   Install ServiceNow Vault. For more information, see [Configuring ServiceNow Vault](../../vault/concept/configuring-servicenow-vault.md).
-   Ensure that the check role access for encrypted column skill is active. For more information, see [Activate a Now Assist skill](https://www.servicenow.com/docs/access?context=configure-a-now-assist-skill&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Role required: sn\_vault\_console.vault\_console\_admin

## Procedure

1.  Navigate to **All** &gt; **Vault** &gt; **Vault console**.

2.  In the Ask Now Assist panel, select **Check role access for encrypted column** and specify the details.

    Example prompt: `Which roles have decryption key access to an encrypted column? Access includes read access.`


**Parent Topic:**[Using Now Assist for Vault](../concept/using-now-assist-vault.md)

