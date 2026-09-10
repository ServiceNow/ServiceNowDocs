---
title: Build Agent release notes
description: The ServiceNow Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto.The ServiceNow Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto.The ServiceNow Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto.The ServiceNow Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto.The ServiceNow Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto.The ServiceNow Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto.The ServiceNow Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto.The ServiceNow Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-08-31"
reading_time_minutes: 13
keywords: [Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI, Now Assist, AI Agents, generative AI, agentic AI]
---

# Build Agent release notes

The ServiceNow® Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto®.

## About Build Agent

-   Use Build Agent in ServiceNow Studio.
-   Work with additional Model Context Protocol \(MCP\) support.
-   Create apps and newly supported metadata in the global scope.
-   Choose from newly supported models.
-   Search external content without leaving Build Agent.

See  for more information.

## Activation and other requirements

-   **Activation information**

    Build Agent is a ServiceNow AI Platform feature that is active by default.

    **Note:** Build Agent is dependent on ServiceNow Otto for Creator. For more information, see [ServiceNow Otto for Creator release notes]().


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/build-automate-rn-landing.md)

## September 2026

The ServiceNow® Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto®.

### What's new

-   **Playbook support updates**

    Build Agent includes the following updates to Playbook support:

    -   Build Agent now consolidates all records related to a playbook into a single XML update set file.
    -   Build Agent can now generate runtime permissions at the playbook level and at the stage level.
    -   Build Agent can now generate and configure the Set Playbook Outputs activity for nested playbooks.
    -   Build Agent can now configure agentic fields on form-based and record-based activities when the AI Agent plugin is active.
    -   Build Agent can now generate on-demand playbook launcher configurations.
    -   Build Agent can now define optional activities in a playbook.
-   **New model support**

    Build Agent now supports the following models:

    -   Azure OpenAI GPT 5.6 Sol
    -   Anthropic Claude on AWS Opus 5
-   **Test suite authoring and execution**

    Create and run ATF test suites from Build Agent. Group multiple tests under a single suite and execute the suite to run regression testing without selecting individual tests. Execution status and any errors are reported in the chat panel.

-   **ATF list step support**

    Test Agent can now generate ATF tests that use list and related list test steps, including validate related list visibility and apply filter to list. List step support extends test coverage beyond form-based interactions to include the full list view experience on the ServiceNow AI Platform.

-   **Support for Box MCP server**

    Build Agent now supports integrations with Box MCP server.

-   **Domain separation for ServiceNow Fluent**

    ServiceNow Fluent, which Build Agent uses to create apps, now supports domain separation on records and APIs. You can set the **sys\_domain** field and use **sys\_override** fields when working with records in domain-separated environments, so ServiceNow Fluent operates correctly across domains in your instance.

-   **Additional metadata support**

    The following metadata are now supported in Build Agent:

    -   Service Catalog dependent question support
    -   Transition condition
    -   UI style
-   **Right-click to configure ServiceNow AI Platform metadata**

    When you right-click a record or artifact and select **Configure**, the metadata editor now opens in ServiceNow Studio.

-   **Automatic upgrades for Build Agent**

    Build Agent now supports automatic upgrades through the ServiceNow Store. Instances running Australia Patch 5 and later releases or Zurich Patch 12 and later releases that have Build Agent installed receive automatic upgrades when a new version is published.


-   **Automatic test maintenance**

    Test Agent in Build Agent automatically updates or removes Automated Test Framework tests that are outdated as your application changes, keeping the test suite aligned with the current state of your code. UI tests don't run automatically during updates, because they can take additional time and interrupt the development flow. To automatically keep tests synced, you must enable the new **Sync ATF tests with app** setting in Build Agent.

-   **UI testing**

    Generate comprehensive UI tests for applications you build with Build Agent. UI testing extends the existing functional test capability to cover browser-level interactions, such as multi-step page navigation flows. To run UI tests automatically on update, you must enable the **Run UI ATF tests** setting in Test Agent.

    **Note:** You can also prompt Build Agent to generate UI tests.

-   **Get prompted to test**

    After each development action, Build Agent can prompt you to generate ATF tests for what you just built. Accept or decline the prompt at each step to keep test coverage in sync with your development work.

    **Note:** You must enable getting prompted to test in the Build Agent settings.

