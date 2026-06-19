---
title: Verify expected results for Shodan
description: Observables are generated automatically by a security incident and scanned by the application. Enrichment results are displayed on the Observable Enrichment Results and Network Banners tabs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/shodan-verify-expected-results.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Shodan integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Verify expected results for Shodan

Observables are generated automatically by a security incident and scanned by the application. Enrichment results are displayed on the **Observable Enrichment Results** and **Network Banners** tabs.

## Before you begin

Role required: sn\_si.analyst.

## Procedure

1.  Open the security incident you're working with and verify that the lookup has run successfully.

    Once the application is configured, the workflow launches automatically on incident creation. The execution and completion status of the lookup is displayed in the work notes in the security incident.

2.  Review the work notes for more information and how to proceed if you can't verify that the lookup ran successfully.

3.  Navigate to the bottom of the security incident and select the **Show All Related Lists** link in **Related Links**.

    Results are displayed in the **Observable Enrichment Results** and **Network Banners** tabs at the bottom of the security incident.

4.  With the **Network Banners** tab selected, select the blue information icon next to an observable.

5.  In the dialog box that is displayed, select **Open Record** to view raw data and more details.


If you don't see results under the **Observable Enrichment Results** and **Network Banners** tabs, verify that the observable is a type that is supported for lookup by the integration.

**Parent Topic:**[Shodan integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/shodan-lookups.md)

**Previous topic:**[Install and configure Shodan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/install-and-configure-shodan.md)

**Next topic:**[\(Optional\) Manually attach an observable for Shodan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/manually-attach-an-observable-shodan.md)

