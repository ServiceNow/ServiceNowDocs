---
title: Quick start tests for Employee Center Pro
description: Validate the continued functionality of Employee Center Pro after any configuration change such as an upgrade or after developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Quick start tests for Employee Center Pro

Validate the continued functionality of Employee Center Pro after any configuration change such as an upgrade or after developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.

All test suites and tests should pass on a default implementation. To validate a custom implementation, copy the automated tests and configure them for your customizations.

Quick start tests are disabled and read-only test templates. By default, they only produce a pass result when you run them with the default demo data that is provided with the application or feature plugin.

To make quick start tests produce a pass result when you run them with your instance-specific data, copy and configure them to use your instance data.

Use Performance Profiling to compare tests to detect performance degradation when you upgrade your instance, so you can investigate and fix the issues. See [Performance profiling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-perf-prof.md).

The Agile Development 2.0 \(com.snc.sdlc.agile.2.0\) and the Agile Development 2.0 - ATF Tests \(com.snc.sdlc.agile.2.0.atf\) plugins must be enabled.

**Note:** When running, demo data is required.

## Employee Center Pro

<table id="table_bwq_z3p_5dc"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

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

ESC: Submit a Record Producer which creates Universal Request and HR Case

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
</table>|Test|Description|Release version|
|----|-----------|---------------|
|Content Publishing: Audience|Tests the audience configurations for Content Publishing.|Orlando|
|Content Publishing: Create Banner type content in SCA|Ensures the Create Banner type can be created when using Streamlined Content Authoring \(SCA\) under the Content Publishing module.|Rome|
|Content Publishing: Create Styled content \(Video\) type content in SCA|Verifies an admin can create styled content that is a video type using Content Publishing.|Rome|
|Create news content via Content Library|Creates and publishes a news article to the portal.|Xanadu|
|Content Publishing: Schedule Portal Content \(Banner, Calendar, Event, and Rich Text|Creates and schedules test portal content.|Yokohama|
|Create and publish new styled content \(block and banner\)|Verifies that a user can create a styled content banner and block, and publish the content items to a topic page.|Yokohama|

|Test|Description|Release version|
|----|-----------|---------------|
|Content Experiences: Create and Publish a Campaign|Creates and publishes a campaign with portal content.|Orlando|
|Create and publish campaign - Styled content \(block\), event, and calendar|Verifies that a user can create a campaign for immediate publication containing styled content \(block\), event, calendar content types.|Yokohama|
|Create and publish Fixed Date stage campaign - Styled Content \(Block\), Event and Calendar|Verifies that a user can create a campaign with a specific publication date containing styled content \(block\), event, calendar content types.|Yokohama|
|Content Experiences: Portal preview|Verifies that a campaign manager is able to preview portal content using the portal preview.|Rome|
|Content Experiences: Preview individual content before Publishing a Campaign|Verifies a campaign manager can preview any individual content for a campaign.|San Diego|

|Test|Description|Release version|
|----|-----------|---------------|
|Content Governance - New Content Request E2E Workflow|Provides end-to-end testing from creating a content request through publishing the content.|San Diego|

**Related topics**  


[Quick start tests for Employee Center](quick-start-tests-employee-center.md)

