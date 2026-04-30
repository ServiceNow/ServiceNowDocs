---
title: Prepare your instance for GlideEncrypter deprecation
description: Use an instance scan script to find and remove GlideEncrypter API calls on your instance. Removing these calls is a necessary step in deprecating 3DES encryption on your instance.
locale: en-US
release: xanadu
product: Platform Encryption
classification: platform-encryption
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Key Management Framework, Encryption]
---

# Prepare your instance for GlideEncrypter deprecation

Use an instance scan script to find and remove GlideEncrypter API calls on your instance. Removing these calls is a necessary step in deprecating 3DES encryption on your instance.

## Before you begin

Role required: admin

The GlideEncrypter API is planned for deprecation as of the Zurich release of ServiceNow. Removing GlideEncrypter calls from your script is also a necessary step before deprecating 3DES encryption on your instance.

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Suites**.

2.  In the **Suites** list, select **GlideEncrypter to identify the records with GlideEncrypter usages**

3.  In the **Suites** record, select **GlideEncrypter to identify the records with GlideEncrypter usages** from the **Checks** related list.

    The **Column Type Check** displays. This record contains a description of the check, and information on and links regarding how to update the records found by the check.

4.  In the **Column Type Check** record, select **Test Check** to run the scan.

    During the scan execution a **Execute Test Scan**, a window displays the progress of the scan.![Scan progress window](../image/scan-progress.png)

    **Note:** This scan checks only records that have been created or modified by the customer.

5.  When the scan is complete, select **Go to Result** to view the **Scan Result** record.

    In the **Scan Result** record, the **Scan Findings** list displays a list of records on your instance that are using the **GlideEncrypter** API.

6.  Select the **Count** field on the **Scan Findings** list to navigate to a record.

7.  Modify any scripts in the record that uses the **GlideEncrypter** API.

    For details on alternatives to **GlideEncrypter**, see [Alternatives to deprecated GlideEncrypter APIs](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1320986).

    **Note:** You do not need to modify base system \(out-of-box\) records if you have not made any changes to them. These records are handled by ServiceNow.

8.  After removing **GlideEncrypter** calls from your scripts, run the scan again to ensure that there are no remaining calls to the API.

    ![Completed scan with no errors, warnings, or findings](../image/scan-progress-2.png)


## What to do next

[Deprecate GlideEncrypter usage of 3DES for password2 fields](../concept/password2-3des-deprecation.md)

**Parent Topic:**[Key Management Framework](../../encryption/concept/encryption.md)

