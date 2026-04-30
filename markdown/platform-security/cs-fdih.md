---
title: Sign the flows, subflows, and actions in the protected instance
description: Use update sets to sign and validate the flows, subflows, and actions by enabling the Code Signing in protected and trusted instances.Sign and validate the existing flow, subflows, and actions by enabling the code signing in production and trusted instances.Sign and validate new flow, subflows, and actions by enabling the Code Signing in protected and trusted instances.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Code Signing, Code Signing, Platform Security]
---

# Sign the flows, subflows, and actions in the protected instance

Use update sets to sign and validate the flows, subflows, and actions by enabling the Code Signing in protected and trusted instances.

-   Establish Circle of Trust between the protected and trusted instances.
-   Role required: security\_admin

**Parent Topic:**[Using Code Signing](../concept/using-code-signing.md)

## Sign the existing flow, subflows, and actions

Sign and validate the existing flow, subflows, and actions by enabling the code signing in production and trusted instances.

### Before you begin

Role required: sn\_kmf.cryptographic\_manager

### Procedure

1.  In the trusted instance, sign the records in the Step Instance table.

    1.  Navigate to **System Security** &gt; **Security Jobs** &gt; **All**.

    2.  Click **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the record.|
        |Type|Type of the encryption job. Select **Mass Sign Records**.|
        |Table|Table from which the records should be signed. Select **Step Instance**.|

    4.  Click **Export Code Signing job to production**.

        Two locally signed update sets are created.

        -   One update set for the KMF signature.
        -   Another update set from the encryption job to export the code signing job.
2.  In the trusted instance, export the local update set to an XML file.

    1.  Navigate to **System Update Sets** &gt; **Local Update Sets**.

    2.  Open the update set you had created for mass signing the records.

    3.  Click the **Export to XML** related link and save the XML file.

3.  In the protected instance, import the XML file.

    1.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

    2.  Click the **Import Update Set from XML** related link to import the update set that is exported from the trusted instance.

        For more information, see  .

        The update set is committed successfully.

4.  In the protected instance, run the encryption job you had earlier created in the trusted instance.

    1.  Navigate to **System Security** &gt; **Security Jobs** &gt; **All**.

    2.  Open the encryption job you had earlier created in the trusted instance.

    3.  Click **Start** to start the job.

    A confirmation message is displayed mentioning that the records are signed.


## Sign new flow, subflows, and actions

Sign and validate new flow, subflows, and actions by enabling the Code Signing in protected and trusted instances.

### Before you begin

Role required: sn\_kmf.cryptographic\_manager

### Procedure

1.  In the trusted instance, start an update set.

2.  In the trusted instance, create the required flows, subflows, or actions, and publish them.

    The flows, subflows, or actions are added to the update set.

3.  In the trusted instance, change the state of the update set to **Complete** and click **Update**.

4.  In the trusted instance, sign the update set by creating an encryption job.

    1.  Navigate to **System Security** &gt; **Security Jobs** &gt; **All**.

    2.  Click **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the record.|
        |Type|Type of the encryption job. Select **Sign Update Set**.|
        |Table|Update set from which the records should be signed.|

    4.  Click **Submit**.

    5.  Click **Start** to sign the update set.

        -   **Summary** is updated that the records are signed.
        -   The update set is updated and includes the signature.
5.  In the trusted instance, open the signed update set record and export it to an XML.

6.  In the protected instance, import the signed update set.

    1.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

    2.  Select the **Import Update Set from XML** related link to import the update set that is exported from the trusted instance.

        For more information, see Import and commit the quick-start update set.

        The update set is committed successfully.


