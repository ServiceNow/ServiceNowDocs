---
title: GlideEncrypter deprecation
description: Learn how to remove the use legacy GlideEncrypter calls from the scripts on your instance.
locale: en-US
release: zurich
product: Platform Encryption
classification: platform-encryption
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Prepare your instance for GlideEncrypter deprecation, Key Management Framework, Encryption]
---

# GlideEncrypter deprecation

Learn how to remove the use legacy GlideEncrypter calls from the scripts on your instance.

## GlideEncrypter availability in the Zurich release

The availability of GlideEncrypter in the Zurich release depends on whether your instance was created in or upgraded from a previous release.

-   **New instances**

    In new instances created in Zurich or later, this API turned off by default. All base system scripts have been updated and no longer use calls to this API.

-   **Upgraded instances**

    Zurich instances that have been upgraded from a previous release are still able to use the legacy GlideEncypter API, but the API has been updated to use AES256-GCM encryption via the [Key Management Framework](../../encryption/concept/encryption.md). This change replaces the use of the legacy 3DES encryption standard to comply with NIST guidelines, while allowing any scripts still using GlideEncrypter to operate.


## Enable or disable GlideEncrypter

The availability of GlideEncrypter is controlled by the **glide.security.glideencrypter.allow** system property. This system property is set to **false** by default in new Zurich instances and can’t be updated. In instances upgraded to Zurich, this property can be changed by administrators with the security\_admin role.

<table id="table_r5p_4pk_4fc"><thead><tr><th>

Value

</th><th>

Behavior

</th></tr></thead><tbody><tr><td>

true

</td><td>

When true, GlideEncypter can still be called in scripts, but uses the AES256-GCM encryption via the [Key Management Framework](../../encryption/concept/encryption.md).

</td></tr><tr><td>

false

</td><td>

When false, GlideEncrypter calls return `null`, and administrators see this error:```
Unsupported call to GlideEncrypter. Details: GlideEncrypter is deprecated and now returns null, please refer [KB1320986](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1320986)
```

</td></tr></tbody>
</table>**Parent Topic:**[Prepare your instance for GlideEncrypter deprecation](../task/check-3des.md)

