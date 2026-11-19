---
title: \(Optional\) Manually attach an observable for PhishTank
description: You can manually attach observables to a security incident. You manually attach observables when you want to perform threat lookups on observables that are not attached to a security incident on the initial event trigger. Also, you might perform this task when you want more information about a related observable.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/security-incident-response/attach-an-observable-manually-phishtank.html
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [PhishTank integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# \(Optional\) Manually attach an observable for PhishTank

You can manually attach observables to a security incident. You manually attach observables when you want to perform threat lookups on observables that are not attached to a security incident on the initial event trigger. Also, you might perform this task when you want more information about a related observable.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to your open security incident.

2.  On the open security incident record, click the **Show IoC**link in **Related Links** to display the **Observables** tab.

    \[Omitted image "phishtank-new-incident.png"\] Alt text: Observables tab in the security record.

3.  Click **New**.

    The Observable form is displayed.

4.  In the **Value** field, enter a URL.

5.  Click the search icon and from the **Observable Type Categories** dialog box, click **URL** in the list to populate the field.

    \[Omitted image "phishtank-observable.png"\] Alt text: Observables type Categories list.

6.  Click **Submit**.

    The flow launches and checks for the new observable. The execution and completion status is displayed in the work notes section on the Security Incident record.

    \[Omitted image "flows-phishtank.png"\] Alt text: Security Operations - PhishTank integration flow.

7.  Navigate to your security incident and review the work notes.

    \[Omitted image "flows-phishtank-worknotes.png"\] Alt text: Look up status in work notes.

8.  Click the **Show All Related Lists** related link at the bottom of the security incident.

9.  Click the **Threat Lookup Results** tab to view the results.

    \[Omitted image "phishtank-lookup.png"\] Alt text: Look up results on the security record.

10. In the **Observable** column, click the blue information icon next to a given observable for more information and raw data.

    \[Omitted image "phishtank-lookup-icon.png"\] Alt text: Information icon on security record.

11. In the dialog box that is displayed, click **Open Record**.


Review the work notes for more information and how to proceed if you cannot verify that the lookup ran successfully.

**Parent Topic:**[PhishTank integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/security-incident-response/phishtank-lookups.md)

**Previous topic:**[Verify expected results for PhishTank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/security-incident-response/verify-expected-results-phishtank.md)

**Next topic:**[Proofpoint integration for Security Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/security-incident-response/proofpoint-integration-secops-landing.md)

