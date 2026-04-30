---
title: Verify expected results for RISKIQ SSL certificate lookups
description: When a security incident generates observables for URLs, domains, IP addresses, certificate file hashes \(SHA-1 fingerprint\), and certificate serial numbers, security incident analysts use the SSL certificate lookup results to verify sites have certificates that have been issued by a trusted public Certificate Authority \(CA\).
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [RISKIQ and WHOISIQ integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Verify expected results for RISKIQ SSL certificate lookups

When a security incident generates observables for URLs, domains, IP addresses, certificate file hashes \(SHA-1 fingerprint\), and certificate serial numbers, security incident analysts use the SSL certificate lookup results to verify sites have certificates that have been issued by a trusted public Certificate Authority \(CA\).

## Before you begin

Role required: sn\_si.analyst

## About this task

For supported observables, the ServiceNow AI Platform scans for the most recent occurrence of URLs, domains, IP addresses, certificate file hashes \(SHA-1 fingerprint\), and certificate serial numbers. These are possible outcomes from the scan:

-   **An exact match is found**

    A valid issuer of an SSL certificate is listed on the Security Incident record.

-   **No certificate results are found**

    No results are listed on the Security Incident record.

-   **An exact match is found for a self-signed, or internally generated certificate**

    Results for an internally generated SSL certificate are displayed on the Security Incident record.

-   **An exact match is not found for a primary SSL certificate**

    A lookup value returns multiple entries and a primary certificate cannot be identified. A summary message is displayed on the Security Incident record.


## Procedure

1.  To view the observables and verify lookup results, open the security incident record you are working with and locate the work notes.

    To illustrate examples for the possible lookup results for this integration, suppose that a security incident was generated with the following observables:

    -   community.servicenow.com
    -   invalidsubdomain.servicenow.com
    -   mail.dgnetworks.com
    -   servicenow.com
    |Observable \(example\)|Scan results|Description and location|
    |----------------------|------------|------------------------|
    |community.servicenow.com|Found certificate with a SHA1 hash.|An exact match is found, and a valid issuer of an SSL certificate is listed. Results for the exact match are displayed on the **SSL Certificates** tab on the security incident record.|
    |invalidsubdomain.servicenow.com|No certificates found.|A summary that indicates no certificate results were found is displayed on the **Observable Enrichment Results** tab on the security incident record.|
    |mail.dgnetworks.com|Found certificate with SHA1 hash.|An exact match is listed for a self-signed, or internally generated certificate. Results are displayed on the **SSL Certificates** tab on the security incident record.|
    |servicenow.com|Search returned 138 certificates, and a single primary certificate could not be identified.|An exact match is not found for a primary SSL certificate, because a lookup value returns multiple certificates. A summary that indicates no primary certificate was found is displayed on the **Observable Enrichment Results** tab on the security incident record.|

    After the application is configured, the flow launches automatically. The lookup status and the observables are displayed in the work notes.

2.  Verify that the lookup ran successfully.

    ![Lookup status in work notes.](../image/flows-riskiq-whois-worknotes-start.png)

    ![Lookup status execution in work notes.](../image/flows-riskiq-whois-worknotes-end.png)


If you cannot view expected results, verify that the observable is supported by the SSL certificate lookup for the integration.

-   **[RISKIQ SSL certificate lookups that return an exact match](../reference/riskiq_ssl_exact_match.md)**  
RISKIQ SSL certificate lookup results for an exact match are displayed on the **SSL Certificates** tab on the security incident record. An exact match provides a valid certificate authority name, which helps a security incident analyst determine the validity of a website.
-   **[RISKIQ SSL certificate lookups that return multiple certificates or no certificates](../reference/riskiq_ssl_no_match.md)**  
A security incident analyst can use multiple SSL certificate results to determine whether a site is part of a common, recognizable entity. No SSL certificate results may indicate sites with obscure or suspicious names have no trusted certificates. Lookup results for observables that do not return SSL certificates, or that return multiple SSL certificates, are displayed on the Observable Enrichment Results tab on the security incident record.

**Parent Topic:**[RISKIQ and WHOISIQ integration](../concept/riskiq-lookups.md)

**Previous topic:**[Install and configure RISKIQ and WHOISIQ](install-and-config-riskiq.md)

**Next topic:**[RISKIQ SSL certificate lookups that return an exact match](../reference/riskiq_ssl_exact_match.md)

**Related topics**  


[Supported observables for RISKIQ and RISKIQ WHOISIQ](../reference/riskiq_supported_obsv.md)

