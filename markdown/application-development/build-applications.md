---
title: Building applications
description: Learn how to become an application developer using ServiceNow AI Platform tools. Start with what you know and use AI-powered tools, a library of reusable components, and published applications to modernize your legacy processes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/build-applications.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 11
---

# Building applications

Learn how to become an application developer using ServiceNow AI Platform tools. Start with what you know and use AI-powered tools, a library of reusable components, and published applications to modernize your legacy processes.

## Get started

<table id="table_dzv_wmz_bvb" class="nav-card"><tbody><tr><td>

Learning about creating applications \[Omitted image "bus-learn.svg"\] Alt text: Learn basic information about application development.

</td><td>

[Phase 1: Planning your application \[Omitted image "bus-task-list.svg"\] Alt text: Plan how your application will work.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/planning-applications.md)

</td><td>

[Phase 2: Agentically developing your application \[Omitted image "bus-artificial-intelligence.svg"\] Alt text: Use AI tools such as Build Agent to agentically develop your application with natural language prompts.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/use-ai-capabilities-in-custom-apps.md)

</td></tr><tr><td>

[Phase 3: Developing your application \[Omitted image "bus-application-development.svg"\] Alt text: Add components and content to your application.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developing-applications.md)

</td><td>

[Phase 4: Testing and debugging your application \[Omitted image "bus-automated-testing-framework.svg"\] Alt text: Verify that the application meets your business requirements.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/testing-and-debugging-applications.md)

</td><td>

[Phase 5: Deploying your application \[Omitted image "bus-rocketship.svg"\] Alt text: Deploy your application to your production environment.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/deploying-applications.md)

</td></tr><tr><td>

[Phase 6: Maintaining your application \[Omitted image "bus-optimize-manage.svg"\] Alt text: Review the status of your application and make changes as needed.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/maintaining-applications.md)

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>## What's new

Build apps smarter and deliver them faster with the new ServiceNow Studio. ServiceNow Studio empowers platform developers with a modern, unified environment for building on the ServiceNow AI Platform. ServiceNow Studio features streamlined navigation to applications and metadata, integrated low-code tools, efficient tracking and packaging of development work that accelerates development processes and enhances productivity.

## App development phases

-   **\[Omitted image "bus-learn.svg"\] Alt text: Learning about creating applications**

    Decide whether you want to build a new application or extend an existing application. Check the ServiceNow Store and the ServiceNow Community for existing solutions.

    Before building your first application, you may want to learn some basic information about application development. This phase is optional, and you can complete it at any time while you work on other phases.

    -   How [ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-platform/now-platform-landing.md) is made up of tables and records. Learn how to convert a spreadsheet into record data.
    -   How to [Get a development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/get-dev-instance.md) to practice creating applications.
    -   How to find out [Licensing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/licensing.md) for which application features require a subscription.
    -   How to contact [Support for developers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/r_support-servicenow-developers.md) to ask questions about application development.
-   **\[Omitted image "bus-task-list.svg"\] Alt text: [Phase 1: Planning your application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/planning-applications.md)**

    The application development process starts with planning. Consider how the application will work, who will use it, and how it will improve your users' experience. Your application plan should answer the following questions:

    -   What are the goals, objectives, and outputs of your application?
    -   Who uses your application?
    -   Who has access to parts of the application?
    -   What tasks do people complete with your application?
    -   Where does the data come from?
    -   How do people interact with your application?
    -   What processes must the application support?
    -   What UI experience does the application use?
    -   Is there an existing application available on the ServiceNow Store or the ServiceNow Community that you can use or extend?
    -   What subscriptions does your application require?
-   **\[Omitted image "bus-artificial-intelligence.svg"\] Alt text: [Phase 2: Agentically developing your application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/use-ai-capabilities-in-custom-apps.md)**

    You can use AI tools to help you plan and agentically develop your application. Agentic development, or vibe coding, is an AI-driven approach to application development. Use agentic development and ServiceNow agentic-assisted app building tools, such as Build Agent, to describe your goals in natural language, and have the ServiceNow AI Platform generate full-stack applications, workflows, and integrations. As successful agentic development depends on the quality of your prompts, consider the following guidelines when working with agentic development tools:

    -   Use clear, focused prompts with as much detail as possible to generate more accurate and relevant output.
    -   If you're using Build Agent, include as much context as possible in your first prompt to enable more robust development. Include roles, data requirements, and success criteria.
    -   When switching between two separate applications in Build Agent, specify the new application context.
    -   Save your successful prompts to repurpose and reuse. For more information, see [Example prompts for agentic development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/vibe-coding-example-prompts.md).
    -   Save your session to quickly resume working where you stopped.
    -   Use the Build Agent chat panel for iterative development.
    -   Validate compliance using Vault Console to check audit trails and security settings before deployment.
    -   Develop in a sandbox using Developer Sandboxes for isolation and safety, or use a Personal Development Instance \(PDI\) or a non-production instance to avoid production deployment.
