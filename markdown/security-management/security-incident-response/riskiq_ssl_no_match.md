---
title: RISKIQ SSL certificate lookups that return multiple certificates or no certificates
description: A security incident analyst can use multiple SSL certificate results to determine whether a site is part of a common, recognizable entity. No SSL certificate results may indicate sites with obscure or suspicious names have no trusted certificates. Lookup results for observables that do not return SSL certificates, or that return multiple SSL certificates, are displayed on the Observable Enrichment Results tab on the security incident record.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Verify expected results for RISKIQ SSL certificate lookups, RISKIQ and WHOISIQ integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# RISKIQ SSL certificate lookups that return multiple certificates or no certificates

A security incident analyst can use multiple SSL certificate results to determine whether a site is part of a common, recognizable entity. No SSL certificate results may indicate sites with obscure or suspicious names have no trusted certificates. Lookup results for observables that do not return SSL certificates, or that return multiple SSL certificates, are displayed on the Observable Enrichment Results tab on the security incident record.

## No SSL certificate results or multiple SSL certificate results

Follow the steps to view the results for observables that do not return SSL certificates, or that return multiple certificates.

1.  In the security incident record, click the **Observable Enrichment Results** tab.

    ![Observable Enrichment Results tab.](../image/riskiq-obs-enrichment-results.png "Observable Enrichment Results tab")

    The observable enrichment results for the RISKIQ and WHOISIQ lookup are displayed.

    In the **Observable** column, `servicenow.com` corresponds to the `Search returned 138 certificates` message in the **Summary** column. Similarly, `invalidsubdomain.servicenow.com` corresponds to `No certificates were found` in the **Summary**column. These summaries indicate that multiple SSL certificates were found, and that no exact matches for SSL certificates were found, respectively.

2.  In the **Observable** column, click **servicenow.com**.

    ![Multiple results for SSL certificates lookup.](../image/riskiq-sn-rcd.png "Multiple SSL certificates")

    The summary message that is displayed on the record indicates that multiple results for SSL Certificates were returned for `servicenow.com`, and a primary SSL Certificate could not be matched. This message is often returned on lookups that include common domain names, such as `servicenow.com`.

    If you require more information on a common domain, you can perform the search directly with the RISKIQ API.

3.  Navigate back to the **Observable Enrichment Results** tab, and in the **Observable** column, click **invalidsubdomain.servicenow.com**.

    ![No results for SSL Certificates lookup.](../image/riskiq-invalidsubdomain.png "No SSL Certificates")

    **Note:**

    -   If no SSL certificates are found for the current observable, then the Summary field displays the message, `No certificates were found`.
    -   If no active SSL certificates are found for the current observable, then the Summary field displays the message, `No active certificates were found`.

**Parent Topic:**[Verify expected results for RISKIQ SSL certificate lookups](../task/verify-expected-rslts-for-riskiq.md)

