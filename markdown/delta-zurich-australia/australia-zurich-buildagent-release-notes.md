---
title: Combined Build Agent release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Build Agent from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-buildagent-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 18
breadcrumb: [Products combined by family]
---

# Combined Build Agent release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Build Agent from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Build Agent release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Build Agent to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Build Agent.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Automatic test maintenance](https://www.servicenow.com/docs/access?context=build-agent-testing&family=zurich&ft:locale=en-US)**

Test Agent in Build Agent automatically updates or removes Automated Test Framework tests that are outdated as your application changes, keeping the test suite aligned with the current state of your code. UI tests don't run automatically during updates, because they can take additional time and interrupt the development flow. To automatically keep tests synced, you must enable the new **Sync ATF tests with app** setting in Build Agent.

-   **[UI testing](https://www.servicenow.com/docs/access?context=build-agent-testing&family=zurich&ft:locale=en-US)**

Generate comprehensive UI tests for applications you build with Build Agent. UI testing extends the existing functional test capability to cover browser-level interactions, such as multi-step page navigation flows. To run UI tests automatically on update, you must enable the **Run UI ATF tests** setting in Test Agent.

**Note:** You can also prompt Build Agent to generate UI tests.

-   **[Get prompted to test](https://www.servicenow.com/docs/access?context=build-agent-testing&family=zurich&ft:locale=en-US)**

After each development action, Build Agent can prompt you to generate ATF tests for what you just built. Accept or decline the prompt at each step to keep test coverage in sync with your development work.

**Note:** You must enable getting prompted to test in the Build Agent settings.

-   **[SDK test execution](https://www.servicenow.com/docs/access?context=build-agent-testing&family=zurich&ft:locale=en-US)**

Execute ATF tests from the ServiceNow SDK. Test execution and troubleshooting were previously available only in ServiceNow Studio and the ServiceNow IDE.

-   **[Updated model support](https://www.servicenow.com/docs/access?context=ba-models-versions&family=zurich&ft:locale=en-US)**

The following new models are supported for Build Agent:

    -   Gemini 3.5 is now the default model for Google
    -   GPT 5.5 is now the default model for Azure OpenAI
    -   Opus 4.8
-   **[Change model version in chat](https://www.servicenow.com/docs/access?context=ba-models-versions&family=zurich&ft:locale=en-US)**

Change the AI model versions in Build Agent without navigating out to the table on the ServiceNow AI Platform.

-   **[Define custom skills and rules](https://www.servicenow.com/docs/access?context=ba-configure-custom-skills-rules&family=zurich&ft:locale=en-US)**

Create custom skills and rules to control how Build Agent behaves during a session.

    -   Custom rules are injected into the system prompt on every run, so Build Agent behaves consistently at the scope you choose.
    -   Custom skills provide internal guidelines for specific tasks. You can apply skills and rules at the instance level, application level, or user level.
-   **[Background script execution](https://www.servicenow.com/docs/access?context=build-agent-tools&family=zurich&ft:locale=en-US)**

Run server-side scripts as part of app-building flows in Build Agent using the new run script and rollback script tools. Before a script runs, an approval prompt shows the generated script, its stated intent, and the target application scope so you can review the operation before approving.

-   **[Conversation handoff to Build Agent](https://www.servicenow.com/docs/access?context=access-build-agent&family=zurich&ft:locale=en-US)**

Build applications by receiving context from ServiceNow Otto \(formerly Now Assist\) conversations and continuing work in Build Agent without repeating yourself. The full conversation transcript is attached to the session so you can reference details beyond the summary. Conversation handoff is available only in ServiceNow Studio.

-   **[Use Build Agent in a sandbox](https://www.servicenow.com/docs/access?context=access-build-agent&family=zurich&ft:locale=en-US)**

Use Build Agent in Developer Sandboxes to isolate development and provide admin access to developers in a protected environment.

-   **[View MCP tools per server](https://www.servicenow.com/docs/access?context=accelerate-design-to-development-with-figma-mcp-server&family=zurich&ft:locale=en-US)**

View the list of tools available on each connected MCP server in the Build Agent settings panel.

-   **[Knowledge base access metadata support](https://www.servicenow.com/docs/access?context=build-agent-supported-metadata&family=zurich&ft:locale=en-US)**

Work with the knowledge base access metadata type in Build Agent.


-   **[Web search tool](https://www.servicenow.com/docs/access?context=build-agent-tools&family=zurich&ft:locale=en-US)**

Access public web content from Build Agent using two new search tools. Use the web search tool to find information on the public web, and use the web fetch tool to retrieve content from a URL that you supply.

-   **[Consolidated update sets](https://www.servicenow.com/docs/access?context=ba-update-sets&family=zurich&ft:locale=en-US)**

Track changes generated by Build Agent and manual edits in update sets for checkpointing and rollback. Update sets can be merged into a single update set before deployment. All changes to your application are captured in the same scope, making it easier to review what was modified and merge updates to other environments.

-   **[Expanded metadata support](https://www.servicenow.com/docs/access?context=build-agent-supported-metadata&family=zurich&ft:locale=en-US)**

Work with more metadata types in Build Agent, which now supports connection and credential alias, data lookup, playbooks, rest message/HTTP method, and user criteria.


-   **[MCP server support in ServiceNow Studio](https://www.servicenow.com/docs/access?context=ba-connct-mcp-server&family=zurich&ft:locale=en-US)**

Connect Build Agent to external MCP servers in ServiceNow Studio. Previously, MCP server connectivity was only available in the ServiceNow IDE.

-   **[Additional MCP server integrations](https://www.servicenow.com/docs/access?context=accelerate-design-to-development-with-figma-mcp-server&family=zurich&ft:locale=en-US)**

Integrate Build Agent with newly supported MCP servers.

-   **[Access update sets from Build Agent](https://www.servicenow.com/docs/access?context=ba-update-sets&family=zurich&ft:locale=en-US)**

View update sets created by Build Agent from within the chat panel in ServiceNow Studio. Each checkpoint includes a button that opens the relevant update set in a new tab.

-   **[UI validation tool in ServiceNow Studio](https://www.servicenow.com/docs/access?context=build-agent-tools&family=zurich&ft:locale=en-US)**

Validate user interface output during app creation with the UI validation tool in Build Agent, available in ServiceNow Studio.

-   **[Search retrieval tool support](https://www.servicenow.com/docs/access?context=ba-about-creating-in-app-agents&family=zurich&ft:locale=en-US)**

Use the Search retrieval tool to enable agents to fetch and present relevant information from configured data sources in response to user queries. Agents can retrieve knowledge articles, catalog items, and other indexed content directly within the agentic workflow, reducing the need for users to navigate to separate search interfaces.

-   **[Support for more file types](https://www.servicenow.com/docs/access?context=ba-supported-file-types&family=zurich&ft:locale=en-US)**

Upload more types of files to Build Agent to describe what you want to build, including images, documents, and text and code files.

-   **[Expanded metadata support](https://www.servicenow.com/docs/access?context=build-agent-supported-metadata&family=zurich&ft:locale=en-US)**

Work with more metadata types in Build Agent, which now supports assignment rules, forms, and data policies.


-   **[MCP Client integration](https://www.servicenow.com/docs/access?context=ba-connct-mcp-server&family=zurich&ft:locale=en-US)**

Connect Build Agent to external MCP servers to bring tools and data sources directly into your build workflow. External resources participate alongside Build Agent on the ServiceNow AI Platform, which reduces the need to switch between tools and transfer data manually.

-   **[Create workflows, agents, and skills](https://www.servicenow.com/docs/access?context=create-custom-ai-agent&family=zurich&ft:locale=en-US)**

Turn business requirements into fully configured agents, skills, and agentic workflows for your custom applications. Build Agent inspects the existing tables, roles, business rules, and metadata in your app to create tailored in-app agents and tools.

-   **[Test Agent for Build Agent](https://www.servicenow.com/docs/access?context=build-agent-testing&family=zurich&ft:locale=en-US)**

Use Test Agent to execute Automated Test Framework \(ATF\) tests right from the Build Agent chat panel for test artifacts created in the same session. When tests fail, the generated tests and test results are saved in the standard ATF record tables and can be scheduled for continued regression testing for the app. If Test Agent modifies tests during troubleshooting, those changes are automatically saved to the test records.

-   **[UI validation tool](https://www.servicenow.com/docs/access?context=exploring-build-agent&family=zurich&ft:locale=en-US)**

Validate user interface output during Build Agent app creation in the ServiceNow IDE using the integrated UI validation. UI validation runs Playwright-based UI checks on Cloud Runner and surfaces failures with diagnostic context directly in the Build Agent panel.

-   **[Semantic search for instance artifact discovery](https://www.servicenow.com/docs/access?context=build-agent-tools&family=zurich&ft:locale=en-US)**

Use semantic search in Build Agent to locate relevant instance artifacts, including tables, scripts, and business rules during build and edit tasks. Find files, applications, and knowledge on your instance based on meaning instead of exact keywords.

-   **[Additional model support](https://www.servicenow.com/docs/access?context=exploring-build-agent&family=zurich&ft:locale=en-US)**

Choose the provider and model that fits your organizational needs in Build Agent, which now supports Anthropic Claude on AWS Sonnet 4.6 and Azure OpenAI GPT 5.4.

-   **[Expanded metadata support](https://www.servicenow.com/docs/access?context=build-agent-supported-metadata&family=zurich&ft:locale=en-US)**

Work with more metadata types in Build Agent, which now supports flows, Service Catalog configurations, inbound email actions, dictionary overrides, choice lists, condition builder query conditions, and enhanced Service Portal capabilities.

-   **[Contextual launch for Build Agent](https://www.servicenow.com/docs/access?context=access-build-agent&family=zurich&ft:locale=en-US)**

Include context from ServiceNow Studio tabs and component preview screens when you open Build Agent. Context helps reduce the need to manually search for and specify context in the chat panel.


-   **[Additional metadata support](https://www.servicenow.com/docs/access?context=build-agent-supported-metadata&family=zurich&ft:locale=en-US)**

Work with more metadata types in Build Agent, which now supports email.


-   **[Build Agent in ServiceNow Studio](https://www.servicenow.com/docs/access?context=build-agent-in-servicenow-studio&family=zurich&ft:locale=en-US)**

Access Build Agent in ServiceNow Studio to build apps conversationally in a consolidated development environment.

-   **[Improved LLM support](https://www.servicenow.com/docs/access?context=exploring-build-agent&family=zurich&ft:locale=en-US)**

Use AWS Claude Opus 4.6 and Sonnet 4.5 in Build Agent for contextual conversations.

-   **[New metadata support](https://www.servicenow.com/docs/access?context=build-agent-supported-metadata&family=zurich&ft:locale=en-US)**

Work with more metadata types, as Build Agent now supports the following:

    -   Email integration
    -   List controls
    -   Service Catalog items
    -   UI components
    -   UI policies
    -   UI views
    -   Workspaces

</td></tr><tr><td>

Australia

</td><td>

-   **[Automatic test maintenance](https://www.servicenow.com/docs/access?context=build-agent-testing&family=australia&ft:locale=en-US)**

Test Agent in Build Agent automatically updates or removes Automated Test Framework tests that are outdated as your application changes, keeping the test suite aligned with the current state of your code. UI tests don't run automatically during updates, because they can take additional time and interrupt the development flow. To automatically keep tests synced, you must enable the new **Sync ATF tests with app** setting in Build Agent.

-   **[UI testing](https://www.servicenow.com/docs/access?context=build-agent-testing&family=australia&ft:locale=en-US)**

Generate comprehensive UI tests for applications you build with Build Agent. UI testing extends the existing functional test capability to cover browser-level interactions, such as multi-step page navigation flows. To run UI tests automatically on update, you must enable the **Run UI ATF tests** setting in Test Agent.

**Note:** You can also prompt Build Agent to generate UI tests.

-   **[Get prompted to test](https://www.servicenow.com/docs/access?context=build-agent-testing&family=australia&ft:locale=en-US)**

After each development action, Build Agent can prompt you to generate ATF tests for what you just built. Accept or decline the prompt at each step to keep test coverage in sync with your development work.

**Note:** You must enable getting prompted to test in the Build Agent settings.

-   **[SDK test execution](https://www.servicenow.com/docs/access?context=build-agent-testing&family=australia&ft:locale=en-US)**

Execute ATF tests from the ServiceNow SDK. Test execution and troubleshooting were previously available only in ServiceNow Studio and the ServiceNow IDE.

-   **[Updated model support](https://www.servicenow.com/docs/access?context=ba-models-versions&family=australia&ft:locale=en-US)**

The following new models are supported for Build Agent:

    -   Gemini 3.5 is now the default model for Google
    -   GPT 5.5 is now the default model for Azure OpenAI
    -   Opus 4.8
-   **[Change model version in chat](https://www.servicenow.com/docs/access?context=ba-models-versions&family=australia&ft:locale=en-US)**

Change the AI model versions in Build Agent without navigating out to the table on the ServiceNow AI Platform.

-   **[Define custom skills and rules](https://www.servicenow.com/docs/access?context=ba-configure-custom-skills-rules&family=australia&ft:locale=en-US)**

Create custom skills and rules to control how Build Agent behaves during a session.

    -   Custom rules are injected into the system prompt on every run, so Build Agent behaves consistently at the scope you choose.
    -   Custom skills provide internal guidelines for specific tasks. You can apply skills and rules at the instance level, application level, or user level.
-   **[Background script execution](https://www.servicenow.com/docs/access?context=build-agent-tools&family=australia&ft:locale=en-US)**

Run server-side scripts as part of app-building flows in Build Agent using the new run script and rollback script tools. Before a script runs, an approval prompt shows the generated script, its stated intent, and the target application scope so you can review the operation before approving.

-   **[Conversation handoff to Build Agent](https://www.servicenow.com/docs/access?context=access-build-agent&family=australia&ft:locale=en-US)**

Build applications by receiving context from ServiceNow Otto \(formerly Now Assist\) conversations and continuing work in Build Agent without repeating yourself. The full conversation transcript is attached to the session so you can reference details beyond the summary. Conversation handoff is available only in ServiceNow Studio.

-   **[Use Build Agent in a sandbox](https://www.servicenow.com/docs/access?context=access-build-agent&family=australia&ft:locale=en-US)**

Use Build Agent in Developer Sandboxes to isolate development and provide admin access to developers in a protected environment.

-   **[View MCP tools per server](https://www.servicenow.com/docs/access?context=accelerate-design-to-development-with-figma-mcp-server&family=australia&ft:locale=en-US)**

View the list of tools available on each connected MCP server in the Build Agent settings panel.

-   **[Knowledge base access metadata support](https://www.servicenow.com/docs/access?context=build-agent-supported-metadata&family=australia&ft:locale=en-US)**

Work with the knowledge base access metadata type in Build Agent.


-   **[Web search tool](https://www.servicenow.com/docs/access?context=build-agent-tools&family=australia&ft:locale=en-US)**

Access public web content from Build Agent using two new search tools. Use the web search tool to find information on the public web, and use the web fetch tool to retrieve content from a URL that you supply.

-   **[Consolidated update sets](https://www.servicenow.com/docs/access?context=ba-update-sets&family=australia&ft:locale=en-US)**

Track changes generated by Build Agent and manual edits in update sets for checkpointing and rollback. Update sets can be merged into a single update set before deployment. All changes to your application are captured in the same scope, making it easier to review what was modified and merge updates to other environments.

-   **[Expanded metadata support](https://www.servicenow.com/docs/access?context=build-agent-supported-metadata&family=australia&ft:locale=en-US)**

Work with more metadata types in Build Agent, which now supports connection and credential alias, data lookup, playbooks, rest message/HTTP method, and user criteria.


-   **[MCP server support in ServiceNow Studio](https://www.servicenow.com/docs/access?context=ba-connct-mcp-server&family=australia&ft:locale=en-US)**

Connect Build Agent to external MCP servers in ServiceNow Studio. Previously, MCP server connectivity was only available in the ServiceNow IDE.

-   **[Additional MCP server integrations](https://www.servicenow.com/docs/access?context=accelerate-design-to-development-with-figma-mcp-server&family=australia&ft:locale=en-US)**

Integrate Build Agent with newly supported MCP servers.

-   **[Access update sets from Build Agent](https://www.servicenow.com/docs/access?context=ba-update-sets&family=australia&ft:locale=en-US)**

View update sets created by Build Agent from within the chat panel in ServiceNow Studio. Each checkpoint includes a button that opens the relevant update set in a new tab.

-   **[UI validation tool in ServiceNow Studio](https://www.servicenow.com/docs/access?context=build-agent-tools&family=australia&ft:locale=en-US)**

Validate user interface output during app creation with the UI validation tool in Build Agent, available in ServiceNow Studio.

-   **[Search retrieval tool support](https://www.servicenow.com/docs/access?context=ba-about-creating-in-app-agents&family=australia&ft:locale=en-US)**

Use the Search retrieval tool to enable agents to fetch and present relevant information from configured data sources in response to user queries. Agents can retrieve knowledge articles, catalog items, and other indexed content directly within the agentic workflow, reducing the need for users to navigate to separate search interfaces.

-   **[Support for more file types](https://www.servicenow.com/docs/access?context=ba-supported-file-types&family=australia&ft:locale=en-US)**

Upload more types of files to Build Agent to describe what you want to build, including images, documents, and text and code files.

-   **[Expanded metadata support](https://www.servicenow.com/docs/access?context=build-agent-supported-metadata&family=australia&ft:locale=en-US)**

Work with more metadata types in Build Agent, which now supports assignment rules, forms, and data policies.


-   **[MCP Client integration](https://www.servicenow.com/docs/access?context=ba-connct-mcp-server&family=australia&ft:locale=en-US)**

Connect Build Agent to external MCP servers to bring tools and data sources directly into your build workflow. External resources participate alongside Build Agent on the ServiceNow AI Platform, which reduces the need to switch between tools and transfer data manually.

-   **[Create workflows, agents, and skills](https://www.servicenow.com/docs/access?context=create-custom-ai-agent&family=australia&ft:locale=en-US)**

Turn business requirements into fully configured agents, skills, and agentic workflows for your custom applications. Build Agent inspects the existing tables, roles, business rules, and metadata in your app to create tailored in-app agents and tools.

-   **[Test Agent for Build Agent](https://www.servicenow.com/docs/access?context=build-agent-testing&family=australia&ft:locale=en-US)**

Use Test Agent to execute Automated Test Framework \(ATF\) tests right from the Build Agent chat panel for test artifacts created in the same session. When tests fail, the generated tests and test results are saved in the standard ATF record tables and can be scheduled for continued regression testing for the app. If Test Agent modifies tests during troubleshooting, those changes are automatically saved to the test records.

-   **[UI validation tool](https://www.servicenow.com/docs/access?context=exploring-build-agent&family=australia&ft:locale=en-US)**

Validate user interface output during Build Agent app creation in the ServiceNow IDE using the integrated UI validation. UI validation runs Playwright-based UI checks on Cloud Runner and surfaces failures with diagnostic context directly in the Build Agent panel.

-   **[Semantic search for instance artifact discovery](https://www.servicenow.com/docs/access?context=build-agent-tools&family=australia&ft:locale=en-US)**

Use semantic search in Build Agent to locate relevant instance artifacts, including tables, scripts, and business rules during build and edit tasks. Find files, applications, and knowledge on your instance based on meaning instead of exact keywords.

-   **[Additional model support](https://www.servicenow.com/docs/access?context=exploring-build-agent&family=australia&ft:locale=en-US)**

Choose the provider and model that fits your organizational needs in Build Agent, which now supports Anthropic Claude on AWS Sonnet 4.6 and Azure OpenAI GPT 5.4.

-   **[Expanded metadata support](https://www.servicenow.com/docs/access?context=build-agent-supported-metadata&family=australia&ft:locale=en-US)**

Work with more metadata types in Build Agent, which now supports flows, Service Catalog configurations, inbound email actions, dictionary overrides, choice lists, condition builder query conditions, and enhanced Service Portal capabilities.

-   **[Contextual launch for Build Agent](https://www.servicenow.com/docs/access?context=access-build-agent&family=australia&ft:locale=en-US)**

Include context from ServiceNow Studio tabs and component preview screens when you open Build Agent. Context helps reduce the need to manually search for and specify context in the chat panel.


-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Additional metadata support](https://www.servicenow.com/docs/access?context=build-agent-supported-metadata&family=australia&ft:locale=en-US)**

Work with more metadata types in Build Agent, which now supports email.


-   **[Build Agent in ServiceNow Studio](https://www.servicenow.com/docs/access?context=build-agent-in-servicenow-studio&family=australia&ft:locale=en-US)**

Access Build Agent in ServiceNow Studio to build apps conversationally in a consolidated development environment.

-   **[Improved LLM support](https://www.servicenow.com/docs/access?context=exploring-build-agent&family=australia&ft:locale=en-US)**

Use AWS Claude Opus 4.6 and Sonnet 4.5 in Build Agent for contextual conversations.

-   **[New metadata support](https://www.servicenow.com/docs/access?context=build-agent-supported-metadata&family=australia&ft:locale=en-US)**

Work with more metadata types, as Build Agent now supports the following:

    -   Email integration
    -   List controls
    -   Service Catalog items
    -   UI components
    -   UI policies
    -   UI views
    -   Workspaces

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Build Agent features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[ServiceNow Otto rebrand](https://www.servicenow.com/docs/access?context=exploring-build-agent&family=zurich&ft:locale=en-US)**

ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Build Agent. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

-   **[Licensing change for in-app agents and skills](https://www.servicenow.com/docs/access?context=ba-about-creating-in-app-agents&family=zurich&ft:locale=en-US)**

Only users with Build Agent - Prime can create agents and skills.


-   **[Improved checkpoint and update set management](https://www.servicenow.com/docs/access?context=ba-conversational-change-log&family=zurich&ft:locale=en-US)**

Build Agent handles checkpoints and update sets differently in the following ways:

    -   Checkpoint 0 no longer creates an update set.
    -   Checkpoint 1 is the base update set for all subsequent changes.
    -   Update sets use human-readable naming.
-   **[Enhanced semantic metadata search tool](https://www.servicenow.com/docs/access?context=build-agent-tools&family=zurich&ft:locale=en-US)**

An updated semantic metadata search tool improves performance replaces the previous semantic search tool.


-   **[Build Agent version parity for PDIs](https://www.servicenow.com/docs/access?context=exploring-build-agent&family=zurich&ft:locale=en-US)**

Personal development instances \(PDIs\) are now updated to match the latest Build Agent version, delivering a consistent experience across both personal and production-track instances. Developers testing and building on PDIs have access to the same capabilities available in production environments.

-   **[Updated interaction limits](https://www.servicenow.com/docs/access?context=exploring-build-agent&family=zurich&ft:locale=en-US)**

To provide developers more room to iterate, the following Build Agent limits have been increased:

    -   Build Agent \(Trial\): 100 prompts per instance per 30-day cycle
    -   PDIs: 25 prompts per instance per cycle
**Note:** Limits are per-instance, not per-user. Only submitted prompts contribute to the limit. Plan approvals are not counted.


-   **[Support for global scope](https://www.servicenow.com/docs/access?context=exploring-build-agent&family=zurich&ft:locale=en-US)**

Build apps and metadata in the global scope.


</td></tr><tr><td>

Australia

</td><td>

-   **[ServiceNow Otto rebrand](https://www.servicenow.com/docs/access?context=exploring-build-agent&family=australia&ft:locale=en-US)**

ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Build Agent. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

-   **[Licensing change for in-app agents and skills](https://www.servicenow.com/docs/access?context=ba-about-creating-in-app-agents&family=australia&ft:locale=en-US)**

Only users with Build Agent - Prime can create agents and skills.


-   **[Improved checkpoint and update set management](https://www.servicenow.com/docs/access?context=ba-conversational-change-log&family=australia&ft:locale=en-US)**

Build Agent handles checkpoints and update sets differently in the following ways:

    -   Checkpoint 0 no longer creates an update set.
    -   Checkpoint 1 is the base update set for all subsequent changes.
    -   Update sets use human-readable naming.
-   **[Enhanced semantic metadata search tool](https://www.servicenow.com/docs/access?context=build-agent-tools&family=australia&ft:locale=en-US)**

An updated semantic metadata search tool improves performance replaces the previous semantic search tool.


-   **[Build Agent version parity for PDIs](https://www.servicenow.com/docs/access?context=exploring-build-agent&family=australia&ft:locale=en-US)**

Personal development instances \(PDIs\) are now updated to match the latest Build Agent version, delivering a consistent experience across both personal and production-track instances. Developers testing and building on PDIs have access to the same capabilities available in production environments.

-   **[Updated interaction limits](https://www.servicenow.com/docs/access?context=exploring-build-agent&family=australia&ft:locale=en-US)**

To provide developers more room to iterate, the following Build Agent limits have been increased:

    -   Build Agent \(Trial\): 100 prompts per instance per 30-day cycle
    -   PDIs: 25 prompts per instance per cycle
**Note:** Limits are per-instance, not per-user. Only submitted prompts contribute to the limit. Plan approvals are not counted.


-   **[Support for global scope](https://www.servicenow.com/docs/access?context=exploring-build-agent&family=australia&ft:locale=en-US)**

Build apps and metadata in the global scope.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Build Agent features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Build Agent features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Build Agent.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Build Agent is a ServiceNow AI Platform feature that is active by default.

**Note:** Build Agent is dependent on ServiceNow Otto for Creator. For more information, see [ServiceNow Otto for Creator release notes](https://www.servicenow.com/docs/access?context=now-assist-for-creator-rn&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Build Agent is a ServiceNow AI Platform feature that is active by default.

**Note:** Build Agent is dependent on ServiceNow Otto for Creator. For more information, see [ServiceNow Otto for Creator release notes](https://www.servicenow.com/docs/access?context=now-assist-for-creator-rn&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Build Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Build Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Build Agent, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Build Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Build Agent we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Use Build Agent in ServiceNow Studio.
-   Work with additional Model Context Protocol \(MCP\) support.
-   Create apps and newly supported metadata in the global scope.
-   Choose from newly supported models.
-   Search external content without leaving Build Agent.

 See [Build Agent](https://www.servicenow.com/docs/access?context=build-agent&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Use Build Agent in ServiceNow Studio.
-   Work with additional Model Context Protocol \(MCP\) support.
-   Create apps and newly supported metadata in the global scope.
-   Choose from newly supported models.
-   Search external content without leaving Build Agent.

 See [Build Agent](https://www.servicenow.com/docs/access?context=build-agent&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

