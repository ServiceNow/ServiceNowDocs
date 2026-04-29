---
title: Understanding client side Secrets Management
description: Learn how use Secrets Management to manage access to secrets and groups.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Secrets Management, Secrets Management, Platform Security]
---

# Understanding client side Secrets Management

Learn how use Secrets Management to manage access to secrets and groups.

## Terminology

Client side secrets management is designed to provide a method for managing secrets without the use of proxies, and without giving ServiceNow access to your decrypted data. To understand this process, begin with the following encryption terms.

<table id="table_qft_qw1_vvb"><thead><tr><th>

Term

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Symmetric encryption

</td><td>

Symmetric encryption uses a single same key both to encrypt and decrypt data. If data is encrypted with a symmetric key, this key is all that is needed to decrypt it.

</td></tr><tr><td>

Symmetric key

</td><td>

The symmetric key encrypts a secret, turning your clear text password into unreadable cyphertext.

</td></tr><tr><td>

Asymmetric encryption

</td><td>

Asymmetric Encryption uses two keys, one to encrypt and the other to decrypt.

</td></tr><tr><td>

Public key

</td><td>

The public key is one half of the asymmetric key pair. This key is stored on your instance, which uses the key to encrypt a symmetric key. This encrypted symmetric key can only be decrypted when paired with the private key.

</td></tr><tr><td>

Private key

</td><td>

The private key is one half of the asymmetric key pair. This key is stored in a keystore on your MID server. ServiceNow has not access to this key.

 Combined with the public key, the asymmetric key pair is used to decrypt your secrets.

</td></tr></tbody>
</table>## Client side encryption process

<table id="table_ibg_vvh_vvb"><tbody><tr><td>

A symmetric key encrypts a credential \(in this case, an admin password\), changing it from readable cleartext into encrypted cyphertext.

</td><td>

 

</td></tr><tr><td>

The symmetric key \(represented in green\) can be applied to the credential to encrypt or decrypt it.

</td><td>

 

</td></tr><tr><td>

At this point, asymmetric encryption begins using public\(yellow\) and private key\(blue\) keys.

</td><td>

 

</td></tr><tr><td>

The public key encrypts the credential along with the symmetric key. The symmetric key is now protected, so it can’t be used to decrypt the credential. Although the public key can perform this encryption, it can’t be used alone to decrypt.

</td><td>

 

</td></tr><tr><td>

After being encrypted with the public key, the private key is needed to decrypt the credential. Since the customer alone has this key, they’re the only ones who may access the encrypted credential.

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Secrets Management](exploring-secrets-management.md)

