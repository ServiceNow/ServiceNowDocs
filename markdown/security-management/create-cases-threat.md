---
title: Create a case from IoCs or observables
description: In Threat Intelligence, you can create a case from artifacts \(IoCs or observables\). After the IoCs or observables have been used to create a case, you can use Security Case Management to analyze the data.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [IoCs and observables in cases, Case creation from security artifacts, Security Case Management, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Create a case from IoCs or observables

In Threat Intelligence, you can create a case from artifacts \(IoCs or observables\). After the IoCs or observables have been used to create a case, you can use Security Case Management to analyze the data.

## Before you begin

The Threat Intelligence plugin must be activated to use Security Case Management.

Role required: sn\_ti.case\_user\_write

## Procedure

1.  Navigate to the artifacts \(IoCs or observables\) you want to use to create a case.

    -   To create a case from IoCs, navigate to **Threat Intelligence** &gt; **IoC Repository** &gt; **Indicators**.
    -   To create a case from observables, navigate to **Threat Intelligence** &gt; **IoC Repository** &gt; **Observables**.
2.  In the list, select the artifacts you want added to a new case.

    **Note:** If you select multiple IoCs or observables, they are all added to the case.

3.  From the **Actions on selected items** drop-down list, select **Add to Security Case**.

    ![Add indicators to a new case](../image/add-to-case.png)

    The **Add to Security Case** dialog box opens. If you already have cases assigned to you, they display in the list.

    ![Add an indicator to the case](../image/add-to-security-case.png)

4.  Click **Create New Case**.

5.  Fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Case Name|Enter a name for this case.|
    |Description|Enter a description that would be of value to the case analyst.|

6.  Click **Submit**.

    A message at the top of the list indicates that a new case has been created, along with a link to the case in Security Case Management.

7.  Click the link to view the new case.


**Parent Topic:**[IoCs and observables in cases](../concept/cases-in-threat.md)

**Related topics**  


[Add IoCs and observables to an existing case](add-records-to-cases-threat.md)

[Create an observable from a case](create-an-observable-from-a-case.md)

[Run a sightings search on observables in a case](run-local-sighted-srch.md)

