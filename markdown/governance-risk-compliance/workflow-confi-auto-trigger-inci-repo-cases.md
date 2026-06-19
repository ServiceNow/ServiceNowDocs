---
title: Configure Digital resilience incident reporting
description: Digital Resilience Incident administrators can configure conditions in Workflow Studio to auto-trigger incident reporting in Digital resilience incident reporting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/workflow-confi-auto-trigger-inci-repo-cases.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Configure Digital resilience incident reporting

Digital Resilience Incident administrators can configure conditions in Workflow Studio to auto-trigger incident reporting in Digital resilience incident reporting.

## Setting up templates and modules

Operational Resilience administrators set up Word templates, Template configurations, and the Digital resilience incident \(DRI\) case type required for Digital resilience incident reporting as shown in the example.

\[Omitted image "drir-config-module.png"\] Alt text: Set up the templates.

Configure Word Templates and Template Configurations for generating reports in Microsoft Word format. For more information, see [Generating Microsoft Word reports using Document designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/gen-word-reports.md).

The Digital Resilience Incident Case module lists all Digital Resilience Incident Cases associated with an incident or security incident. A new 'Regulation Mappings' related list is now available in each Digital Resilience Incident Case record. It displays the relationships between entities related to the cases and their corresponding regulations.

## Prerequisite data setup for DRI questionnaires

Several reference questions in the DRI Initial report, Intermediate report, and Final report templates use the legal-entity and third-party tables from the Digital Resilience Third-Party Registers application \(sn\_dora\_accel\_entity and sn\_dora\_accel\_third\_party\). Populate these tables \(manually or via the Excel upload request\) before generating an initial report so that fields such as 'Name of the entity submitting the report', 'LEI code of the financial entity affected', and 'Name of the third party provider' can be filled in by the responder.

For details, see [Maintaining Digital resilience third-party registers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/digi-resi-third-party-registers.md), [Create a third party and enhance digital resilience data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-drtp-reg-third-party.md), and [Create a legal entity and enhance digital resilience data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-legal-entity.md).

## Conditions for setting up the Workflow

Workflow Studio contains preconfigured flows and conditions for creating DRI case tasks from incidents in the Incident Management or Security Incident Response applications. Access the Digital resilience incident reporting flows by navigating to **Workflow Studio** &gt; **Flows** &gt; **Flow Designer**.

The following flows, previously used in the Digital resilience incident reporting application, have been deprecated:

1.  Digital Resilience Incident Flow
2.  Digital Resilience SIR Flow
3.  DRI Business service Trigger

**Note:** To use the previously deployed flows, deactivate the new flows \(listed in this section\) and then activate the Digital Resilience Incident Flow, Digital Resilience SIR Flow, and DRI Business Service Trigger Flow.

The following flows in Digital resilience incident reporting are still active:

1.  Digital Resilience Incident Approval Flow
2.  DRI case create/update on incident update
3.  DRI case create/update on security incident update
4.  DRI case creation on incident entity insert
5.  DRI case creation on SIR entity insert

New flows have been introduced in Digital resilience incident reporting to manage action tasks, regulations, and trigger conditions for multiple regulators, as illustrated in the example:

1.  Action task automation for regulation addition
2.  Action task automation on action task update
3.  Action task automation on DRI case updates
4.  Action task automation on regulation updates
5.  DRI Business Service Trigger For Multiple Regulators

\[Omitted image "trigger-flows-wf-studio.png"\] Alt text: Digital resilience incident reporting flows. For the text description, refer to the text that precedes this image.

**Note:** If the Security Incident Response application is installed in your instance, flows related to the security incidents \(SIR\) are listed in the Flows list view.

The Digital Resilience Incident Flow and Digital Resilience SIR Flow are prebuilt into the Digital resilience incident reporting application. The flow configuration impacts all incident records in the instance. As administrators of the Operational Resilience application, you can update \(customize\) the flow configurations to meet your organizational requirements as shown in the example.

\[Omitted image "flow-conditions.png"\] Alt text: Conditions. For the text description of the conditions, refer to the text that follows.

-   **Insert condition**

    Conditions such as the priority of the incident is Critical, the urgency is High, and the incident has been open for more than 24 hours, are prebuilt in the flow. When all these conditions are met, it’s automatically reported in the Digital resilience incident reporting application.

-   **Update condition**

    When an incident is reopened or updated, that classification condition is also defined in the flow. When the configured conditions are met, the incident is reported in the Digital resilience incident reporting application.


**Note:** The Digital resilience incident reporting application is licensed under the Integrated Risk Management \(IRM\) application family.

## Required and optional plugins

The Digital resilience incident reporting application is available from the ServiceNow Store. This section details its required and optional plugins.

|Application name|Plugin|
|----------------|------|
|Document designer|\(com.sn\_grc\_doc\_design\)|
|Digital Operational Resilience Management|\(com.sn\_app\_grc\_digital\_resilience\)|
|GRC|\(app-grc\)|
|GRC Base Workspace|\(app-grc-base-workspace\)|
|GRC: Compliance Case Management|\(app-grc-case-mgmt\)|
|GRC Operational Resilience|app-grc-operational-resilience \(com.sn\_grc\_oper\_res\)|
|GRC: Policy and Compliance Management|\(com.sn\_compliance\)|
|Regulatory Agency Library|\(com.sn\_reg\_body\_mgmt\)|
|Reusable impact framework|\(sn-reusable-impact-framework\)|
|Smart Assessment impact automation|\(app-smart-assessment-impact-automation\)|
|Smart Assessment response automation|\(app-smart-assessment-response-automation\)|
|Smart Assessment Core|\(sn\_smart\_asmt\)|
|Smart Assessment designer|\(sn\_smart\_asmt\_desg\)|

|Application name|Plugin|
|----------------|------|
|Security Incident Response|\(app-sir\)|
|Digital Resilience Third-party Information Register|\(sn\_info\_reg\)|

