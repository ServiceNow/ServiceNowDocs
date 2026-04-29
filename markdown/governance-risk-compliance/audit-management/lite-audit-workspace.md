---
title: Audit Workspace limited
description: The Lite Audit workspace is a simplified version of the Audit Management workspace. In this workspace, you can access engagements, add existing entities to an engagement, and create activities. If the advanced core store app is installed, evidence\(s\) can also be associated with the engagement.
locale: en-US
release: australia
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Audit Workspace Overview, Audit Management, Governance, Risk, and Compliance]
---

# Audit Workspace limited

The Lite Audit workspace is a simplified version of the Audit Management workspace. In this workspace, you can access engagements, add existing entities to an engagement, and create activities. If the advanced core store app is installed, evidence\(s\) can also be associated with the engagement.

The Lite Audit Workspace comes with the following roles:

-   sn\_audit.shared\_admin
-   sn\_audit.shared\_manager
-   sn\_audit.shared\_user
-   sn\_audit.shared\_approver

## Access of the different roles

The following table lists the features that you can access with the different roles.

|Features|Create|Read|Update|Delete|
|--------|------|----|------|------|
|Engagement|Shared audit manager|Shared audit user|Shared audit manager|Shared audit admin|
|Activity|Shared audit manager|Shared audit user|Shared audit manager|Shared audit admin|
|Entity to engagement|Shared audit manager|Shared audit user|Shared audit manager|Shared audit manager|

## Accessing the Lite Audit Workspace Home page

Navigate to **All** &gt; **Audit Workspace**.

![Lite Audit home page.](../image/lite_audit_homepage.png)

You can view all engagements where you are assigned as the Auditor or Engagement Lead. You can also view the activities associated with those engagements.

From the homepage, if you have the sn\_audit.shared\_manager role, you can create new engagements and if you have the sn\_grc\_advanced.evidence\_requester role, you can create evidence requests.

![Lite Audit Engagement access.](../image/lite_audit_homepage_engagement.png)

## Evidence feature access

The Evidence feature provides access to evidence requests, collection details, and evidence responses. The following feature roles are introduced to perform various operations:

-   sn\_grc\_advanced.evidence\_reader: Can read evidence requests, collection details, and evidence responses.
-   sn\_grc\_advanced.evidence\_requester: Can create and update evidence requests, collection details, and evidence responses. Also, have access to review, approve, or reject evidence responses.
-   sn\_grc\_advanced.evidence\_responder: Can create and update evidence requests, collection details, and evidence responses.
-   sn\_grc\_advanced.evidence\_admin: Can create, read, update, and delete evidence requests, collection details, and evidence responses.

## Entity scoping

Scoping an entity in an engagement identifies which entities are involved in the audit. For example, in a financial audit, this may include the finance department and all business services it depends on.

## Activity Audit task

Audit activities involve collecting and documenting evidence to show that the organization complies with external regulations and internal policies. For more information, see [Create an audit task activity](../../grc-audit/task/t_CreateAnActivity.md).

## Evidence request

Audit evidence refers to all information used by auditors to form their audit opinion. This includes data from accounting records, financial statements, and other relevant sources. Evidence is cumulative and may come from current audit procedures as well as prior audits. For more information, see [Request evidence for audit](../../grc-audit/task/request-evidence.md).

