---
title: Manage collaboration requests
description: As an admin, view and approve or reject collaboration requests in the App Engine Management Center \(AEMC\) from developers who want assistance building their applications.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage requests, Manage app development, Use, App Engine Management Center, Governing app development, Building applications]
---

# Manage collaboration requests

As an admin, view and approve or reject collaboration requests in the App Engine Management Center \(AEMC\) from developers who want assistance building their applications.

## Before you begin

To view collaboration requests in AEMC, you must first set up Pipelines and Deployments in your production instance. Otherwise, requests are created on the instance where they originated \(that is, the instance with App Engine Studio \(AES\) installed\).

Role required: sn\_app\_eng\_notify.app\_engine\_admin

## About this task

Developers with collaboration permissions can access and develop certain parts of an application. Requests for collaboration may come from App Engine Studio or Creator Studio.

Requests from collaborators may be approved automatically depending on permissions or roles they already have.

-   For AES collaboration requests, users who have the AES User role are approved automatically.
-   Creator Studio users who have already created an app \(or have had one created for them\) have delegated development permissions, and are automatically approved to collaborate on other apps.
-   Current delegated developers without the Creator Studio User or Creator Studio Restricted User roles are automatically approved to collaborate in Creator Studio.

For more information about managing collaboration and permissions, see [Collaborate with other developers](../concept/aes-collaboration-feature-overview.md#).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Administration** &gt; **App Engine Management Center**.

    The AEMC dashboard shows the number of pending collaboration requests.

    **Note:** To view a list of all collaboration requests, either select the number of requests or select the Requests page.

2.  Select a collaboration request to review its details.

3.  Return to the **Details** tab and review the request.

4.  Approve or reject the request.

    -   If the request is approved, the user invited to be a collaborator is added as a developer to the specified app. The collaborator can now work on the parts of the app defined in the Collaboration Descriptor, but cannot concurrently develop other apps in AES. For more information about the AES User role, see [Components installed with App Engine Studio](../reference/installed-with-aes.md).
    -   If the request is rejected, the request is closed, and the primary developer is notified by email.

**Parent Topic:**[Managing requests using AEMC](../concept/manage-aemc-requests.md)

