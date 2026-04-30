---
title: Edge Encryption limitations
description: Edge Encryption impacts system functions. Carefully evaluate the impact of encrypting a field.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Planning for Edge Encryption, Edge Encryption, Encryption]
---

# Edge Encryption limitations

Edge Encryption impacts system functions. Carefully evaluate the impact of encrypting a field.

## Field type restrictions

You can encrypt only the following field types:

-   Date
-   Email
-   Date/Time
-   HTML
-   IP Address
-   Journal
-   Journal Input
-   Multi-line text
-   Single-line text
-   String
-   URL

You cannot encrypt the following field types:

-   Choice fields
-   Virtual fields
-   Fields in system tables, except for certain fields in sys\_user
-   System fields in tables
-   Number fields or fields associated with an auto-numbering scheme
-   Any other field type not listed above

Additional restrictions:

-   When a Journal field is encrypted, the **Post** button is inactive, even if there are multiple Journal fields and only one of those fields is encrypted.
-   Encrypted fields aren’t available in **Go to** and header filter boxes.
-   When encrypting fields used as an index, you can use only order-preserving and equality-preserving encryption types. Indexed fields can’t be encrypted using the standard encryption type.

For more information, see [Field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Filtering and searching restrictions

-   **Standard encryption**

    When you select a String, Date, Date/Time, or URL field with a standard encrypted field configuration as the left operand in a filter, no filtering options are available.

-   **Equality-preserving encryption**

    When you select a String, Date, Date/Time, or URL field with an equality-preserving encrypted field configuration as the left operand in a filter, the following operators are available:

    -   **is**
    -   **is not**
    -   **is empty**
    -   **is not empty**
-   **Order-preserving encryption**

    When you select a String field with an order-preserving encrypted field configuration as the left operand in a filter, the following operators are available, in addition to **is**, **is not**, **is empty**, and **is not empty**:

    -   **greater than**
    -   **less than**
    When you select a Date or Date/Time field with an order-preserving encrypted field configuration as the left operand in a filter, the following operators are available, in addition to **is**, **is not**, **is empty**, and **is not empty**:

    -   **after**
    -   **before**
    -   **after or on**
    -   **before or on**
-   **Date and Date/Time pickers**

    For Date fields, use the date picker to specify the date: ![Date picker](../../encryption/image/date-picker.png)

    For Date/Time fields, use the date and time picker to specify the date and time:![Date/Time picker](../../encryption/image/date-time-picker.png)

-   **List condition filters**

    The **Show Matching** and **Filter Out** options are supported in lists. Only exact matches are returned or filtered out.

    **Note:** Adding encrypted fields in condition filters is supported in scripts such as UI policies and business rules.


## Configuration restrictions

Restrictions and behavior of encryption configurations:

-   After you add a field to the Edge Encryption Configuration table, you can’t delete the configuration record. If you no longer want a field to be encrypted, deactivate the record in the Edge Encryption Configuration table and schedule an encryption job to decrypt the data.
-   If a field in a parent table is marked to be encrypted, the field is also encrypted in all inherited tables. For example, if the **Short description** field in the Task table is encrypted, then the contents of the **Short description** field in the Incident table are encrypted.
-   If a field inherited from a parent table is marked to be encrypted, the field in the parent table can’t be encrypted. For example, if the **Short description** in the Incident table is marked to be encrypted, then the **Short description** in the Task table can’t be encrypted. In this example, you can encrypt the **Short description** in the Problem table.
-   When a field with an encryption configuration defined is exported to any format, the output includes encrypted values even when exported through the proxy server.
-   You can’t import data to a field with an encryption configuration defined.
-   You can’t encrypt inherited Date and Date/Time fields. Date or Date/Time fields inherited from a parent table aren’t listed on the **Column** field drop-down list, and you can’t create Date or Date/Time encryption configurations for those fields.
-   You can encrypt a String or URL field only from a parent table or a child table, but not both.

## Instance restrictions

Impact of using Edge Encryption on the instance:

-   Back-end logic can’t process encrypted data. When the instance contains encrypted data, any business rule, back-end script, or back-end feature that relies on evaluating the data in the encrypted field doesn’t run correctly.

    **Note:** Data encrypted with equality-preserving or order-preserving encryption still passes equivalence checks when compared against an identical encrypted value.

-   Since email processing goes from the mail systems straight to the instance and can’t pass through the Edge proxy, data sent in or out via email can’t be encrypted or decrypted by the Edge proxy.
    -   Data and attachments in inbound emails aren’t encrypted.
    -   Data and attachments in outbound emails remain encrypted and can’t be decrypted.
-   Scripts run on the server can’t change encrypted data.
-   Global search isn’t supported. Because global search attempts to search both encrypted and clear text data, the results may not be as expected.
-   Encrypted data can’t be copied and pasted into a record where the field isn’t encrypted.
-   Depending on the type of encryption selected, the user interface functionality for the encrypted fields is reduced. For example, being able to compare, group by, sort, and search may be impacted. Generally, the stronger the encryption selected, the more functionality is reduced.
-   Except for Java KeyStore, SafeNet, and Unbound Technology, no third-party software or hardware encryption key management is supported.
-   Although multiple proxy servers connected to a single instance are supported, encryption proxy cluster management and monitoring aren’t available. Each proxy must be managed separately.
-   System configurations such as workload and the number of encrypted fields can impact the performance of encrypted fields.
-   The Edge Encryption proxy server can only connect to a single instance.
-   If your instance uses an Oracle database and the String field you’re marking to be encrypted is greater than 2925 characters, that field can’t be sorted even when order preserving encryption is selected.
-   If your instance uses an Oracle database, Unicode AL32UTF8 is the only supported character set.
-   Encrypted data can’t be used in reports.
-   Edge Encryption can’t be used with Data Archiving.
-   Edge Encryption proxies cannot encrypt requests that use the batch REST request API. If you are using Edge Encryption proxies, disable REST batching by setting the `glide.uxf.disable_rest_batching` system property to true.

**Parent Topic:**[Planning for Edge Encryption](../concept/c_EdgeEncryptionPlanning.md)

