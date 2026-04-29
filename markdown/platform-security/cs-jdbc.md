---
title: Sign the JDBC data source records in the protected instance
description: Use update sets to sign and validate the JDBC data sources by enabling the code signing in protected and trusted instances.Use update sets to bring mass signing jobs to the protected instance.Use update sets to bring the signed update set to the protected instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Code Signing, Code Signing, Platform Security]
---

# Sign the JDBC data source records in the protected instance

Use update sets to sign and validate the JDBC data sources by enabling the code signing in protected and trusted instances.

-   Establish Circle of Trust between the protected and trusted instances.
-   Role required: security\_admin

**Note:**

-   MID Server doesn't handle the file data sources and hence, these data sources are not code signed.
-   LDAP data sources can't be code signed.

**Parent Topic:**[Using Code Signing](using-code-signing.md)

## Sign existing data sources of the JDBC type

Use update sets to bring mass signing jobs to the protected instance.

### Before you begin

Role required: security\_admin

### Procedure

1.  In the trusted instance, configure the KMF signing job to sign the data sources.

    1.  Navigate to **System Security** &gt; **Security Jobs** &gt; **All**.

    2.  Click **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the record.|
        |Type|Type of the encryption job. Select **Mass Sign Records**.|
        |Table|Table from which the records should be signed. Select **Data Source**.|

    4.  Click **Export Code Signing job to production**.

        A confirmation message is displayed that the update set is signed.

    5.  Export the generated update set to an XML file.

2.  In the protected instance, import and commit the update set to retrieve the mass signed jobs from trusted instance.

    1.  Navigate to **System Security** &gt; **Security Jobs** &gt; **All**.

    2.  Open the update set exported from the trusted instance.

    3.  Click **Start**.

        A confirmation message is displayed that the records are signed.


## Sign new data sources of the JDBC type

Use update sets to bring the signed update set to the protected instance.

### Before you begin

Role required: sn\_kmf.cryptographic\_manager

### Procedure

1.  In the trusted instance, start an update set.

    ![Start an update set.](../image/start-an-updtset.png)

2.  In the trusted instance, create the required data sources.

    ![Create a JDBC source.](../image/create-jdbc-ds.png)

    The data sources are added to the update set.

3.  In the trusted instance, change the state of the update set to **Complete** and click **Update**.

    ![Mark the update set as Complete.](../image/complete-updtset.png)

4.  In the trusted instance, sign the update set by creating an encryption job.

    1.  Navigate to **System Security** &gt; **Security Jobs** &gt; **All**.

    2.  Click **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the record.|
        |Type|Type of the encryption job. Select **Sign Update Set**.|
        |Table|Update set from which the records should be signed.|

        ![](../image/jdbc-sign-updtset-new.png)

    4.  Click **Submit**.

    5.  Click **Start** to sign the update set.

        ![Signed update set.](../image/updated-updtset.png)

        -   **Summary** is updated that the records are signed.
        -   The update set is updated and includes the signature.
5.  In the trusted instance, open the signed update set record and export it to an XML.

6.  In the protected instance, import the signed update set.

    1.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

    2.  Click the **Import Update Set from XML** related link to import the update set that is exported from the trusted instance.

        For more information, see Import and commit the quick-start update set.

        The update set is committed successfully.


