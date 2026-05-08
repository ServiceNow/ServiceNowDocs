---
title: Managing content requests
description: Content Governance provides a streamlined way for employees to ask for content to be created, track the progress, preview the content, and approve it before it is published.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Managing content requests

Content Governance provides a streamlined way for employees to ask for content to be created, track the progress, preview the content, and approve it before it is published.

Content Governance integrates with Content Publishing to provide content managers and admins an efficient way to fulfill and manage content requests. Content managers and admins can view these requests, assign it to a content creator, review the content, approve or make suggestions, and publish the content to make it available to their employees.

![Content Governance and Content Publishing features enable the end-to-end content request, fulfilment, and publishing process](../images/ecpro-content-gov-pubs.png)

## Content Governance components

-   **Content request**

    A content request is a system-generated record that tracks the status of an employee's content request and facilitates the Content Governance workflow.

-   **Content request item**

    A content request item provides additional details about the content request and the type of content to be created. You can have multiple content request items associated with a content request.

    Content request items also provide a status or state of the content being created.

-   **Reviewers**

    By default, the employee who made the content request is also responsible for approving the content for publishing. The requester or manager can select additional reviewers.

-   **Assignment groups**

    An assignment group is a group of users that receive the content request. Content Governance includes two assignment groups out of the box: Content Admin and Content Manager, which contain the users with those roles. To configure a new assignment group, see Configure assignment group types


## Content request process overview

The following process overview provides a high-level understanding of how employees and content-producing teams use Content Governance.

-   **Step 1: Request content**

    A user fills out the Content Request form, providing details about the needed content. Once the user submits the form, the system creates a content request record, where the user can add comments and attach files.

    ![Content request form](../images/content-gov-request.png)

    [Requesting content](ec-content-gov-request.md#)

-   **Step 2: Content request is created and assigned**

    The content manager opens the content request record to review the request details and assign it to an employee responsible for creating content.

    ![Content manager can view the request details and assign the request to the content creator](../images/content-gov-request-record.png)

    [Tracking content requests](ec-content-gov-track.md)

    [Assign content request to content creator](../task/assign-content-request.md)

-   **Step 3: Content is created and scheduled**

    Once the request is assigned to a content manager and the content request is updated to the **Work In Progress** state, the content manager can create content in the content library directly from the request page. This associates the content with the content request for tracking purposes.

    **Note:** Content can only be associated with one content request.

    ![The assigned content creator can create content from the Content Governance interface](../images/content-gov-create-content.png)

    [Creating content through Content Governance](../task/creating-content-governance.md)

-   **Step 4: Content is sent to requester for review**

    When the content creator is done, they send the content to the requester for review. Content must be associated with a publish plan before it can be sent for review.

    **Note:** Once a Content Request record is in the Review state, the associated content is locked to prevent further editing.

    ![Content creators can send content for review from the Content Library interface](../images/content-gov-send-review.png)

-   **Step 5: Content is reviewed and approved**

    The requester receives the review request as a new task in their portal and via email notification. The content requester and any additional approvers do the following:

    -   Review the content

        **Note:** Only rich content, news, and portal type content can be previewed

    -   Suggest edits or changes
    -   Approve the content
    ![The requester and other reviewers access the review request from the My Tasks button in the portal](../images/content-gov-request-review.png)

    [Previewing and approving a content request item](ec-content-gov-preview.md)

-   **Step 6: Content is published**

    After the content creator implements any feedback and the content is approved, the content is published based on the configured publish plan.


