---
title: Managing risk responses
description: A risk response is the strategy used to deal with risks after the risks are assessed.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Advanced Risk Assessment, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Managing risk responses

A risk response is the strategy used to deal with risks after the risks are assessed.

After risks are assessed, the assessor determines how to approach those risks. To deal with the risks, the assessor can choose from the following types of risk responses or strategies:

-   Accept: Accept the risk as it is.
-   Mitigate: Identify and implement additional controls to mitigate the risk.
-   Avoid: Change the plan to completely avoid the risk.
-   Transfer: Transfer or share the risk with a third party.

After an assessor identifies the appropriate risk response strategy, they can create risk response tasks and assign them to users with any of the following roles:

-   sn\_grc.business\_user
-   sn\_grc.business\_user\_lite
-   sn\_risk.implementation\_business\_user \(feature role\)

Each strategy is explained as follows:

-   **Risk acceptance**

    When risk users accept a risk, they provide a plan for how they want to accept the risk, provide a justification for accepting the risk, and seek additional approval from the risk owner. Closure of the acceptance task implies you are accepting this risk for that time period. The risk then moves to the Monitor state. After the specified time period is over, you can re-initiate the workflow to assess the risk and then you can again respond to the risk. The risk owner can then respond with one of the following options:

    -   Approve
    -   Reject
    -   Cancel
    -   Request more information
    -   Decide that it is no longer required
-   **Risk mitigation**

    When risk users choose to mitigate a risk, a risk mitigation task is created. The risk user must provide a plan for how to mitigate the risk and request a review from the risk manager. When the risk mitigation task is in the Draft or Work In Progress state, you can either create more risk-mitigating controls for the risk or add existing controls from the library. The reviewer with the role sn\_risk.manager then reviews the plan and selects one of the following options:

    -   Close
    -   Revert to draft state and provide additional comments
    -   Cancel
    -   Delete
-   **Risk avoidance**

    When risk users choose to avoid a risk, they provide a plan for how they want to avoid the risk and request a review from the risk manager. The reviewer then reviews the plan and can select one of the following options:

    -   Close
    -   Revert to Draft state and provide additional comments
    -   Cancel
    -   Delete
-   **Risk transfer**

    When risk users choose to transfer a risk, they provide a plan for how they want to transfer the risk and request a review from the risk manager. The reviewer then reviews the plan and can select one of the following options:

    -   Close
    -   Revert to Draft state and provide additional comments
    -   Cancel
    -   Delete

**Note:** The risk response workflow is not available for an object assessment.

**Parent Topic:**[Advanced Risk Assessment](../../grc-risk/concept/advanced-risk-assessment.md)

