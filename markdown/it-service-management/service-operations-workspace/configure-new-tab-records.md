---
title: Configure record creation from the new tab menu in Service Operations Workspace
description: Customize the records that can be created from the new tab menu in all pages of Service Operations Workspace.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Landing page configurations in SOW for ITSM, Getting started, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure record creation from the new tab menu in Service Operations Workspace

Customize the records that can be created from the new tab menu in all pages of Service Operations Workspace.

## Before you begin

Role required: admin

## About this task

By default, an interaction or incident record can be created from the new tab menu in all pages of Service Operations Workspace.

![Record creation from tab in workspace pages](../image/tab-record-creation.png "Record creation from tab")

You can customize the JSON value to provide a variety of options. For example, use this method to create a knowledge article directly from the new tab menu. For more information about knowledge article creation, go to [Knowledge Management in Service Operations Workspace](../concept/knowledge-articles-sow.md).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences**.

2.  From the list of UX applications, select **Service Operations Workspace**.

3.  On the UX Application form, from the UX Page Properties related list, select the **chrome\_tab** property.

4.  On the UX Page Property page, when the **Type** field is set to **json**, edit the **Value** field, for example, to add or delete routes or tables.

    To add a new option, for example, to create a knowledge article, add a new JSON object inside the **newTabMenu** object. Provide the name and the action performed when you select the option as a key-value pair inside the **newTabMenu** object. Following is an example for creating a problem.

    ```
    "label": { 
    
    "translatable": true, 
    
    "message": "New Problem" 
    
    }, 
    
    "routeInfo": { 
    
    "route": "record", 
    
    "fields": { 
    
    "table": "problem", 
    
    "sysId": "-1" 
    
    }, 
    
    "multiInstField": "sysId" 
    
    }, 
    
    "condition": { 
    
    "tableDescription": { 
    
    "table": "problem", 
    
    "canCreate": true 
    
    } 
    
    } 
    
    }, 
    ```

5.  Click **Update**.


