---
title: Sign the existing REST and SOAP messages
description: Sign and validate the existing REST and SOAP messages by enabling the Code Signing in protected and trusted instances.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [REST and SOAP Signing, Using Code Signing, Code Signing, Platform Security]
---

# Sign the existing REST and SOAP messages

Sign and validate the existing REST and SOAP messages by enabling the Code Signing in protected and trusted instances.

## Before you begin

Role required: sn\_kmf.cryptographic\_manager

## Procedure

1.  In the trusted instance, configure the KMF signing job to sign the UI actions.

    1.  Navigate to KMF Signature Configuration.

    2.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Table Name|Glide table name. For example, select **UI Actions \[sys\_ui\_action\]**.|
        |KMF Signature Purpose|Purpose of signing the records. Select **ECC Queue**.|
        |Signature Generation Fields|Fields in the data source that you want to sign. If any changes are made to the values in one or more of these fields, the previously generated signature becomes invalid. Select **Name** and **Script**.|
        |Signature Generation Filter|Filter criteria that must be met to sign the records.|
        |Sign Attachment|Option to sign the attachment in the glide record.|
        |Instance Key|Option to use the instance key.|

    3.  Right-click the form header and click **Save**.

2.  In the trusted instance, sign the required records.

    1.  Navigate to **System Security** &gt; **Security Jobs** &gt; **All**.

    2.  Click **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the record.|
        |Type|Type of the encryption job. Select **Mass Sign Records**.|
        |Table|Table from which the records should be signed. Select **UI Action**.|

    4.  Click **Export Code Signing job to production**.

        Two locally signed update sets are created.

        -   One update set for the UI action configuration.
        -   Another update set from the encryption job to export the code signing job.
3.  In the trusted instance, export the local update set to an XML file.

    1.  Navigate to **System Update Sets** &gt; **Local Update Sets**.

    2.  Open the update set you had created for mass signing the records.

    3.  Click the **Export to XML** related link and save the XML file.

4.  In the protected instance, import the update sets.

    1.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

    2.  Click the **Import Update Set from XML** related link to import the update set that is exported from the trusted instance.

        For more information, see Import and commit the quick-start update set.

        The update set is committed successfully.

5.  In the protected instance, run the encryption job you had earlier created in the trusted instance by selecting **Start**.

    A confirmation message is displayed mentioning that the records are signed.


**Parent Topic:**[Sign the REST and SOAP messages in the production instance](cs-rest-soap.md)

