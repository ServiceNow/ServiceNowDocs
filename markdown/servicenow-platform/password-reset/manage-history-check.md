---
title: Enable history check for password reset
description: Manage the process to perform a history check for the old used passwords when users reset their passwords. The history check ensures that they don’t reuse old passwords which can lead to significant security risk.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2024-10-22"
reading_time_minutes: 1
breadcrumb: [Credentials Store for Password Reset for Active Directory, Credential stores for Password Reset, Configure your Password Reset process, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable history check for password reset

Manage the process to perform a history check for the old used passwords when users reset their passwords. The history check ensures that they don’t reuse old passwords which can lead to significant security risk.

## Before you begin

Role required: password reset admin

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Extensions** &gt; **Credential Store types**.

2.  Select **Microsoft AD Credential Store type**.

3.  Select the **Supports history check** option.

4.  Select the credential store record, and then select the **Enforce history policy** option to enforce the history policy \(password reuse\) check.

    For more information on credential store for password reset, see [Credentials Store for Password Reset for Active Directory](../concept/credentials-store-AD.md).

5.  Select **Update**.


**Parent Topic:**[Credentials Store for Password Reset for Active Directory](../concept/credentials-store-AD.md)

