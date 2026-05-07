---
title: Create a system module access policy
description: Create a module access policy \(MAP\) for a matched user to encrypt attachments when inbound email processing runs as that user.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 1
breadcrumb: [Module access policies for inbound email attachment encryption, Encrypting fields and attachments, Using Field Encryption, Field Encryption, Encryption]
---

# Create a system module access policy

Create a module access policy \(MAP\) for a matched user to encrypt attachments when inbound email processing runs as that user.

## Before you begin

Role required: **security\_admin** and **sn\_kmf.crypto\_manager** \(or **sn\_kmf.admin**\)

## About this task

These instructions create a system-based MAP for the system user's role. See [Configure module access policies for Field Encryption](maps-for-fe.md) for information.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Field Encryption Experience**.

2.  Select **Access Policies** in the tile of the module configured for the target table's encryption configuration.

3.  Select **Create new**.

4.  Enter a name for your MAP in the **Policy name** field.

5.  Select **Role** in the **Type** field.

6.  In the **Target role** field, select the system user's role.

7.  Fill out the rest of the form accordingly.

    ![System Module Access Policy Example](../image/fe-system-map.png)

8.  Select **Save**.


## Result

The system MAP has been created.

**Parent Topic:**[Module access policies for inbound email attachment encryption](../concept/fe-maps-inbound-email-attachment-encryption.md)