-   **\[Omitted image "bus-application-development.svg"\] Alt text: [Phase 3: Developing your application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developing-applications.md)**

    During the development phase, you add the components and content of your application. Most applications consist of the following:

    -   **Data**

        Information is stored in your application via tables that you configure. For example, employee phone numbers or office locations.

    -   **Experience**

        Experiences are graphical interfaces that your users interact with. For example, you can create a portal where users find information, submit requests, or complete business tasks.

    -   **Logic and automation**

        Automate all the work in your application by adding logic and automation. For example, you can build a flow that sends a notification to the admin when someone makes a request.

    -   **Security**

        Configure roles and access controls to limit who can use your application. For example, you can restrict access to application data to users who have a specific role.

    Choose a builder that matches the type of user experience that your application provides.

    -   See [ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/servicenow-studio-landing.md) to learn about the unified developer experience on the ServiceNow AI Platform.
    -   See [Build apps using App Engine Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-studio/aes-overview.md) to learn about low-code development.
    -   See [Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/creator-studio/creator-studio-landing.md) to learn about no-code development.
    -   See [Build workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/build-workflows.md) to learn about creating automation with Workflow Studio.
    -   See [Builder library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/builder-library-table.md) to learn about specialized application resources.
-   **\[Omitted image "bus-artificial-intelligence.svg"\] Alt text: [Phase 3: Agentically developing your application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/use-ai-capabilities-in-custom-apps.md)**

    You can use AI tools to help you plan and agentically develop your application. Agentic development, or vibe coding, is an AI-driven approach to application development. Use agentic development and ServiceNow agentic-assisted app building tools, such as Build Agent, to describe your goals in natural language, and have the ServiceNow AI Platform generate full-stack applications, workflows, and integrations. As successful agentic development depends on the quality of your prompts, consider the following guidelines when working with agentic development tools:

    -   Use clear, focused prompts with as much detail as possible to generate more accurate and relevant output.
    -   If you're using Build Agent, include as much context as possible in your first prompt to enable more robust development. Include roles, data requirements, and success criteria.
    -   When switching between two separate applications in Build Agent, specify the new application context.
    -   Save your successful prompts to repurpose and reuse. For more information, see [Example prompts for agentic development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/vibe-coding-example-prompts.md).
    -   Save your session to quickly resume working where you stopped.
    -   Use the Build Agent chat panel for iterative development.
    -   Validate compliance using Vault Console to check audit trails and security settings before deployment.
    -   Develop in a sandbox using Developer Sandboxes for isolation and safety, or use a Personal Development Instance \(PDI\) or a non-production instance to avoid production deployment.
-   **\[Omitted image "bus-automated-testing-framework.svg"\] Alt text: [Phase 4: Testing and debugging your application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/testing-and-debugging-applications.md)**

    Verify that the application meets your business requirements. Your testing should cover the following elements:

    -   Record operations, such as create, read, update, and delete.
    -   User interface elements, such as views and UI policies.
    -   Runtime operations, such as business rules and event script actions.
-   **\[Omitted image "bus-rocketship.svg"\] Alt text: [Phase 5: Deploying your application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/deploying-applications.md)**

    After successfully testing an application, deploy it to your production environment with your builder tool.

    -   See [ReleaseOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/releaseops/releaseops-landing.md) to learn about the improved and automated deployment process with ReleaseOps.
    -   See [App Engine Management Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/app-engine-management-center.md) to learn about the unified app governance and deployment experience on the ServiceNow AI Platform.
    -   See [ServiceNow application repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/application-repository-self-hosted/app-repo.md) to learn about the Application Repository.
    -   See [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/system-update-sets/system-update-sets.md) to learn about classic deployment using update sets.
-   **\[Omitted image "bus-optimize-manage.svg"\] Alt text: [Phase 6: Maintaining your application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/maintaining-applications.md)**

    Use your Phase 2 builder tool to update and modify your application. Use your Phase 3 testing tool to verify that your application still functions properly.


## Applications and features

-   [Learning about developing on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/getting-started-with-building-applications.md)
-   [Planning your application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/planning-applications.md)
-   [Agentically developing your application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/use-ai-capabilities-in-custom-apps.md)
-   [Developing your application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developing-applications.md)
-   [Testing and debugging applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/testing-and-debugging-applications.md)
-   [Deploying applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/deploying-applications.md)
-   [Maintaining your application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/maintaining-applications.md)

