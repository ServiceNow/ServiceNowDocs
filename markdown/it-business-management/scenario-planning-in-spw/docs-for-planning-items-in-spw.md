---
title: Docs for planning items in Strategic Planning
description: Store and manage all kinds of documentation for planning items from a centralized location of Strategic Planning Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/docs-for-planning-items-in-spw.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2026-06-21"
reading_time_minutes: 3
breadcrumb: [Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Docs for planning items in Strategic Planning

Store and manage all kinds of documentation for planning items from a centralized location of Strategic Planning Workspace.

## Docs overview

Product and portfolio managers can store information for planning items using the Docs feature.

-   Each planning item can have a separate doc page to capture the information related to it.

    For example, for an Epic planning item, you create a doc page for high level business objectives or technical product requirements.

-   Each planning item can have multiple doc pages associated to it to help you effectively organize key artifacts.
-   Predefined templates such as Project Brief, Product Requirements, Brainstorming Ideas, and Meeting notes are available. Create doc pages for your planning items using one of these templates or start with a blank page.

## Features of Docs

The following are the key features of Docs:

-   Auto-save content.
-   See who is viewing or working on a doc page using the feature of live user presence.
-   Create documents using pre-defined templates.
-   Use rich text paragraph formatting, which includes headings, lists, alignment, and others.
-   Move text blocks to change their placement using block-level editing.
-   Tag team members inline or insert tables using the **/** command.
-   Add reference to other ServiceNow AI Platform tables to connect work across teams.
-   Insert images by uploading files or using web URLs.

    **Note:** The experience of inserting Google Images links might not work.


## Summarize Docs content using Now Assist for SPM

Use Now Assist capabilities to elaborate, shorten, and summarize selected content in Docs, or to get a summary of the whole document.

-   Summarize, elaborate, or shorten selected text.

    \[Omitted image "eap-now-assist-selected-content.png"\] Alt text: Summarize, elaborate, or shorten the selected text

-   Summarize the entire content on the page.

    \[Omitted image "eap-now-assist-doc-summarize.png"\] Alt text: Summarize the entire content on the page


**Note:**

-   Now Assist for Docs requires an SPM Pro + license. For more information, see [Configure Now Assist Admin features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/configuring-na-spm.md).
-   If there is more content to summarize, you can remove some content and retry.
-   Because the information in these fields is AI generated, it's a good idea to review the text and make sure it's accurate.

## Real-time collaboration within planning item Docs

With the feature of real-time collaboration, edit a doc page concurrently with multiple other editors. Colored cursors denote the current location of each editor on the page. You can choose to show or hide these live presence indicators based on your preference while working on or reviewing the content of the page.

\[Omitted image "cwm-docs-rtc.png"\] Alt text: Docs real-time collaboration.

**Note:** Huge number of users editing the same block of content simultaneously might result in issues with application performance.

## Dynamic data linking in Docs

Keep record information in your documentation always current and reduce manual effort with the Dynamic data linking feature in Docs. You can now reference any ServiceNow application record and Docs will automatically reflect the latest updates from those records.

For example, if you add a reference to a Project record, the reference shows the latest field information of the project in Docs without requiring manual edits. Selecting the project reference opens up the project form so that you can view the full details of the project and make any necessary changes.

A hover popover displays the details of the mentioned record, providing quick access to additional information without leaving the current context.

\[Omitted image "cwm-docs-dynamic-record.png"\] Alt text: Dynamic linking a project record in SPW Docs.

Dynamic linking also enables adding references to a particular field of a record, such as Assigned to of a Project record.

\[Omitted image "cwm-docs-dynamic-field.png"\] Alt text: Dynamic linking the Assigned to field of a project record in SPW Docs.

You can add references from any ServiceNow table you have access to, with no setup or configuration needed.

This feature reduces the need to switch between multiple ServiceNow applications within your instance and helps maintain a single, reliable source of truth for collaborative work, making it easier for teams to stay aligned and informed.

