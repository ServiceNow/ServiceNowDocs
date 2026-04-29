---
title: Add an architectural decision record version
description: Create multiple versions of architectural decision records \(ADR\) in the Enterprise Architecture Workspace. Creating multiple ADR versions enable you to capture the evolution of architectural decisions over time or capture details of alternatives to existing architectural decisions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage architectural decision records \(ADR\), Working with information portfolio, Working with Portfolio list view, Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Add an architectural decision record version

Create multiple versions of architectural decision records \(ADR\) in the Enterprise Architecture Workspace. Creating multiple ADR versions enable you to capture the evolution of architectural decisions over time or capture details of alternatives to existing architectural decisions.

## Before you begin

The ADR feature in Enterprise Architecture Workspace uses the ServiceNow Docs component \(sn\_docs\) to create pages in the Artifacts section. Docs component v6.0.0 is automatically installed with Enterprise Architecture Workspace v3.4.0.

If you’re using an older version of Enterprise Architecture Workspace with Docs component v6.0.0, upgrade the workspace to v3.4.0 to fully use the ADR functionality. For more information, see [KB2017926](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2017926).

Role required: Depends on the role permissions set for a particular ADR.

## About this task

## Procedure

1.  Navigate to **Workspace** &gt; **Enterprise Architecture Workspace**.

2.  Open the Portfolio List view by selecting the Portfolio icon ![Portfolio icon](../../image/portfolio-icon.png).

3.  Select the expand row icon \(![Expand Row icon](../../image/ExpandIcon.png)\) next to **Information Portfolio**.

4.  Select **Architectural Decision Record**.

5.  Select the ADR that you want to add a new version for.

    A page appears displaying the details of the ADR.

6.  Select **New Version**.

7.  On the **Create new version** pop-up window, select the **Copy the content from previous version** check box if you want to copy over the existing content from the current version of the ADR.

    You can skip this step if you don’t want to copy over the existing ADR data.

8.  Select **Create**.


## Result

The new version of ADR is created. The new version number of the ADR is auto-selected in the version drop-down and the ADR doc is refreshed.

You can view version specific ADR content using the version drop-down. The versions drop-down displays the following information:

-   Version number
-   ADR status
-   Date of last update

On selecting a particular version, you’re directed to the ADR artifact content page for that version.

![ADR artifact content page with the version drop-down highlighted](../../image/eaw-image/adr-version-dropdown.png)

**Parent Topic:**[Manage architectural decision records \(ADR\)](../../concept/eaw-concept/eaw-manage-adr.md)

**Related topics**  


[Manage access to architectural artifacts](eaw-manage-access-to-architectural-artifacts.md)

[Tag users or records in Architectural Decision Records](eaw-tag-users-or-records-in-adr.md)

[Add or edit an architectural decision record \(ADR\)](eaw-create-edit-adr.md)

[Request approval for an architectural artifact version of type Architectural Decision Record](eaw-request-approval-adr.md)

[Create and manage pages and subpages for architectural decision records](eaw-create-and-mng-page-subpage-for-adr.md)

[Enable referencing additional records in architectural decision records](eaw-update-system-property-to-allow-tagging-of-additional-records-in-adr-doc.md)

