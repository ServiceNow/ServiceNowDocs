---
title: General guidelines and use cases for Developer Sandboxes
description: Follow some general guidelines to ensure you're optimizing your use of sandboxes.
locale: en-US
release: australia
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Developer Sandboxes, Developing your application, Building applications]
---

# General guidelines and use cases for Developer Sandboxes

Follow some general guidelines to ensure you're optimizing your use of sandboxes.

## Number of Developer Sandboxes users

Each sandbox should have only one person working in it. Multiple users per sandbox would negate the benefits of parallel development.

Entitlements can be stacked, supporting up to 30 sandboxes per instance.

**Note:** The number of sandboxes does not impact the instance performance.

Users can be signed into the base instance and multiple sandboxes at the same time. Sandbox users use the same login credentials for their sandbox as the base instance. If you use Single Sign-On \(SSO\) for login, when you allow it to connect to your account on the base instance, Developer Sandboxes authenticates using the same mechanism and credentials as the base instance. For information on enabling SSO, see [Installing Developer Sandboxes](dev-sbx-installing.md).

**Note:** Instances with vanity URLs support SSO.

## Timing for Developer Sandboxes

Use Developer Sandboxes to create intentionally transient environments. The longer they last, the farther they get from the original base instance. Thus, Developer Sandboxes should be as short-lived as possible.

Sandboxes are temporary and can be aligned to short development periods. For example, in Agile development, sandboxes can last as long as the following:

1.  A sprint
2.  A story
3.  A round of testing

## Examples of sandbox allocation

The following are examples of how sandboxes can be used:

-   Create branches at the start of a sprint.
-   A new branch should be created for each sandbox.
-   If you need to fix a bug in the middle a sprint, instead of stashing changes, create a second sandbox with a new branch and fix the bug there. Then merge those changes into the release branch and deploy the bug fix to production.
-   Create a sandbox to test a story or feature by pulling in the changes to a new sandbox, which you will retire when the testing is complete.

## Developer Sandboxes vs. non-production instances

Developer Sandboxes are not a replacement for non-production instances. Developer Sandboxes are intended to be temporary, while non-production instances are more permanent and intended for use long-term.

The following table compares how non-production instances and Developer Sandboxes are most effectively used.

|Non-production instances|Developer Sandboxes|
|------------------------|-------------------|
|Partition your company's work by team or project|Isolate developer metadata changes within a project.|
|Groups start from significantly different configurations|All developers begin with the same baseline instance configuration.|
|Concurrent workstreams are isolated or minimally aligned|Development activities follow a consistent cadence.|
|Durable environment for long-term changes|Work can be completed in a temporary environment and committed to version control.|

For more information on setting up sandboxes on instances, see [Installing Developer Sandboxes](dev-sbx-installing.md).

## Developer Sandboxes and ServiceNow Fluent

Developer Sandboxes work best with ServiceNow Fluent and ServiceNow IDE.

Low-code changes represented in XML markup sometimes cause merging issues, because the generated file structure can make it challenging to align changes. When using low-code builders on the ServiceNow AI Platform, the best long-term strategy is to save changes in ServiceNow Fluent instead of XML.

ServiceNow Fluent is a domain-specific programming language that you can use to define application metadata in source code. Developers and admins can easily look up changes in version control, such as Git. For details, see [ServiceNow Fluent](../../servicenow-sdk/concept/servicenow-fluent.md).

You can use Developer Sandboxes with System Update Sets, but a more forward-looking solution is to use ServiceNow IDE. Pairing your sandboxes and ServiceNow IDE with version control and deployment apps \(such as App Engine Management Center\) enables a cleaner, more streamlined deployment ecosystem. For more information, see [ServiceNow IDE](../../servicenow-ide/concept/servicenow-ide-landing.md).

## Developer Sandboxes FAQs

See the ServiceNow Community article on [Developer Sandboxes: FAQ and Getting Started Guide](https://www.servicenow.com/community/app-engine-blog/developer-sandboxes-faq-and-getting-started-guide/ba-p/3433961).

