---
title: \(Optional\) Run enrichment lookup and verify expected results for Whois
description: Run the Whois integration to perform enrichment lookups on the domains returned from the Reverse Whois integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/verify-expected-results-for-whois.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reverse Whois integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# \(Optional\) Run enrichment lookup and verify expected results for Whois

Run the Whois integration to perform enrichment lookups on the domains returned from the Reverse Whois integration.

## Before you begin

Verify that you have installed and configured the Reverse Whois and Whois plugins. Perform these steps only after you have run the domain lookup with the Reverse Whois plugin successfully.

Role required: sn\_si.analyst

## About this task

Results are displayed on the **Observable Enrichment Results** tab on the Observable record.

## Procedure

1.  Navigate to **All** &gt; **Security Incidents** &gt; **Incidents** &gt; **Show All Incidents** and locate the security incident you are working with that has run the domain lookup successfully.

2.  Open the record and select **Show All Related Lists** related link.

3.  Select the **Reverse Whois Domains** tab at the bottom of the record.

    In the **Domains** column, the list of returned domains is displayed.

4.  In the **Observable** column, select an observable.

    On the **Child Observables** tab, the child observables are displayed. The child observables are generated only if the initial scan of the observable by the Reverse Whois application returned domains.

5.  Select the child observables you want to run the observable enrichment on, and, in the **Action on selected rows** list, select **Run Observable Enrichment**.

    The **Run Observable Enrichment** dialog box is displayed.

6.  Move the Whois integration from **Available** to **Selected** and select **Submit**.

    Results are displayed on the **Observable Enrichment Results** tab of the observable record.

7.  Select the blue information icon then select **Open Record** in the dialog box that is displayed.

    More information and raw data related to the original domain lookup is displayed, such as the registration date, name of registrar, and country of origin.


If you can't locate child observables or enrichment results, verify that the Reverse Whois integration ran successfully and returned domains. Also, refer to the work notes on the record for more information.

**Parent Topic:**[Reverse Whois integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/reversewhois-lookups.md)

**Previous topic:**[Verify expected results for Reverse Whois](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/verify-expected-rslts-rvrsewhois.md)

**Next topic:**[RISKIQ and WHOISIQ integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/riskiq-lookups.md)

**Related topics**  


[Install and configure Reverse Whois](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/install-and-config-reversewhois.md)

[Verify expected results for Reverse Whois](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/verify-expected-rslts-rvrsewhois.md)

