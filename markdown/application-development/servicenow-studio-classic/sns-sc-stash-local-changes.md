---
title: Stash local changes
description: Stash local application file changes in ServiceNow Studio to save them temporarily, pull the latest version from the repository, and recover the stashed changes at a later time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/sns-sc-stash-local-changes.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 1
breadcrumb: [Work with changes in Git, Source control in ServiceNow Studio, Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Stash local changes

Stash local application file changes in ServiceNow Studio to save them temporarily, pull the latest version from the repository, and recover the stashed changes at a later time.

## Before you begin

[Link an app to source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/link-app-to-source-control.md)

At least one changed application file must exist before stashing.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the file navigator, select the application you want to open.

3.  Select **App details** to open the app in the canvas.

4.  Select **Source control** &gt; **Stash changes**.

    The system displays a list of locally changed files.

5.  Enter a **Stash description**.

6.  Select **Stash changes**.


## Result

The local changes are saved to the stash. Pull the latest version from the repository and apply the stashed changes when ready.

**Parent Topic:**[Work with changes in Git](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-sc-work-with-changes-in-git.md)

