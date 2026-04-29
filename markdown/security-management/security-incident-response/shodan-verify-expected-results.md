---
title: Verify expected results for Shodan
description: Observables are generated automatically by a security incident and scanned by the application. Enrichment results are displayed on the Observable Enrichment Results and Network Banners tabs.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Shodan integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Verify expected results for Shodan

Observables are generated automatically by a security incident and scanned by the application. Enrichment results are displayed on the **Observable Enrichment Results** and **Network Banners** tabs.

## Before you begin

Role required: sn\_si.analyst.

## Procedure

1.  Open the security incident you are working with and verify that the lookup has run successfully.

    ![Status on the work notes.](../image/shodan-activities.png)

    Once the application is configured, the workflow launches automatically upon incident creation. The execution and completion status of the lookup is displayed in the work notes in the security incident.

2.  Review the work notes for more information and how to proceed if you cannot verify that the lookup ran successfully.

3.  Navigate to the bottom of the security incident and click the **Show All Related Lists** link in **Related Links**.

    **Note:** The figures in the following steps are shown with the **Tabbed forms** setting active in the System Settings. If tabbed forms are not displayed, in the upper-right corner of the banner frame, click the Settings gear icon. In the **System Settings** dialog box that is displayed, click **Forms** and verify that **Tabbed forms** and **With the Form** are selected.

    ![Look up results on the incident record.](../image/shodan-related-lists.png)

    Results are displayed in the **Observable Enrichment Results** and **Network Banners** tabs at the bottom of the security incident.

4.  With the **Network Banners** tab selected, click the blue information icon next to an observable.

    ![Click the information icon to open the record and view raw data.](../image/shodan-enrichment-results.png)

5.  In the dialog box that is displayed, click **Open Record** to view raw data and more details.


If you do not see results under the **Observable Enrichment Results** and **Network Banners** tabs, verify that the observable is a type that is supported for lookup by the integration.

**Parent Topic:**[Shodan integration](../concept/shodan-lookups.md)

**Previous topic:**[Install and configure Shodan](install-and-configure-shodan.md)

**Next topic:**[\(Optional\) Manually attach an observable for Shodan](manually-attach-an-observable-shodan.md)

