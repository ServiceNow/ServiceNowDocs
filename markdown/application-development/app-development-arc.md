---
title: App development in Arc
description: Arc builds ServiceNow apps for you with the Now SDK, from planning the app to installing it on your instance, through a conversation in a chat.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/app-development-arc.html
release: australia
topic_type: concept
last_updated: "2026-10-27"
reading_time_minutes: 1
keywords: [app development, Now SDK, Fluent, ServiceNow App Development skill, scoped app]
breadcrumb: [Use, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# App development in Arc

Arc builds ServiceNow apps for you with the Now SDK, from planning the app to installing it on your instance, through a conversation in a chat.

Arc includes the ServiceNow App Development skill, which it uses when you ask Arc to create, build, or change an app.

**Note:** App development isn't supported on Windows.

## How Arc builds an app

1.  Arc shows you a build plan and waits for your approval before it creates any files.
2.  Arc asks which folder on your computer should get the app's source.
3.  Arc creates the project in its sandbox and writes the app's metadata as source files.
4.  Arc builds the app and checks that each item compiled.
5.  Arc saves the source as an archive file in the folder you chose.
6.  Arc asks for your approval before it installs the app or makes any other change on your instance. Approval rules that your administrator sets also apply.
7.  Arc checks each item on the instance after the install and reports only the items it verified.

For each part of a request, Arc decides whether it belongs in the app's source or needs another route, such as a change on the instance itself, and tells you which route it uses.

## App source and existing projects

The project lives in the Arc sandbox. The archive saved on your computer is your copy of the source. If the sandbox is recreated, attach that archive in a chat to continue working on the app.

For an existing project, Arc uses the Now SDK version that the project specifies and follows that version's documentation.

-   **[Build a ServiceNow app with Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/build-app-arc.md)**  
Describe the app you need, approve the plan, and let Arc build the app, save its source to your computer, and install it on your instance.

**Parent Topic:**[Using ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-using.md)

