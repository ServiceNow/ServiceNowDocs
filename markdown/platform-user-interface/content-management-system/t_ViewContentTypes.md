---
title: View content types
description: The following is an example of where you might use Content Types.
locale: en-US
release: zurich
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Content types, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# View content types

The following is an example of where you might use Content Types.

## Before you begin

This example uses the out-of-box Employee Self-Service \(ESS\) site as an example.

Role required: content\_admin or admin

## About this task

Use any out-of-box instance of a CMS site.

## Procedure

1.  Launch an out-of-box CMS site `https://<instance name>.service-now.com/ess`.

2.  Under Get Help, click **Issue Status**.

    The Issue Status, or incident\_status CMS page contains two content blocks: Common Answer and Current Issues. These content blocks both use Content Types to render results.

3.  From `https://<instance name>.service-now.com`, navigate to **Blocks** &gt; **Lists** &gt; **Portal - Common Answers**.

    This block matches the Common Answers section of the Issue Status page. The Table field describes the Content Type associated with Common Answers.

4.  Use the link to view existing Content Types.

5.  Click the Content Type to view the XML that determines how the list and record are rendered in CMS.

    The Default Detail Page field indicates a CMS page that displays a record selected from a List of Content block.

6.  Click the Information icon next to the Default Detail Page, to go to that page.

7.  From the Default Detail Page, under Related Links, click **Edit Page**.

    The Detail Block contains a content type formatter. When editing or viewing the page, it is looking for a URL to be passed to determine the record to display, which is why it says "Detail record could not be located".

8.  Click the pencil icon to edit and view the Detailed Content block.

    The Type drop down list has "Show the page's current document" selected, which indicates that the document\_id must be passed to this block from the CMS pages, then it can display the record based on the content type listed in the document\_id.

9.  From the Common Answers block, on the Self Service page, select a record.

    The page opens with a URL similar to: `https://<intance name>.service-now.com/ess/knowledge.do?sysparm_document_key=kb_knowledge,02255450d731310013ab49547e61038e`

    The table `sysparm_document_key=kb_knowledge` and sys\_id `02255450d731310013ab49547e61038e` determine the record. The associated content type, kb\_knowledge, renders the content on the Default Detail Page, Portal - Knowledge Detail / url\_suffix=knowledge.


**Parent Topic:**[Content types](../concept/c_ContentTypes.md)

