---
title: Create and manage pages and subpages for architectural decision records
description: Flexibly organize information for your architectural decision records \(ADR\) by creating, duplicating, and deleting pages and subpages in the Enterprise Architecture Workspace.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-04-16"
reading_time_minutes: 2
breadcrumb: [Manage architectural decision records \(ADR\), Working with information portfolio, Portfolio list view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Create and manage pages and subpages for architectural decision records

Flexibly organize information for your architectural decision records \(ADR\) by creating, duplicating, and deleting pages and subpages in the Enterprise Architecture Workspace.

## Before you begin

An ADR can have multiple doc pages associated with it to help you organize key architectural artifact details. Predefined ServiceNow Docs component \(sn\_docs\) templates are available. You can create ADR pages using one of these templates or start with a blank page.

**Note:** The ADR feature in Enterprise Architecture Workspace uses the ServiceNow Docs component \(sn\_docs\) to create pages in the Artifacts section. Docs component v6.0.0 is automatically installed with Enterprise Architecture Workspace v3.4.0.

If you’re using an older version of Enterprise Architecture Workspace with Docs component v6.0.0, upgrade the workspace to v3.4.0 to fully use the ADR functionality. For more information, see [KB2017926](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2017926).

Role required: sn\_apm.apm\_user and you should have **Editor** access to the ADR.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Portfolio List view by selecting the Portfolio icon ![Portfolio icon](../../image/portfolio-icon.png).

3.  Select the expand row icon \(![Expand Row icon](../../image/ExpandIcon.png)\) next to **Information Portfolio**.

4.  Select **Architectural Decision Records \(ADR\)**.

5.  Select the ADR that you would like to create a doc page for.

6.  To create a page, you can create an empty page or start with a predefined template.

    -   For an empty page, select **Create page**.
    -   To create from templates:
        1.  Select **Create Page from template**.

            ![Create page and create page from template buttons.](../../image/eaw-image/create-adr-page.png)

        2.  Choose a template from the Template Center and select **Use**.![Page displaying some of the available ADR templates.](../../image/eaw-image/adr-template.png).

            The new page is created and added to your ADR with the name of the selected template, which you can rename.

7.  To create a subpage, select the Page Actions menu icon \(![Page actions menu](../../image/eaw-image/more-actions-menu.png)\) and select **Create subpage**.

    ![Page actions menu with the create subpage button highlighted.](../../image/eaw-image/create-adr-subpage.png)

8.  To delete a page or a subpage, select the Page Actions menu \(![Page actions menu](../../image/eaw-image/more-actions-menu.png)\) and select **Delete**.


**Parent Topic:**[Manage architectural decision records \(ADR\)](../../concept/eaw-concept/eaw-managing-arch-decision-records.md)

**Related topics**  


[Tag users or records in Architectural Decision Records](eaw-tag-users-or-records-in-adr.md)

[Generate a summary for Architectural Decision Records \(ADRs\)](../../../now-assist-ea/task/summarize-docs-genai-skill-ea.md)

[Elaborate or shorten content in the Architectural Decision Records \(ADRs\)](../../../now-assist-ea/task/elaborate-shorten-content-ew.md)

