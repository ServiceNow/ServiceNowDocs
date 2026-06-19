---
title: Verify expected results for PhishTank
description: Observables are generated automatically by a security incident and scanned by the application. Lookup results are displayed on the Threat Lookup Results tab at the bottom of the security incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/verify-expected-results-phishtank.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [PhishTank integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Verify expected results for PhishTank

Observables are generated automatically by a security incident and scanned by the application. Lookup results are displayed on the Threat Lookup Results tab at the bottom of the security incident record.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Open the security incident form you're working with and verify that the lookup has run successfully.

    After the application is configured, the flow launches automatically on incident creation. The execution and completion status of the lookup is then displayed in the work notes in the security incident record.

2.  Review the work notes for more information and how to proceed if you can't verify that the lookup ran successfully.

3.  Navigate to the bottom of the security incident and select the **Show All Related Lists** related link.

    **Note:** If tabbed forms aren't displayed, in the upper-right corner of the banner frame, select the Settings gear icon. In the **System Settings** dialog box that is displayed, select **Forms** and verify that **Tabbed forms** and **With the Form** are selected.

    The **Threat Lookup Results** tab at the bottom of the security incident record displays the lookup results.

    The **Finding** column displays `Unknown` for records not determined to be malicious. For results matching malicious, `Malicious` is displayed in the **Finding** column.

4.  In the **Observable** column, select an observable to open a record and display more information.

    On the observable record, for lookups matching malicious, `Malicious` is displayed the **Finding** field. The observable is tagged with the Threat Intelligence source that found it to be malicious, in this case, the PhishTank application.

5.  To view raw data, navigate back to the security incident and select the blue information icon next to an observable.

    \[Omitted image "phishtank-lookup-icon.png"\] Alt text: Information icon on security record.

6.  In the window that is displayed, select **Open Record**.

    The link created by the API and the **Finding** field displayed with the results.


If you don't see results under the **Threat Lookup Results** tab, verify that the observable is a type that is supported for lookup by the integration.

**Parent Topic:**[PhishTank integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/phishtank-lookups.md)

**Previous topic:**[Install and configure PhishTank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/install-and-configure-phishtank.md)

**Next topic:**[\(Optional\) Manually attach an observable for PhishTank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/attach-an-observable-manually-phishtank.md)

