---
title: Exploring the UI component CLI extension
description: Learn about UI component CLI extension concepts and features.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/exploring-ui-component-cli-extension.html
release: australia
topic_type: concept
last_updated: "2026-10-24"
reading_time_minutes: 1
breadcrumb: [UI component CLI extension, Building pro-code applications, Developing your application, Classic app development, Building applications]
---

# Exploring the UI component CLI extension

Learn about UI component CLI extension concepts and features.

The UI component CLI extension abstracts the workflows that you use to build Next Experience UI Framework components. Instead of running separate tools for each stage, you run commands from the ServiceNow CLI.

## Component development workflow

The extension supports the following stages of component development:

-   Project scaffolding, which creates the files that a new project needs.
-   A local development server, which runs components so that you can evaluate and iterate on them.
-   Deployment, which installs the component into a ServiceNow instance.

\[Omitted image "workflow-snc.png"\] Alt text: Diagram showing the stages of Next Experience UI component development, from project scaffolding through local development to deployment in a ServiceNow instance.

## Scope and deployment

Next Experience UI Framework components deploy to a ServiceNow instance as part of a scoped application. Each component is written to the records of a specific scope.

You define the scope name for a project in the `now-ui.json` file. When the component deploys, its records are written to the tables that belong to that scope. Only one project can deploy to a single scope.

A valid scope name meets the following requirements:

-   It is unique on the instance.
-   It uses snake case and has no more than 18 characters.
-   It follows the form `x_customerprefix_componentname`, where the customer prefix matches the value of the `glide.appcreator.company.code` system property.

If you don't provide a scope name, the extension creates one from the vendor prefix and the package name. A scope name that does not meet these requirements can prevent the project from deploying.

