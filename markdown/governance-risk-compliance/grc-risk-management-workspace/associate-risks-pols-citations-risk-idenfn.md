---
title: Associate risks, citations, policies, and controls with a risk identification record
description: After the inherent assessment is completed, you can associate risks, citations, policies, and controls with the risk identification record. You can identify what methods to use to mitigate the risks.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Application risk assessment using Advanced Risk Assessment, Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Associate risks, citations, policies, and controls with a risk identification record

After the inherent assessment is completed, you can associate risks, citations, policies, and controls with the risk identification record. You can identify what methods to use to mitigate the risks.

## Before you begin

Role required: sn\_risk.manager and sn\_compliance.manager

## About this task

Risks, citations, and policies can be associated manually or by using the recommendation engine. The recommendation engine provides automatic suggestions for risk, citations, and policies. The choice to enable the recommendation engine is made in the risk identification configuration record. The choice is available only for the business application table. For the recommendations to be enabled, the risks statements, citations, and policies must have information objects.

## Procedure

1.  Navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Risk Identification** &gt; **All**.

2.  Open the record for which you want to associate risks, citations, and policies.

    This is the record for which you performed the inherent assessments.

3.  Click **Associate Risks**.

    The Information Objects Mapping related list and the Risks related list appear. At this stage, you can either manually add risks or allow the recommendation engine to recommend risks.

4.  To add risks manually, click **Add from library**.

5.  To use the recommendation engine, do the following:

    1.  Click **Recommend Risks** to use the recommendation engine.

    2.  Select the appropriate risk statement and click **Add Risks**.

6.  To add citations and policies, click **Associate Citations and Policies**.

    The Citations related list and Policies related list appear.

7.  Add the required citations and policies either manually from the library or by using the recommended policies and citations.

8.  To associate controls, click **Associate Controls**.

9.  Add the required controls either manually from the library or by clicking **Recommended Controls**.

    The controls are created based on the control objectives.

10. To move a control to the Attest state, select the control and click **Initiate Attestation**.

11. Click **Monitor** to move the record to Monitor state.


-   **[Recommendation engine for risk and compliance mapping](../concept/recommendation-engine.md)**  
A recommendation engine is a system that suggests products, services, and information to users based on data analysis. A recommendation engine boosts revenues and other essential metrics.
-   **[Information objects](../reference/information-objects.md)**  
Information objects are a part of the information portfolio management capability in the Application Portfolio Management application.

**Parent Topic:**[Application risk assessment using Advanced Risk Assessment](../concept/risk-and-apm-better-together.md)

**Related topics**  


[Recommendation engine for risk and compliance mapping](../concept/recommendation-engine.md)

