---
title: Verify expected results for Reverse Whois
description: Enrichment results are displayed on the ReverseWhois Domains tab at the bottom of the security incident record. Locate the lookup results to verify that the lookup ran successfully.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reverse Whois integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Verify expected results for Reverse Whois

Enrichment results are displayed on the **ReverseWhois Domains** tab at the bottom of the security incident record. Locate the lookup results to verify that the lookup ran successfully.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  If not already open, navigate to **Security Incidents** &gt; **Incidents** &gt; **Show All Incidents** and locate the security incident you are working with.

    ![Work notes for the successful flow.](../images/flows-worknotes-start.png)

    After the application is configured and you have attached an observable, the flow launches automatically. The work notes on the security incident record display the execution and completion status of the lookup.

    ![Work notes for the successful flow completion.](../images/flows-worknotes-end.png)

2.  If you cannot verify that the lookup ran successfully, review the work notes for more information on how to proceed.

    ![Work notes for an error.](../images/flows-reversewhois-error.png)

3.  Navigate to the bottom of the security incident and click the **Show All Related Lists** related link.

    **Note:** For the filtered lookup results shown in the following figure, the configuration settings in the Reverse Whois API configuration tile were saved with **1991-06-01** entered in the **Since date** field.

    ![Domain lookup results.](../images/reverse-386-results.png)

    Enrichment results are displayed on the **ReverseWhois Domains** tab. The active domains for this observable are displayed in the **Domain** column.

4.  Click the blue information icon next to an item then click **Open record** in the dialog box that is displayed.

    ![Raw data on an observable.](../images/reverse-raw-data.png)

    The record is displayed with enrichment details, including the raw data.

5.  Navigate back to the security incident, and with the **ReverseWhois Domains** tab selected, click an observable in the **Observable** column to open a record.

    ![Child observables tab with results.](../images/reverse-child-observables.png)

    The child observables are displayed on the **Child Observables** tab on the Observable record. The child observables are generated only if the Reverse Whois application has returned domains.


If the lookup does not successfully complete, verify that the search terms you entered are supported by the integration. Review the work notes for more information.

## What to do next

For more enrichment data on the domain lookup results, you can run the Whois integration to perform enrichment lookups on the child observables returned by the Reverse Whois integration. This enrichment data on the child observables includes information on registration date, name of registrar, and country of origin.

**Parent Topic:**[Reverse Whois integration](../concept/reversewhois-lookups.md)

**Previous topic:**[Initiate lookup for Reverse Whois](manually-attch-an-obsvrble-reversewhois.md)

**Next topic:**[\(Optional\) Run enrichment lookup and verify expected results for Whois](verify-expected-results-for-whois.md)

