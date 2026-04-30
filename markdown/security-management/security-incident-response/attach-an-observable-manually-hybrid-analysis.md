---
title: \(Optional\) Manually attach an observable for Hybrid Analysis
description: You can manually attach observables when you want to perform threat lookups on observables that are not attached to a security incident on the initial event trigger. Also, you might perform this task when you want more information about a related observable.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Hybrid Analysis integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# \(Optional\) Manually attach an observable for Hybrid Analysis

You can manually attach observables when you want to perform threat lookups on observables that are not attached to a security incident on the initial event trigger. Also, you might perform this task when you want more information about a related observable.

## Before you begin

Verify the observable is of a type supported by the integration. The integration performs lookups on the following types of observables:

-   File hashes
-   IP addresses
-   URLs

Role required: sn\_si.analyst

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents** and open a security incident to which you want to attach the observable.

2.  On the open security incident, click the **Show IoC**link in **Related Links**.

    ![Observables tab on the incident record.](../image/hybrid-analysis-new-incident.png)

3.  On the **Observables** tab, click **New**.

    The Observable form is displayed.

4.  In the **Value** field, enter an observable \(file hash, IP addresses, or URL\).

5.  Click the search icon and from the **Observable Type Categories** dialog box, click the desired observable type in the list to populate the field.

    ![Observable Type Category list.](../image/hybrid-analysis-observable.png)

6.  Click **Submit**.

    The flow launches and checks for the new observable. The execution and completion status is displayed in the work notes section on the security incident record.

7.  Navigate to your security incident and review the work notes.

    ![Lookup status in the work notes.](../image/hybridanalysis-worknotes.png)

8.  At the bottom of the record, click the **Show All Related Lists** related link.

9.  Click the **Threat Lookup Results** tab to view the results.

    ![Threat lookup results tab.](../image/hybridanalysis-lookup-results.png)

10. In the **Observable** column, click the blue information icon next to a given observable for more information and raw data.

    ![Task: Click the information symbol.](../image/hybridanalysis-information.png)

11. In the dialog box that is displayed, click **Open Record** to view the raw data and more details.

    Alternatively, you can also attach an existing observable to the security incident record.

12. With the **Observables** tab selected, click **Edit**.

13. In the **Edit Members** form that is displayed, move an existing observable from **Collection** to **Observables List** and click **Save**.

    You are returned to the security incident.

14. In the far left column, select the observables you want to run the lookup on, and from the **Actions on selected rows...** choice list, select **Run threat lookup**.

    A message is displayed across the top of the record that the request is being processed. Verify that the lookup has run successfully.


Review the work notes for more information and how to proceed if you cannot verify that the lookup ran successfully.

**Parent Topic:**[Hybrid Analysis integration](../concept/hybrid-analysis-lookups.md)

**Previous topic:**[Verify expected results for Hybrid Analysis](verify-expected-results-hybrid-analysis-.md)

**Next topic:**[IBM QRadar Offense Ingestion Integration](../../secops-integration-sir/secops-integration-qradar-ibm/concept/qradar-ibm.md)

