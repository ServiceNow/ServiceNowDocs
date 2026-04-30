---
title: Sighting searches in MISP
description: You can perform sighting searches on observables in the MISP instance to determine how often certain types of attacks, such as phishing attacks or communications with a malicious IP or URL, occur in your network. Each occurrence is considered a sighting.Enable the sighting search in MISP to run automatically so that the Security Operations Integration - Sightings Search workflow is triggered whenever new observables are associated with a security incident.Select individual or multiple observables and perform a manual sighting search in the ServiceNow AI Platform MISP integration for Security Operations application to determine the prevalence of a threat over time.Report threat data sightings so that you can react to false positives in your data and increase your awareness when a true positive threat occurs. You can also add an expiration date for a particular observable or attribute.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Using MISP to investigate and analyze threats, MISP integration for Security Operations, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Sighting searches in MISP

You can perform sighting searches on observables in the MISP instance to determine how often certain types of attacks, such as phishing attacks or communications with a malicious IP or URL, occur in your network. Each occurrence is considered a sighting.

## Sightings in MISP

Sightings denote that an indicator, object, or attribute, was seen and its validity is confirmed. Sightings in MISP is a system that allows you to respond to attributes on an event. It is designed to provide an easy method for your users to confirm that they have seen a given attribute, giving it more credibility. You can sight an attribute multiple times.

**Note:** Observables are known as attributes in MISP.

Some attributes are considered as false positives, which means that they are not valid sightings. Other attributes are valid for only a certain duration, such as a phishing campaign that runs for only one week. You can assign an expiration date to the attributes that are valid for a certain duration, but each organization can assign only one valid expiration date to an attribute.

Sightings that are created in MISP by users of organizations that are marked as local in the corresponding MISP server are known as internal sightings. Sightings that are created in MISP by users of organizations that are marked as remote in the corresponding MISP server are known as external sightings.

## Sighting searches in SIR

The [Security Operations Integration - Sightings Search workflow](../../security-operations-integrations/task/secops-integration-sightings-search-workflow.md) executes the sightings search. This workflow accepts a list of observables, finds any implementing capabilities, creates the queries that are based on the sighting search configurations, and executes the searches that are based on the configured workflow.

