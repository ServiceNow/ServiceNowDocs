---
title: Load required key pairs and certificates for Code Signing
description: Establish the relationship in a designated trusted instance using Code Signing. This first step loads two cryptographic keys into the trusted environment to establish a trusted source for updates to the production instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Code Signing, Platform Security]
---

# Load required key pairs and certificates for Code Signing

Establish the relationship in a designated trusted instance using Code Signing. This first step loads two cryptographic keys into the trusted environment to establish a trusted source for updates to the production instance.

## Before you begin

Roles required: security\_admin and sn\_kmf.cryptographic\_manager

## About this task

The first step in establishing the relationship is to establish the trust foundation in a designated trusted instance using Code Signing. To perform this task, you need the following.

-   You must have two 4096-bit RSA public/private key pairs to load into Code Signing cryptographic modules:

    -   One pair for the cm\_code\_signing cryptographic module
    -   One pair for the cm\_code\_attest cryptographic module
    For more information on these keys, see [Create Code Signing key pairs and certificates](../reference/create-key-pairs-and-certs.md).

    **Important:** These key pairs must be signed by a public certificate authority or signed by your organizations internal certificate authority. The certificate can't be self-signed.

-   A Public Key Cryptography Standard \#12 \(.p12\) file containing your leaf and intermediate certificates.

## Procedure

1.  Import your keys from the keystore.

    1.  Navigate to **All** &gt; **Key Management** &gt; **Cryptographic Modules** &gt; **All**.

    2.  Find and open the cryptographic module named `cm_code_signing`.

    3.  In the **Crypto Specifications** list, select the name of the crypto specification to open it.

    4.  In the **Import key from keystore** screen, select **Import key**.

2.  Repeat the first step to import the cryptographic module named `cm_code_attest`.

3.  In the **Enter Keystore Password** field, enter the challenge password you created when generating your RSA certificate.

    **Note:** The challenge password that you created is referred to here as the **keystore password**. In other parts of the process, this may be referred to as either a **import password** or **export password**. In all cases, this password is the same challenge password that you created in the previous steps.

4.  Select the **Browse** button next to **Import Keystore/Certificate**.

5.  Select a Public Key Cryptography Standard \#12 \(.p12\) file containing your distribution certificate \(mentioned in the before you begin section at the top of this doc\).

6.  Select **OK**.

    **Important:** If you’re using your own internal certificate authority, you must upload the internal certificate authority’s intermediate certificates using the process in steps 5–6.

    With a successful import of your key and certificate\(s\), a confirmation message is displayed.

    You can validate that the key and certificates are present on your instance on the X.509 Certificates \[sys\_certificate\] table. These records have a type of **Trust Store Cert**.

    You can validate your key on the Cryptographic Modules \[sys\_kmf\_crypto\_module\] table.


## What to do next

Export the certificate to production. See [Prepare Circle of Trust certificates](create-updateset-nonprod.md) for details.

**Parent Topic:**[Configuring Code Signing](../concept/config-code-signing.md)

