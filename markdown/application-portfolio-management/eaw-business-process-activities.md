---
title: Exploring business process activities
description: Business process activities represent discrete units of work within workflows. Knowing how they differ from business processes helps you model organizational tasks accurately.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/eaw-business-process-activities.html
release: zurich
topic_type: concept
last_updated: "2026-08-03"
reading_time_minutes: 1
keywords: [business process activity, business process, business actor]
breadcrumb: [Exploring the business architecture, Exploring Portfolio list view, Explore, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Exploring business process activities

Business process activities represent discrete units of work within workflows. Knowing how they differ from business processes helps you model organizational tasks accurately.

A business process activity represents a specific task, step, or action performed within your organization, such as a manual task, an approval step, or a system-triggered action.

## Business processes vs. business process activities

Business processes and business process activities serve different purposes:

-   Business process — Models the overall workflow your organization uses to achieve a business outcome. Business processes are organized into a hierarchy of levels \(L0, L1, L2, and deeper\) using CI relationships. Each level represents a broader or narrower scope of the same workflow.
-   Business process activity — A standalone record that represents a discrete unit of work, classified by an activity type \(for example, **Manual Task**\). Unlike business process levels, a business process activity is not part of the L0-L2 hierarchy — instead, it is associated with the business actors who perform it.

You can:

-   Create and edit business process activities
-   Classify activities by type
-   Assign owners and managing groups
-   Link activities to business actors who perform them

When you model a business process activity in a diagram, the default relationship between a business process activity and a business actor is Performed by:Performs.

**Parent Topic:**[Exploring the business architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-business-architecture.md)

**Related topics**  


[Manage business process activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/eaw-manage-business-process-activities.md)

