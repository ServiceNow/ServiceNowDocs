---
title: Legacy - Search within application files
description: Studio allows application developers to search within application files for matching record values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/servicenow-studio-classic/t\_SearchWithinApplicationFiles.html
release: xanadu
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Search within application files

Studio allows application developers to search within application files for matching record values.

## Before you begin

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/servicenow-studio-classic/servicenow-studio-landing.md).

Role required: admin

This procedure requires creating a scoped application.

## About this task

You can search within application files to add, remove, or update application file values.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **Applications**.

2.  From the **Develop** tab, click the **Edit** button next to the application you want to modify.

    The system opens the application in the Studio.

3.  From the header, click **Code Search**.

    You can also use a Studio keyboard shortcut.

<table id="table_ServiceNowStudioOpenSearch"><thead><tr><th>

Keyboard combination

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Windows: Control+Shift+F

 Mac: Command+Shift+F

</td><td>

**Code Search**. Search for any file or value.

</td></tr></tbody>
</table>    Studio opens the Search pop-up window.

4.  In **Search term**, enter a search string.

    \[Omitted image "CreateNowStudioSearch.png"\] Alt text: Search term dialog

5.  Select any additional search criteria.

<table id="choicetable_anv_2xz_bs"><tbody><tr><td id="d125937e242">

**Select a table to search**

</td><td>

Search for matches only within the selected file type.

</td></tr><tr><td id="d125937e251">

**Search in all applications**

</td><td>

Search for matches throughout the instance, not just within the current application.

</td></tr></tbody>
</table>    **Note:** Searches across all applications can take a long time.

6.  Click **Search**.

    The Studio conducts a case-insensitive search of the application files you selected. While the search is running, Studio displays a search progress indicator. You can click the cancel icon to stop the search. When the search is complete, the system opens a new tab in the content frame to display the search results by application file type. Each application file type displays the number of matching search results.

    \[Omitted image "CreateNowStudioSearchResults.png"\] Alt text: A sample search results tab displaying seven matches for the string SAMPLE in the current application.

7.  From the search results tab, expand an application file type and click a record name.

    Studio opens the application file record in a new tab in the content frame.


**Parent Topic:**[Legacy - ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/servicenow-studio-classic/c_ServiceNowStudio.md)

