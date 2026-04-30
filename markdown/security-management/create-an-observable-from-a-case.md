---
title: Create an observable from a case
description: New observables can be created from cases in Security Case Management.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [IoCs and observables in cases, Case creation from security artifacts, Security Case Management, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Create an observable from a case

New observables can be created from cases in Security Case Management.

## Before you begin

Role required: sn\_ti.case\_user

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence** &gt; **Case Management** &gt; **All Cases**.

    The Security Cases list opens.

2.  Either open an existing case or click **New** to [create a new case](create-cases-in-case-mgmt.md).

3.  Click the **Case Artifacts** related link and click the **Observables** tab.

4.  Click **New** and enter the requested information.

    |Field|Description|
    |-----|-----------|
    |Value|\[Read only\] The case number.|
    |Observable type|Enter a descriptive name for the case.|
    |Observable type category|Select the type of case being investigated.|
    |Incident count|Select the importance of this case \(from Critical to Low\).|
    |Finding|\[Read only\] The date and time the case was last updated.|
    |Notes|A brief description of the case.|

5.  Click the **Additional Case Details** tab.

6.  Fill in the fields as appropriate.

    |Field|Description|
    |-----|-----------|
    |Created by|\[Read only\] The name of the user who created this case.|
    |State|The current state of the case. At case creation, the State defaults to Draft.|
    |Work notes list|Click the check box to display the work notes in the Additional Case Details section of the case record.|
    |Work Notes|If needed, type a work note for the case. If the **Work notes list** is selected, the work note appears in the Additional Case Details section of the case record.|

7.  Click **Submit**.

    As needed, you can click the **Case Artifacts** tab and [add artifacts to the case](add-records-to-cases.md).


**Parent Topic:**[IoCs and observables in cases](../concept/cases-in-threat.md)

**Related topics**  


[Create a case from IoCs or observables](create-cases-threat.md)

[Add IoCs and observables to an existing case](add-records-to-cases-threat.md)

[Run a sightings search on observables in a case](run-local-sighted-srch.md)

