---
title: Deploy changes
description: Deploy your project from Lux Lab to a connected instance, where you can preview and publish your experiences, pages, and widgets. Lux Lab builds the project and installs it on the instance in one action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/deploy-changes.html
release: zurich
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [Deploy changes, Deploy drop-down list options]
breadcrumb: [Using Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# Deploy changes

Deploy your project from Lux Lab to a connected instance, where you can preview and publish your experiences, pages, and widgets. Lux Lab builds the project and installs it on the instance in one action.

## Before you begin

Your machine meets the minimum system requirements in [Configuring Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/configuring-lux-lab.md).

Lux Lab is connected to an instance. For instructions, see [Connect Lux Lab to an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/connecting-lux-lab-to-an-instance.md).

Role required: admin

## About this task

You can deploy manually, as the following steps describe, or conversationally with an AI agent in the Agent Chat Harness.

To show more options, select the arrow next to **Deploy**.

|Option|Description|
|------|-----------|
|Build|Build step only, without deploying|
|Custom Deploy|Deployment to a different, previously connected instance instead of the one you're logged into|
|Project scripts|Scripts defined in the current project's `package.json`, runnable directly from the drop-down list|

## Procedure

1.  Select **Deploy** in the title bar, or press `Cmd+Shift+D` \(macOS\) or `Ctrl+Shift+D` \(Windows\).

2.  If you have multiple projects open in the workspace, select the project to deploy.


## Result

Lux Lab builds the application, compiling and bundling the source code into deployable artifacts. It then runs `now-sdk install` to deploy the built artifacts to your active connected instance. Build and deploy output streams into the **Build** tab of the bottom panel. If the deployment succeeds, a confirmation banner appears.

## What to do next

Preview and test your changes on your instance.

