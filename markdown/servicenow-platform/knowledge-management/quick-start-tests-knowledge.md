---
title: Quick start tests for Knowledge Management
description: Validate that Knowledge Management still works after you make any configuration change, such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Knowledge Management reference, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Quick start tests for Knowledge Management

Validate that Knowledge Management still works after you make any configuration change, such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

Knowledge Management quick start tests require activating the Knowledge Management Core plugin \(com.glideapp.knowledge\), the Knowledge Management Advanced Installer plugin \(com.snc.knowledge\_advanced.installer\), the Knowledge Blocks plugin \(com.snc.knowledge\_blocks\), and the Customer Service Management Demo Data plugin \(com.snc.customerservice.demo\).

<table id="table_whf_nfg_h1c"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

KM : Create KCS Template Article with Approval Publish workflow

</td><td>

Verify the creation of a KCS template article with approval publish workflow.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Madrid

</td></tr><tr><td>

KM: Create MultiVersioned standard Article with approval publish workflow

</td><td>

Verify the creation of a multi-versioned standard article with approval publish workflow.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Madrid

</td></tr><tr><td>

KM: Article level subscription

</td><td>

Verify that users can subscribe to a knowledge article.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

New York

</td></tr><tr><td>

KM: User criteria covering canRead and canContribute for KnowledgeBase and canRead at Article level

</td><td>

Verify the creation of canRead and canContribute user criteria for knowledge base and canRead user criteria for article.**Note:** Requires the Knowledge Management Core plugin.

</td><td>

Madrid

</td></tr><tr><td>

KM: Create a KCS article from a case

</td><td>

Verify the creation of a KCS article from a case.**Note:** Requires the Knowledge Management Advanced Installer and Customer Service Management Demo Data plugins.

</td><td>

Madrid

</td></tr><tr><td>

KM: Knowledge Base Level Subscriptions

</td><td>

Verify that users can subscribe to a Knowledge Base.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

New York

</td></tr><tr><td>

KM: AQI

</td><td>

Verify the creation, assignment, and review of an AQI checklist.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

New York

</td></tr><tr><td>

KM: Requestor performs search, view the article, provide feedback \(Helpful No with Feedback Task\)

</td><td>

Verify the search request, review, provision of feedback as not helpful, and creation of a feedback task for an article on the Knowledge Management Service Portal.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

New York

</td></tr><tr><td>

KM: Create and edit an article from Feedback Task form

</td><td>

Confirm the availability of the **Create Article** and **Edit Article** buttons on a Knowledge Feedback Task form.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

New York

</td></tr><tr><td>

KM: Search for pinned articles and checking the highest click rank

</td><td>

Verify the search request and that the click rank value of a pinned article was added to the Knowledge Searches \(ts\_query\_kb\) table.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

New York

</td></tr><tr><td>

KM: Create an Ownership Group and check edit permissions and subscriptions

</td><td>

Verify the assignment of an article to an ownership group, that all members of the ownership group are subscribed to the article, and have permission to edit.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

New York

</td></tr><tr><td>

KM: Create, search for, and view knowledge articles with knowledge blocks

</td><td>

Verify the creation of a knowledge block and its addition to a knowledge article. Also, verify that the knowledge block content is searchable.**Note:** Requires the Knowledge Blocks plugin.

</td><td>

Orlando

</td></tr><tr><td>

KM: Validate the Knowledge - Approval Retire workflow

</td><td>

Verify the success of Knowledge - Approval Retire workflow by retiring a published knowledge article.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Orlando

</td></tr><tr><td>

KM: Validate feedback task assignment to the ownership group manager

</td><td>

Verify the assignment of a feedback task to the ownership group manager of a knowledge article.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Orlando

</td></tr><tr><td>

KM: Validate that the article template selector includes knowledge bases and article templates

</td><td>

Verify that the article template selector includes all knowledge bases with contribute access and article templates applicable to each knowledge base.**Note:** Requires Knowledge Management Advanced Installer.

</td><td>

Orlando

</td></tr><tr><td>

KM: Validate the Knowledge - Approval Publish workflow

</td><td>

Verify the success of a Knowledge - Approval Publish workflow by recalling, rejecting, and then approving a knowledge article through the approval process.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Orlando

</td></tr><tr><td>

KM: Make an outdated version of an article the latest version

</td><td>

Verify that an outdated version of a knowledge article is made the latest version.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Orlando

</td></tr><tr><td>

KM: Validate that the mapped related articles appear in the Related articles widget

</td><td>

Verify that the related articles mapped to a knowledge article appear in the Related articles widget on the knowledge article view page.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Orlando

</td></tr><tr><td>

KM: Validate that the mapped related catalog items appear in the Related items widget

</td><td>

Verify that the related catalog items mapped to a knowledge article appear in the Related items widget on the knowledge article view page.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Orlando

</td></tr><tr><td>

KM: Validate that a versioned article is created, published, checked out, and retired

</td><td>

Verify the success of UI actions on a versioned knowledge article by creating, publishing, updating, and retiring the knowledge article in Agent Workspace.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Quebec

</td></tr><tr><td>

KM: Verify the scheduled publish feature for knowledge articles

</td><td>

Verify the scheduled publish feature for knowledge articles by creating an article in approval publish workflow, putting it for scheduled for publish and observing the change in workflow state from the**Scheduled for publish** state to the **Published** state.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Quebec

</td></tr><tr><td>

KM: Validate the Knowledge - Approval Publish workflow in Agent Workspace

</td><td>

Verify the success of a Knowledge - Approval Publish workflow by recalling and then approving a knowledge article through the approval process in Agent Workspace.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Quebec

</td></tr></tbody>
</table>**Parent Topic:**[Knowledge Management reference](../../../product/knowledge-management/reference/knowledge-management-reference.md)

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

