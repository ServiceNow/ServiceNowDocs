---
title: Create encryption keys using the Java KeyStore keytool
description: You can use the keytool shipped with the encryption proxy distribution to create AES 128-bit and AES 256-bit encryption keys.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up a Java KeyStore keystore, Set up a keystore and encryption keys, Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Create encryption keys using the Java KeyStore keytool

You can use the keytool shipped with the encryption proxy distribution to create AES 128-bit and AES 256-bit encryption keys.

## Before you begin

Role required: admin

You must use the Java 1.8 version of the keytool utility. A copy of the utility can be found in `<proxy install dir>/java/jre/bin/keytool`.

To find out more about the keytool utility, see the [Java SE Documentation](http://docs.oracle.com/javase/6/docs/technotes/tools/windows/keytool.html).

## About this task

**Note:** The Java KeyStore requires that the alias name \(key name, key alias\) use lowercase letters and numbers.

## Procedure

1.  Change to the keystore directory, `<installation directory>/keystore/`.

2.  To create the encryption key, run one of the following commands.

    **Note:** If you choose to run these commands from a directory other than the keystore directory, that is you skipped the previous step, you must change the -keystore option to include the path from your current directory to the keystore directory. For example, if you were in the `<installation directory>\bin` directory, the option would be `-keystore ../keystore/keystore.jceks`.

<table id="choicetable_ozy_1tw_rt"><tbody><tr><td id="d149432e106">

**AES 128**

</td><td>

`keytool -genseckey -alias 128bitkey -keyalg aes -keysize 128 -keystore keystore.jceks -storetype jceks`

</td></tr><tr><td id="d149432e118">

**AES 256**

</td><td>

`keytool -genseckey -alias 256bitkey -keyalg aes -keysize 256 -keystore keystore.jceks -storetype jceks`

</td></tr></tbody>
</table>    You add the alias on the instance when you assign default keys.

    **Note:** The key password must be the same as the keystore password.


**Parent Topic:**[Set up a Java KeyStore keystore](t_JavaKeyStoreSetUp.md)

