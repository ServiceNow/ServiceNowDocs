---
title: Email encryption - S/MIME protocol
description: Secure/Multipurpose Internet Mail Extensions \(S/MIME\) is an end-end encryption protocol for sending digitally signed and encrypted emails that support data confidentiality, authenticity, and integrity.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email encryption - S/MIME protocol

Secure/Multipurpose Internet Mail Extensions \(S/MIME\) is an end-end encryption protocol for sending digitally signed and encrypted emails that support data confidentiality, authenticity, and integrity.

## Introduction to S/MIME

An administrator with privileges can enable and configure S/MIME. Understanding of the following is required when using the full capabilities of S/MIME:

-   Digital signatures and signature verification
-   Message encryption and decryption
-   Public key
-   Digital certificates

## Digital signatures and verification

With digital signature, S/MIME verifies the identity of the sender of the email. This verification ensures the following:

-   Message in the email is the exact message sent by the sender.
-   Message is received from the right sender and not someone pretending to be the sender.

## Message encryption and decryption

S/MIME uses encryption to protect the content of the email, which ensures that only the receiver can decrypt the content. Encryption creates coded information so that it cannot be read or understood until it is decoded and readable. Message encryption helps with the two key security factors of confidentiality and data integrity.

## Public key

S/MIME uses key pairs and asymmetric cryptography. A private key in a key pair belongs only to the sender. If the private key has been used, the owner of that key has used it.

Public key cryptography ensures secure communication between the sender and the receiver. Both have a key-pair, with one being private and the other public​.

Public keys are shared between the sender and the receiver. A public key is paired to only one private key. The corresponding public key is used to identify its paired private key and only its paired private key. A public key can be used by multiple recipients.

A key pair can be used to

-   Sign and verify a signature
-   Encrypt and decrypt the content of an email

S/MIME digital signatures and encryption require each sender and recipient to have it enabled. They also need to send or exchange public keys though digital certificates to identify each other.

For more information about key management and cryprographic module, see [Key Management Framework Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/platform-encryption/understanding-kmf.md).

## Digital certificates

Digital certificates help in delivering the public key in the key pair. A digital certificate is a digital credential that provides information about the identity, validity, and any other required information. Digital certificates are issued by a certification authority \(CA\) and are valid for only a specific period of time.

**Note:** ServiceNow® does not provide S/MIME certificates for ServiceNow mail infra users. Users should get their S/MIME certificates issued from the third party S/MIME certificate solution providers.

## S/MIME outbound emails

**Signing outbound​ mails**

The ServiceNow AI Platform uses the private key of the sender \(instance email account\)​ and the receiver uses the public key to verify signatures.

**Encrypting outbound​ mails**

The ServiceNow AI Platform uses public keys of the recipients to encrypt the emails and every recipient uses their private key to decrypt the email.

## S/MIME for inbound email

**Sign verification for inbound​ mails**

The sender uses a private key to sign the email and the ServiceNow AI Platform uses the public key of the sender to verify the signature.

**Decrypting inbound​ mails**

The sender uses the public key to encrypt the email and the ServiceNow AI Platform uses the private key to decrypt the email.

-   **[Activate S/MIME Email](../task/activate-smime-plugin.md)**  
You can activate the S/MIME Email plugin \(com.glide.email.smime\) for Notifications if you have the admin role.
-   **[Setting up S/MIME for email](smime-for-email-signing-and-encryption.md)**  
S/MIME is a protocol for sending digitally signed and encrypted emails to ensure the confidentiality, authenticity and integrity.

**Parent Topic:**[Email Administration](email-administration-landing.md)

