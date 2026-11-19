---
title: Configure PR and PO Progress Tracker states
description: Configure which states appear in the Progress Tracker, and how they flow, by editing the PR Stage Display Config and PO Stage Display Config records—no code deployment required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/configure-pr-po-states.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 3
keywords: [purchase requisition, purchase order, Progress Tracker, state configuration, S2P Custom Configuration]
breadcrumb: [Configure the Progress Tracker, Use Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure PR and PO Progress Tracker states

Configure which states appear in the Progress Tracker, and how they flow, by editing the PR Stage Display Config and PO Stage Display Config records—no code deployment required.

## Before you begin

Role required: sn\_fin.finance\_admin

## About this task

You can customize purchase requisition \(PR\) and purchase order \(PO\) state flows without code deployment. State graphs—including happy path, terminals, deviations, and the punchout variant—are defined in configuration records rather than hardcoded in script. You can add, remove, or reorder states by editing a record's script field.

Configuration records are separate for PR and PO. The **PR Stage Display Config** record targets Purchase Requisition objects, and the **PO Stage Display Config** record targets Purchase Order objects, so you can change one independently of the other.

Editing the script field directly requires familiarity with ServiceNow scripts. Work with a developer if you are not comfortable editing scripts.

## Procedure

1.  Navigate to **All** &gt; **Finance Common** &gt; **S2P Custom Configuration**.

    \[Omitted image "progress-tracker-s2p-custom-config.png"\] Alt text: List view showing PR Stage Display Config and PO Stage Display Config records in S2P Custom Configuration table.

2.  Open **PR Stage Display Config** to edit the PR state graph, or **PO Stage Display Config** to edit the PO state graph.

3.  In the **Script** field, edit the following arrays to add, remove, or reorder states: **STATE**, **happyPath**, **terminals**, and **deviations**.

    \[Omitted image "progress-tracker-pr-stage-display-config.png"\] Alt text: Script editor showing STATE map and happyPath array in PR Stage Display Config record.

    The PR configuration also defines a punchout variant happy path \(`state=10,20,30,40,100,45,50`—inserting Pending Supplier Confirmation before Pending Submission\) separately from the standard happy path \(`state=10,20,30,40,45,50`\). For the full state reference, see the PR state model topic.

    The arrays now reflect your state flow changes.

4.  For the PO configuration, edit the same graph-shaped fields, plus the PO-specific schema fields: **statusField**, **variantField**, **choiceTable**, **workItemsText**, **pillsFrom**, and **headerAssigneeField** / **headerAssigneeStates**.

    **Important:** The PO configuration script runs under GlideScopedEvaluator in the sn\_fin scope. Use plain string literals for state values, field names, and table names—do not reference sn\_shop.PurchaseOrder constants, which are not accessible in that scope.

    \[Omitted image "progress-tracker-po-stage-display-config.png"\] Alt text: Script editor showing schema field documentation in PO Stage Display Config record header comment.

    The PO-specific schema fields are updated.

5.  Select **Update**.

    State-graph definitions are cached per transaction, so your change takes effect on the next request without a manual cache clear.


## Result

The updated state graph takes effect on the next transaction for a PR or PO record. For the current state list and happy-path order, see the PR state model and PO state model topics.

## Remove Final Review from PR happy path

To remove Final Review from the PR happy path, delete its state value from the **happyPath** array in the PR Stage Display Config script.

Before:

```
happyPath: [10, 20, 30, 40, 45, 50]
```

After:

```
happyPath: [10, 20, 30, 45, 50]
```

The stepper shows Pending Review → Pending Approval → Awaiting Task Completion → Pending Submission → Closed Complete, skipping Final Review.

## What to do next

The `ProcessStateMachine` script include reads this configuration. Its output reaches the stepper UI through the get\_pr\_stepper\_data data broker transform \(PR\) and the equivalent PO data broker. Both data brokers run under an execute ACL requiring the sn\_shop.shopper role for the viewing user. See the configure tracker visibility topic for system-wide visibility, and the PR state model and PO state model topics for the resulting state model.

**Parent Topic:**[Configure the Progress Tracker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/configure-progress-tracker.md)

**Related topics**  


[Configure Progress Tracker visibility]()