-   **SDK test execution**

    Execute ATF tests from the ServiceNow SDK. Test execution and troubleshooting were previously available only in ServiceNow Studio and the ServiceNow IDE.

-   **Updated model support**

    The following new models are supported for Build Agent:

    -   Gemini 3.5 is now the default model for Google
    -   GPT 5.5 is now the default model for Azure OpenAI
    -   Opus 4.8
-   **Change model version in chat**

    Change the AI model versions in Build Agent without navigating out to the table on the ServiceNow AI Platform.

-   **Define custom skills and rules**

    Create custom skills and rules to control how Build Agent behaves during a session.

    -   Custom rules are injected into the system prompt on every run, so Build Agent behaves consistently at the scope you choose.
    -   Custom skills provide internal guidelines for specific tasks. You can apply skills and rules at the instance level, application level, or user level.
-   **Background script execution**

    Run server-side scripts as part of app-building flows in Build Agent using the new run script and rollback script tools. Before a script runs, an approval prompt shows the generated script, its stated intent, and the target application scope so you can review the operation before approving.

-   **Conversation handoff to Build Agent**

    Build applications by receiving context from ServiceNow Otto \(formerly Now Assist\) conversations and continuing work in Build Agent without repeating yourself. The full conversation transcript is attached to the session so you can reference details beyond the summary. Conversation handoff is available only in ServiceNow Studio.

-   **Use Build Agent in a sandbox**

    Use Build Agent in Developer Sandboxes to isolate development and provide admin access to developers in a protected environment.

-   **View MCP tools per server**

    View the list of tools available on each connected MCP server in the Build Agent settings panel.

-   **Knowledge base access metadata support**

    Work with the knowledge base access metadata type in Build Agent.


### What's changed

-   **Build Agent in ServiceNow Studio UI updates**

    Several changes have been made to how you access Build Agent in ServiceNow Studio:

    -   The central chat area on the ServiceNow Studio home page is the starting point for new Build Agent conversations.
    -   To open an existing conversation, select the Conversations icon \[Omitted image "ba-sns-otto-nav-icon.png"\] Alt text: in the Navigator panel.
    -   The Build Agent panel now opens on the Navigator panel of ServiceNow Studio.

## August 2026

The ServiceNow® Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto®.

### What's changed

-   **Organized settings with tabs**

    Find Build Agent easier now that the Settings panel has tabs: **General**, **Skills**, **Rules**, and **MCP**.


-   **ServiceNow Otto rebrand**

    ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Build Agent. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

-   **Licensing change for in-app agents and skills**

    Only users with Build Agent - Prime can create agents and skills.


## July 2026

The ServiceNow® Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto®.

### What's new

-   **Web search tool**

    Access public web content from Build Agent using two new search tools. Use the web search tool to find information on the public web, and use the web fetch tool to retrieve content from a URL that you supply.

-   **Consolidated update sets**

    Track changes generated by Build Agent and manual edits in update sets for checkpointing and rollback. Update sets can be merged into a single update set before deployment. All changes to your application are captured in the same scope, making it easier to review what was modified and merge updates to other environments.

-   **Expanded metadata support**

    Work with more metadata types in Build Agent, which now supports connection and credential alias, data lookup, playbooks, rest message/HTTP method, and user criteria.


### What's changed

-   **Enhanced semantic metadata search tool**

    An updated semantic metadata search tool improves performance replaces the previous semantic search tool.


## June 2026

The ServiceNow® Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto®.

### What's new

-   **MCP server support in ServiceNow Studio**

    Connect Build Agent to external MCP servers in ServiceNow Studio. Previously, MCP server connectivity was only available in the ServiceNow IDE.

-   **Additional MCP server integrations**

    Integrate Build Agent with newly supported MCP servers.

-   **Access update sets from Build Agent**

    View update sets created by Build Agent from within the chat panel in ServiceNow Studio. Each checkpoint includes a button that opens the relevant update set in a new tab.

-   **UI validation tool in ServiceNow Studio**

    Validate user interface output during app creation with the UI validation tool in Build Agent, available in ServiceNow Studio.

-   **Search retrieval tool support**

    Use the Search retrieval tool to enable agents to fetch and present relevant information from configured data sources in response to user queries. Agents can retrieve knowledge articles, catalog items, and other indexed content directly within the agentic workflow, reducing the need for users to navigate to separate search interfaces.

