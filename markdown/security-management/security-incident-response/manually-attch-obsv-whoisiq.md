---
title: Create an observable for manual WHOISIQ lookups
description: Security incident analysts use information from observable enrichment with the WHOISIQ API to learn more about the email addresses, names, and phone numbers of organizations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/security-management/security-incident-response/manually-attch-obsv-whoisiq.html
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [RISKIQ and WHOISIQ integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create an observable for manual WHOISIQ lookups

Security incident analysts use information from observable enrichment with the WHOISIQ API to learn more about the email addresses, names, and phone numbers of organizations.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to **All** &gt; **IoC Repository** &gt; **Observables**.

    \[Omitted image "riskiq-obs-enter.png"\] Alt text: Enter Observables in the navigation panel.

    Under the navigation panel, the Observables module is displayed.

    \[Omitted image "riskiq-obsv-navfilter.png"\] Alt text: Observables module.

2.  Click the **Observables** module to display the Observables list.

    \[Omitted image "riskiq-o-list.png"\] Alt text: Observables list

3.  Click **New** to create a new observable.

4.  On Observable form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Value**|Email address, organization name, phone number, or mailing address. For example, `test1gmail.com`|
    |**Observable type**|The field is automatically cleared.|
    |**Finding**|The field is automatically set to **Unknown**.|

    \[Omitted image "riskiq-testmail-new.png"\] Alt text: Enter a value in the field.

5.  Click **Submit**.

    You are returned to the Observables list. In the **Value** column, your new observable is displayed.

    **Note:** If you cannot locate your observable on the part of the list that is displayed, use the search functionality to find it.

6.  Edit the **Observable type** field to change the type from **Unknown** to **Email address** to match your observable.

    1.  In the **Observable type** column, single-click to the right of the **Unknown** text to select it.

        \[Omitted image "riskiq-test1email-unknown.png"\] Alt text: Click off of the text and in the column to select the field.

        The selected field is outlined in blue.

    2.  With the field outlined in blue, double-click anywhere inside the highlighted field to open the editor.

    3.  In the field that is displayed, enter the observable type \(`Email address`\) and click the green check mark to save the value.

        \[Omitted image "riskiq-test1email-edit.png"\] Alt text: Enter the observable type in the editor and click the green check to save it.

        In the **Observable type** column on the list, `Email Address` is displayed for your new observable.

        \[Omitted image "riskiq-test1email-edited.png"\] Alt text: Observable type field updated with new observable.


## What to do next

If you have created and edited an observable for lookup, run the observable enrichment lookup from the Observable record with the WHOISIQ API.

**Parent Topic:**[RISKIQ and WHOISIQ integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/security-incident-response/riskiq-lookups.md)

**Previous topic:**[Verify expected results for WHOISIQ URL lookups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/security-incident-response/verify-expctd-rslts-url-lookups-riskiq.md)

**Next topic:**[Verify expected results for manual WHOISIQ lookups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/security-incident-response/verify-expected-rslts-whoisiq.md)

