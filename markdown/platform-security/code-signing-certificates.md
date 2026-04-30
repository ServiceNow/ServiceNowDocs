---
title: Key Pair and Certificates
description: The Key Pair and Certificates dashboard displays details about the cryptographic keys and digital certificates used for Code Signing. It includes information such as key type, certificate issuer, expiration date, and validity status. Use this dashboard to manage code signing certificate credentials, verify their validity, and help ensure secure and trusted Code Signing operations.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Health and Status Dashboard, Code Signing, Platform Security]
---

# Key Pair and Certificates

The Key Pair and Certificates dashboard displays details about the cryptographic keys and digital certificates used for Code Signing. It includes information such as key type, certificate issuer, expiration date, and validity status. Use this dashboard to manage code signing certificate credentials, verify their validity, and help ensure secure and trusted Code Signing operations.

The Key Pair and Certificates Configuration dashboard displays the following reports:

<table id="table_w3q_t1h_cfc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Certificate Name

</td><td>

Text field

</td><td>

The unique identifier \(name\) assigned to a digital certificate used for Code Signing.

</td></tr><tr><td>

Crypto Module

</td><td>

Text field

</td><td>

The cryptographic component used to generate, store, and manage private keys for Code Signing. It ensures secure key operations and helps protect sensitive cryptographic material from unauthorized access.

</td></tr><tr><td>

Type

</td><td>

Text field

</td><td>

The classification of the cryptographic key or certificate used for Code Signing. Example:

-   ServiceNow
-   Third party

</td></tr><tr><td>

Expires

</td><td>

Text field

</td><td>

Date when the digital certificate expires and is no longer valid for use.

</td></tr><tr><td>

Status

</td><td>

Text field

</td><td>

Current validity of the digital certificate.-   **Valid**: The certificate is active and can be used for Code Signing.
-   **Expired**: The certificate has passed its expiration date and is no longer valid.
-   **Expiring Soon**: The certificate is nearing its expiration date. Use this status to take proactive steps for renewal to avoid disruptions in code signing operations.

</td></tr><tr><td>

Chain

</td><td>

Text field

</td><td>

The certificate chain, which includes the digital certificate along with the intermediate and root certificates that establish a trust path.Select **View Chain** to view the certificate chain.

</td></tr></tbody>
</table>**Parent Topic:**[Code Signing Health and Status Dashboard](code-signing-health-and-status-dashboard.md)

