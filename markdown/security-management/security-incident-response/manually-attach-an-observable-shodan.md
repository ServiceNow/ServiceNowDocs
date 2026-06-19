---
title: \(Optional\) Manually attach an observable for Shodan
description: You can manually attach observables to a security incident. You manually attach observables when you want to perform threat lookups on observables that are not attached to a security incident on the initial event trigger. Also, you might perform this task when you want more information about a related observable.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/manually-attach-an-observable-shodan.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Shodan integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# \(Optional\) Manually attach an observable for Shodan

You can manually attach observables to a security incident. You manually attach observables when you want to perform threat lookups on observables that are not attached to a security incident on the initial event trigger. Also, you might perform this task when you want more information about a related observable.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents** and open a security incident to which you want to attach the observable.

2.  At the bottom of the record, select **Show IoC**link in **Related Links**.

3.  On the **Observables** tab, select **New**.

    The Observable form is displayed.

4.  In the **Value** field, enter an observable \(IP address or URL\).

5.  Select the search icon and from the **Observable Type Categories** dialog box, select the desired observable type in the list to populate the field.

6.  Select **Submit**.

    The workflow launches and checks for the new observable. The execution and completion status is displayed in the work notes section on the security incident record.

7.  Navigate to your security incident and review the work notes.

8.  At the bottom of the record, select the **Show All Related Lists** related link.

9.  Select the **Observable Enrichment Results** or **Network Banners** tabs for results, and select the blue information icon next to an observable for more information on a specific item.

10. In the dialog that is displayed, select **Open Record** to view raw data and more details.

11. Select the blue settings icon near the search icon to personalize column output and order.

12. In the **Personalize List Columns**, select available settings, move them to the **Selected** column, and select **OK**.


Review the **Work notes** for more information and how to proceed if you can't verify that the lookup ran successfully.

**Parent Topic:**[Shodan integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/shodan-lookups.md)

**Previous topic:**[Verify expected results for Shodan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/shodan-verify-expected-results.md)

**Next topic:**[Secureworks CTP Ticket Ingestion Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/secureworks-ctp-about.md)

