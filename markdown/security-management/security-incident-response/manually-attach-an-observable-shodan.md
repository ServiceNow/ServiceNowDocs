---
title: \(Optional\) Manually attach an observable for Shodan
description: You can manually attach observables to a security incident. You manually attach observables when you want to perform threat lookups on observables that are not attached to a security incident on the initial event trigger. Also, you might perform this task when you want more information about a related observable.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Shodan integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# \(Optional\) Manually attach an observable for Shodan

You can manually attach observables to a security incident. You manually attach observables when you want to perform threat lookups on observables that are not attached to a security incident on the initial event trigger. Also, you might perform this task when you want more information about a related observable.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents** and open a security incident to which you want to attach the observable.

2.  At the bottom of the record, click the **Show IoC**link in **Related Links**.

    ![Observables tab.](../image/shodan-incident.png)

3.  On the **Observables** tab, click **New**.

    The Observable form is displayed.

4.  In the **Value** field, enter an observable \(IP address or URL\).

5.  Click the search icon and from the **Observable Type Categories** dialog box, click the desired observable type in the list to populate the field.

    ![Observables Type Categories list.](../image/shodan-observable.png)

6.  Click **Submit**.

    The workflow launches and checks for the new observable. The execution and completion status is displayed in the work notes section on the security incident record.

7.  Navigate to your security incident and review the work notes.

    ![Look up status in work notes.](../image/shodan-activities.png)

8.  At the bottom of the record, click the **Show All Related Lists** related link.

9.  Click the **Observable Enrichment Results** or **Network Banners** tabs for results, and click the blue information icon next to an observable for more information on a specific item.

    ![Look up results on security form.](../image/shodan-enrichment-results.png)

10. In the dialog that is displayed, click **Open Record** to view raw data and more details.

11. Click the blue settings icon near the search icon to personalize column output and order.

12. In the **Personalize List Columns**, select available settings, move them to the **Selected** column, and click **OK**.


Review the **Work notes** for more information and how to proceed if you cannot verify that the lookup ran successfully.

**Parent Topic:**[Shodan integration](../concept/shodan-lookups.md)

**Previous topic:**[Verify expected results](shodan-verify-expected-results.md)

**Next topic:**[Secureworks CTP Ticket Ingestion Integration](../../secops-integration-sir/secops-integration-secureworks-ticket/concept/secureworks-ctp-about.md)

