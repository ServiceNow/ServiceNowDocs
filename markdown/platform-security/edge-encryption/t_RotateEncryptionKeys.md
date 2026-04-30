---
title: Configure encryption keys on the instance
description: Edge Encryption provides the tools to manage encryption keys without taking the proxy offline.
locale: en-US
release: yokohama
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Configure encryption keys on the instance

Edge Encryption provides the tools to manage encryption keys without taking the proxy offline.

## Before you begin

Role required: security\_admin

Before setting up new encryption keys on the instance:

1.  Create the encryption key.
2.  Make the new key available to all encryption proxies. Either copy the file or Java KeyStore file to each proxy, or ensure that each proxy has access to the Java KeyStore or Enterprise Key Management \(EKM\) device.

## About this task

Key aliases must be unique. Each key alias must have the same key size and type on each proxy, or the key cannot be assigned as the default.

## Procedure

1.  Navigate to **All** &gt; **Edge Encryption Configuration** &gt; **Encryption Key Configuration** &gt; **Set Up Keys**.

2.  On the Add New Keys section of the form, complete the following steps to add a new key.

    **Important:** If using SafeNet versioned keys, an additional column appears for the **Key version**. The **Key version** cannot be edited. Click the **Retrieve latest key versions** link in the Related Links to retrieve the latest version of each key from the Edge proxy.

    Rows in the list with an **X** in the left column can be deleted. Keys that have been used as the default or that have a **Status** of **Available** cannot be deleted.

    1.  Double-click in the row that says **Insert a new row.**.

    2.  In the edit box, enter a name for the key, then click the check mark.

        Key aliases are lowercase letters and numbers. Capital letters are changed to lowercase letters when you click **Update**. Key aliases must be unique.

        **Note:** If using Unbound technology keys, add the encryption key alias. The encryption key alias is the file name of the wrapped encryption key added to the `<proxy-installation-directory>/keys` directory. For example, if the file in the directory is named `myunboundkey`, add this name to the **Key alias** field.

    3.  In the same row, double-click in the **Key size** column.

    4.  In the select box, select a key size, either **128 bits** or **256 bits**, then click the check mark.

    5.  In the same row, double-click in the **Type** column.

    6.  In the select box, select a key type, either **File**, **Keystore**, **SafeNet**, or **Unbound**, then click the check mark.

    7.  When you are done adding keys, click **Next Step**.

        You must specify an alias, key size, and key type for each key before moving on.

3.  On the Keys Status section of the form, check the **State** of the key and ensure that it is **Available**.

4.  When the key is **Available**, click **Next Step**.

    This might take a few minutes.

    **Note:** If using SafeNet versioned keys, an additional column appears for the **Key version**. The **Key version** cannot be edited.

    The instance tracks the status of every encryption key available to any proxy. When a key is available on all proxies, its state becomes **Available**. If the state does not change after a few minutes, check to ensure that the key is available on all proxies. If the state remains **Unavailable**, one or more of the proxies does not have the key.

    |Status|Description|
    |------|-----------|
    |Available|All online proxies have the key.|
    |Unavailable|This is a new key and the proxies have not yet loaded the key, or at least one proxy failed to load the key.|

5.  On the Change Default Keys section of the form, do one of the following:

    -   Type in the key alias.
    -   Click the magnifying glass icon and select an alias.
    **Note:** If using SafeNet versioned keys, an additional field appears for the **Key version**. The **Key version** is grayed out and cannot be edited. Choose only the most recent key version. If you choose an earlier version, the following message appears when you click **Update** or **Next Step**.

    ```
    One of the default keys chosen is not the latest version available for the key. Please use the latest version.
    ```

    If the default keys are not the latest versions of the SafeNet keys, an **Update default keys to latest version** link appears in the Related Links. Click the link to update the default keys to use the latest version.

6.  On the Schedule Key Rotation section of the form, schedule a mass key rotation job or single key rotation job to encrypt existing data using the new encryption key.

    If you do not run a mass key rotation job or single key rotation job, existing data remains encrypted with the old key until the data is accessed again.


**Parent Topic:**[Install the Edge Encryption proxy server using the command line installer](manual-proxy-install.md)

**Previous topic:**[Create an encryption key stored in a file](t_CreateAFileStoreKeyStore.md)

**Next topic:**[Configure additional properties in the Edge Encryption properties file](set-props.md)

