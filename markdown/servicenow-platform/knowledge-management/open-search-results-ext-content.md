---
title: Open knowledge search results in source system
description: While search results are aggregated within your instance, your users can also utilize features available in the source system \(being able to edit in Microsoft SharePoint, for example\). To open knowledge search results in a host system, configure the URL to the external source system to open articles from search results directly in the source system.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration with external knowledge sources, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Open knowledge search results in source system

While search results are aggregated within your instance, your users can also utilize features available in the source system \(being able to edit in Microsoft SharePoint, for example\). To open knowledge search results in a host system, configure the URL to the external source system to open articles from search results directly in the source system.

## Before you begin

Make sure the **Open search results in the original source system** import parameter for the [external knowledge source](define-an-external-knowledge-source.md) is set to **true**.

You can follow this procedure when you have a file as a knowledge article in Microsoft SharePoint, for example.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Open **KBWebDAVContentHandler**.

3.  In the **Script** window, override the function **getFileURL** using script shown below.

    The **getFileURL** function is shown below.

    ```
     //fileObj.getName() - Returns name of the file
          //fileObj.getPath() - Returns path to the file from root folder
          //fileObj.getAbsolutePath() - Returns Absolute WebDAV URL of the file
          //fileObj.getCreationDate() - Returns creation date of the file as GlideDateTime object
          //fileObj.getModifiedDate() - Returns last modified date of the file as GlideDateTime object
          //fileObj.getContentType() - Returns content type of the file as GlideDateTime object
          //fileObj.getSize() - Returns size of the file
    
    ```

    ```
    getFileURL: function(fileObj) {
          //write your logic here
    },
    ```

4.  Click **Update**.


**Parent Topic:**[Integration with external knowledge sources](../concept/knowledge-external-content-integration.md)

