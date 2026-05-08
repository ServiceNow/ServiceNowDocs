---
title: Build Agent release notes
description: The ServiceNow Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-30"
reading_time_minutes: 5
---

# Build Agent release notes

The ServiceNow® Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release.

## Build Agent highlights for the Australia release

-   Use Build Agent in ServiceNow Studio.
-   Extended Model Context Protocol \(MCP\) support.
-   Support for the global scope for apps and metadata.
-   Upgraded support for additional models.
-   Extended metadata support.

See Build Agent for more information.

## New in the Australia release

-   **MCP Client integration**

    Connect Build Agent to external MCP servers to bring tools and data sources directly into your build workflow. External resources participate alongside Build Agent on the ServiceNow AI Platform, which helps reduce context switching and manual data transfer between tools.

-   **Create agentic workflows, agents, and skills**

    Turn business requirements into fully configured agents, skills, and agentic workflows for your custom applications. Build Agent inspects the existing tables, roles, business rules, and metadata in your app to create tailored in-app agents and tools.

-   **Test Agent for Build Agent**

    Use Test Agent to execute Automated Test Framework \(ATF\) tests right from the Build Agent chat panel for test artifacts created in the same session. When tests fail, the generated tests and test results are saved in the standard ATF record tables and can be scheduled for continued regression testing for the app. If tests are edited by the test agent after troubleshooting, those edits are automatically saved to the test records.

-   **UI validation tool**

    Validate user interface output automatically during Build Agent app creation using the integrated UI validation, which runs Playwright-based UI checks on Cloud Runner and surfaces failures with diagnostic context directly in the Build Agent panel.

-   **Semantic search for instance artifact discovery**

    Use semantic search in Build Agent to locate relevant instance artifacts, including tables, scripts, and business rules during build and edit tasks. Find files, applications, and knowledge on your instance based on meaning instead of exact keywords.

-   **Additional model support**

    Choose the provider and model that fits your organizational needs in Build Agent, which now supports Anthropic Claude on AWS Sonnet 4.6 and Azure OpenAI GPT 5.4.

-   **Expanded metadata support**

    Work with more metadata types in Build Agent, which now supports flows, Service Catalog configurations, inbound email actions, dictionary overrides, choice lists, condition builder query conditions, and enhanced Service Portal capabilities.

-   **Contextual launch for Build Agent**

    Build Agent pulls context from ServiceNow Studio tabs and component preview screens which helps reduce the need to manually search for and specify context within the Build Agent chat panel.


-   **ServiceNow product tiers**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **Additional metadata support**

    Work with more metadata types inBuild Agent, which now supports email.


-   **Build Agent in ServiceNow Studio**

    Access Build Agent in ServiceNow Studio to build apps conversationally in a consolidated development environment.

-   **Improved LLM support**

    Use AWS Claude Opus 4.6 and Sonnet 4.5 in Build Agent for contextual conversations.

-   **New metadata support**

    Work with more metadata types, as Build Agent now supports the following:

    -   Email integration
    -   List controls
    -   Service Catalog items
    -   UI components
    -   UI policies
    -   UI views
    -   Workspaces

## UI changes

-   **Generated artifact preview**

    Preview generated tables, flows, and scripts that Build Agent creates in ServiceNow Studio so you can review and approve changes inline before saving or committing them to the application.


## Changed in this release

-   **Build Agent version parity for PDIs**

    Personal Development Instances \(PDIs\) are now updated to match the latest Build Agent version, delivering a consistent experience across both personal and production-track instances. Developers testing and building on PDIs have access to the same capabilities available in production environments.

-   **Updated interaction limits**

    To provide developers more room to iterate, the following Build Agent limits have been increased:

    -   Build Agent \(Trial\): 100 prompts per instance per 30-day cycle
    -   PDIs: 25 prompts per instance per cycle
    **Note:** Limits are per-instance, not per-user. Only submitted prompts, which doesn't include plan approvals, contribute to the limit.


-   **Support for global scope**

    Build apps and metadata in the global scope.


## Activation information

Build Agent is a ServiceNow AI Platform feature that is active by default.

**Note:** Build Agent is dependent on Now Assist for Creator. For more information, see [Now Assist for Creator release notes](now-assist-for-creator-rn.md).

## Related ServiceNow applications and features

-   **ServiceNow Studio**

    Use ServiceNow Studio to build, configure, and deploy custom ServiceNow apps from a single development environment.

-   **ServiceNow IDE**

    Create and develop scoped applications in source code in an integrated development environment \(IDE\) on the ServiceNow AI Platform to improve collaboration across development teams and accelerate application development.

-   **Now Assist for Creator**

    Access generative AI skills and AI agents that can help you develop on the ServiceNow AI Platform efficiently.

-   **Vibe coding and AI-assisted development on the ServiceNow AI Platform**

    Use vibe coding and ServiceNow agentic-assisted app building tools to describe your goals in natural language, and have the ServiceNow AI Platform generate full-stack applications, workflows, and integrations.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

