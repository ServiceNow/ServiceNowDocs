---
title: Create Code Signing key pairs and certificates
description: Create two key pairs to signed certificates to establish trust between your production and trusted instances.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Code Signing, Code Signing, Platform Security]
---

# Create Code Signing key pairs and certificates

Create two key pairs to signed certificates to establish trust between your production and trusted instances.

To establish trust between your instances, you must create a key pair and certificate for each of the `cm_code_attest` and `cm_code_signing` cryptographic modules.

Creating key pairs and certificates is done using a cryptographic tool installed on your local device, such as the OpenSSL tool. For more information on this tool, see [https://www.openssl.org](https://www.openssl.org). If your organization uses other cryptographic tools, such as LibreSSL or GnuTLS, refer to the documentation for those products for similar steps.

## Key pair specifications

The key pairs you create must meet these requirements.

<table id="table_sdh_wzy_mzb"><tbody><tr><td>

Type

</td><td>

RSA

</td></tr><tr><td>

Key length

</td><td>

4096

</td></tr><tr><td>

Signing algorithm

</td><td>

RSASSA\_PKCS1\_V1\_5\_SHA\_512

</td></tr></tbody>
</table>## Certificate specifications

Certificates must be signed by a public certificate authority.

**Parent Topic:**[Configuring Code Signing](../concept/config-code-signing.md)

