---
title: Verify expected results for WHOISIQ URL lookups
description: When a security incident generates observables for URLs or domains, the WHOISIQ API performs the observable enrichment automatically upon security incident creation. The lookup results are displayed on the Observable Enrichment Results and SSL Certificates tabs on the security incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/security-incident-response/verify-expctd-rslts-url-lookups-riskiq.html
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [RISKIQ and WHOISIQ integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Verify expected results for WHOISIQ URL lookups

When a security incident generates observables for URLs or domains, the WHOISIQ API performs the observable enrichment automatically upon security incident creation. The lookup results are displayed on the **Observable Enrichment Results** and **SSL Certificates** tabs on the security incident record.

## Before you begin

**Note:** The figures in the following steps are shown with the **Tabbed forms** setting active in the System Settings.

Role required: sn\_si.analyst

## About this task

Observable enrichment results are displayed on the **Observable Enrichment Results** tab at the bottom of the security incident record. For supported observables, an SSL certificate search is also run and the results are displayed on the **SSL Certificates tab**.

## Procedure

1.  Open the security incident record you are working with and verify that the lookup has run successfully in the work notes.

    \[Omitted image "riskiq-url-wknotes.png"\] Alt text: Work notes for URL observable.

    Once the application is configured, the flow launches automatically upon incident creation. The execution and completion status of the lookup is displayed in the work notes in the Security Incident record.

2.  If you cannot verify that the lookup ran successfully, review the work notes for more information on how to proceed.

3.  On the open security incident, click the **Show All Related Lists** related link.

4.  Click the **Observable Enrichment Results** tab to select it.

5.  In the **Summary** column, click the first item, **Domain: uber.com Registrar: Markmonitor...**.

    \[Omitted image "riskiq-url-1.png"\] Alt text: Observable Enrichment Results tab and select an item in the Summary column.

    \[Omitted image "uber\_obs\_enrich\_whois.png"\] Alt text: Domain record with information.

    The record that is displayed contains information about the domain.

6.  Navigate back to the **Observable Enrichment Results** tab, and, in the **Summary** column, click the second item, **Found certificate with SHA1 hash...**.

    \[Omitted image "uber\_obs\_enrich\_cert.png"\] Alt text: SSL Certificate record with file hash.

    This record indicates that an SSL Certificate was found with a file hash.

7.  Navigate back to the security incident record and click the **SSL Certificates** tab.

    \[Omitted image "url-2.png"\] Alt text: SSL Certificates tab on URL lookup.

    The SSL Certificate results for the file hash are also displayed here.


If you cannot view expected results, review the work notes. Also, verify the observable is supported for the lookup by the integration.

**Parent Topic:**[RISKIQ and WHOISIQ integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/security-incident-response/riskiq-lookups.md)

**Previous topic:**[RISKIQ SSL certificate lookups that return multiple certificates or no certificates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/security-incident-response/riskiq_ssl_no_match.md)

**Next topic:**[Create an observable for manual WHOISIQ lookups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/security-incident-response/manually-attch-obsv-whoisiq.md)

**Related topics**  


[Supported observables for RISKIQ and RISKIQ WHOISIQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/security-incident-response/riskiq_supported_obsv.md)

