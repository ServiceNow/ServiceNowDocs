---
title: Advanced Risk release notes
description: The ServiceNow Advanced Risk application enables you to identify, analyze, evaluate, treat, and monitor risks that could impact your organization in achieving its business objectives. Advanced Risk was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
---

# Advanced Risk release notes

The ServiceNow® Advanced Risk application enables you to identify, analyze, evaluate, treat, and monitor risks that could impact your organization in achieving its business objectives. Advanced Risk was enhanced and updated in the Zurich release.

## Advanced Risk highlights for the Zurich release

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

-   Use the Risk Suggestion AI Agent to discover potential risks for an entity, giving risk managers better insights for informed decision-making.
-   Use the risk reporting view to view all assessments under a specific Risk Assessment Methodology \(RAM\), including factor responses, scores, issues, and risks.
-   Use generative AI to generate risk event summary to quickly understand the risk event key details for faster decisions.
-   Assess multiple risks and controls side-by-side, make bulk edits, and prioritize entries efficiently using the spreadsheet-style layout.
-   Use matrix report in the Risk Workspace to assess and analyze the risk posture of your organization.
-   Use large language models \(LLMs\) from the third party providers to generate the risk assessment summary.

See [Advanced Risk Assessment](https://www.servicenow.com/docs/access?context=advanced-risk-assessment&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Advanced Risk is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Identify risks for an entity](https://www.servicenow.com/docs/access?context=suggest-potential-risks-workflow&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    If you’re a Workspace user with the sn\_grc\_sharegenai.risk\_suggestion\_aiagent\_user role, you can use the Risk Suggestion AI Agent to identify risks related to an entity. The AI agent analyzes the entity and suggests relevant risks from various sources, consolidating them into a reviewable list to verify for accuracy. Risk managers can then confirm and promote these risks to the risk register for further assessment. This feature automates risk discovery, helping identify potential risks and prepare for compliance requirements.

-   **[Reporting views from Risk Assessment Methodology](https://www.servicenow.com/docs/access?context=reporting-views-from-ram&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The reporting view provides an overview of all assessments under a specific Risk Assessment Methodology \(RAM\). It consolidates assessment data such as factor responses, scores, issues, controls, and associated risks into a single structure. When a RAM is published, the system automatically creates this view, which you can use to review assessments and build custom reports. It simplifies report and dashboard creation for risk assessments.

    **Note:** Automatic creation of Reporting views is not supported on Xanadu. For instructions on creating them manually, refer to [KB2547071](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2547071)

-   **[Risk event summarization](https://www.servicenow.com/docs/access?context=generate-risk-event-summary-in-the-risk-workspace&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Generate risk event summary using the Now Assist for IRM application. Risk event summarisation is a Generative AI driven capability that generates clear and consistent summaries automatically. It reduces the need for manual effort, helps risk managers save time, and enables approvers to quickly understand the key details for faster decisions. Check your entitlements to confirm whether you have access to risk event summarization.

-   **[Grid based risk and control assessment](https://www.servicenow.com/docs/access?context=perform-assessment-risk-assessment-project-grid-view&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Gain efficient control over risk assessments with the new grid-based Risk and Control Self Assessment \(RCSA\). Quickly compare, edit, and prioritize risks and controls using the flexible, spreadsheet-style interface. Use side-by-side views and bulk editing to complete assessments faster.

-   **[Matrix report in Risk Workspace](https://www.servicenow.com/docs/access?context=matrix-report-in-risk-workspace&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Access and analyze the risk posture of your organization using entity-related data, such as risks, controls, KRIs, and events in a centralized, configurable grid-based view. This feature reduces time spent switching views and helps risk managers assess data more easily, leading to more proactive and streamlined risk management.

-   **[Support third party large language models](https://www.servicenow.com/docs/access?context=generate-risk-assessment-summary-genai&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Risk assessment summarization and Risk event summarization support the LLMs from the third party providers, such as Anthropic Claude, Google Gemini, and OpenAI, in addition to Now LLM. This enhancement gives you greater flexibility to choose the model that best fits your organization’s needs for generating risk assessment and risk event summaries.


## UI changes

-   **[Downstream risks related list](https://www.servicenow.com/docs/access?context=entities-in-risk-ws&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The Downstream risks related list on the entity record page has been renamed Risks.

-   **Summary section**

    In the classic UI, the Summary section on the risk event record has been renamed Impacts.

    In the Risk Workspace, the Summary section on the risk event overview page has been renamed Impacts and approvals.


## Changed in this release

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

## Removed in this release

To enhance the Risk Workspace home page load performance and reduce latency, the **Tasks** widget has been removed from the home page.

## Activation information

Install Advanced Risk by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Reflow for Risk heatmap**

    The Risk Heatmap component was updated to support reﬂow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

    This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations.


## Related ServiceNow applications and features

-   **[GRC Risk Management](https://www.servicenow.com/docs/access?context=grc-risk-overview&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Use the Risk Management application with the ServiceNow® Advanced Risk application to identify and monitor high-impact risks, improve your risk-based decision-making, and reduce reaction time.

-   **[GRC Risk Workspace](https://www.servicenow.com/docs/access?context=risk-workspace&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Using Risk Workspace with the ServiceNow® Advanced Risk application provides a simplified user experience with a single-pane view for all your risk-related activities.


**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

