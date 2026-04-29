---
title: MID Server FIPS Enforced Mode
description: The MID Server supports the National Security Cloud \(NSC\) IL-5 environment, which requires all utilized cryptography to be FIPS validated. The MID server can be run in FIPS Enforced Mode, where only cryptographic algorithms which are FIPS validated are utilized.The MID server can be run in FIPS Enforced Mode, where only cryptographic algorithms which are FIPS validated are utilized.The MID server can be run in FIPS Enforced Mode, where only cryptographic algorithms that are FIPS-validated are utilized.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server FIPS Enforced Mode

The MID Server supports the National Security Cloud \(NSC\) IL-5 environment, which requires all utilized cryptography to be FIPS validated. The MID server can be run in FIPS Enforced Mode, where only cryptographic algorithms which are FIPS validated are utilized.

<table id="table_yfh_kv4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>The Federal Information Processing Standards are a group of standards compiled by the National Institute of Standards and Technology for use in computer systems. There are many FIPS publications, but for the sake of this discussion we are specifically referring to [FIPS 140-2: Security Requirements for Cryptographic Modules](https://csrc.nist.gov/publications/detail/fips/140/2/final). Cryptographic algorithms can proceed through a validation process specified by the NIST. For the purposes of our new secure cloud environment, the MID server will be utilizing algorithms that have been validated by such process.

Only MID Servers of the Rome release family or later with a JRE version of 11.0.9+11 or later can be set to run in FIPS Enforced Mode.

## FIPS Enforced Mode

The following algorithms are not available for use in these SSH functions by the MID Server in FIPS Enforced Mode.

-   **Key Exchange:**

    diffie-hellman-group1-sha1

-   **Mac:**
    -   hmac-md5
    -   hmac-md5-96

The following restrictions are now in place for SNMP for use by the MID Server in FIPS Enforced Mode.

-   SNMP v1 and v2 are completely disabled.
-   For SNMP v3, the following protocol uses are not permitted by the MID Server in FIPS Enforced Mode:
    -   auth protocol: none or MD5
    -   privacy protocol: none or DES

Other functionality that utilizes the MID Server may be impacted when run in FIPS Enforced Mode. Please refer to that functionality's specific documentation for details.

**Parent Topic:**[Securing and encrypting MID Server data](mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies](mid-security-checks.md)

[Encrypt or decrypt MID Server configuration file values](../task/mid-server-manual-encryption.md)

[MID Server configuration file security](../reference/mid-server-encrypter-api.md)

[MID Server authentication credentials and SOAP requests](mid-authentication-soap-requests.md#)

[MID Server unified key store](mid-unified-keystore.md#)

[Enable MID Server mutual authentication](../task/install-mid-mutual-auth.md)

[MID Server Azure Key Vault integration](../task/mid-azure-key-vault-integration.md#)

[MID Server command audit log](mid-audit-log.md)

[Rekey a MID Server](../task/t_RekeyAMIDServer.md)

[Add SSL certificates for the MID Server](../task/add-ssl-certificates.md#)

[MID Server SSH cryptographic algorithms](../reference/mid-ssh-algorithms.md)

[Attach a script file to a file synchronized MID Server](../task/mid-server-script-attach.md#)

[MID Server Governance](mid-timeout.md)

## Enable MID Server FIPS Enforced Mode

The MID server can be run in FIPS Enforced Mode, where only cryptographic algorithms which are FIPS validated are utilized.

### Before you begin

Role required: admin

### Procedure

1.  Deploy a new MID Server or upgrade existing MID Servers to the Rome family release or later.

2.  Shut down the MID Server.

3.  Execute the following bundled script provided to convert the MID to run in FIPS Enforced Mode:

    -   For Windows hosts: `> <MID install directory>\agent\bin\scripts\set-fips-enforced-mode.bat on`
    -   For Linux hosts: `$ <MID install directory>/agent/bin/scripts/set-fips-enforced-mode.sh on`
    Success will be logged to the console including the location of modified files and any backups generated during the conversion process. If invoked programmatically, success will be indicated by a 0 return code.

4.  Start the MID Server.


### What to do next

The mode the MID is running in can be confirmed via two methods:

1.  Check the agent logs after start-up and look for the following log line: `Running in FIPS Enforced mode`
2.  Check the ecc\_agent table on the instance and look for the value of the **FIPS Enforced** boolean column.

## Manually convert the MID Server to FIPS Enforced Mode

The MID server can be run in FIPS Enforced Mode, where only cryptographic algorithms that are FIPS-validated are utilized.

### Before you begin

Role required: admin

### About this task

To manually convert the MID Server to FIPS Enforced Mode while using an external JRE, you must perform the following steps while the MID Server is shut down:

-   Convert the JRE’s TrustStore to BCFKS type.

-   Set the JRE’s default KeyStore type to be BCFKS.

-   Set the FIPS Enforced Mode flag in the MID Server's configuration file.


### Procedure

1.  Convert the JRE’s cacerts file type to BCFKS by using the [Java Keytool](https://docs.oracle.com/javase/8/docs/technotes/tools/unix/keytool.html) with a command similar to:

    `$ keytool -importkeystore -srckeystore **&lt;source keystore path&gt;** -srcstoretype **&lt;source keystore type&gt;** -srcstorepass changeit -destkeystore **&lt;destination keystore path&gt;** -deststoretype BCFKS -deststorepass changeit -provider org.bouncycastle.jcajce.provider.BouncyCastleFipsProvider -providerpath **&lt;BouncyCastle FIPS jar path&gt;**`

    **Note:** Rome and later MID installations contain a BouncyCastle jar suitable for this purpose. It can be found at: `…/agent/lib/bc-fips.jar`

2.  The JRE’s default KeyStore type can be set in the `<JRE installation directory>\conf\security\java.security` file.

3.  In that file, find the `keystore.type` line and set its value as follows: `keystore.type=bcfks`

4.  In the MID Server's `…/agent/conf/wrapper-override.conf` file, uncomment the FIPS line and set its value to true.

    The line should read: `wrapper.java.additional.106=-Dorg.bouncycastle.fips.approved_only=true`


