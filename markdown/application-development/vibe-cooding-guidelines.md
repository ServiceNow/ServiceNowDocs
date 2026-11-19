---
title: General guidelines for agentic development
description: General guidelines for agentic development on the ServiceNow AI Platform cover prompt writing, context management, compliance validation, and development environment setup.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/vibe-cooding-guidelines.html
release: brazil
topic_type: concept
last_updated: "2026-11-03"
reading_time_minutes: 2
keywords: [agentic development, prompt writing, context management, compliance validation, development environment, build agent, developer sandboxes, iterative development, vault console]
breadcrumb: [Explore, Agentic development guide, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# General guidelines for agentic development

General guidelines for agentic development on the ServiceNow AI Platform cover prompt writing, context management, compliance validation, and development environment setup.

## Agentic development guidelines

-   Use clear, focused prompts with as much detail as possible to generate more accurate and relevant output.
-   If you're using Build Agent, include as much context as possible in your first prompt to enable more robust development. Include roles, data requirements, and success criteria.
-   When switching between two separate applications in Build Agent, specify the new application context.
-   Save your successful prompts to repurpose and reuse. For more information, see [Example prompts for agentic development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/vibe-coding-example-prompts.md).
-   Save your session to quickly resume working where you stopped.
-   Use the Build Agent chat panel for iterative development.
-   Develop each page or feature in a separate chat. Implement and test the feature, and then start a new chat for the next one.
-   For large or complex implementations, use Autonomous Engineer. It interviews you, generates a plan with work items, and builds the work items in parallel. For more information, see [Autonomous Engineer in Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/vc-autonomous-engineer.md).
-   Define custom skills and rules to apply your organization's standards in every session. For more information, see [Configure custom skills and rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ba-configure-custom-skills-rules.md).
-   Validate compliance using Vault Console to check audit trails and security settings before deployment.
-   Develop in a sandbox using Developer Sandboxes for isolation and safety, or use a Personal Developer Instance \(PDI\) or a non-production instance to avoid production deployment.
-   Use one sandbox for each developer, keep sandboxes short-lived, and retire a sandbox when the work is complete. For more information, see [General guidelines and use cases for Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-general-guidelines.md).

**Parent Topic:**[Exploring agentic development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/exploring-vibe-coding.md)

