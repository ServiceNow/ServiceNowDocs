---
title: Manage intake requests
description: View details of intake requests submitted by developers in App Engine Studio in the App Engine Management Center \(AEMC\) dashboard, and approve or reject them.
locale: en-US
release: australia
product: App Engine Management Center
classification: app-engine-management-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage requests, Manage app development, Use, App Engine Management Center, Governing app development, Building applications]
---

# Manage intake requests

View details of intake requests submitted by developers in App Engine Studio in the App Engine Management Center \(AEMC\) dashboard, and approve or reject them.

## Before you begin

Before intake requests can be displayed in AEMC, you must confirm that the Application Intake application has been properly configured. For more information, see [Configure Application Intake](config-app-intake.md). For more information about how to submit intake requests, see [Submit your idea for app development](submit-intake-request.md).

App requests submitted from Creator Studio restricted users are managed on the App tab on the Requests page. For more information, see [Manage app requests from Creator Studio](manage-app-requests-creator-studio.md).

Role required: sn\_app\_eng\_notify.app\_engine\_admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Administration** &gt; **App Engine Management Center**.

    The AEMC dashboard shows the number of pending intake requests.

    **Note:** To view a list of all intake requests, either select the number of requests or select the Requests page.

2.  Select an intake request to review its details.

    ![Pending application intake request to review](../image/app-intake-record.png "Pending intake request")

3.  Return to the **Details** tab and review the request.

    **Note:** The **Administration** section includes a **Development instance** field. Make sure that the development instance the developer intends to use has been selected. Also, if the user isn’t defined on that instance, a message displays and you must manually add the user to that instance. For more information, see [Create a user](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

4.  Use the **Permission type** list in the Administration section to select one of the following options for provisioning groups to this application.

<table id="choicetable_ok3_pfq_vbc"><thead><tr><th align="left" id="d66087e220">

Permission type

</th><th align="left" id="d66087e223">

Description

</th></tr></thead><tbody><tr><td id="d66087e229">

**Select group\(s\)**

</td><td>

Option to give one or more of the following groups permission to develop this application.-   App Engine Studio User Limited
-   App Engine Studio Users
-   Creator Studio Restricted Users
-   Creator Studio Users
For more information about how to control which groups show up in this list, see [Manage user groups for Application Intake](manage-app-intake-user-groups.md).

</td></tr><tr><td id="d66087e278">

**I will manually provision user**

</td><td>

Option to add groups to the application manually.

</td></tr><tr><td id="d66087e287">

**Do not give requestor permissions**

</td><td>

Option not to add any groups to the application at the time of the request.

</td></tr></tbody>
</table>5.  Approve or reject the request.

    -   If the request is approved, the user is added to the App Engine Studio User group and granted the App Engine Studio User role. The AES User role enables developers to begin creating their application in AES in the approved instance. The user also receives an email notification with a link to the provisioned instance. For more information about the AES User role, see [Components installed with App Engine Studio](../reference/installed-with-aes.md).
    -   If the request is rejected, a rejection email is sent to the user. The user can submit new requests. However, the rejected request can’t be edited.

**Parent Topic:**[Managing requests using AEMC](../concept/manage-aemc-requests.md)

