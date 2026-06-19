---
title: Change a field or attachment's encryption type
description: You can change a field or attachment's encryption type by selecting a new encryption type in the existing encryption configuration record. A specific table and field combination can only have one active configuration at a time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/edge-encryption/t\_ChangeAFieldsEncryptionType.html
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Change a field or attachment's encryption type

You can change a field or attachment's encryption type by selecting a new encryption type in the existing encryption configuration record. A specific table and field combination can only have one active configuration at a time.

## Before you begin

Role required: security\_admin

## Procedure

1.  Navigate to **Edge Encryption Configuration** &gt; **Encryption Configurations** &gt; **All**.

    The **Edge Encryption Configurations** list is shown.

2.  Open the record for the encryption configuration to be changed.

3.  Click the **Encryption type** dropdown and select a new encryption type.

    **Note:** For attachments, only Standard AES128 and Standard AES256 are allowed.

4.  If needed, run an [encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_ConfigureCloudEdge.md) or [attachment encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_EncryptingAttachments.md) job.

    It is not necessary to run an encryption job. If you do not run an encryption job, the field or attachment is encrypted using the new encryption type the next time the field or attachment is changed.


**Parent Topic:**[Configuring Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/edge-config.md)

