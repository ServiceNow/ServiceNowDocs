---
title: Using the Signing Tool
description: Learn how to use the Signing Tool to sign supported records in ServiceNow applications.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Standalone Signing Tool, Using Code Signing, Code Signing, Platform Security]
---

# Using the Signing Tool

Learn how to use the Signing Tool to sign supported records in ServiceNow applications.

## Before you begin

Role required: admin

To perform these steps, you must have the following:

-   A ServiceNow application that has records to be signed.
-   A private key for signing records.
-   The `signRecords.sh` script in your local environment, with execute permission.

    **Important:** The `signRecords.sh` script is included as part of the signing-tool jar file, which you must request from [ServiceNow customer support](https://support.servicenow.com/).


## Procedure

1.  In your local environment, navigate to the directory containing the `signRecords.sh` script.

2.  Use the following command format to sign your records:

    ```
    ./signRecords.sh -d [Path to the root directory of the ServiceNow Application to Sign] -f [Path to the Keystore file]
    ```

    For example:

    ```
    ./signRecords.sh -d /users/abc/ServiceNow-App-1 -f /users/abc/codesigning.p12
    ```

3.  If prompted, enter the password for the keystore.

    Press Enter if there’s no password.

4.  Review the output to confirm a successful signing.

    ```
    Sep 26, 2022 2:41:09 PM com.snc.java.commands.ACommand start
    INFO: CODESIGN: executing codesigning...
    Sep 26, 2022 2:41:09 PM com.snc.core.codesigning.CodeSignerSupplier get
    INFO: CODESIGN: signing record for documentId: 65e811327702111057416efe7c5a994f
    Sep 26, 2022 2:41:11 PM com.snc.java.commands.ACommand start
    INFO: CODESIGN: codesigning successfully completed!
    
    ```

    In the preceding output example, the Signing Tool used the provided keystore file to sign the record. You can also see that:

    -   The script found a supported record `65e811327702111057416efe7c5a994f` and signed it.
    -   In the ServiceNow-App-1 directory, two records created: `sys_certificate.xml` and `sn_kmf_record_signature.xml`.
5.  Import the updated application back into your instance by applying remote changes in Studio.

    For more information, see [Legacy - Apply remote changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/t_ApplyRemoteChanges.md).


**Parent Topic:**[Standalone signing tool](../concept/sa-code-signing-tool.md)

