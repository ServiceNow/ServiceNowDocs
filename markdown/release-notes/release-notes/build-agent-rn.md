---
title: Build Agent release notes
description: The ServiceNow Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-04"
reading_time_minutes: 6
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
---

# Build Agent release notes

The ServiceNow® Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release.

## Build Agent highlights for the Australia release

-   Use Build Agent in ServiceNow Studio.
-   Work with additional Model Context Protocol \(MCP\) support.
-   Create apps and metadata in the global scope.
-   Choose from newly supported models.
-   Access update sets created in Build Agent directly from the chat panel.

See  for more information.

## New in the Australia release

-   **MCP server support in ServiceNow Studio**

    Connect Build Agent to external MCP servers in ServiceNow Studio. Previously, MCP server connectivity was only available in the ServiceNow IDE.

-   **Additional MCP server integrations**

    Integrate Build Agent with newly supported MCP servers.

-   **Access update sets from Build Agent**

    View update sets created by Build Agent from within the chat panel in ServiceNow Studio. Each checkpoint includes a button that opens the relevant update set in a new tab.

-   **UI validation tool in ServiceNow Studio**

    Validate user interface output during app creation with the UI validation tool in Build Agent, now available in ServiceNow Studio.

-   **Search retrieval tool support**

    Use the Search retrieval tool to enable agents to fetch and present relevant information from configured data sources in response to user queries. Agents can surface knowledge articles, catalog items, and other indexed content directly within the agentic workflow, reducing the need for users to navigate to separate search interfaces.

-   **Support for more file types**

    Upload more types of files to Build Agent to describe what you want to build, including images, documents, and text and code files.


-   **MCP Client integration**

    Connect Build Agent to external MCP servers to bring tools and data sources directly into your build workflow. External resources participate alongside Build Agent on the ServiceNow AI Platform, which helps reduce context switching and manual data transfer between tools.

-   ****

    Turn business requirements into fully configured agents, skills, and agentic workflows for your custom applications. Build Agent inspects the existing tables, roles, business rules, and metadata in your app to create tailored in-app agents and tools.

-   **Test Agent for Build Agent**

    Use Test Agent to execute Automated Test Framework \(ATF\) tests right from the Build Agent chat panel for test artifacts created in the same session. When tests fail, the generated tests and test results are saved in the standard ATF record tables and can be scheduled for continued regression testing for the app. If tests are edited by the test agent after troubleshooting, those edits are automatically saved to the test records.

-   **UI validation tool**

    Validate user interface output during Build Agent app creation in the ServiceNow IDE using the integrated UI validation, which runs Playwright-based UI checks on Cloud Runner and surfaces failures with diagnostic context directly in the Build Agent panel.

-   **Semantic search for instance artifact discovery**

    Use semantic search in Build Agent to locate relevant instance artifacts, including tables, scripts, and business rules during build and edit tasks. Find files, applications, and knowledge on your instance based on meaning instead of exact keywords.

-   **Additional model support**

    Choose the provider and model that fits your organizational needs in Build Agent, which now supports Anthropic Claude on AWS Sonnet 4.6 and Azure OpenAI GPT 5.4.

-   **Expanded metadata support**

    Work with more metadata types in Build Agent, which now supports flows, Service Catalog configurations, inbound email actions, dictionary overrides, choice lists, condition builder query conditions, and enhanced Service Portal capabilities.

-   **Contextual launch for Build Agent**

    Include context from ServiceNow Studio tabs and component preview screens when you open Build Agent, which helps reduce the need to manually search for and specify context in the chat panel.


-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
    Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **Additional metadata support**

    Work with more metadata types in Build Agent, which now supports email.


-   ****

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

-   **New button prompt to add AI to an app**

    A new **Add AI** button when you first open the Build Agent chat panel starts a guided conversation to help you define and generate a skill or agent.

    **Note:** You must have a Now Assist for Creator license for the new button to appear.

-   **Open Build Agent from ServiceNow Studio banner**

    A new icon \[Omitted image "ba-sns-ai-sparkle.png"\] Alt text: in the ServiceNow Studio application banner provides another way to access Build Agent.


-   **Generated artifact preview**

    Preview generated tables, flows, and scripts that Build Agent creates in ServiceNow Studio so you can review and approve changes inline before saving or committing them to the application.


## Changed in this release

-   **Build Agent version parity for PDIs**

    Personal development instances \(PDIs\) are now updated to match the latest Build Agent version, delivering a consistent experience across both personal and production-track instances. Developers testing and building on PDIs have access to the same capabilities available in production environments.

-   **Updated interaction limits**

    To provide developers more room to iterate, the following Build Agent limits have been increased:

    -   Build Agent \(Trial\): 100 prompts per instance per 30-day cycle
    -   PDIs: 25 prompts per instance per cycle
    **Note:** Limits are per-instance, not per-user. Only submitted prompts, which doesn't include plan approvals, contribute to the limit.


-   **Support for global scope**

    Build apps and metadata in the global scope.


## Activation information

Build Agent is a ServiceNow AI Platform feature that is active by default.

**Note:** Build Agent is dependent on Now Assist for Creator. For more information, see [Now Assist for Creator release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-for-creator-rn.md).

## Related ServiceNow applications and features

-   ****

    Use ServiceNow Studio to build, configure, and deploy custom ServiceNow apps from a single development environment.

-   ****

    Create and develop scoped applications in source code in an integrated development environment \(IDE\) on the ServiceNow AI Platform to improve collaboration across development teams and accelerate application development.

-   ****

    Access generative AI skills and AI agents that can help you develop on the ServiceNow AI Platform efficiently.

-   ****

    Use vibe coding and ServiceNow agentic-assisted app building tools to describe your goals in natural language, and have the ServiceNow AI Platform generate full-stack applications, workflows, and integrations.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/build-automate-rn-landing.md)

