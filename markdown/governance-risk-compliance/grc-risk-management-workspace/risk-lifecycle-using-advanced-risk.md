---
title: Workflow of a risk using Advanced Risk
description: When you migrate to advanced risk assessment, you can view the various states of risks and take the necessary actions from the risk form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/grc-risk-management-workspace/risk-lifecycle-using-advanced-risk.html
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Manage risks, risk statements, and risk frameworks, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Workflow of a risk using Advanced Risk

When you migrate to advanced risk assessment, you can view the various states of risks and take the necessary actions from the risk form.

When your risk administrator enables the **Migrate to Advanced Risk Assessments** property located under **Advanced Risk Assessment** &gt; **Administration** &gt; **Properties**, the life cycle of classic or legacy risks changes. You can also initiate a risk assessment directly from the risk form.

**Note:** After you enable this property, you can't disable it.

Before version 14.0, when the **Migrate to Advanced Risk Assessments** property was enabled, risks were only classified as either active or inactive. Starting with version 14.0, as a risk owner, when you enable Advanced Risk, you can view the following states of your risks.

1.  Draft
2.  Assess
3.  Respond
4.  Review
5.  Monitor
6.  Retired

\[Omitted image "risk-lifecycle-ara.png"\] Alt text: States of a risk with advanced risk assessments enabled.

The following table describes all states and the actions available for each state.

<table id="table_q3p_y4j_xsb"><thead><tr><th>

State

</th><th>

Description

</th><th>

Actions available

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

State of a risk when it is created by the second line of defense or identified by the first line of defense.The objective in this state is to map and identify the risk pertaining to your organization. If you modify the entity or the primary risk assessment methodology \(RAM\) for a risk, the risk state updates based on the primary RAM's latest assessment.

</td><td>

-   **Save**
-   **Assess**: Pushes the workflow and initiates the risk assessment.
-   **Monitor**: Skips assessment and moves the risk directly to the Monitor state.
-   **Retire**: The risk is retired along with all underlying risk assessment and risk response.
-   **Navigate to assessment scope**: Shortcut to risk assessment scope. The primary risk assessment methodology is passed.
-   **360 degree**: View the complete 360-degree relationships for the risk.

</td></tr><tr><td>

Assess

</td><td>

State of a risk when advanced risk assessment is initiated and being performed. If there is a response strategy, the risk moves to the Respond state. Otherwise, it moves to the Monitor state after the assessment is completed.

</td><td>

-   **Save**
-   **View assessment**: Navigates to the actual risk assessment form.
-   **Cancel assessment**: Cancels the current assessment. The respective risk assessor is notified.
-   **Return to draft**: Cancels the current assessments and returns the risk to the previous state.
-   **Retire**
-   **Navigate to assessment scope**
-   **360 degree**

</td></tr><tr><td>

Respond

</td><td>

State of the risk when the risk response task is in progress.After the risk response task is closed, the risk moves to the Monitor state.

</td><td>

-   **Save**
-   **Assess**: Returns the risk to the Assess state. The in-progress risk response task is canceled.
-   **Retire**
-   **Navigate to assessment scope**
-   **360 degree**
-   **Return to draft**

</td></tr><tr><td>

Review

</td><td>

State of a risk after an assessment is submitted for review. A user with the sn\_risk.user role can submit an assessed risk for review if the risk has no attestation. From this state, a risk manager can move the risk to Monitor or Respond.

</td><td>

-   **Monitor**: Available to users with the sn\_risk.manager role.
-   **Respond**: Available to users with the sn\_risk.manager role.
-   **Return to draft**
-   **Retire**

</td></tr><tr><td>

Monitor

</td><td>

State of the risk when the risk has been assessed and the response task is closed.If KRIs are defined through Metrics, they run to monitor the risk.

</td><td>

-   **Save**
-   **Assess**: Moves the risk back to Assess state and initiates the risk assessment.
-   **Retire**
-   **Navigate to assessment scope**
-   **360 degree**
-   **Return to draft**

</td></tr><tr><td>

Retired

</td><td>

State of the risk when the risk is no longer valid but the organization wants to retain a record for audit purposes.

</td><td>

-   **360 degree**
-   **Activate**: Reactivates the risk and moves it back to Draft state.
-   **Navigate to assessment scope**.

</td></tr></tbody>
</table>**Parent Topic:**[Manage risks, risk statements, and risk frameworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/grc-risk-management-workspace/r_RiskRegister.md)

**Related topics**  


[Manage risks linked to the same risk statement]()

[Risk hierarchy and scoring]()

