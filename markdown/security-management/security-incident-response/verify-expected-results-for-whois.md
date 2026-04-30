---
title: \(Optional\) Run enrichment lookup and verify expected results for Whois
description: Run the Whois integration to perform enrichment lookups on the domains returned from the Reverse Whois integration.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
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

2.  Open the record and click the **Show All Related Lists** related link.

3.  Select the **Reverse Whois Domains** tab at the bottom of the record.

    ![Domain results from the lookup.](../images/reverse-205.png)

    In the **Domains** column, the list of returned domains is displayed.

4.  In the **Observable** column, click an observable.

    On the **Child Observables** tab, the child observables are displayed. The child observables are generated only if the initial scan of the observable by the Reverse Whois application returned domains.

    ![Child observables tab with results.](../images/reverse-child-observables.png)

5.  Select the child observables you want to run the observable enrichment on, and, in the **Action on selected rows** choice list, select **Run Observable Enrichment**.

    ![Child observable selected and choice list.](../images/reverse-run-observable-enrichment.png)

    The **Run Observable Enrichment** dialog box is displayed.

6.  Move the Whois integration from **Available** to **Selected** and click **Submit**.

    ![Whois integration selected for observable enrichment.](../images/reverse-who-is-run-observable-dialog.png)

    Results are displayed on the **Observable Enrichment Results** tab of the observable record.

7.  Click the blue information icon then click **Open Record** in the dialog box that is displayed.

    ![The observable record.](../images/reverse-run-enrich-rslts.png)

    ![Raw data returned from the child observable enrichment.](../images/reverse-raw-data-enrich.png)

    More information and raw data related to the original domain lookup is displayed, such as the registration date, name of registrar, and country of origin.


If you cannot locate child observables or enrichment results, verify that the Reverse Whois integration ran successfully and returned domains. Also, refer to the work notes on the record for more information.

**Parent Topic:**[Reverse Whois integration](../concept/reversewhois-lookups.md)

**Previous topic:**[Verify expected results for Reverse Whois](verify-expected-rslts-rvrsewhois.md)

**Next topic:**[RISKIQ and WHOISIQ integration](../../secops-integration-riskiq/concept/riskiq-lookups.md)

**Related topics**  


[Install and configure Reverse Whois](install-and-config-reversewhois.md)

[Verify expected results for Reverse Whois](verify-expected-rslts-rvrsewhois.md)

