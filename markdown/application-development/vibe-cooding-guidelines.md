---
title: General guidelines for agentic development
description: General guidelines for agentic development on the ServiceNow AI Platform cover prompt writing, context management, compliance validation, and development environment setup.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/vibe-cooding-guidelines.html
release: australia
topic_type: concept
last_updated: "2026-11-03"
reading_time_minutes: 2
keywords: [agentic development, prompt writing, context management, compliance validation, development environment, build agent, developer sandboxes, iterative development, vault console]
breadcrumb: [Explore, Agentic development, Agentic development on the ServiceNow AI Platform, Building applications]
---

# General guidelines for agentic development

General guidelines for agentic development on the ServiceNow AI Platform cover prompt writing, context management, compliance validation, and development environment setup.

## Agentic development guidelines

-   Use clear, focused prompts with as much detail as possible to generate more accurate and relevant output.
-   If you're using Build Agent, include as much context as possible in your first prompt to enable more robust development. Include roles, data requirements, and success criteria.
-   When switching between two separate applications in Build Agent, specify the new application context.
-   Save your successful prompts to repurpose and reuse. For more information, see [Example prompts for agentic development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/vibe-coding-example-prompts.md).
-   Save your session to quickly resume working where you stopped.
-   Use the Build Agent chat panel for iterative development.
-   For large implementations with well-defined requirements, use Autonomous Engineer, which generates a plan with work items and builds them in parallel. Review and approve the plan before it starts building. For more information, see [Autonomous Engineer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/autonomous-engineer.md).
-   Develop each feature in a separate chat. Implement and test the feature, then start a new conversation for the next feature.
-   Use custom skills and rules to define instructions that Build Agent follows in every session. For more information, see [Configure custom skills and rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/ba-configure-custom-skills-rules.md).
-   Use a markdown file in your project directory to document your organizational standards for Build Agent. Markdown files for Build Agent are currently available only in the ServiceNow IDE. For more information, see [General guidelines for Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/build-agent-general-guidelines.md).
-   Validate compliance using Vault Console to check audit trails and security settings before deployment.
-   Develop in a sandbox using Developer Sandboxes for isolation, or use a Personal Developer Instance \(PDI\) or a non-production instance to avoid production deployment. Use one person per sandbox, keep sandboxes short-lived, create a new branch for each sandbox, and retire the sandbox when the work is complete. For more information, see [General guidelines and use cases for Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-general-guidelines.md).

