---
title: Exploring Developer Sandboxes
description: Developer Sandboxes provide isolated development environments that enable parallel building and testing on top of a shared development instance. Use sandboxes to reduce code conflicts, accelerate delivery, and safely test configurations without affecting other team members' work.
locale: en-US
release: australia
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [developer sandbox, sandbox developer, servicenow sandbox enabled, development sandbox, dev sandbox, sandbox management, sandbox enabled servicenow, sandbox crm]
breadcrumb: [Developer Sandboxes, Developing your application, Building applications]
---

# Exploring Developer Sandboxes

Developer Sandboxes provide isolated development environments that enable parallel building and testing on top of a shared development instance. Use sandboxes to reduce code conflicts, accelerate delivery, and safely test configurations without affecting other team members' work.

![Developer Sandboxes architecture and workflow. For the text description, refer to the following sections.](../image/dev-sbx-infographic1-updated.png "How Developer Sandboxes work")

-   Developer Sandboxes are isolated environments for parallel building and testing.
-   Each sandbox is provisioned on demand and fully isolated from others.
-   Every sandbox contains the full metadata of the base instance.
-   Sandboxes can be assigned to specific stories, developers, test plans, or custom criteria.

## Developer Sandboxes overview

Developer Sandboxes aim to provide lower-cost developer isolation and parallelism for customer development environments and instances. Developer Sandboxes are workflow-agnostic and are broadly applicable across workflows for both smaller and larger companies.

Organizations can face challenges when addressing urgent defects and critical feature enhancements simultaneously in applications. Traditional shared development environments introduce risks such as code conflicts, configuration overlaps, and deployment delays, making it difficult to manage parallel workstreams efficiently. Development teams struggle to deliver urgent fixes and new features concurrently without disrupting each others' progress. The absence of isolated, independent development environments slows down delivery, increases rework, and hampers overall agility.

Developer Sandboxes enables better development in the following ways:

-   Isolation: Each developer works in an independent sandbox, ensuring changes do not affect other team members’ work.
-   Faster delivery: Teams can work concurrently, reducing development cycle time and enabling faster turnaround for urgent fixes and enhancements.
-   Safe testing: Developers can test configurations, workflows, and integrations within their sandbox without risking system stability.
-   On-demand provisioning: Admins and developers can quickly provision sandboxes for specific tasks or experiments without waiting for shared resources.

**Note:** Personal Development Instances \(PDIs\) are still available, but they don't have a controlled baseline configuration like Developer Sandboxes do.

![Sandbox Management home dashboard.](../image/sandboxes-management-home.png)

The Sandbox Management home dashboard displays the total, available, and allocated sandboxes in your instance. The dashboard also displays information relevant to each sandbox, including, the status, data utilization, owner, last accessed date, and when the sandbox was allocated.

Check your entitlements to determine whether you have access to Developer Sandboxes. For more information, see [Developer Sandboxes entitlements](dev-sbx-entitlements.md).

Upgrading an instance automatically backs up update sets to the base instance and recreates the sandboxes on that instance. Sandboxes are recreated in a base state, so you must restore backed up update sets. For details, see [Cloning and upgrading considerations for Developer Sandboxes](dev-sbx-clone-upgrade-info.md).

**Note:** Build Agent it not yet supported in Developer Sandboxes.

## Integrate sandboxes with source control

Developer Sandboxes provide an isolated environment that integrates with source control, such as Git. Using merge tools helps eliminate conflicts and enables parallel development. For more information, see [Source control and Developer Sandboxes](dev-sandboxes-source-control.md).

## Developer Sandboxes users

|User|Description|
|----|-----------|
|Delegated developers|Delegated developers can request, allocate, or retire sandboxes.|
|Admins|Admins can allocate or retire sandboxes.|
|Sandbox managers|Sandbox managers can administer the lifecycle of all sandboxes without full admin privileges.|
|Sandbox users|Sandbox users can request and view Developer Sandboxes.|

Sandbox users use the same login credentials for their sandbox as the base instance. If you use Single Sign-On \(SSO\) for login, when you enable it to connect to your account on the base instance, Developer Sandboxes authenticates using the same mechanism and credentials as the base instance. For information on enabling SSO, see [Installing Developer Sandboxes](dev-sbx-installing.md).

**Note:** Instances with vanity URLs support SSO.

## Developer Sandboxes workflow

The delegated developer or admin of a sandbox would procure a sandbox, make changes or experiment with development, test their changes, push their changes, and wait for an admin to clone the instance.

1.  A Developer Sandboxes user \(either admin or dev\) allocates a sandbox to start story work.
2.  The developer makes development changes and tests them out in their fully isolated sandbox.

    **Note:** The work done in one sandbox doesn't appear in other sandboxes or other instances.

3.  Once the developer is content with their work and ready to promote their changes to a shared, integrated environment, they push their changes to the desired upstream shared instance. For example, a `test`/`QA` instance. There are two ways to promote changes:
    1.  Using source control \(preferable\) or exports through Git
    2.  Using update sets and imports \(supported, but not as easy to merge changes\)
4.  Further testing can be done on the shared instance.
5.  The admin of a sandbox instance clones changes from the `test`/`QA` instance to make those changes the default for all future allocated sandboxes.

## Developer Sandboxes benefits

<table id="table_fw5_sqm_bcc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Enable parallel development

</td><td>

Enable multiple developers the ability to work on different stories or features at the same time using the same starting source code, all while keeping the non-production baseline instance clean.

</td><td>

-   Admins
-   Delegated developers

</td></tr><tr><td>

Reduce merge conflicts with source control

</td><td>

Enables integration with source control for more successful co-development. For more information, see [Source control and Developer Sandboxes](dev-sandboxes-source-control.md).

</td><td>

Delegated developers

</td></tr><tr><td>

Reuse sandbox templates

</td><td>

Enables the optional setup of a repository configuration. You can create a template once, and reuse any existing templates when creating sandboxes. For more information, see [Using sandbox templates](../task/create-sandbox-template.md).

</td><td>

-   Admins
-   Delegated developers

</td></tr><tr><td>

Sandbox alias

</td><td>

Enables you to easily reference the sandbox you want to allocate.

</td><td>

-   Admins
-   Delegated developers

</td></tr><tr><td>

Allocate to

</td><td>

Enables you to allocate a sandbox to yourself, or for an admin to allocate a sandbox to someone else.

</td><td>

-   Admins
-   Delegated developers

</td></tr></tbody>
</table>## What to explore next

To learn more about installing and configuring Developer Sandboxes, refer to [Installing Developer Sandboxes](dev-sbx-installing.md).

