---
title: HR synonym dictionary
description: HR Service Delivery provides a Synonym Dictionary that helps expand text searches with additional keywords.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR synonym dictionary

HR Service Delivery provides a Synonym Dictionary that helps expand text searches with additional keywords.

## Before you begin

Role required: admin, ts\_admin

## About this task

You can edit the HR Synonym Dictionary to reflect your business and terminology.

**Note:** You must be in the Global scope to edit.

## Procedure

-   Complete the following tasks:

    -   **Load the HR Synonym Dictionary**

        The HR Synonym Dictionary loads automatically when you check the **Load demo data** box and activate the Human Resources Scoped App: Core \[com.sn\_hr\_core\] plugin.

    -   **Activate the HR Synonym Dictionary**
        1.  Navigate to **System Properties** &gt; **Text Search**.
        2.  Check **Yes** in the **Enable Synonym \(which can be defined in Synonym Dictionaries\)** field.
        3.  Click **Save**.
    -   **Edit the HR Synonym Dictionary**
        1.  Navigate to **System Definition** &gt; **Text Index Synonym Dictionaries**.
        2.  Click **HRSD Synonym Dictionary**.
        3.  The base system provides five default Synonym Sets.
        4.  Click a Synonym Set to edit.
        5.  Add words in the **Synset** box separated by commas. The words in this box are your custom words that you feel your employees use in search.
        6.  Or, click **Insert a new row** to add a Synonym Set.
        7.  Click **Update**.
    -   **Publish the HR Synonym Dictionary**
        1.  The HRSD Synonym Dictionary form appears.
        2.  Click **Publish Dictionary** under Related Links.
        3.  The Synonym Dictionary is active after a few minutes.

**Parent Topic:**[HR Administration](../concept/c_AdministerHRServiceManagement.md)

