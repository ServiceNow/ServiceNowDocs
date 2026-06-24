---
title: General guidelines for Build Agent
description: Use these guidelines to get the most out of Build Agent in your development workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/build-agent-general-guidelines.html
release: zurich
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# General guidelines for Build Agent

Use these guidelines to get the most out of Build Agent in your development workflow.

## Development guidelines

To maximize Build Agent effectiveness, use the following practices:

-   Design before coding: Think through and document the requirements for your application across the data and UI layers, for example using Workflow Studio or Figma.
-   Start with a clear plan: Collaborate with Build Agent to define scope, required tables, and metadata types.
-   Instruct with context: Write instructions for what you want to achieve with your application using Markdown in your file system, and ask Build Agent to use the file as context for its work.
-   Use specific terminology: Treat Build Agent as your development partner. Provide specific, clear instructions using ServiceNow platform terminology such as table names, field names, roles, and artifact types.
-   Test early and often: Add sample records, test on the instance, and build ATF tests throughout development.
-   Use version control: Use Git for tracking changes and maintaining a clean workspace structure.
-   Provide visual context: Give screenshots to Build Agent to troubleshoot UI issues and request changes.
-   Extend with third-party libraries: Integrate third-party Node Package Manager \(NPM\) libraries, such as React JS, for enhanced interfaces.
-   Maintain documentation: Keep clear rules and documentation in project folders; use Build Agent to create knowledge base articles.
-   Iterate and experiment: Prototype freely, then ask Build Agent for an ideal prompt to recreate the result once your vision is complete.

## Prompting guidelines

Use the following guidelines to get better results from Build Agent.

-   **Ask Build Agent to prompt for you**

    Ask Build Agent to suggest an ideal prompt for your goal or coach you on common pitfalls for a given metadata type. To learn more, see this Community article on [The fastest way to learn Build Agent prompting? Ask Build Agent](https://www.servicenow.com/community/now-assist-for-creator-articles/the-fastest-way-to-learn-build-agent-prompting-ask-build-agent/ta-p/3533544).

-   **Be comprehensive**

    One detailed prompt can provide better results than several vague ones. Include tables, fields, roles, and automation in a single prompt.

-   **Use the planning tool**

    For complex apps, ask Build Agent to create a plan first. Review and approve before it starts building.

-   **Let Build Agent interview you**

    For broad ideas, let Build Agent ask clarifying questions before planning. This produces better results than guessing at details yourself.

-   **Use specific ServiceNow terminology**

    Say `reference to sys_user` instead of `add a field for who ordered`. Naming the table, field, scope, role, or artifact reduces interview cycles and produces more accurate output on the first attempt. Conversational prompts work well for early exploration, while precision works better as the build progresses.

-   **Draft offline**

    Write prompts in a text editor, refine them, then paste into the chat, which saves prompts and can help to produce better results.

-   **Develop incrementally**

    Develop each page or feature in separate chats. Implement and test, then start a new conversation for the next feature.

-   **Use markdown**

    Place a markdown file \(for example, named `GUIDE_*.md` or `BUILD_AGENT_RULES.md`\) in your project directory. Build Agent reads these grounding files and follows your conventions throughout the session.

    **Note:** Markdown for Build Agent is currently available only in the ServiceNow IDE. Teams that get the most value from Build Agent markdown files document their organizational standards in these files, including the following:

    -   Naming conventions: table names, field names, business rule naming patterns, and scope prefixes
    -   Technical standards: coding practices, preferred patterns, and anti-patterns to avoid
    -   Development cadence: processes, update set management, and code review requirements
    -   Last-resort actions that require explicit approval: creating new tables, changing ACLs or roles, modifying system properties, and altering base system business rules
-   **Use ESLint**

    Use ESLint on the ServiceNow AI Platform to define your preferred coding style, and ask Build Agent to manage and enforce the ESLint configuration, for example using snake case for variables.


**Parent Topic:**[Exploring Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/exploring-build-agent.md)

