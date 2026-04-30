---
title: Import content from an external knowledge source
description: Run an import job manually or set up a schedule to process the integrated external content.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integration with external knowledge sources, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Import content from an external knowledge source

Run an import job manually or set up a schedule to process the integrated external content.

## Before you begin

Role required: admin or knowledge\_admin

## About this task

Each external source is associated with two handlers: the **Acquire handler** and the **Process handler**, for running the import job. The acquire handler uses a WebDAV client to acquire external content to create articles. You can customize the process handler to assign categories to articles or populate additional metadata for the knowledge articles.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **External Knowledge Sources**.

2.  Select the external knowledge source from which you would like to import content.

3.  In the **Handler**tab, set a schedule to run the acquire and process handlers.

4.  In the Related Links section, click **Run Scheduled Job**.

5.  To view all jobs scheduled to run to import content for the external source, click the **Jobs**.

    You can open the most recent job to monitor the status.


## Result

For each file in the external content source, a blank knowledge article is created and the external file is added as an attachment to the article. The short description of the article is derived from the file name of the external content source.

**Note:** If the externally imported content is infected, a notification about each infected file is sent to the users with the knowledge\_admin role and Knowledge Base owners. The notified users can then take required actions on the infected files.

**Parent Topic:**[Integration with external knowledge sources](../concept/knowledge-external-content-integration.md)

