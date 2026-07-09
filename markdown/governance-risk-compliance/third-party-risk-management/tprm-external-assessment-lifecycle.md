---
title: External assessment lifecycle states
description: The process of collecting assessment data from a third party moves through several states. For example, during the Submitted to third party state, the third party responds to tasks, issues, and works to complete the questionnaires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-external-assessment-lifecycle.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-06-30"
reading_time_minutes: 3
breadcrumb: [Third-party \(external\) risk assessment management, Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# External assessment lifecycle states

The process of collecting assessment data from a third party moves through several states. For example, during the **Submitted to third party** state, the third party responds to tasks, issues, and works to complete the questionnaires.

## Third-party assessment states

\[Omitted image "vrm-states.png"\] Alt text: States of an external assessment.

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


**Note:** After the questionnaire is completed and approved, the assessment can proceed to the next stage of onboarding or contracting. The contract process does not begin until the approval process is complete.

## Questionnaire states

In the Classic engine, questionnaire requests \(previously called assessment instances\) and questionnaires themselves have separate state systems. The SAE uses a simplified set of questionnaire states.

**Note:** If you upgraded from Yokohama or earlier and enabled the Smart Assessment Engine \(SAE\) in Zurich, questionnaire states are simplified to the three states shown above. For information about assessment status changes, see [Third-party Risk Management upgrade information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-tprm-upgrade-info.md).

Questionnaire requests track the overall status of a questionnaire request sent to a third party.

|Questionnaire request state|Description|
|---------------------------|-----------|
|**Ready to take**|Questionnaire request is prepared and ready to be sent to the third party.|
|**In progress**|Questionnaire request has been sent to the third party and is being completed.|
|**Complete**|Questionnaire request is complete and the third party has submitted their response.|
|**Canceled**|Questionnaire request is canceled and is no longer active.|

Questionnaires themselves move through additional states that track the workflow of completing and reviewing the questionnaire content.

|Questionnaire state|Description|
|-------------------|-----------|
|**New**|Questionnaire is created but not yet sent to the third party.|
|**Submitted**|Questionnaire is sent to the third party for completion.|
|**In Progress**|Third party is actively working on the questionnaire.|
|**Received**|Third party submits the completed questionnaire for review.|
|**Returned**|Questionnaire is sent back to the third party for updates and corrections.|
|**Canceled**|Questionnaire is canceled and is no longer active.|

|Questionnaire state|Description|
|-------------------|-----------|
|**In progress**|Questionnaire is active and being completed by the third party.|
|**Completed**|Questionnaire is finished and submitted.|
|**Canceled**|Questionnaire is canceled before completion.|

**Parent Topic:**[Third-party \(external\) risk assessment management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-ws-dd-mgt-pg-extrnl-assessment.md)

