---
title: Manage architectural decision records \(ADR\)
description: Use the Architectural Decision Records \(ADR\) to explain your infrastructure. ADR is a type of artifact that helps you to understand the background of a specific architectural decision.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-09-09"
reading_time_minutes: 2
breadcrumb: [Working with information portfolio, Portfolio list view, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Manage architectural decision records \(ADR\)

Use the Architectural Decision Records \(ADR\) to explain your infrastructure. ADR is a type of artifact that helps you to understand the background of a specific architectural decision.

## ADR Overview

An ADR can have multiple doc pages associated with it to help you organize key architectural artifact details. Predefined ServiceNow Docs component \(sn\_docs\) templates are available. You can create ADR pages using one of these templates or start with a blank page.

**Note:** The ADR feature in Enterprise Architecture Workspace uses the ServiceNow Docs component \(sn\_docs\) to create pages in the Artifacts section. Docs component v6.0.0 is automatically installed with Enterprise Architecture Workspace v3.4.0.

If you’re using an older version of Enterprise Architecture Workspace with Docs component v6.0.0, upgrade the workspace to v3.4.0 to fully use the ADR functionality. For more information, see [KB2017926](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2017926).

## Features of ADR

Some features of ADR are:

-   Auto-save content
-   Create documents using pre-defined templates
-   Use rich text paragraph formatting, which includes headings, lists, alignment, and others.
-   Tag users inline or insert record details using the / command.
-   Insert images by uploading files or using web URLs
-   View version specific ADR content using the version drop-down. The versions drop-down displays the following information:

    -   Version number
    -   ADR status
    -   Date of last update
    On selecting a particular version, you’re directed to the ADR artifact content page for that version.

    ![ADR artifact content page with the version drop-down highlighted](../../image/eaw-image/adr-version-dropdown.png)


## Summarize ADR content using Now Assist for Enterprise Architecture \(EA\)

Use Now Assist capabilities to elaborate, shorten, and summarize selected content in ADRs, or to get a summary of the whole ADR. For more information, see [Using Now Assist for Enterprise Architecture \(EA\)](../../../now-assist-ea/concept/using-now-assist-for-ea.md)

-   **[Add or edit an architectural decision record \(ADR\)](../../task/eaw-task/eaw-create-edit-adr.md)**  
Create or update an artifact of the type architectural decision record \(ADR\) to align it with your business requirements.
-   **[Create and manage pages and subpages for architectural decision records](../../task/eaw-task/eaw-create-and-mng-page-subpage-for-adr.md)**  
Flexibly organize information for your architectural decision records \(ADR\) by creating, duplicating, and deleting pages and subpages in the Enterprise Architecture Workspace.
-   **[Tag users or records in Architectural Decision Records](../../task/eaw-task/eaw-tag-users-or-records-in-adr.md)**  
You can tag users or records in architectural decision records \(ADR\) in the Enterprise Architecture Workspace.
-   **[Enable referencing additional records in architectural decision records](../../task/eaw-task/eaw-update-system-property-to-allow-tagging-of-additional-records-in-adr-doc.md)**  
You can customize the default values of the **sn\_apm\_ws.record\_mention\_config** system property, to enable the tagging of additional record tables in an architectural decision record \(ADR\).
-   **[Add an architectural decision record version](../../task/eaw-task/eaw-add-an-adr-version.md)**  
Create multiple versions of architectural decision records \(ADR\) in the Enterprise Architecture Workspace. Creating multiple ADR versions enable you to capture the evolution of architectural decisions over time or capture details of alternatives to existing architectural decisions.
-   **[Request approval for an architectural artifact version of type Architectural Decision Record](../../task/eaw-task/eaw-request-approval-adr.md)**  
Send a version of architectural artifacts of the type Architectural Decision Record \(ADR\) for approval to an Enterprise Architect user. The user reviews and approves the request.

**Parent Topic:**[Working with information portfolio](eaw-information-portfolio.md)