-   **Support for more file types**

    Upload more types of files to Build Agent to describe what you want to build, including images, documents, and text and code files.


### What's changed

-   **New button prompt to add AI to an app**

    A new **Add AI** button when you first open the Build Agent chat panel starts a guided conversation to help you define and generate a skill or agent.

    **Note:** You must have a ServiceNow Otto for Creator license for the new button to appear.

-   **Open Build Agent from ServiceNow Studio banner**

    A new icon in the ServiceNow Studio application banner provides another way to access Build Agent.


-   **Improved checkpoint and update set management**

    Build Agent handles checkpoints and update sets differently in the following ways:

    -   Checkpoint 0 no longer creates an update set.
    -   Checkpoint 1 is the base update set for all subsequent changes.
    -   Update sets use human-readable naming.

## Australia General Availability

The ServiceNow® Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto®.

### What's new

-   **Expanded metadata support**

    Work with more metadata types in Build Agent, which now supports assignment rules, forms, and data policies.


-   ****

    Turn business requirements into fully configured agents, skills, and agentic workflows for your custom applications. Build Agent inspects the existing tables, roles, business rules, and metadata in your app to create tailored in-app agents and tools.

-   **Test Agent for Build Agent**

    Use Test Agent to execute Automated Test Framework \(ATF\) tests right from the Build Agent chat panel for test artifacts created in the same session. When tests fail, the generated tests and test results are saved in the standard ATF record tables and can be scheduled for continued regression testing for the app. If Test Agent modifies tests during troubleshooting, those changes are automatically saved to the test records.

-   **UI validation tool**

    Validate user interface output during Build Agent app creation in the ServiceNow IDE using the integrated UI validation. UI validation runs Playwright-based UI checks on Cloud Runner and surfaces failures with diagnostic context directly in the Build Agent panel.

-   **Semantic search for instance artifact discovery**

    Use semantic search in Build Agent to locate relevant instance artifacts, including tables, scripts, and business rules during build and edit tasks. Find files, applications, and knowledge on your instance based on meaning instead of exact keywords.

-   **Additional model support**

    Choose the provider and model that fits your organizational needs in Build Agent, which now supports Anthropic Claude on AWS Sonnet 4.6 and Azure OpenAI GPT 5.4.

-   **Expanded metadata support**

    Work with more metadata types in Build Agent, which now supports flows, Service Catalog configurations, inbound email actions, dictionary overrides, choice lists, condition builder query conditions, and enhanced Service Portal capabilities.

-   **Contextual launch for Build Agent**

    Include context from ServiceNow Studio tabs and component preview screens when you open Build Agent. Context helps reduce the need to manually search for and specify context in the chat panel.

-   **MCP Client integration**

    Connect Build Agent to external MCP servers to bring tools and data sources directly into your build workflow. External resources participate alongside Build Agent on the ServiceNow AI Platform, which reduces the need to switch between tools and transfer data manually.


### What's changed

-   **Generated artifact preview**

    Preview generated tables, flows, and scripts that Build Agent creates in ServiceNow Studio so you can review and approve changes inline before saving or committing them to the application.



## April 2026

The ServiceNow® Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto®.

### What's new

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **Additional metadata support**

    Work with more metadata types in Build Agent, which now supports email.


### What's changed

-   **Build Agent version parity for PDIs**

    Personal development instances \(PDIs\) are now updated to match the latest Build Agent version, delivering a consistent experience across both personal and production-track instances. Developers testing and building on PDIs have access to the same capabilities available in production environments.

-   **Updated interaction limits**

    To provide developers more room to iterate, the following Build Agent limits have been increased:

    -   Build Agent \(Trial\): 100 prompts per instance per 30-day cycle
    -   PDIs: 25 prompts per instance per cycle
    **Note:** Limits are per-instance, not per-user. Only submitted prompts contribute to the limit. Plan approvals are not counted.


## Australia Early Availability

The ServiceNow® Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. Build Agent was enhanced and updated in the Australia release, and its Now Assist features have been rebranded to ServiceNow Otto®.

### What's new

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

### What's changed

-   **Support for global scope**

    Build apps and metadata in the global scope.


