---
title: \(Optional\) Manually attach an observable for PhishTank
description: You can manually attach observables to a security incident. You manually attach observables when you want to perform threat lookups on observables that are not attached to a security incident on the initial event trigger. Also, you might perform this task when you want more information about a related observable.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/attach-an-observable-manually-phishtank.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [PhishTank integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# \(Optional\) Manually attach an observable for PhishTank

You can manually attach observables to a security incident. You manually attach observables when you want to perform threat lookups on observables that are not attached to a security incident on the initial event trigger. Also, you might perform this task when you want more information about a related observable.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to your open security incident.

2.  On the open security incident record, select the **Show IoC**link in **Related Links** to display the **Observables** tab.

3.  Select **New**.

    The Observable form is displayed.

4.  In the **Value** field, enter a URL.

5.  Select the search icon and from the **Observable Type Categories** dialog box, Select **URL** in the list to populate the field.

6.  Select **Submit**.

    The flow launches and checks for the new observable. The execution and completion status is displayed in the work notes section on the Security Incident record.

7.  Navigate to your security incident and review the work notes.

8.  Select the **Show All Related Lists** related link at the bottom of the security incident.

9.  Select the **Threat Lookup Results** tab to view the results.

10. In the **Observable** column, select the blue information icon next to a given observable for more information and raw data.

    \[Omitted image "phishtank-lookup-icon.png"\] Alt text: Information icon on security record.

11. In the dialog box that is displayed, select **Open Record**.


Review the work notes for more information and how to proceed if you can't verify that the lookup ran successfully.

**Parent Topic:**[PhishTank integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/phishtank-lookups.md)

**Previous topic:**[Verify expected results for PhishTank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/verify-expected-results-phishtank.md)

**Next topic:**[Proofpoint Integration for Security Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/proofpoint-integration-secops-landing.md)

