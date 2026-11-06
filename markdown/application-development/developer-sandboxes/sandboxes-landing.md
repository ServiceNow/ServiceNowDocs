---
title: Developer Sandboxes
description: Developer Sandboxes are isolated development environments on a shared instance. Delegated developers use them to build and merge changes in parallel, and admins request and manage them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/developer-sandboxes/sandboxes-landing.html
release: australia
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: reference
last_updated: "2026-10-27"
reading_time_minutes: 3
keywords: [developer sandbox, sandbox developer, servicenow sandbox enabled, development sandbox, dev sandbox, sandbox management, delegated developer, parallel development, isolated development environment, clone and upgrade sandboxes]
breadcrumb: [Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Developer Sandboxes

Developer Sandboxes are isolated development environments on a shared instance. Delegated developers use them to build and merge changes in parallel, and admins request and manage them.

## Overview video

\[Omitted video\] Description: Developer Sandboxes overview video

The video explains that Developer Sandboxes are isolated development environments and describes the benefits of that isolation. It also covers the following topics:

-   Basic overview of sandbox benefits and metadata
-   Roles for working with sandboxes
-   Parallel development
-   Sandbox lifecycle, including allocating and retiring sandboxes
-   Tasks that developers can do in a sandbox
-   Updates pushed with Git or update sets
-   Sandbox drift and the base instance configuration

## About Developer Sandboxes

Use Developer Sandboxes to create isolated development environments where users can develop on the ServiceNow AI Platform in parallel. Sandboxes are temporary because they drift from the base instance configuration the longer they exist. Sandboxes support Git-based workflows of the software development life cycle and help reduce conflicts.

Use Developer Sandboxes to do the following:

-   Provision isolated development environments on demand
-   Align workspaces to specific stories, developers, test plans, or any custom criteria
-   Enable true parallel development with controlled, independent environments

After allocation, developers can access their sandbox in the following ways:

-   Select the sandbox name on the Sandbox Management Home page.
-   Copy the sandbox URL from the context menu and paste it in a browser.

**Note:** If your instance is in a regulated environment, check with ServiceNow Support for more information about support for Developer Sandboxes.

## Get started

<table id="table_bcm_2pm_bcc" class="nav-card presentation"><tbody><tr><td>

[Explore\[Omitted image "bus-explore.svg"\] Alt text:Learn how Developer Sandboxes isolate changes and who uses them.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/exploring-sandboxes.md)

</td><td>

[Clone and upgrade\[Omitted image "bus-workflow.svg"\] Alt text:Learn what happens to sandboxes and saved work when you clone or upgrade an instance.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-clone-upgrade-info.md)

</td></tr><tr><td>

[Install and configure\[Omitted image "bus-sdlc.svg"\] Alt text:Set up Developer Sandboxes for your instance.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-configuring-landing.md)

</td><td>

[Administer\[Omitted image "bus-try-a-demo.svg"\] Alt text:Request, allocate, and manage sandboxes for developers.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/administering-sandboxes.md)

</td></tr></tbody>
</table>## Troubleshoot and get help

-   [Ask questions and explore other resources for Developer Sandboxes in the ServiceNow Community](https://www.servicenow.com/community/)
-   [Search the Known Error Portal for known error articles \[KB0597477\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [See the Developer Sandboxes FAQ and getting started guide](https://www.servicenow.com/community/app-engine-blog/developer-sandboxes-faq-and-getting-started-guide/ba-p/3433961)
-   [Take the Developer Sandboxes Basics class on ServiceNow University](https://learning.servicenow.com/lxp/en/app-engine/developer-sandbox-basics-english-zurich?id=learning_course_prev&course_id=4bc515cf97047a503845f3f0f053af16&s=1&ssa=3)
-   [Read a Community blog post about Developer Sandboxes](https://www.servicenow.com/community/app-engine-blog/zurich-release-brings-app-dev-to-the-beach/ba-p/3339173)
-   [Watch a YouTube video demo of merging changes in Git](https://www.youtube.com/watch?v=FmzU7HYlV-g)
-   [Contact Customer Service and Support](https://support.servicenow.com/now)

-   **[Exploring Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/exploring-sandboxes.md)**  
Developer Sandboxes provide isolated development environments that enable parallel building and testing on top of a shared development instance. Use sandboxes to reduce code conflicts, accelerate delivery, and safely test configurations without affecting other team members' work.
-   **[Cloning and upgrading considerations for Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dev-sbx-clone-upgrade-info.md)**  
You should understand how plugins and sandboxes work before you clone or upgrade an instance with Developer Sandboxes. Back up your work in a sandbox before any clone or upgrade, either by exporting the update sets or committing to source control.
-   **[Developer Sandboxes installation and configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/dsb-configuring-landing.md)**  
Developer Sandboxes installation and configuration covers Developer Sandboxes on your instance. Review entitlements, install the plugins, assign licenses, and look up the roles, tables, and properties that control how sandboxes work.
-   **[Administering Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/developer-sandboxes/administering-sandboxes.md)**  
If you have permission, you can allocate and retire the sandboxes you've created in your instance.

**Parent Topic:**[Build](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/build-ai-workflow-factory-prime.md)

