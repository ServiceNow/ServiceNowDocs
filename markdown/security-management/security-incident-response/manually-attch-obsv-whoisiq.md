---
title: Create an observable for manual WHOISIQ lookups
description: Security incident analysts use information from observable enrichment with the WHOISIQ API to learn more about the email addresses, names, and phone numbers of organizations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/manually-attch-obsv-whoisiq.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [RISKIQ and WHOISIQ integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create an observable for manual WHOISIQ lookups

Security incident analysts use information from observable enrichment with the WHOISIQ API to learn more about the email addresses, names, and phone numbers of organizations.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to **All** &gt; **IoC Repository** &gt; **Observables**.

    Under the navigation panel, the Observables module is displayed.

2.  Select the **Observables** module to display the Observables list.

3.  Select **New** to create an observable.

4.  On Observable form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Value**|Email address, organization name, phone number, or mailing address. For example, `test1gmail.com`|
    |**Observable type**|The field is automatically cleared.|
    |**Finding**|The field is automatically set to **Unknown**.|

5.  Select **Submit**.

    you're returned to the Observables list. In the **Value** column, your new observable is displayed.

    **Note:** If you can't locate your observable on the part of the list that is displayed, use the search functionality to find it.

6.  Edit the **Observable type** field to change the type from **Unknown** to **Email address** to match your observable.

    1.  In the **Observable type** column, single-click to the right of the **Unknown** text to select it.

        The selected field is outlined in blue.

    2.  With the field outlined in blue, double-click anywhere inside the highlighted field to open the editor.

    3.  In the field that is displayed, enter the observable type \(`Email address`\) and select the green check mark to save the value.

        In the **Observable type** column on the list, `Email Address` is displayed for your new observable.


## What to do next

If you have created and edited an observable for lookup, run the observable enrichment lookup from the Observable record with the WHOISIQ API.

**Parent Topic:**[RISKIQ and WHOISIQ integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/riskiq-lookups.md)

**Previous topic:**[Verify expected results for WHOISIQ URL lookups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/verify-expctd-rslts-url-lookups-riskiq.md)

**Next topic:**[Verify expected results for manual WHOISIQ lookups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/verify-expected-rslts-whoisiq.md)

