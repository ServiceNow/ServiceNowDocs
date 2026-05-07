---
title: Report an operational vulnerability from the Importance assessment
description: Report an operational vulnerability from the Importance and impact assessment in the Operational Resilience Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reporting Operational vulnerability, Managing Operational vulnerability, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Report an operational vulnerability from the Importance assessment

Report an operational vulnerability from the Importance and impact assessment in the Operational Resilience Workspace.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

To create an Operational vulnerability from the assessment record, you can use the Operational vulnerability related list in these records. This example shows creating a vulnerability from the Importance and impact tolerance assessment record. When you associate an assessment record to the Operational vulnerability record, the related area for the vulnerability is displayed in the Related areas related list.

When a vulnerability is reported, it is opened in the **New** state, marking the beginning of its initial review.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Importance and impact tolerance assessment**.

    A list of the available assessments is displayed.

2.  Select an assessment from the list.

    The Importance and impact tolerance assessment record with Operational vulnerabilities related list is displayed.

3.  Check the state of the Importance and impact tolerance assessment.

    If the state is in the **Assessment received** state, you cannot add a vulnerability at this stage as shown in the example. You can add or remove the vulnerability before the vulnerability is in the **Assessment received** state.

    ![Assessment received state.](../image/assmt-in-asmt-recd-state.png)

    You can create an Importance and impact tolerance assessment record and then add a vulnerability.

4.  Create an Importance and impact tolerance assessment record and save it.

5.  Add a service to the Importance and impact tolerance assessment record.

    The service record is shown in the example.

    ![Service list.](../image/op-vul-service-list-in-assmt-record.png)

    When the service is added to the Importance and impact tolerance assessment record, you can add the operational vulnerability and the **New** button is displayed in the Operational vulnerabilities related list.

6.  Select **New** in the Operational vulnerabilities related list and add an operational vulnerability.

7.  On the Vulnerability New record form, fill in the fields.

    The source of the vulnerability is the Importance and impact tolerance assessment. Therefore, the **Source** field on the form shows the source as Importance and impact assessment and the **Source table** field on the form shows the table as Importance and impact tolerance assessment.

    To view more information on the fields, see the [Create New Operational vulnerability form](../reference/create-new-op-vul-form.md).

8.  Select **Save**.

    The Vulnerability record is saved. When you associate the Importance and impact tolerance assessment to the vulnerability, the related area is created as shown in the example.

    ![Related area.](../image/op-vul-related-area.png)

    You can add another related area to the vulnerability.


