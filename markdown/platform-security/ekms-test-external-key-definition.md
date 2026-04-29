---
title: Test an external key definition
description: Test your external encryption key to use in External Key Management Service \(EKMS\).
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring External Key Management Service, External Key Management Service, Field Encryption, Encryption]
---

# Test an external key definition

Test your external encryption key to use in External Key Management Service \(EKMS\).

## Before you begin

Roles required: admin, security\_admin, and sn\_kmf.cryptographic\_manager

To test an external key definition, there must be one configured in EKMS. See [Configure an external key definition](ekms-configure-external-key-definition.md).

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **EKMS Configurations**.

2.  Select the EKMS integration.

3.  Select **Test EKMS Config**.


## Result

The following validation message displays when the external key is properly configured in EKMS: Validation passed for the configuration. You have successfully wrapped and unwrapped the test key in EKMS.

If the test fails, the validation message shows as failed indicating the operation that was unsuccessful. Go back through the configuration process to correct the issue and run the test again. See [Configure an external key definition](ekms-configure-external-key-definition.md).

**Parent Topic:**[Configuring External Key Management Service](../concept/ekms-configuring-external-key-management.md)

**Related topics**  


[Create a cryptographic module with external key wrapping](ekms-create-crypto-module.md)

[Create Encrypted Field Configurations](ekms-create-encrypted-field-config.md)

[Set up Module Access Policies](ekms-set-up-maps.md)

