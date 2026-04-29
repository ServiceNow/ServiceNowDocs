---
title: Request translations in Localization Workspace: Scope
description: Select specific documents to add to a translation request in Localization Workspace.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Requesting translations in Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Request translations in Localization Workspace: Scope

Select specific documents to add to a translation request in Localization Workspace.

## Before you begin

Role required: localization\_requestor

## About this task

In the Scope step of a translation request, you can drill down to select or deselect specific documents from the list of translatable items collected by the Types step.

-   When the Scope screen first opens, all of the retrieved items are selected by default.
-   If you don't want an item to be included in the translation request, deselect that item by clearing its check box.
-   It's possible to select a document for one target language, and deselect the same document for a different target language.
-   From version 2.0.2, you can use a text filter in the column filter row. Filter operators are the same as other tables in your instance \(such as **starts with**, **contains**, and so forth\).
-   If you search for a term in the filter under the Translation Item column, the system searches for that term only in the titles of documents, not in contents.
-   From version 2.0.2, a bulk select/deselect check box is available in the Filter row.

    **Note:** Bulk selection/deselection applies only to the set of items that you have selected in the Types pane. Review and confirm the items in a translation request before submitting.


The following procedure covers step three of four steps in the Translation Request wizard.

## Procedure

1.  Complete steps one and two in the Translation request wizard, then proceed to this one, **Scope**.

2.  Reveal the filter row by selecting the **Show column filter row** icon, if needed.

    ![The Translation Request wizard at step 2, Scope. The Show column filter row toggle is highlighted.](../image/lw-request-translations-scope-show-filter-row.png)

3.  Filter the list according to terms in the document titles \(Translation Item\), or by Translation State or Language.

    ![The Show column filter displays under each column. Under Translation Item, the filter is Operator starts with "How", so only documents whose titles start with the word How are displayed.](../image/lw-request-translations-scope-filter-row.png)

4.  Reveal the Types pane by opening the **Resizable panes divider**, then expand Types by selecting the caret icon. ![In the Scope step, the Types pane is open with the Resizable panes divider highlighted.](../image/lw-request-translations-scope-resizeable-panes.png)

5.  Deselect any retrieved documents that you don't want to include in your request by clearing the item's check box.

    You can use the bulk select/deselect check box in the Filter row to select \(or clear\) a set of items. If anything is highlighted in the Types pane, bulk selection/deselection applies only to the highlighted type or language.![Under the Types pane, one language (Brazilian Portuguese) is selected, and also the bulk select/deselect check box is cleared. This means that Brazilian Portuguese documents are excluded from the request.](../image/lw-request-translations-scope-types-selector.png)

6.  Select **Save**.

    A saved translation request has a status of `Draft` in the **My Requests** list on the Home screen.

7.  Confirm the items you have included or excluded, then select **Next** to proceed to the **Estimate** step of the Translation Request wizard.


## What to do next

Advance to the next step in the Translation Request wizard, **Estimate**, where you can review projected costs and set a due date for the translation request.