Sighting searches helps analysts to determine the prevalence of a threat over time. You can select individual or multiple observables and the date range for your search from a security incident. Results are included in the Security Incident [Sightings](sightings-searches-in-misp.md#), [Sightings Search Results](../../security-operations-common/task/view-sightings-search-results.md), and [Sightings Search Details](../../security-operations-common/task/view-sightings-search-details.md) related lists.

As you start to analyze an incident, you can set up your ServiceNow AI Platform to [automatically perform a sightings search](sightings-searches-in-misp.md#) or [manually perform an observable sightings search](sightings-searches-in-misp.md#) to identify other users in your organization who are impacted by the same phishing attack.

**Parent Topic:**[Using MISP to investigate and analyze threats](using-misp-to-detect-and-analyze-threats.md)

## Enable automatic sighting searches in MISP

Enable the sighting search in MISP to run automatically so that the Security Operations Integration - Sightings Search workflow is triggered whenever new observables are associated with a security incident.

### Before you begin

Verify that the [Sightings Search Configuration profile for MISP](../task/configure-sightings-search.md) is active.

Role required: sn\_si.analyst

### About this task

If you enable [the sighting search capability to run automatically in the MISP integration configuration](../task/review-the-misp-integration-settings.md), the sighting search in MISP triggers when new observables are associated with a security incident. By default, the **Run Sighting Search automatically when new observables are associated with the security incident** option is enabled.

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Show All Incidents**.

2.  Select the security incident that contains the observables that you want to view in the MISP sightings search data.

3.  Review the work notes after new observables have been associated with the security incident.

    A work note is posted when the [Security Operations Integration - Sightings Search workflow](../../security-operations-integrations/task/secops-integration-sightings-search-workflow.md) has triggered.

    The following example shows the work notes section.

    ![View the work notes and verify if the Sightings Search workflow has triggered.](../image/misp-sighting-search-auto.png)

4.  View the aggregated information of observables that are seen across all the events \(global\) and categorized by their internal or external sightings after the workflow execution has completed.

    View the information in the [Sightings](sightings-searches-in-misp.md#table_pxj_2dl_kqb), [Sightings Search Results](../../security-operations-common/task/view-sightings-search-results.md) and [Sightings Search Details](../../security-operations-common/task/view-sightings-search-details.md) related lists.The following example shows the sightings search record that was created in the Sightings related list.

    ![View the Sightings Search record that was created in the Sightings tab.](../image/misp-sightings-tab.png)

<table id="table_pxj_2dl_kqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Date and time that the sightings search record was created.

</td></tr><tr><td>

Observable

</td><td>

Observable that is searched for by the query.

</td></tr><tr><td>

Sighting count

</td><td>

Count of internal and external sightings.

</td></tr><tr><td>

Source

</td><td>

Source of the observable. If the observable is from a MISP organization, the record is preceded with the words `MISP`.

</td></tr><tr><td>

Is local

</td><td>

Status of whether the sighting was reported by an internal user.

</td></tr><tr><td>

Sighting search link

</td><td>

Sighting search link in the MISP instance.

</td></tr><tr><td>

Summary

</td><td>

Type of sightings that are associated with the record. The three types of Sightings are Sighting, False-positive, and Expiration.The Summary column appears only when the MISP integration for Security Operations is installed. If sources other than MISP appears, the Summary column entry is empty for that record.

</td></tr></tbody>
</table>
## Perform a manual sighting search in MISP

Select individual or multiple observables and perform a manual sighting search in the ServiceNow AI Platform MISP integration for Security Operations application to determine the prevalence of a threat over time.

### Before you begin

-   [Review the MISP user role and permissions](../reference/misp-user-roles-and-permissions.md) for using the MISP bi-directional features.
-   Role required: sn\_si.analyst

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Show All Incidents**.

2.  Select the security incident that contains the observables that you want to run the MISP sightings search for.

3.  Click **Show All Related Lists** and the **Associated Observables** tab.

4.  Select the observable and then from the Actions menu, click **Run Sightings Search**.

    You can select multiple observables for a sighting search.

    The Run Sightings Search dialog box opens.

5.  Specify the date range to search for the sightings search data.

<table id="table_qd2_myl_kqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Last

</td><td>

Number of hours or days prior to the creation of the incident to search.The default is 7 days. The limit is 99 hours or days.

</td></tr><tr><td>

between

</td><td>

Range of dates to search. Default dates are as follows:-   The date and time that the incident was created.
-   The date and time that is seven days prior to the opening of the incident.


</td></tr></tbody>
</table>6.  Click **Search**.

    The following example shows the manual sighting search results in the work notes.

    ![Manual sighting search results in the work notes.](../image/misp-manual-sighting-search-worknote.png)


### Result

A Sightings Search record is created. After the workflow execution has completed, you can view the aggregated information of observables that are seen across all the events \(global\) and categorized by their internal or external sightings. Aggregate and associated sightings data are displayed in the security incident under the [Sightings](sightings-searches-in-misp.md#fig_m3s_lgk_kqb), [Sightings Search Results](../../security-operations-common/task/view-sightings-search-results.md), and [Sightings Search Details](../../security-operations-common/task/view-sightings-search-details.md) related lists.

## Report sightings to MISP

Report threat data sightings so that you can react to false positives in your data and increase your awareness when a true positive threat occurs. You can also add an expiration date for a particular observable or attribute.

### Before you begin

-   [Review the MISP user role and permissions](../reference/misp-user-roles-and-permissions.md) for using the MISP bi-directional features.
-   Role required: sn\_si.analyst

### About this task

The MISP integration for Security Operations enables you to report sightings to MISP globally across all events. To report a sighting to a specific event, you must use the MISP instance and report the sighting locally.

To report a sighting to MISP, the observable or the attribute must be available in the MISP instance.

### Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Show All Incidents**.

2.  Select the security incident that contains the observables that you want to report the sightings to MISP for.

3.  Click **Show All Related Lists** and the Sightings related list.

4.  Select the observable and from the Actions menu, select one of the following options.

    |Option|Description|
    |------|-----------|
    |**MISP: Report Observable Sighting**|Report the observable as sighted to MISP. If the observable is associated with multiple events, it is updated in all the events.|
    |**MISP: Report Observable as False Positive**|Report the observable as a false positive to MISP.|
    |**MISP: Report Observable as Expired**|Report the observable as expired to MISP.|

    If you select observables that are not specific to a MISP source, the Actions menu shows the count of relevant MISP sources. The following example shows four out of eight observables as relevant to MISP.The following example shows the actions menu and the relevant observables for submission.

    ![Actions menu shows the relevant observables for MISP.](../image/misp-relevant-source-sightings.png "Actions menu that shows the relevant observables for submission")

5.  If you selected the **MISP: Report Observable Sighting** option, you should fill in the fields of the Report Observable Sighting to MISP dialog box.

    |Field|Description|
    |-----|-----------|
    |Source|Source field that corresponds to the MISP source of the sighting.|
    |Date|Date field that corresponds to the date that the observable is sighted. If the date is empty, the current date and time is populated in MISP.|

    The following example shows how to navigate to the Sightings related list in the security incident. From that list, you can select an observable and report the observable sighting to MISP. The success message shows that the sighting was successfully submitted to MISP.

    ![Reports observable sighting to MISP](../image/misp-report-sighting-to-misp.gif "Reports observable sighting to MISP")

    1.  Click **Report Sighting**.

6.  If you selected the **MISP: Report Observable as False Positive** option, you should fill in the fields of the Report Observable as False Positive to MISP dialog box.

    |Field|Description|
    |-----|-----------|
    |Source \(optional\)|Source field that corresponds to the MISP source. Use this field to declare the observable as a false positive.|
    |Date|Date field that corresponds to the date that the observable was found to be a false positive. If the date is empty, the current date and time is populated in MISP.|

    1.  Click **Report False Positive**.

7.  If you selected the **MISP: Report Observable as Expired** option, you should fill in the fields of the Report Observable Expiration to MISP dialog box.

    |Field|Description|
    |-----|-----------|
    |Source|Source field that corresponds to the MISP source. Use this field to set an observable as expired.|
    |Date|Date field that corresponds to the date that the observable has expired on. If the date is empty, the current date and time is populated in MISP.|

    1.  Click **Report Expiry**.


### Result

The sightings successfully update to the MISP server.

