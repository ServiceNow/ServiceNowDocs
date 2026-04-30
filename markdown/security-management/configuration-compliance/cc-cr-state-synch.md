---
title: State synchronization between change requests and remediation tasks
description: There is a synchronized relationship between the State fields of remediation tasks and the State fields of change requests \(CHGs\) in the Configuration Compliance application.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# State synchronization between change requests and remediation tasks

There is a synchronized relationship between the State fields of remediation tasks and the State fields of change requests \(CHGs\) in the Configuration Compliance application.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

As a change request moves through its life cycle, it also moves the state of any related remediation tasks automatically. State synchronization is enabled by a system property \(sn\_vulc.cr\_state\_sync\) by default in your instance when you download the Configuration Compliance application from the ServiceNow Store starting with v12.0.

When state synchronization is enabled, the CHG State field changes the remediation task State field automatically in the following cases:

-   When a new change request is created for a remediation task, if it is not in **Awaiting Implementation**, the remediation task state moves forward to **Awaiting Implementation**.
-   When an existing change request is associated to a remediation task, if it is not in **Awaiting Implementation**, the remediation task state moves forward to **Awaiting Implementation**.
-   After the tasks on a change request are completed \(`Implemented`\), and the CHG is moved to the **Review** state, the remediation task moves forward to **Resolved**.

For more information and examples of state synchronization, see the following sections.

**Note:** You can still manually move change requests and remediation tasks through the states of their life cycles on their respective records with state synchronization enabled, but when the system registers that a change request has changed its state, or you add a change request or remove it from a remediation task, state synchronization potentially can override your manual intervention. However, change request states do not automatically move the remediation task from the **Closed**.

## Forward state synchronization

The following image illustrates how CHG states automatically move remediation task states in a forward life cycle, that is, from **Open** to **Resolved**.

![How CR states drive CTR states.](../image/cc_trg_cr_synch.png)

You can create new change requests for any remediation task in a state other than **Resolved** or **Closed**. State synchronization automatically moves the TRG bi-directionally through the **Open**, **Under Investigation**, **Awaiting Implementation**, and **Resolved** states. This movement is based on certain values of the state field on the change request. State synchronization between the change request and the remediation task is invoked automatically unless the check box \(**Add CIs to CR**\) is displayed on a form and you choose to clear the check box.

The remediation task does not move forward to **Resolved** when a CHG is in its open states. Any CHG in states prior to **Review** in its life cycle such as, **New**, **Assess**, **Authorize**, **Scheduled** or **Implement**, as shown in the preceding figure, are considered open states for the CHG. Open states do not move the state field on the remediation task, because investigations or tasks on the CHG are not completed. State synchronization is invoked when a CHG is created for, or associated to, the remediation task, or when the state of an existing relationship changes on the CHG. The completed CHG states are **Review** and successfully **Closed**. When a CHG is closed successfully, its closed codes are: **Successful**, or **Successful with issues**, in which case the remediation task moves forward to **Resolved**.

## Backward state synchronization

As a CHG is processed during its life cycle, it may be canceled at some point. In this case, if the CHG is **Canceled**, or **Closed** \(with a close code of **Unsuccessful**\), the remediation task automatically moves back to **Under Investigation**. The remediation task moves back to **Under Investigation**, because there is no active plan to remediate the vulnerability.

If a remediation task is in a **Resolved** state​, and you create a new CHG or associate it to an existing CHG in one of the initial open states​, the remediation task automatically transitions back to **Awaiting Implementation**​. The remediation task moves back to this state, because more work is now assigned to the CHG.

## Remediation tasks with more than one CHG

If a remediation task in **Awaiting Implementation** has more than one CHG associated with it, state synchronization is based on the status of the CHG in the earliest state of its life cycle. For example, say a remediation task has four CHGs associated with it, CHG1, CHG2, CHG3, and CHG4 as shown in the following table.

|CHG number|CHG state|
|----------|---------|
|1|**Implement**|
|2|**Canceled**|
|3|Closed \(close code of **Unsuccessful**\)|
|4|Closed \(close code **Unsuccessful**\)|

State synchronization between the CHG and the remediation task in this case is based on CHG1, which is in the earliest state of the four CHGs, \(**Implement**\). In this case, the remediation task remains in **Awaiting Implementation**.

In another example, if a remediation task is in the **Resolved** state and has an existing CHG that has been implemented and is in the **Review** state, and a new CHG is created, the remediation task moves back from **Resolved** to **Awaiting Implementation**. State synchronization is based on the CHG in the **New** state, which is the CHG in the earliest state.

|CHG number|CHG state|
|----------|---------|
|1|Review|
|2|New|

Also, when remediation tasks have more than one CHG, the state of the remediation task transitions automatically in the following cases:

-   When a CHG moves forward to **Review**, if all other CHGs associated with the remediation task are in **Review** or **Closed** states \(with a successful close code\), ​the remediation task automatically transitions to **Resolved**​. Any other related CHGs that are canceled or closed unsuccessfully are ignored.
-   When a CHG moves to **Canceled** or ​**Closed** \(close code of **Unsuccessful**\), if all other CHGs associated with the remediation task are in the same state, then the remediation task automatically transitions back to **Under Investigation​**.

For more information about remediation task states and what you can do in each state, see [Configuration Compliance states](../concept/vuln-config-compl-states.md).

