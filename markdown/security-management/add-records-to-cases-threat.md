---
title: Add IoCs and observables to an existing case
description: You can add IoCs and observables to existing cases. After the security incidents have been added to cases, you can use Security Case Management to analyze the data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/add-records-to-cases-threat.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [IoCs and observables in cases, Case creation from security artifacts, Security Case Management, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Add IoCs and observables to an existing case

You can add IoCs and observables to existing cases. After the security incidents have been added to cases, you can use Security Case Management to analyze the data.

## Before you begin

The Threat Intelligence plugin must be activated to use Security Case Management.

Role required: sn\_ti.case\_user\_write

## Procedure

1.  Navigate to the artifacts \(IoCs or observables\) you want to add to existing cases.

    -   To add IoCs to one or more cases, navigate to **Threat Intelligence** &gt; **IoC Repository** &gt; **Indicators**.
    -   To add observables to one or more cases, navigate to **Threat Intelligence** &gt; **IoC Repository** &gt; **Observables**.
2.  In the list, select the artifact records you want added to existing cases.

    **Note:** If you select multiple cases, the selected IoCs or observables are added to each of the selected cases.

3.  From the **Actions on selected items** drop-down list, select **Add to Security Case**.

    The **Add to Security Case** dialog box opens. If you already have cases assigned to you, they display in the list.

4.  Select the cases into which you want to add the selected IoCs or observables.

    \[Omitted image "add-observ-to-existing-case.png"\] Alt text: Add an observable to an existing case

5.  Click **Add**.

    A message indicates that the selected records have been added to the cases, along with a link to the cases in Security Case Management.


**Parent Topic:**[IoCs and observables in cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/cases-in-threat.md)

**Related topics**  


[Create a case from IoCs or observables]()

[Create an observable from a case]()

[Run a sightings search on observables in a case]()

