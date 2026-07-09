---
title: FlowKMFEncrypter API
description: The FlowKMFEncrypter API provides secure encryption and decryption for ServiceNow Flow Actions, using the Key Management Framework \(KMF\) crypto operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/platform-encryption/flowkmfencrypter-api.html
release: zurich
product: Platform Encryption
classification: platform-encryption
topic_type: concept
last_updated: "2026-06-22"
reading_time_minutes: 1
keywords: [FlowKMFEncrypter, encryption, decryption, Flow Actions, Key Management Framework, KMF, Flow Engine, Module Access Policy, MAP, encrypt, decrypt]
breadcrumb: [Key Management Framework, Encryption]
---

# FlowKMFEncrypter API

The FlowKMFEncrypter API provides secure encryption and decryption for ServiceNow Flow Actions, using the Key Management Framework \(KMF\) crypto operations.

FlowKMFEncrypter is a ServiceNow Script Include that provides secure encryption and decryption capabilities for Flow Actions using the Key Management Framework \(KMF\) crypto APIs. This API replaces the deprecated GlideEncrypter and work with Flow Engine while adhering to Module Access Policy \(MAP\) requirements.

**Note:** FlowKMFEncrypter works only in Flow Engine use cases. It does not work in script-layer applications.

## How it works

The FlowKMFEncrypter API uses the AES algorithm with symmetric key wrapping and unwrapping operations. The Flow Engine Crypto Module supplies the encryption key. This approach is used to securely handle sensitive data, such as credentials and passwords, within Flow Actions.

## FlowKMFEncrypter\(\) - constructor

Creates a new instance of the FlowKMFEncrypter class. The constructor initializes the encrypter with the necessary KMF crypto operations configuration.

-   **Syntax**

    ```
    new FlowKMFEncrypter()
    ```

-   **Parameters**

    None


## encrypt\(input\)

Encrypts plaintext data using AES symmetric encryption.

-   **Syntax**

    ```
    encrypt(input: String): String
    ```

-   **Parameters**

    |Name|Type|Description|
    |----|----|-----------|
    |input|String|The plaintext string to encrypt.|

-   **Returns**

    |Type|Description|
    |----|-----------|
    |String|An encrypted string in KMF-compatible format that can be securely stored and later decrypted.|


```
var encrypter = new FlowKMFEncrypter();
var plainString = "mySecurePassword123";
var encryptedString = encrypter.encrypt(plainString);
```

## decrypt\(input\)

Decrypts encrypted data back to plaintext using AES symmetric decryption.

-   **Syntax**

    ```
    decrypt(input: String): String
    ```

-   **Parameters**

    |Name|Type|Description|
    |----|----|-----------|
    |input|String|The encrypted string in KMF-compatible format to decrypt.|

-   **Returns**

    |Type|Description|
    |----|-----------|
    |String|The decrypted plaintext string.|


```
var encrypter = new FlowKMFEncrypter();
var encryptedString = "<encrypted value>";
var decryptedString = encrypter.decrypt(encryptedString);
```

-   **[FlowKMFEncrypter in a Flow Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/platform-encryption/allow-flowkmfencrypter-restricted-caller-access.md)**  
Resolve the "undefined is not a function" error that occurs when a Flow Action calls the FlowKMFEncrypter API, by allowing the operation in the Restricted Caller Access Privilege record.

**Parent Topic:**[Key Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/encryption.md)

