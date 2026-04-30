---
title: Tag users or records in Architectural Decision Records
description: You can tag users or records in architectural decision records \(ADR\) in the Enterprise Architecture Workspace.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-04-16"
reading_time_minutes: 2
breadcrumb: [Manage architectural decision records \(ADR\), Working with information portfolio, Portfolio list view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Tag users or records in Architectural Decision Records

You can tag users or records in architectural decision records \(ADR\) in the Enterprise Architecture Workspace.

## Before you begin

**Note:** The ADR feature in Enterprise Architecture Workspace uses the ServiceNow Docs component \(sn\_docs\) to create pages in the Artifacts section. Docs component v6.0.0 is automatically installed with Enterprise Architecture Workspace v3.4.0.

If you’re using an older version of Enterprise Architecture Workspace with Docs component v6.0.0, upgrade the workspace to v3.4.0 to fully use the ADR functionality. For more information, see [KB2017926](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2017926).

Role required: sn\_apm.apm\_user and you should have **Editor** access to the ADR.

## About this task

Tagging users in ADRs ensures that relevant stakeholders are aware of and can contribute to important architectural decisions. Tagging records helps you to organize relevant information systematically and locate records relevant to a particular ADR easily. The records you can tag are:

-   Architectural artifacts or diagrams
-   Business applications
-   Business capabilities
-   Business processes
-   Digital integrations
-   Digital interfaces
-   Information objects
-   TRM products
-   Value stream details

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Portfolio List view by selecting the Portfolio icon ![Portfolio icon](../../image/portfolio-icon.png).

3.  Select the expand row icon \(![Expand Row icon](../../image/ExpandIcon.png)\) next to **Information Portfolio**.

4.  Select **Architectural Decision Records \(ADR\)**.

5.  Select the ADR where you want to tag users or records.

6.  In the body of the ADR docs, enter **/**.![Context menu displaying the available options to tag.](../../image/eaw-image/adr-tag-user-or-records.png)

    A context menu is displayed.

7.  Tag a record or a user.

    -   To tag a record:
        1.  Select **Mention a record**.

            A list of record types you can tag is displayed.

            ![List of available records for tagging.](../../image/eaw-image/adr-available-records-to-tag.png)

        2.  Select a record type.

            A context menu is displayed listing the available records for that record type.

            ![List of available records for the selected record type.](../../image/eaw-image/adr-available-users-to-tag.png)

        3.  Select the relevant record.

            The record is added to the ADR page.

    -   To tag a user:
        1.  Select **Mention a user**.

            A list of users is displayed.

            ![List of available users for tagging.](../../image/eaw-image/adr-tag-users-list.png)

        2.  Select the relevant user. You can also enter the user's name to search for a specific user.

            The user is added in the ADR page.


**Parent Topic:**[Manage architectural decision records \(ADR\)](../../concept/eaw-concept/eaw-managing-arch-decision-records.md)

**Related topics**  


[Generate a summary for Architectural Decision Records \(ADRs\)](../../../now-assist-ea/task/summarize-docs-genai-skill-ea.md)

[Elaborate or shorten content in the Architectural Decision Records \(ADRs\)](../../../now-assist-ea/task/elaborate-shorten-content-ew.md)

