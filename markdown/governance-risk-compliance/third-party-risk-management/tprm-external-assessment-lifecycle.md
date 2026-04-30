---
title: Life cycle states of a external assessment
description: The process of collecting assessment data from a third party moves between several states. For example, during the Submitted to third party state, the third party responds to tasks, issues, and works to complete the questionnaires.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Third-party \(external\) risk assessment management, Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Life cycle states of a external assessment

The process of collecting assessment data from a third party moves between several states. For example, during the **Submitted to third party** state, the third party responds to tasks, issues, and works to complete the questionnaires.

## Third-party assessment states

![States of an external assessment.](../image/vrm-states.png "Third-party assessment states")

-   **Draft**

    An external assessment record is opened in the **Draft** state.

    -   **Assessment template:** A set of external questionnaires and document requests that are auto-generated based on IRQ responses. Alternatively, an administrator could manually specify the questionnaires and document requests.
    -   **Risk rating:** The overall risk rating that is auto-generated based on IRQ responses.
    -   **Owner:** The owner is the person who owns an assessment for audit purposes and monitors and manages overall assessment processes. Owners are responsible for confirming that the assessment is completed in a timely fashion by the third party, reviewing their responses, and creating and resolving issues. To drive the assessment to its completion, owners are notified when an assessment reaches a particular milestone. The owner must have the TPR manager or TPR assessor role.
-   **Submitted to third party**

    The questionnaires and document requests for the assessment have been sent to the third-party contact. Internal stakeholders await responses.

-   **Responses received**

    After contacts at the third party have completed all questionnaires and document requests, your internal third-party risk team reviews and analyzes the responses. The team might return particular questions for follow-up, clarification, or missing answers.

-   **Generating observations**

    When all responses are completed, the system can auto-generate issues for incorrect answers.

    Third-party contacts respond to issues. Your internal third-party risk team makes a final determination to accept the responses or remediate the issues.

-   **Finalizing with a third party**

    Your third-party risk team reviews all assessment data. In some cases, the team resets the assessment to the **Draft** state to restart the assessment life cycle.

-   **Closed**

    When all data is acceptable, the assessment is complete and a member of the team closes the assessment. If the engagement will be contracted, the **Closed** state initiates the contract risk process.


**Parent Topic:**[Third-party \(external\) risk assessment management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-extrnl-assessment.md)

