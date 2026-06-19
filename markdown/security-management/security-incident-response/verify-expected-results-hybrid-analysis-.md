---
title: Verify expected results for Hybrid Analysis
description: Observables are generated automatically by a security incident and scanned by the application. Locate the lookup results on the security incident to verify the threat lookup has run successfully. Also view raw data and run threat lookups on child observables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/verify-expected-results-hybrid-analysis-.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Hybrid Analysis integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Verify expected results for Hybrid Analysis

Observables are generated automatically by a security incident and scanned by the application. Locate the lookup results on the security incident to verify the threat lookup has run successfully. Also view raw data and run threat lookups on child observables.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Open the security incident record you are working with and verify that the lookup has run successfully.

    \[Omitted image "hybridanalysis-worknotes.png"\] Alt text: Lookup status in the work notes.

    After the application is configured, the flow launches automatically upon incident creation. The execution and completion status of the lookup is then displayed in the work notes in the security incident.

2.  Review the work notes for more information on how to proceed if you cannot verify that the lookup ran successfully.

3.  Navigate to the bottom of the security incident record and click the **Show All Related Lists** related link to view results.

    **Note:** The figures in the following steps are shown with the **Tabbed forms** setting active in the System Settings. In the upper-right corner of the banner frame, click the Settings gear icon. In the **System Settings** dialog box that is displayed, click **Forms** and verify that **Tabbed forms** and **With the Form** are selected.

    \[Omitted image "hybridanalysis-lookup-results.png"\] Alt text: Lookup results.

    The **Threat Lookup Results** tab displays the lookup results at the bottom of the security incident record. Note the **Finding** column displays `Unknown` for records not determined to be malicious. For results matching malicious, the **Finding** column displays `Malicious`.

4.  In the **Observable** column, click an observable to open the record.

    \[Omitted image "hybridanalysis-tag.png"\] Alt text: Open observable record with finding and security tag.

    For lookups matching malicious, the **Finding** field displays `Malicious`, and the observable is tagged with the Threat Intelligence source that found it to be malicious, in this case, the Hybrid Analysis integration.

5.  Follow the steps to view raw data, view a list of child observables, and run a threat lookup on selected child observables.

    1.  Navigate back to the security incident and on the **Threat Lookup Results** tab, click the blue information icon next to an observable.

        \[Omitted image "hybridanalysis-information.png"\] Alt text: Information icon on record.

    2.  In the window that is displayed, click **Open Record** to view the data.

        From any observables viewable in the raw data that is displayed from the lookup, the Hybrid Analysis integration also creates child, or related observables.

        \[Omitted image "hybridanalysis-raw-data.png"\] Alt text: Raw data on the observable record.

        The link created by the API, the raw data, and other information are displayed.

    3.  Navigate back to the security incident and click the **Show IoC** related link.

        The child observables are displayed on the **Child Observables** tab on the security incident, because the lookup has found an existing connection between these related observables and the observable initially submitted.

    4.  Click the field next to an observable in the **Child** column to select it, followed by the **Run threat lookup** related link to perform a lookup.

        \[Omitted image "hybridanalysis-childobservable.png"\] Alt text: Child observables tab.

    5.  In the dialog box that is displayed, verify that the Hybrid Analysis integration is selected and click **Submit**.

    6.  In the work notes, verify that the lookup has run successfully, and on the **Threat Lookup Results** tab in the security incident, locate lookup results for the child observables.


If you do not see results under the **Threat Lookup Results** tab, verify that the observable is a type that is supported for lookup by the integration.

**Parent Topic:**[Hybrid Analysis integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/hybrid-analysis-lookups.md)

**Previous topic:**[Install and configure Hybrid Analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/install-and-configure-hybrid-analysis.md)

**Next topic:**[\(Optional\) Manually attach an observable for Hybrid Analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/attach-an-observable-manually-hybrid-analysis.md)

