---
title: MID Server SSH cryptographic algorithms
description: The MID Server utilizes SSH clients to perform many discovery actions. During the SSH handshake, both the client and server first determine which algorithms both parties support, then client picks the highest priority algorithm. For the Host Key Algorithm, the client picks highest priority algorithm which both parties support that matches the key type.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server SSH cryptographic algorithms

The MID Server utilizes SSH clients to perform many discovery actions. During the SSH handshake, both the client and server first determine which algorithms both parties support, then client picks the highest priority algorithm. For the Host Key Algorithm, the client picks highest priority algorithm which both parties support that matches the key type.

<table id="table_kvf_3v4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>## Default supported SSH algorithms by priority

**Key Exchange Algorithm**​

1.  ecdh-sha2-nistp256
2.  ecdh-sha2-nistp384​
3.  ecdh-sha2-nistp521​
4.  diffie-hellman-group-exchange-sha256​
5.  diffie-hellman-group14-sha256​
6.  diffie-hellman-group16-sha512​
7.  diffie-hellman-group14-sha1​
8.  diffie-hellman-group1-sha1​
9.  diffie-hellman-group-exchange-sha1

**Host Key Algorithm**​ \(used for public key signature during authentication\)

1.  ssh-ed25519-cert-v01@openssh.com
2.  rsa-sha2-512-cert-v01@openssh.com
3.  rsa-sha2-256-cert-v01@openssh.com
4.  ssh-ed25519
5.  ecdsa-sha2-nistp256
6.  ecdsa-sha2-nistp384
7.  ecdsa-sha2-nistp521
8.  rsa-sha2-512
9.  rsa-sha2-256
10. ssh-rsa-cert-v01@openssh.com
11. ssh-rsa
12. ssh-dss

**Cipher Algorithm​**

1.  aes128-ctr​
2.  aes192-ctr​
3.  aes256-ctr​
4.  aes128-cbc​
5.  aes192-cbc​
6.  aes256-cbc​

**MAC Algorithm**

1.  hmac-sha2-256​
2.  hmac-sha1​
3.  hmac-sha2-512​
4.  hmac-sha1-96​
5.  hmac-md5-96​
6.  hmac-md5

​

## Customize the SSH algorithms priority list

The MID Server SSH algorithm priorities can be customized based on security needs. Each algorithm is controlled by one of the following MID Server properties.

**Note:** Glide Import on the instance uses the default algorithm list. The four MID Server properties do not affect Glide Import because it is not run on the MID server. SNCSSH is used for Glide Import on instance for SFTP and SCP.

-   Key Exchange algorithms: **mid.ssh.algorithms.kex**​

-   Host Key algorithms: **mid.ssh.algorithms.host\_key**​

-   Cipher algorithms: **mid.ssh.algorithms.cipher**​

-   MAC algorithms: **mid.ssh.algorithms.mac**​


The properties accept comma separated lists with operators. The first name in the list is highest priority, last name in list is lowest priority. Adding a comma separated list without any operators replaces the default algorithm list. The following operators are based on the OpenSSH standard syntax and modify the algorithm priority list.

-   The **+** operator appends the comma separated list of algorithms to the default algorithm list.
-   The **-** operator removes the comma separated list of algorithms from the default algorithm list.
-   The **^** operator places the comma separated list of algorithms at the front of the default algorithm list.

![The MID Server properties using the operators to customize the SSH algorithm lists.](../image/mid-ssh-properties.png)

**Parent Topic:**[Securing and encrypting MID Server data](../concept/mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies](../concept/mid-security-checks.md)

[Encrypt or decrypt MID Server configuration file values](../task/mid-server-manual-encryption.md)

[MID Server configuration file security](mid-server-encrypter-api.md)

[MID Server authentication credentials and SOAP requests](../concept/mid-authentication-soap-requests.md#)

[MID Server unified key store](../concept/mid-unified-keystore.md#)

[Enable MID Server mutual authentication](../task/install-mid-mutual-auth.md)

[MID Server Azure Key Vault integration](../task/mid-azure-key-vault-integration.md#)

[MID Server command audit log](../concept/mid-audit-log.md)

[Rekey a MID Server](../task/t_RekeyAMIDServer.md)

[Add SSL certificates for the MID Server](../task/add-ssl-certificates.md#)

[Attach a script file to a file synchronized MID Server](../task/mid-server-script-attach.md#)

[MID Server FIPS Enforced Mode](../concept/mid-fips-enforced.md#)

[MID Server Governance](../concept/mid-timeout.md)

