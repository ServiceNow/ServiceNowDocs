---
title: Verify expected results for PhishTank
description: Observables are generated automatically by a security incident and scanned by the application. Lookup results are displayed on the Threat Lookup Results tab at the bottom of the security incident record.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [PhishTank integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Verify expected results for PhishTank

Observables are generated automatically by a security incident and scanned by the application. Lookup results are displayed on the Threat Lookup Results tab at the bottom of the security incident record.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Open the security incident form you are working with and verify that the lookup has run successfully.

    ![Lookup status on work notes.](../image/phishtank-worknotes.png)

    After the application is configured, the flow launches automatically upon incident creation. The execution and completion status of the lookup is then displayed in the work notes in the security incident record.

2.  Review the work notes for more information and how to proceed if you cannot verify that the lookup ran successfully.

3.  Navigate to the bottom of the security incident and click the **Show All Related Lists** related link.

    **Note:** The figures in the following steps are shown with the **Tabbed forms** setting active in the System Settings. If tabbed forms are not displayed, in the upper-right corner of the banner frame, click the Settings gear icon. In the **System Settings** dialog box that is displayed, click **Forms** and verify that **Tabbed forms** and **With the Form** are selected.

    ![Threat lookup results.](../image/phishtank-lookup.png)

    The **Threat Lookup Results** tab at the bottom of the security incident record displays the lookup results.

    The **Finding** column displays `Unknown` for records not determined to be malicious. For results matching malicious, `Malicious` is displayed in the **Finding** column.

4.  In the **Observable** column, click an observable to open a record and display more information.

    ![Observable finding and security tag.](../image/phishtank-malicious.png)

    On the observable record, for lookups matching malicious, `Malicious` is displayed the **Finding** field. The observable is tagged with the Threat Intelligence source that found it to be malicious, in this case, the PhishTank application.

5.  To view raw data, navigate back to the security incident and click the blue information icon next to an observable.

    ![Information icon on security record.](../image/phishtank-lookup-icon.png)

6.  In the window that is displayed, click **Open Record**.

    ![Observable raw data.](../image/phishtank-malicious.png)

    The link created by the API and the **Finding** field displayed with the results.


If you do not see results under the **Threat Lookup Results** tab, verify that the observable is a type that is supported for lookup by the integration.

**Parent Topic:**[PhishTank integration](../concept/phishtank-lookups.md)

**Previous topic:**[Install and configure PhishTank](install-and-configure-phishtank.md)

**Next topic:**[\(Optional\) Manually attach an observable for PhishTank](attach-an-observable-manually-phishtank.md)

