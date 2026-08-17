---
title: Reset OAuth for a clone target
description: Reset OAuth to reauthorize the target instance if a clone request fails due to authentication issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/reauthorize-clone-target.html
release: australia
topic_type: task
last_updated: "2026-06-10"
reading_time_minutes: 1
breadcrumb: [Register instance, Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Reset OAuth for a clone target

Reset OAuth to reauthorize the target instance if a clone request fails due to authentication issues.

## Before you begin

The target instance must run an OAuth-capable version of the Clone Admin Console.

Roles required:

-   Source instance: clone\_admin
-   Target instance: clone\_admin and oauth\_admin

## About this task

If a clone request fails due to any errors or authentication issues, the Clone Admin Console displays an Authenticate dialog with the option to reset OAuth. Resetting OAuth reauthorizes the target instance so you can retry the clone request.

## Procedure

1.  In the Authenticate dialog, select **Reset OAuth**.

    The target instance opens in a new browser tab and displays the OAuth setup dialog.

2.  Select **Set up OAuth**.

    The page generates a new client ID.

    If the client ID is not generated, verify that you have the oauth\_admin role on the target instance and that the page is loaded completely before selecting **Set up OAuth**.

3.  Copy the client ID and return to the source instance browser tab.

4.  Paste the client ID in the **Client ID** field.

5.  Select **Complete Setup**.

    The Authorization Required dialog is displayed.

6.  Select **Proceed**.

    The browser redirects to the target instance to complete authorization.

7.  Select **Allow** to grant consent.

    If your session has expired, log in to the target instance before granting consent.

    The browser redirects to the source instance to submit the clone request.


## Result

The target instance is reauthorized.

## What to do next

To submit a clone request to the reauthorized target, see [Request a clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_StartAClone.md).

