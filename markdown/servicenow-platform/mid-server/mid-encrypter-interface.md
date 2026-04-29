---
title: MID Server IMidServerEncrypter interface
description: Use the methods in this interface to create a custom external encrypter for the MID Server config.xml file.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [MID Server configuration file security, Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server IMidServerEncrypter interface

Use the methods in this interface to create a custom external encrypter for the MID Server **config.xml** file.

**Note:** These methods are contained in the **snc-automation-api.jar** file, located in the MID Server installation folder.

## initialize

This method initializes the encrypter with additional configuration parameters and does not return a value.

<table id="table_nsq_g2p_jbb"><tbody><tr><td>

```
void intialize(java.util.Properties properties)
        throws java.lang.Exception
```

</td></tr></tbody>
</table>|Parameter|Description|
|---------|-----------|
|properties|Initialization properties.|

<table id="table_zfw_n2p_jbb"><tbody><tr><td>

`java.lang.Exception`

</td></tr></tbody>
</table>## encrypt

This method encrypts the unencrypted data and returns a **byte\[ \]** type value.

<table id="table_sp1_dfp_jbb"><tbody><tr><td>

```
byte[] encrypt(byte[] unencryptedData)
        throws java.lang.Exception
```

</td></tr></tbody>
</table>|Parameter|Description|
|---------|-----------|
|unencryptedData|The data unencrypted.|

<table id="table_xn1_3fp_jbb"><tbody><tr><td>

Encrypted data

</td></tr></tbody>
</table><table id="table_kjt_3fp_jbb"><tbody><tr><td>

`java.lang.Exception`

</td></tr></tbody>
</table>## decrypt

This method decrypts encrypted data and returns a **byte\[ \]** type value.

<table id="table_kn1_5fp_jbb"><tbody><tr><td>

```
byte[] decrypt(byte[] encryptedData)
        throws java.lang.Exception
```

</td></tr></tbody>
</table>|Parameters|Description|
|----------|-----------|
|encryptedData|The data decrypted.|

<table id="table_k3s_bgp_jbb"><tbody><tr><td>

Decrypted data.

</td></tr></tbody>
</table><table id="table_w5r_2gp_jbb"><tbody><tr><td>

`java.lang.Exception`

</td></tr></tbody>
</table>**Parent Topic:**[MID Server configuration file security](mid-server-encrypter-api.md)

