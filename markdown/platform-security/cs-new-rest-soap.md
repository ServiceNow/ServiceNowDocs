---
title: Sign new REST and SOAP messages
description: Sign and validate the new REST and SOAP messages from the trusted instance by enabling the Code Signing in protected and trusted instances.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [REST and SOAP Signing, Using Code Signing, Code Signing, Platform Security]
---

# Sign new REST and SOAP messages

Sign and validate the new REST and SOAP messages from the trusted instance by enabling the Code Signing in protected and trusted instances.

## Before you begin

Role required: security\_admin

## Procedure

1.  In the trusted instance, start an update set.

2.  In the trusted instance, create the required REST or SOAP messages.

    The messages are added to the update set.

3.  In the trusted instance, change the state of the update set to **Complete** and click **Update**.

4.  In the trusted instance, sign the update set by creating an encryption job.

    1.  Navigate to **System Security** &gt; **Security Jobs** &gt; **All**.

    2.  Click **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the record.|
        |Type|Type of the encryption job. Select **Sign Update Set**.|
        |Table|Update set from which the records should be signed. Select **Sign new Rest V2 update set - 1**.|

    4.  Click **Submit**.

    5.  Click **Start** to sign the update set.

        -   **Summary** is updated that the records are signed.
        -   The update set is updated and includes the signature.
5.  In the trusted instance, open the signed update set record and export it to an XML.

6.  In the protected instance, import the update set.

    1.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

    2.  Select the **Import Update Set from XML** related link to import the update set that is exported from the trusted instance.

        For more information, see Import and commit the quick-start update set.

        The update set is committed successfully.


**Parent Topic:**[Sign the REST and SOAP messages in the production instance](cs-rest-soap.md)

