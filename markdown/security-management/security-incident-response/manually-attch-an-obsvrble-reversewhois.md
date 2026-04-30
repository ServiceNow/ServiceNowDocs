---
title: Initiate the lookup for Reverse Whois
description: Initiate domain lookups using search terms in observables that you manually attach to a security incident record.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reverse Whois integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Initiate the lookup for Reverse Whois

Initiate domain lookups using search terms in observables that you manually attach to a security incident record.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  If not open, navigate to **Security Incident** &gt; **Incidents** &gt; **Show All Incidents** and open the security incident you are working with.

2.  At the bottom of the record, click the **Show IoC** related link to display the Observables tab.

    **Note:** The figures in the following steps are shown with the **Tabbed forms** setting active in the System Settings. If you do not see tabs on the security incident, in the upper-right corner of the banner frame, click the **Settings** gear icon. In the **System Settings** dialog box that is displayed, click **Forms** and verify that **Tabbed forms** and **With the Form** are selected.

    ![The Observables tab on the Security Incident Form.](../images/reverse-whois-new-observable.png)

3.  On the Observables tab, click **New**.

4.  Fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Value|Unique search term for a domain.|
    |Observable type|This field is automatically cleared.|
    |Finding|This field is automatically set to **Unknown**.|

    ![Required fields on the new observable record.](../images/reverse-observable-mitchell-new.png)

5.  Click **Submit**.

    You are returned to the security incident record and the flow initiates the lookup.


## What to do next

Verify the lookup results on the security incident. See [Verify expected results for Reverse Whois](verify-expected-rslts-rvrsewhois.md).

**Parent Topic:**[Reverse Whois integration](../concept/reversewhois-lookups.md)

**Previous topic:**[\(Optional\) Install and configure Whois](whois-install-and-config.md)

**Next topic:**[Verify expected results for Reverse Whois](verify-expected-rslts-rvrsewhois.md)

