---
title: Choosing your build approach
description: Understand when to use AI-assisted tools like the app generation skill with Now Assist for Creator and Build Agent versus when to build an application manually on the ServiceNow AI Platform.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-31"
reading_time_minutes: 3
breadcrumb: [Use AI to build apps faster, Getting Started guide for developers, Building applications]
---

# Choosing your build approach

Understand when to use AI-assisted tools like the app generation skill with Now Assist for Creator and Build Agent versus when to build an application manually on the ServiceNow AI Platform.

ServiceNow offers a spectrum of development approaches, from AI-driven app generation to fully manual builds. The right approach depends on the complexity of your application, how well defined your requirements are, and how much control you need over the implementation details. Many projects benefit from a hybrid approach, using AI tools to accelerate routine work while applying manual techniques where precision matters most.

## When to use AI-assisted tools

AI-assisted tools are most effective when you want to accelerate development, reduce repetitive work, or quickly explore what is possible on the ServiceNow AI Platform. Consider using Build Agent or the app generation skill available with Now Assist for Creator when your project meets one or more of the following conditions:

-   **Requirements are clear and well-scoped.**

    AI tools perform best when you can describe the application's purpose, key data model, and core workflows in plain language. If you can explain the app in a few sentences, AI can often produce a useful starting point quickly.

-   **You're prototyping or validating an idea.**

    The app generation skill and Build Agent can generate a working application scaffold in minutes, making it easy to test assumptions with stakeholders before committing to a full build.

-   **The application follows common patterns.**

    Apps that rely on standard ServiceNow patterns, such as request management, approval workflows, or record-keeping, are well-suited for AI generation because these AI tools are trained on standard ServiceNow patterns.

-   **You want to accelerate individual development tasks.**

    Even if you plan to build most of an app manually, contextual skills within Now Assist for Creator can help with discrete tasks such as generating flows, writing scripts, or creating business rules, saving time without requiring a full AI-driven build.

-   **You're newer to using the ServiceNow AI Platform.**

    AI tools can help developers who are less familiar with ServiceNow conventions by generating conformant app structures and metadata, which you can then learn from and extend.


## When to build manually

Manual development gives you direct control over every aspect of your application. Consider a manual approach when your project has characteristics that AI tools may not handle well:

-   **Requirements are complex or highly specialized.**

    Applications with intricate data relationships, advanced security requirements, or non-standard integration patterns may require design decisions that AI tools cannot reliably make. Manual development enables you to apply domain expertise at every step.

-   **You need precise control over the implementation.**

    When performance, scalability, or specific ServiceNow AI Platform behaviors are critical, building manually helps to verify that the implementation meets your exact specifications without requiring significant rework of AI-generated output.

-   **The application has extensive custom business logic.**

    If your workflows involve complex conditional logic, multi-step orchestration, or heavy scripting, manually authoring that logic gives you greater reliability and easier long-term maintenance.

-   **You're extending or modifying an existing application.**

    When working within an established application that has its own patterns, naming conventions, and data model, manual development can enable consistency and help to avoid conflicts that AI-generated components might introduce.

-   **Governance or Compliance requirements demand manual oversight.**

    In environments where every configuration decision must be documented and reviewed, manually building and reviewing each application component may be more appropriate than reviewing and accepting AI-generated output.


## Combining AI and manual techniques

AI and manual app development are not mutually exclusive. A common strategy is to use Build Agent or the app generation skill to create an initial application scaffold, and then refine the result manually. For example, you might generate the data model and basic views with AI, and then hand-author complex business rules, integrations, and access controls. This approach can significantly reduce your time to value, while preserving full developer control over the parts of the application that matter most.

**Parent Topic:**[Use AI to build apps faster](dev-get-start-use-ai-to-build-faster.md)

