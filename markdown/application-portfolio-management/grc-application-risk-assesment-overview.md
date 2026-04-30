---
title: Risk management for business applications
description: Integrate Enterprise Architecture with Governance, Risk, and Compliance \(GRC\) to simplify the work of application owners and risk managers by identifying the risks associated with business applications and adding the controls necessary to mitigate the risks.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Explore, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Risk management for business applications

Integrate Enterprise Architecture with Governance, Risk, and Compliance \(GRC\) to simplify the work of application owners and risk managers by identifying the risks associated with business applications and adding the controls necessary to mitigate the risks.

ServiceNow® Enterprise Architecture integration with Risk Management enables you to determine the inherent and comprehensive risk on a business application and identify tasks to mitigate the risk.

ServiceNow® Enterprise Architecture integration with Policy and Compliance enables you to view the controls determined on a business application, verify whether those controls are compliant, and determine the tasks required to make the business application compliant with the controls.

The key benefits of this integration are:

-   Reduces the time spent by risk managers and application owners on digital risks.
-   Provides faster and efficient communication between the application owners and risk managers.
-   Provides an overview of the digital risk posture of business applications.

## High-level workflow of the GRC and Enterprise Architecture integration solution

The high-level workflow of the GRC and Enterprise Architecture integration solution is as follows:

1.  A business application is created.
2.  Based on the GRC Profile Generation scheduled job that runs in the background, GRC detects a new business application and creates an entity in GRC.
3.  When the new application is created as a GRC entity, a new risk identification record is created.
4.  The risk manager can modify the configuration record and determine the workflow of the assessment. After a risk identification configuration is published, the risk manager can modify only some fields in the configuration record.
5.  A questionnaire is initiated to collect details about the application from the application manager.
6.  The application owner responds to the questionnaire.
7.  The risk manager reviews the responses and sends the questionnaire back if further information or clarification is needed.

    **Note:** The application owner's responses are retained when the questionnaire is sent back.

8.  When the risk manager is satisfied with the responses, the inherent assessment is initiated based on the risk assessment methodology configuration in GRC. For more information, see [Configure inherent assessment](https://www.servicenow.com/docs/access?context=configure-inherent-assessment&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US).
9.  GRC maps the risks and compliance objects based on the entity types.
10. The risk manager reviews the information object mapping.
11. The system executes the recommendation engine based on the algorithm selected in the configuration.
12. The risk manager reviews and maps the recommended risks, policies, and citations based on the associated information objects.
13. The recommended controls based on associated citation policies and risks are associated.
14. The application owner manages the control life cycle by working with relevant stakeholders to implement controls.

**Related topics**  


[Application risk assessment using Advanced Risk Assessment](https://www.servicenow.com/docs/access?context=risk-and-apm-better-together&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)

