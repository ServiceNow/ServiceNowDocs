---
title: Create user guide help
description: User guide help documents are grouped in appropriate sections on the page and listed in a configurable order. Add your sections to a help page.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [System user guide, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create user guide help

User guide help documents are grouped in appropriate sections on the page and listed in a configurable order. Add your sections to a help page.

## Before you begin

Create all your help documents from within the section record. This allows you to refine their titles, adjust their placement, and decide if they are appropriate for the section.

Role required: admin

## Procedure

1.  Create a page.

    1.  Navigate to **System User Guide** &gt; **Administration** &gt; **Help Pages** and click **New**.

    2.  Complete the form.

        |Field|Description|
        |-----|-----------|
        |ID|Page identification used by the system to create a help URL.|
        |Application|Application scope for this help page. This field is read-only and defaults to the **Global** scope.|
        |Title|Display title for this page.|

    3.  Click **Submit**.

        ![User guide help page](../image/UserGuidePage.png)

2.  Create help page sections and associate them with the page.

    1.  Navigate to **System User Guide** &gt; **Administration** &gt; **Help Page Sections** and click **New**.

        ![User guide section definition](../image/UserGuideSection.png)

    2.  Give your section a unique and concise title, and then click **Submit**.

        The view returns to the list of sections.

    3.  Create additional sections for your help page.

    4.  Navigate to **System User Guide** &gt; **Administration** &gt; **Help Pages** and open your new page.

    5.  In the **Page to Sections** related list, click **New**.

    6.  Complete the form.

        |Field|Description|
        |-----|-----------|
        |Column|Column location on the page for this section. The first column is designated as **0** and the second column is designated as **1**. There must be at least one entry for column **0** for the sections to display.|
        |Order|Order in which the sections display in the columns on the page. If no order number is defined, the system lists the sections in alphabetical order.|
        |Application|Application scope for this record. This field is read-only and defaults to the **Global** scope.|
        |Page|Help page on which this section appears. You can use the lookup field to change the page on which a section appears.|
        |Section|Name of the section to display on the selected page.|

        ![Placing sections on a help page](../image/UserGuideSectionToPage.png)

    7.  Click **Submit**.

    8.  Add sections to the help page as needed.

3.  Create one or more documents.

    1.  Navigate to **System User Guide** &gt; **Administration** &gt; **Help Page Sections**.

    2.  Open a section record you created.

    3.  In the **Help** related list, click **New** to create a help document for that section.

    4.  Complete the form.

        |Field|Description|
        |-----|-----------|
        |Number|Document number generated automatically by the system.|
        |Section|Section in which this document appears.|
        |Order|Listing order for this document in the selected section.|
        |Published|Date this document was created.|
        |Updated|Date this document was last updated.|
        |Short description|Brief description of the content of this document. This description is used as the title for the document on the help page.|
        |Text|Document content, including graphics and tables. You can format your entry, create bulleted or numbered lists, and attach images.|

        ![User guide help document](../image/UserGuideDocument.png)

    5.  Click **Submit**.

    6.  Repeat the process to create the necessary help documents for that section.

        ![Section record with help documents](../image/UserGuideSectionAndContent.png)


**Parent Topic:**[System user guide](../concept/c_SystemUserGuide.md)

