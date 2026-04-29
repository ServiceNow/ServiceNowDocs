---
title: Configure properties for customer-supplied key
description: Review the system properties for the ephemeral public wrapping key that your instance uses to unwrap customer-supplied keys.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Customer-supplied keys for Field Encryption Enterprise, Configuring Field Encryption, Field Encryption, Encryption]
---

# Configure properties for customer-supplied key

Review the system properties for the ephemeral public wrapping key that your instance uses to unwrap customer-supplied keys.

## Before you begin

Role required: sn\_kmf.admin or sn\_kmf.cryptographic manager

## About this task

You must wrap your symmetric data encryption key with a ServiceNow ephemeral public wrapping key before you can upload it to your instance.

When your key is uploaded to your instance, the instance unwraps it using the private side of the public key.

You can use system properties on your instance to define key padding, ephemeral key pair size, and a key validity period for this ephemeral public key.

<table id="table_tzk_j4k_f2c"><thead><tr><th>

System Property

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

glide.kmf.ephemeral\_key.key\_padding

</td><td>

Key padding scheme for the ephemeral key.

</td><td>

`OAEPWithSHA256AndMGF1Padding`OAEP SHA256, but SHA1 is supported.

</td></tr><tr><td>

glide.kmf.ephemeral.key\_size

</td><td>

Key size of the ephemeral key pair.

</td><td>

`4096`4096 bits, but 2048 bits are also supported.

</td></tr><tr><td>

Glide.kmf.ephemeral\_key.key\_validity\_period

</td><td>

Period for which the ephemeral key pair is valid.

</td><td>

`02:00:00`2 Hours

</td></tr></tbody>
</table>## Procedure

1.  Contact ServiceNow Support if you need to change any of these properties.

    **Note:** These system properties are not visible to admins, and do not appear in the System properties \[sys\_properties\] list. Use the table above to see their default values.


## What to do next

Once your properties are configured to your needs, proceed to [Wrap your customer-supplied key](wrap-your-customer-supplied-key.md).

**Parent Topic:**[Configure Customer-supplied keys for Field Encryption Enterprise](fe-config-customer-supplied-keys.md)

