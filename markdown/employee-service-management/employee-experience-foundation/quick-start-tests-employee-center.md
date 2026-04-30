---
title: Quick start tests for Employee Center
description: Validate the continued functionality of the Employee Center after any configuration change such as an upgrade or after developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Configure, Employee Center, Employee Service Management]
---

# Quick start tests for Employee Center

Validate the continued functionality of the Employee Center after any configuration change such as an upgrade or after developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.

All test suites and tests should pass on a default implementation. To validate a custom implementation, copy the automated tests and configure them for your customizations.

Quick start tests are disabled and read-only test templates. By default, they only produce a pass result when you run them with the default demo data that is provided with the application or feature plugin.

To make quick start tests produce a pass result when you run them with your instance-specific data, copy and configure them to use your instance data.

Use Performance Profiling to compare tests to detect performance degradation when you upgrade your instance, so you can investigate and fix the issues. See [Performance profiling](https://www.servicenow.com/docs/access?context=atf-perf-prof&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

The Agile Development 2.0 \(com.snc.sdlc.agile.2.0\) and the Agile Development 2.0 - ATF Tests \(com.snc.sdlc.agile.2.0.atf\) plugins must be enabled.

**Note:** When running, demo data is required.

## Employee Center and Employee Center Pro

<table id="atf-tests-hr-esc"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

Create Adhoc Delegation for Approval Task

</td><td>

Ensures an adhoc delegation for an approval task can be created from the My Tasks form in the Employee Center.

</td><td>

San Diego

</td></tr><tr><td>

Create Adhoc Delegation for HR Task

</td><td>

Ensures an adhoc delegation for an HR task can be created from the My Tasks form in the Employee Center.

</td><td>

San Diego

</td></tr><tr><td>

Employee Center - My Favorites

</td><td>

Verifies the favorite functionality in the Employee Center. Also verifies when a KB article or catalog item is added to the Favorite widget.

</td><td>

San Diego

</td></tr><tr><td>

Employee Center - Approval Hub Approve Request

</td><td>

Verifies the approval functionality in the Employee Center. Also verifies that when a request is approved, it appears in the user's **Completed** column.

</td><td>

San Diego

</td></tr><tr><td>

Employee Center - Approval Hub Reject Request

</td><td>

Verifies the rejection functionality. Also verifies that when a request is rejected, it appears in the user's **Completed** column.

</td><td>

San Diego

</td></tr><tr><td>

Employee center - Employee Profile Generation

</td><td>

Verifies that employee profiles are generated as per the employee definition.

</td><td>

Xanadu

</td></tr><tr><td>

Employee Center - Topic Page

</td><td>

Associates a KB article or catalog item to a topic and verifies they display on the topic page.

</td><td>

San Diego

</td></tr><tr><td>

Employee Center - Validate home page widgets

</td><td>

Validates the following widgets are present on the Employee Center home page:-   Relevant for you
-   Popular topics
-   My Active Items
-   Quick tasks
-   Homepage Search

</td><td>

San Diego

</td></tr><tr><td>

Employee Center Pro - App launcher

</td><td>

Verifies the following on the My Application page:-   Creates an application and verifies it is visible on the application page.
-   Creates a topic/category and associates the application and verifies it is visible under the topic and category.

</td><td>

San Diego

</td></tr><tr><td>

Employee Center Pro - Validate home page widgets

</td><td>

Validates the following widgets are present on the Employee Center Pro home page:-   Content Experience
-   Recommended for you
-   Popular topics
-   Upcoming Events
-   My Active Items
-   Videos
-   App launcher
-   Homepage Search

</td><td>

San Diego

</td></tr><tr><td>

ESC: Employee can see ticket updates

</td><td>

Employees can view updates to their tickets.

</td><td>

Quebec

</td></tr><tr><td>

ESC: Post General HR Inquiry questions on ESC portal

</td><td>

Verifies an HR employee can create a General Inquiry case and post general HR inquiry questions on the ESC.

</td><td>

Quebec

</td></tr><tr><td>

ESC: Submit a Record Producer which crates Universal Request and HR Case

</td><td>

Verifies a user can submit an HR catalog item that creates a Universal Request. Also verifies the Universal Request and HR case are created and linked.

</td><td>

Quebec

</td></tr><tr><td>

ESC: Verify Standard Ticket page on ESC for HR Case

</td><td>

Creates a general inquiry case from the service portal and verifies it appears on the standard Ticket page.

</td><td>

Quebec

</td></tr><tr><td>

ESC: Verify widget contents in Catalog items

</td><td>

Verifies the widget content in a Catalog page.

</td><td>

Orlando

</td></tr><tr><td>

ESC: Verify widget contents in knowledge pages

</td><td>

Verifies the widget content in a Knowledge page.

</td><td>

Orlando

</td></tr><tr><td>

HR: Search catalog items &amp; KBs in ESC

</td><td>

Verifies the search functionality in the ESC.

</td><td>

Quebec

</td></tr><tr><td>

Taxonomy and Topic Creation

</td><td>

Creates taxonomy and topics and then adds content to the topic.

</td><td>

San Diego

</td></tr></tbody>
</table>**Note:** Requires plugin activation of:

-   Human Resources Scoped App: Core plugin \(com.sn\_hr\_core\)
-   Employee Center Core \[app-ex-employee-center-core\]
-   Employee Center \[app-ex-employee-center\]
-   Employee Center Pro \[app-ex-employee-center-pro-content\]
-   Content Publishing \[app-content-publishing\]
-   Content Experiences \[app-content-experiences\]

|Test|Description|Release version|
|----|-----------|---------------|
|Content Experiences: Create and Publish a Campaign|Creates and publishes a campaign with portal content and verifies against the Content Experiences portal.|Orlando|
|Content Experiences: Portal preview|Verifies that a campaign manager is able to preview portal content using the portal preview.|Rome|
|Content Experiences: Preview individual content before Publishing a Campaign|Verifies a campaign manager can preview any individual content for a campaign.|San Diego|

**Note:** Requires plugin activation of:

-   Human Resources Scoped App: Core plugin \(com.sn\_hr\_core\)
-   Employee Center Core \[app-ex-employee-center-core\]
-   Employee Center \[app-ex-employee-center\]
-   Employee Center Pro \[app-ex-employee-center-pro-content\]
-   Content Experiences \[app-content-experiences\]

|Test|Description|Release version|
|----|-----------|---------------|
|Content Governance - New Content Request E2E Workflow|Provides end-to-end testing from creating a content request through publishing the content.|San Diego|

**Note:** Requires plugin activation of:

-   Human Resources Scoped App: Core plugin \(com.sn\_hr\_core\)
-   Employee Center Core \[app-ex-employee-center-core\]
-   Employee Center \[app-ex-employee-center\]
-   Employee Center Pro \[app-ex-employee-center-pro-content\]
-   Content Publishing \[app-content-publishing\]
-   Content Experiences \[app-content-experiences\]
-   Content Governance \[app-content-governance\]

|Test|Description|Release version|
|----|-----------|---------------|
|Content Publishing: Audience|Tests the audience configurations for Content Publishing.|Orlando|
|Content Publishing: Create Banner type content in SCA|Ensures the Create Banner type can be created when using Streamlined Content Authoring \(SCA\) under the Content Publishing module.|Rome|
|Content Publishing: Create Styled content \(Video\) type content in SCA|Verifies an admin can create styled content that is a video type using Content Publishing.|Rome|
|Content Publishing: Schedule Portal Content|Creates and schedules test content for the Content Publishing demo portal.|Orlando|
|Create news content via Content Library|Creates and publishes a news article to the portal.|Xanadu|

**Note:** Requires plugin activation of:

-   Human Resources Scoped App: Core plugin \(com.sn\_hr\_core\)
-   Employee Center Core \[app-ex-employee-center-core\]
-   Employee Center \[app-ex-employee-center\]
-   Employee Center Pro \[app-ex-employee-center-pro-content\]
-   Content Publishing \[app-content-publishing\]
-   Content Experiences \[app-content-experiences\]

-   **[Run quick start tests for Employee Center](../../../product/human-resources/task/atf-employee-center.md)**  
Employee Center provides several quick start tests you can run.

**Parent Topic:**[Configuring Employee Center](../../../product/employee-center/concept/setup-emp-center.md)

**Related topics**  


[Employee Center users and roles](../../../product/employee-center/concept/emp-center-personas.md)

[Understanding Employee Center plugins](../../../product/employee-center/concept/install-plugins.md)

[Setup browse experience features](../../../product/employee-center/concept/setup-browse-experience.md)

[Setup search experience features](../../../product/employee-center/concept/setup-search-experience.md)

[Setup task management and integration features](../../../product/employee-center/concept/setup-task-mgmt.md)

[Setup continuous improvement features](../../../product/employee-center/concept/setup-continuous-improvement.md)

[Setup employee communications](../../../product/employee-center/concept/setup-employee-comms.md)

[Configure your Employee Center portal](../../../product/employee-center/concept/configure-ec-portal.md)

[Moveworks for Employee Center](../../../product/employee-center/concept/moveworks-for-employeecenter.md)

[Employee Center Pro Kiosk](../../../product/employee-center/concept/deskless-kiosk-overview.md)

[Configuring Employee Center for mobile](../../../product/employee-center/concept/ec-mobile-configrations.md)

