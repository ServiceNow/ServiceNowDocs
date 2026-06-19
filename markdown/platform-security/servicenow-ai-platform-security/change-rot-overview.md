---
title: Change your Root of Trust configuration
description: Trust and use your own certificates instead of relying on ServiceNow build certificates \(default\) by changing to use your Root of Trust \(ROT\). ServiceNow components like script includes, business rules, etc., are signed at build time using a ServiceNow build time key \(verification certificate is the ServiceNow build certificate\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/servicenow-ai-platform-security/change-rot-overview.html
release: australia
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Code Signing, Platform Security]
---

# Change your Root of Trust configuration

Trust and use your own certificates instead of relying on ServiceNow build certificates \(default\) by changing to use your Root of Trust \(ROT\). ServiceNow components like script includes, business rules, etc., are signed at build time using a ServiceNow build time key \(verification certificate is the ServiceNow build certificate\).

## Changing the root of trust

To change the Root of Trust for these records signatures, you must follow the change of Root of Trust process.

-   Generate and migrate a new set of signatures for all provided components, using your provided certificate.
-   Disable the Root of Trust property using a scheduled job.

Learn more about these steps in [Migrate signatures to use a customer certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/migrate-sigs-customer-rot.md) and [Disable ServiceNow Root of Trust](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/disable-sn-rot.md).

## Impact on the signature generation and verification process

By default, Code Signing build certificates are trusted during the signature verification process. After making this change, your instance accepts signatures only from your own Code Signing certificate.

\[Omitted image "root-of-trust-1.png"\] Alt text: Before and after changing the ROT configuration

<table id="table_txw_zd2_pzb"><thead><tr><th>

ROT property set to false \(default\)

</th><th>

ROT property set to true

</th></tr></thead><tbody><tr><td>

-   When verifying, signatures with build certificates are trusted.
-   When signing, if you don't provide keys, the instance signing key is used as a backup key.
-   The signature REST end point **api/sn\_kmf/signature/certificates** returns ServiceNow Code Signing build certificates along with other certificates present on the instance.

</td><td>

-   When verifying, signatures with build certificates aren’t trusted.
-   When signing, if you don't provide keys, signing isn’t performed.
-   The signature REST end point **api/sn\_kmf/signature/certificates** excludes ServiceNow build certificates \(San Diego, Vancouver PKI, W PKI\).

</td></tr></tbody>
</table>## Impact on your MID Server

-   **When the ROT property is set to false**

    If you choose to leave your ROT property at its default value \(false\), there’s no impact on your MID Server.

-   **When Code Signing is enabled and the ROT property is set to true**
    -   The isTrusted\(\) API returns `false` for signatures with a build certificate.
    -   The isTrusted\(\) API returns `true` for signatures with your certificate.
    -   The REST API call for certificates excludes build certificates.
    -   You may see MID Server issues, such as `signature validation failed` messages in the logs.

