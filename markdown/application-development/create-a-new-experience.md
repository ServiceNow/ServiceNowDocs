---
title: Create an experience
description: Build a Lux experience from scratch in Lux Lab. The new project comes with sample pages, widgets, and the standard project structure, ready for you to add your own pages and widgets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/create-a-new-experience.html
release: zurich
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [Create a new experience]
breadcrumb: [Using Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# Create an experience

Build a Lux experience from scratch in Lux Lab. The new project comes with sample pages, widgets, and the standard project structure, ready for you to add your own pages and widgets.

## Before you begin

Your machine meets the minimum system requirements in [Configuring Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/configuring-lux-lab.md). Lux Lab is connected to an instance. For instructions, see [Connect Lux Lab to an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/connecting-lux-lab-to-an-instance.md).

Role required: admin

## About this task

To create an experience that extends an existing application instead, see [Extend an existing experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/extend-an-existing-experience.md).

## Procedure

1.  Select the project name in the title bar.

2.  Select **New Project**.

3.  In the **Create New Project** dialog, on the **Create New** tab, select the **Base AIUX template**.

4.  Enter a **Project Name**.

5.  Select a **Project Location** on your local drive.

    To pick a folder, select **Browse**.

6.  Confirm or edit the **Scope**.

    The field is auto-filled from your connected instance, for example with `x_snc_`. The full scope takes the form `x_abc_myapp`.

7.  Select **Create Project**.


## Result

Lux Lab scaffolds the project, installs dependencies, and opens it in the app automatically. The new project contains sample pages, widgets, and other Lux Lab experience metadata, following the standard project structure \(`aiux.json`, `application.js`, `pages/`, `widgets/`, and so on\).

## What to do next

Start creating pages and widgets in your experience. For the ways to add a page, see [Create a page with Lux Lab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/create-a-page-with-lux-lab.md).

