---
title: Component development lifecycle
description: The stages of building a Next Experience UI Framework component with the ui-component extension, from project creation through deployment and maintenance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/ui-component-development-lifecycle.html
release: australia
topic_type: concept
last_updated: "2026-10-27"
reading_time_minutes: 1
breadcrumb: [Explore, UI component CLI extension, Building pro-code applications, Developing your application, Classic app development, Building applications]
---

# Component development lifecycle

The stages of building a Next Experience UI Framework component with the ui-component extension, from project creation through deployment and maintenance.

The UI component CLI extension supports each stage of developing a Next Experience UI Framework component. The stages run in sequence, and each one prepares the project for the next. Most stages use the ServiceNow CLI, so the connection to your instance is set up before development begins.

## Setting up the environment

Development requires a configured development environment and a default ServiceNow CLI connection profile. The profile stores the connection details that the CLI uses for every command that connects to an instance. For the installation and profile procedures, see [Install the ServiceNow CLI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cli/download-cli.md) and [Create a default profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cli/create-default-profile.md).

## Creating a project

The project command creates the structure that a component project needs. The command generates the directory structure, the configuration files that the UI component CLI extension reads, and a component tag name. The tag name starts with the customer prefix from the connected instance, so the component name is consistent with the instance it deploys to.

## Developing components

A new component renders an empty container until you add content to its source. Changes appear in the browser through the local development server, which refreshes the page as you save. Projects can contain more than one component. Each additional component uses a tag name that starts with the company code, which is the first argument to the createCustomElement function.

## Deploying components

Deployment writes the component to a ServiceNow instance as a scoped application. The deployment depends on a valid default connection profile and on a scope name that the instance accepts. A project created offline must have its scope name confirmed against the instance before deployment, because the offline setup skips that check. For the scope name rules, see the component configuration properties reference.

## Maintaining project dependencies

A component depends on other published components, and those dependencies change over time. Updating a dependency version in the project package file changes the version the project uses. Package managers can keep older versions cached, so a dependency update can require removing the installed modules and reinstalling them.

