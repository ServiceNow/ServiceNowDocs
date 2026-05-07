---
title: External Key Management Service and instance automation
description: Understand requirements and limitations for instance automation operations when External Key Management Service is enabled.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-23"
reading_time_minutes: 3
breadcrumb: [Using External Key Management Service, External Key Management Service, Field Encryption, Encryption]
---

# External Key Management Service and instance automation

Understand requirements and limitations for instance automation operations when External Key Management Service is enabled.

When External Key Management Service \(EKMS\) is enabled on your instance, you must plan for instance automation operations such as cloning, backup and restore, copying, moving, and toggling between instances. These operations require compatible EKMS configurations between source and target instances to succeed.

You can't clone or restore externally encrypted data unless the target instance can access the same external encryption key. The preflight check validates EKMS compatibility before instance automation operations begin. If configurations are incompatible, the operation is blocked and you must follow the manual resolution steps in [KB2540187](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2540187).

## Instance automation compatibility

The following table shows which instance automation operations are supported based on your source and target instance configurations.

<table id="table_hmx_ffm_1jc"><thead><tr><th>

Source instance

</th><th>

Target instance

</th><th>

Result

</th></tr></thead><tbody><tr><td>

No EKMS

</td><td>

No EKMS

</td><td>

Supported

</td></tr><tr><td>

EKMS in use

</td><td>

Supports EKMS

</td><td>

Supported

</td></tr><tr><td>

EKMS in use

</td><td>

Older release without EKMS support

</td><td>

Supported

</td></tr><tr><td>

Older release without EKMS support

</td><td>

Supports EKMS but not configured

</td><td>

Supported

</td></tr><tr><td>

Supports EKMS

</td><td>

Older release without EKMS support

</td><td>

Supported

</td></tr><tr><td>

EKMS configured

</td><td>

EKMS with matching configuration and key wrapping strategy

</td><td>

Supported

</td></tr><tr><td>

EKMS configured

</td><td>

EKMS with compatible configuration

</td><td>

Supported

</td></tr><tr><td>

EKMS configured with key status not ACTIVE

</td><td>

Any

</td><td>

Blocked- see Key status requirements below

</td></tr><tr><td>

EKMS configured

</td><td>

EKMS with different configuration

</td><td>

Blocked- see [KB2540187](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2540187)

</td></tr><tr><td>

Internal key wrapping

</td><td>

External key wrapping

</td><td>

Blocked- see [KB2540187](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2540187)

</td></tr><tr><td>

EKMS configured

</td><td>

EKMS with different configuration or wrapping strategy

</td><td>

Blocked- see [KB2540187](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2540187)

</td></tr><tr><td>

EKMS present but not configured

</td><td>

EKMS in use

</td><td>

Blocked- see [KB2540187](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2540187)

</td></tr><tr><td>

Older release without EKMS support

</td><td>

EKMS configured

</td><td>

Blocked- see [KB2540187](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2540187)

</td></tr><tr><td>

Supports EKMS but not configured

</td><td>

EKMS configured

</td><td>

Blocked- see [KB2540187](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2540187)Activate EKMS on source first.

</td></tr><tr><td>

EKMS configured

</td><td>

EKMS with incompatible configuration

</td><td>

Blocked- see [KB2540187](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2540187)

</td></tr></tbody>
</table>## Key status requirements

Instance automation operations require that your AWS KMS key status isACTIVE. If the external key status isn'tACTIVE, cryptographic operations may fail during or after the instance automation operation.

Before performing instance automation with EKMS:

-   Verify the key status in your EKMS Configuration shows as ACTIVE.
-   Don't proceed with instance automation while the key status is disabled, pending deletion, unavailable, or deleted.
-   If the key status isn't ACTIVE, resolve the issue before attempting instance automation.

Key status issues and resolutions:

-   Disabled: Re-enable the key in AWS KMS.
-   Pending deletion: Cancel the deletion schedule in AWS, then re-enable the key if needed.
-   Unavailable: Restore EKMS connectivity by verifying credentials, region access, and endpoint availability.
-   Deleted: Contact ServiceNow Support for recovery strategy and reconfiguration planning. This is a critical and irreversible situation.

After resolving key status issues, wait for the EKMS Health Check job to update the instance status to ACTIVE, then re-run the preflight check before proceeding.

## Legacy key management support

By default, instance automation between instances using different key management architectures \(legacy and current\) isn't supported. You can enable support for legacy key management scenarios by setting the system property glide.ekms.ia.non\_bagheera\_support to true.

To enable legacy key management support:

1.  Navigate to **System Properties** &gt; **All Properties**.
2.  Search for **glide.ekms.ia.non\_bagheera\_support**.
3.  Set the value to **True**.
4.  Select **Save**.

You must have the admin role to modify system properties.

This property enables instance automation in the following scenarios:

-   The source instance uses legacy key management and the target instance uses current key management architecture.
-   Both the source and target instances use legacy key management.
-   The source instance uses current key management architecture and the target instance uses legacy key management.

Even with this property enabled, if the preflight check detects incompatible configurations, you must follow the manual resolution steps in [KB2540187](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2540187).

**Parent Topic:**[Using External Key Management Service](../concept/ekms-using-external-key-management.md)

