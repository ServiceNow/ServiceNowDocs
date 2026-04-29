---
title: Verify expected results for manual WHOISIQ lookups
description: Run a manual lookup on an observable when it does not automatically generate a security incident. For observable enrichment lookups using the WHOISIQ API for email addresses, organization names, phone numbers, or mailing addresses, initiate the lookup manually from the Observables table.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [RISKIQ and WHOISIQ integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Verify expected results for manual WHOISIQ lookups

Run a manual lookup on an observable when it does not automatically generate a security incident. For observable enrichment lookups using the WHOISIQ API for email addresses, organization names, phone numbers, or mailing addresses, initiate the lookup manually from the Observables table.

## Before you begin

Role required: sn\_si.analyst

## About this task

Create an observable for a manual lookup using the WHOISIQ API. For more information on how to create and edit an observable, see [Create an observable for manual WHOISIQ lookups](manually-attch-obsv-whoisiq.md).

## Procedure

1.  Navigate to **All** &gt; **IoC Repository** &gt; **Observables** and locate the observable in the list you are working with.

2.  Click your observable in the **Value** column to open the record.

    ![Click the observable you want to lookup.](../image/riskiq-test1email-select.png)

3.  Click the **Run Observable Enrichment** related link to run the lookup.

    ![Run Observable Enrichment in Related Links.](../image/riskiq-new-obsv-b4-run.png)

4.  In the **Run Observable Enrichment** window, move **RiskIQ Whois** to the Selected list.

    ![Move RsikIQ Whois to Selected.](../image/riskiq-run-whois.png)

5.  Click **Submit**.

    Lookup results are displayed on the **Observable Enrichment Results** tab on the observable record.

    ![Observable Enrichment Results tab and lookup results.](../image/riskiq-test1gmail-rslts.png)


If no results are returned for the observable, a message is displayed in the **Summary** column. If you do not see results, verify the observable is supported by the API.

**Parent Topic:**[RISKIQ and WHOISIQ integration](../concept/riskiq-lookups.md)

**Previous topic:**[Create an observable for manual WHOISIQ lookups](manually-attch-obsv-whoisiq.md)

**Next topic:**[Shodan integration](../../secops-integration-shodan/concept/shodan-lookups.md)

**Related topics**  


[Supported observables for RISKIQ and RISKIQ WHOISIQ](../reference/riskiq_supported_obsv.md)

