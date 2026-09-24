---
title: Build Agent and Autonomous Engineer release notes
description: The ServiceNow Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. See the following sections for release notes by version.Build Agent includes enhancements in the September 2026 release, such as Autonomous Engineer for spec-driven full-stack development, expanded Automated Test Framework capabilities, and MCP support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/build-agent-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-21"
reading_time_minutes: 5
keywords: [Build Agent, Test Agent, ATF, automated testing, test suite, Autonomous Engineer, scheduled prompts, scheduled jobs, implementation plan, GraphQL, ACL, playbook, Playbook Designer, optional activity, launcher configuration, playbook permissions, agentic activity]
breadcrumb: [App development and low-code release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Build Agent and Autonomous Engineer release notes

The ServiceNow® Build Agent application enables developers to create, edit, and deploy full-stack applications and metadata through a conversational interface. See the following sections for release notes by version.

## About Build Agent

-   Accelerate development by reducing backlogs and enabling faster deployment of new business applications, without requiring developers to manually handle repetitive build, test, and deployment steps.
-   Describe an application in natural language to autonomously generate code, organize files, and manage both UI and back-end components, making development available to users at any level.
-   Support automated testing through Automated Test Framework \(ATF\) test suite generation and execution, reducing the manual effort required to validate new or updated applications.
-   Decrease development costs because Build Agent handles code compilation, quality checks, and documentation of existing applications automatically.
-   Enable agentic development by letting you create agentic workflows, custom AI agents, and skills tailored to your organization directly from within ServiceNow Studio.

See [Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/build-agent.md) for more information.

## Activation and other requirements

-   **Activation information**

    Build Agent \(Trial\) is a ServiceNow AI Platform feature that is active by default starting with the Brazil release. For Build Agent, you must install ServiceNow Otto for Creator.

-   **Additional requirements**

    Build Agent is dependent on ServiceNow Otto for Creator.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/build-automate-rn-landing.md)

## Brazil Early Availability

Build Agent includes enhancements in the September 2026 release, such as Autonomous Engineer for spec-driven full-stack development, expanded Automated Test Framework capabilities, and MCP support.

### What's new

-   **[Generate implementations from specifications with Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/autonomous-engineer.md)**

    Use Autonomous Engineer, powered by Build Agent, to generate a complete implementation plan from your requirements.

    1.  Provide requirements as a prompt or a file upload.
    2.  Autonomous Engineer prompts you with questions to clarify ambiguous requirements, queries your instance to identify existing artifacts. For example, it might ask questions about tables, roles, and catalog items, and generates a plan with work items. Work items include acceptance criteria and test criteria in an Agile user story format.
    3.  After you approve the plan, Autonomous Engineer generates a background agent for each work item. It then builds all work items in parallel in the background, generates and runs ATF tests, and attempts to resolve test failures.
    4.  Items that require human intervention appear in the dashboard and in the chat panel.
    5.  When the plan is complete, an update set is generated for deployment to your UAT or production environment.
    Autonomous Engineer uses agent packs to give background agents product-specific domain knowledge during execution. The Custom app development agent pack is available in this release, which gives Autonomous Engineer awareness of platform tables, roles, and configuration patterns specific to custom app development.

-   **[Automatic test generation from plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/build-agent-testing.md)**

    When you use Autonomous Engineer to plan an application, Test Agent automatically generates Automated Test Framework tests for each work item and acceptance criteria that can be validated through automated testing. Generated tests are executed immediately, and Test Agent identifies and resolves any failures.

-   **[New model support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-models-versions.md)**

    Build Agent and Autonomous Engineer now support the following models:

    -   Azure OpenAI GPT 5.6 Sol
    -   Anthropic Claude on AWS Opus 5
-   **[Test suite authoring and execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/build-agent-testing.md)**

    Create and run ATF test suites from Build Agent and Autonomous Engineer. Group multiple tests under a single suite and execute the suite to run regression testing without selecting individual tests. Execution status and any errors are reported in the chat panel.

-   **[ATF list step support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/build-agent-testing.md)**

    Test Agent can now generate ATF tests that use list and related list test steps, including validate related list visibility and apply filter to list. List step support extends test coverage beyond form-based interactions to include the full list view experience on the ServiceNow AI Platform.

-   **[Support for Box MCP server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/accelerate-design-to-development-with-figma-mcp-server.md)**

    Build Agent now supports integrations with Box MCP server.

-   **[Domain separation for ServiceNow Fluent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-domain-separation.md)**

    ServiceNow Fluent, which Build Agent uses to create apps, now supports domain separation on records and APIs. You can set the **sys\_domain** field and use **sys\_override** fields when working with records in domain-separated environments, so ServiceNow Fluent operates correctly across domains in your instance.

-   **[Additional metadata support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/build-agent-supported-metadata.md)**

    The following metadata are now supported in Build Agent and Autonomous Engineer:

    -   Service Catalog dependent question support
    -   Transition condition
    -   UI style
-   **[Right-click to configure ServiceNow AI Platform metadata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/access-build-agent.md)**

    When you right-click a record or artifact and select **Configure**, the metadata editor now opens in ServiceNow Studio.

-   **[Build Agent \(Trial\) automatically installed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/exploring-build-agent.md)**

    Build Agent \(Trial\) is available by default on all instances, without requiring installation.

-   **[Automatic upgrades for Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/install-build-agent.md)**

    Build Agent now supports automatic upgrades through the ServiceNow Store. Instances running Australia Patch 5 and later releases or Zurich Patch 12 and later releases that have Build Agent installed receive automatic upgrades when a new version is published.

-   **[Playbook support updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-update-sets.md)**

    Build Agent includes the following updates to Playbook support:

    -   Build Agent now consolidates all records related to a playbook into a single XML update set file.
    -   Build Agent can now generate runtime permissions at the playbook level and at the stage level.
    -   Build Agent can now generate and configure the Set Playbook Outputs activity for nested playbooks.
    -   Build Agent can now configure agentic fields on form-based and record-based activities when the AI Agent plugin is active.
    -   Build Agent can now generate on-demand playbook launcher configurations.
    -   Build Agent can now define optional activities in a playbook.

### What's changed

-   **[Build Agent in ServiceNow Studio UI updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/access-build-agent.md)**

    Several changes have been made to how you access Build Agent in ServiceNow Studio:

    -   The central chat area on the ServiceNow Studio home page is the starting point for new Build Agent conversations.
    -   To open an existing conversation, select the Conversations icon \[Omitted image "ba-sns-otto-nav-icon.png"\] Alt text: in the Navigator panel.
    -   The Build Agent panel now opens on the Navigator panel of ServiceNow Studio.

