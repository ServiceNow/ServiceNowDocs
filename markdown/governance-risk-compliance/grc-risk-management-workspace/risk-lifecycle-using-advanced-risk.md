---
title: Workflow of a risk using Advanced Risk
description: When you migrate to advanced risk assessment, you can view the various states of the risks take the necessary actions. This ability simplifies your view of the risk form.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Manage risks, risk statements, and risk frameworks, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Workflow of a risk using Advanced Risk

When you migrate to advanced risk assessment, you can view the various states of the risks take the necessary actions. This ability simplifies your view of the risk form.

When your risk administrator enables the **Migrate to Advanced Risk Assessments** property located under **Advanced Risk Assessment** &gt; **Administration** &gt; **Properties**, the life cycle of the classic or legacy risks undergo a change. You can also initiate a risk assessment directly from the risk form.

**Note:** Once you enable this property, you cannot disable it.

Prior to version 14.0, when the **Migrate to Advanced Risk Assessments** property was enabled, the risks were only classified as either active or inactive. Starting with version 14.0, as a risk owner, when you enable Advanced Risk, you can view the following states of your risks.

1.  Draft
2.  Assess
3.  Respond
4.  Monitor
5.  Retired

![States of a risk with advanced risk assessments enabled.](../../grc-workspace-risk/image/risk-lifecycle-ara.png "States of a risk with advanced risk assessment")

All the states and the actions available for each state are explained in the following table.

<table id="table_q3p_y4j_xsb"><thead><tr><th>

State

</th><th>

Description

</th><th>

Actions available

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

This is the state of a risk when a risk is created by the second line of defense or identified by the first line of defense.The objective in this state is to map and identify the risk pertaining to your organization. If you modify the entity or the primary risk assessment methodology \(RAM\) for a risk, the state of the risk gets updated based on the primary RAM's latest assessment.

</td><td>

-   **Save**
-   **Assess**: Pushes the workflow and initiates the risk assessment.
-   **Monitor**: If you do not want to assess the risk but want to monitor the risk.
-   **Retire**: The risk is retired along with all underlying risk assessment and risk response.
-   **Navigate to assessment scope**: Shortcut to risk assessment scope. The primary risk assessment methodology is passed.
-   **360 degree**: View the complete 360-degree relationships for the risk.

</td></tr><tr><td>

Assess

</td><td>

This is the state of a risk when advanced risk assessment is initiated and being performed. If there is a response strategy, then the risk moves to the Respond state otherwise it moves to the Monitor state once the assessment is completed.

</td><td>

-   **Save**
-   **View assessment**: Navigates to the actual risk assessment form.
-   **Cancel assessment**: If you want to cancel the current assessment. The respective risk assessor is notified about the canceled assessment.
-   **Return to draft**: Cancels the current assessments and returns the risk to the previous state.
-   **Retire**
-   **Navigate to assessment scope**
-   **360 degree**

</td></tr><tr><td>

Respond

</td><td>

This is the state of the risk when the risk response task is in progress. Once the risk response task is closed, the risk is automatically moved into the Monitor state

</td><td>

-   **Save**
-   **Assess**: Pushes the workflow back in the workflow. The in-progress risk response task would be canceled.
-   **Retire**
-   **Navigate to assessment scope**
-   **360 degree**
-   **Return to draft**

</td></tr><tr><td>

Monitor

</td><td>

This is the state of the risk when the risk has been assessed and the response task is closed.If KRIs are defined \(through Metrics\), they are executed to monitor the risk.

</td><td>

-   **Save**
-   **Assess**: Moves the risk back to Assess state and initiates the risk assessment.
-   **Retire**
-   **Navigate to assessment scope**
-   **360 degree**
-   **Return to draft**

</td></tr><tr><td>

Retire

</td><td>

This is the state of the risk when the risk is no longer valid but the organization wants to keep a system of record for audit purposes.

</td><td>

-   **360 degree**
-   **Activate**: Reactivates the risk and moves it back to Draft state.
-   **Navigate to assessment scope**.

</td></tr></tbody>
</table>**Parent Topic:**[Manage risks, risk statements, and risk frameworks](../reference/r_RiskRegister.md)

**Related topics**  


[Manage risks linked to the same risk statement](manage_risks_linked_to_same_risk_stmnt.md)

[Risk hierarchy and scoring](../reference/risk-hierarchy-scoring.md)

