---
title: Create an observable for manual WHOISIQ lookups
description: Security incident analysts use information from observable enrichment with the WHOISIQ API to learn more about the email addresses, names, and phone numbers of organizations.
locale: en-US
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

    ![Enter Observables in the navigation panel.](../image/riskiq-obs-enter.png "Enter Observables in navigation filter")

    Under the navigation panel, the Observables module is displayed.

    ![Observables module.](../image/riskiq-obsv-navfilter.png "Observables module")

2.  Click the **Observables** module to display the Observables list.

    ![Observables list](../image/riskiq-o-list.png "Observables list")

3.  Click **New** to create a new observable.

4.  On Observable form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Value**|Email address, organization name, phone number, or mailing address. For example, `test1gmail.com`|
    |**Observable type**|The field is automatically cleared.|
    |**Finding**|The field is automatically set to **Unknown**.|

    ![Enter a value in the field.](../image/riskiq-testmail-new.png "Create a new observable")

5.  Click **Submit**.

    You are returned to the Observables list. In the **Value** column, your new observable is displayed.

    **Note:** If you cannot locate your observable on the part of the list that is displayed, use the search functionality to find it.

6.  Edit the **Observable type** field to change the type from **Unknown** to **Email address** to match your observable.

    1.  In the **Observable type** column, single-click to the right of the **Unknown** text to select it.

        ![Click off of the text and in the column to select the field.](../image/riskiq-test1email-unknown.png "Select the Observable type field")

        The selected field is outlined in blue.

    2.  With the field outlined in blue, double-click anywhere inside the highlighted field to open the editor.

    3.  In the field that is displayed, enter the observable type \(`Email address`\) and click the green check mark to save the value.

        ![Enter the observable type in the editor and click the green check to save it.](../image/riskiq-test1email-edit.png "Edit the Observable type field")

        In the **Observable type** column on the list, `Email Address` is displayed for your new observable.

        ![Observable type field updated with new observable.](../image/riskiq-test1email-edited.png "Updated Observable type field")


## What to do next

If you have created and edited an observable for lookup, run the observable enrichment lookup from the Observable record with the WHOISIQ API.

**Parent Topic:**[RISKIQ and WHOISIQ integration](../concept/riskiq-lookups.md)

**Previous topic:**[Verify expected results for WHOISIQ URL lookups](verify-expctd-rslts-url-lookups-riskiq.md)

**Next topic:**[Verify expected results for manual WHOISIQ lookups](verify-expected-rslts-whoisiq.md)

