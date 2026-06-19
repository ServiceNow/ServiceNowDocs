---
title: Initiate the lookup for Reverse Whois
description: Initiate domain lookups using search terms in observables that you manually attach to a security incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/manually-attch-an-obsvrble-reversewhois.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reverse Whois integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Initiate the lookup for Reverse Whois

Initiate domain lookups using search terms in observables that you manually attach to a security incident record.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  If not open, navigate to **Security Incident** &gt; **Incidents** &gt; **Show All Incidents** and open the security incident you're working with.

2.  At the bottom of the record, select the **Show IoC** related link to display the Observables tab.

    **Note:** If you don't see tabs on the security incident, in the upper-right corner of the banner frame, select the **Settings** gear icon. In the **System Settings** dialog box that is displayed, select **Forms** and verify that **Tabbed forms** and **With the Form** are selected.

3.  On the Observables tab, select **New**.

4.  Fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Value|Unique search term for a domain.|
    |Observable type|This field is automatically cleared.|
    |Finding|This field is automatically set to **Unknown**.|

5.  Select **Submit**.

    You're returned to the security incident record and the flow initiates the lookup.


## What to do next

Verify the lookup results on the security incident. See [Verify expected results for Reverse Whois](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/verify-expected-rslts-rvrsewhois.md).

**Parent Topic:**[Reverse Whois integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/reversewhois-lookups.md)

**Previous topic:**[\(Optional\) Install and configure Whois](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/whois-install-and-config.md)

**Next topic:**[Verify expected results for Reverse Whois](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/verify-expected-rslts-rvrsewhois.md)

