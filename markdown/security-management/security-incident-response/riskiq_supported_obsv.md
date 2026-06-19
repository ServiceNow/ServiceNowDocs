---
title: Supported observables for RISKIQ and RISKIQ WHOISIQ
description: The RISKIQ API supports automatic SSL certificate lookups on IP address, file hash, Certificate Serial Number, domain, and URL observables. URL and domain observables are enriched automatically with the WHOISIQ API. For observable enrichment on other types of observables with the WHOISIQ API, create observables and run lookups manually from the Observables table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/riskiq\_supported\_obsv.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [RISKIQ and WHOISIQ integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Supported observables for RISKIQ and RISKIQ WHOISIQ

The RISKIQ API supports automatic SSL certificate lookups on IP address, file hash, Certificate Serial Number, domain, and URL observables. URL and domain observables are enriched automatically with the WHOISIQ API. For observable enrichment on other types of observables with the WHOISIQ API, create observables and run lookups manually from the Observables table.

## Supported observables

The following table lists the type of APIs used in this integration, and the observables each API supports. The table also indicates whether a lookup occurs automatically when security incidents are created, or if the lookup is run manually from the Observables table.

<table id="table_ep4_jlq_hdb"><thead><tr><th>

API

</th><th>

Supported observables

</th><th>

Lookup \(automated or manual\)

</th></tr></thead><tbody><tr><td>

RISKIQ SSL certificate API

</td><td>

-   IP address
-   File hash \(certificate thumb print\). See the following figure for an example of a file hash.
-   Certificate Serial Number, or Serial Number. This string is a unique ID for the entity. See the following figure for an example of a certificate serial number.
-   Domain \(`www.site.com`, or `site.com`\)
-   URL

**Note:** automatic scans are run for the URL format using the `https://` protocol, for example,`https://example.com/index.html`


</td><td>

Automated lookup when incidents are created.Results are displayed on the **SSL Certificates** tab of the security incident record.

</td></tr><tr><td>

RISKIQ WHOISIQ API

</td><td>

-   Domain
-   URL

</td><td>

Automated lookup when incidents are created.Results are displayed on the **Observable Enrichment Results** tab on the security incident record.

</td></tr><tr><td>

RISKIQ WHOISIQ API

</td><td>

-   Email address
-   Organization name
-   Phone number
-   Mailing address

</td><td>

Manual lookup is run from the Observables table.Results are displayed on the **Observable Enrichment Results** tab on the Observable record.

</td></tr></tbody>
</table>**Parent Topic:**[RISKIQ and WHOISIQ integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/riskiq-lookups.md)

**Previous topic:**[RISKIQ and WHOISIQ integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/riskiq-lookups.md)

**Next topic:**[Install and configure RISKIQ and WHOISIQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/install-and-config-riskiq.md)

