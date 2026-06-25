---
title: Verify expected results for manual WHOISIQ lookups
description: Run a manual lookup on an observable when it does not automatically generate a security incident. For observable enrichment lookups using the WHOISIQ API for email addresses, organization names, phone numbers, or mailing addresses, initiate the lookup manually from the Observables table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/verify-expected-rslts-whoisiq.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [RISKIQ and WHOISIQ integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Verify expected results for manual WHOISIQ lookups

Run a manual lookup on an observable when it does not automatically generate a security incident. For observable enrichment lookups using the WHOISIQ API for email addresses, organization names, phone numbers, or mailing addresses, initiate the lookup manually from the Observables table.

## Before you begin

Role required: sn\_si.analyst

## About this task

Create an observable for a manual lookup using the WHOISIQ API. For more information on how to create and edit an observable, see [Create an observable for manual WHOISIQ lookups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/manually-attch-obsv-whoisiq.md).

## Procedure

1.  Navigate to **All** &gt; **IoC Repository** &gt; **Observables** and locate the observable in the list you're working with.

2.  Select your observable in the **Value** column to open the record.

3.  Select the **Run Observable Enrichment** related link to run the lookup.

4.  In the **Run Observable Enrichment** window, move **RiskIQ Whois** to the Selected list.

5.  Select **Submit**.

    Lookup results are displayed on the **Observable Enrichment Results** tab on the observable record.


If no results are returned for the observable, a message is displayed in the **Summary** column. If you don't see results, verify the observable is supported by the API.

**Parent Topic:**[RISKIQ and WHOISIQ integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/riskiq-lookups.md)

**Previous topic:**[Create an observable for manual WHOISIQ lookups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/manually-attch-obsv-whoisiq.md)

**Next topic:**[Shodan integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/shodan-lookups.md)

**Related topics**  


[Supported observables for RISKIQ and RISKIQ WHOISIQ](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/riskiq_supported_obsv.md)

