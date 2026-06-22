---
title: Find an app or app file using code search
description: Use code search in ServiceNow Studio to search through all applications and tables on an instance to locate a specific app, app file, or code snippet.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/find-app-app-file-using-code-search.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 2
breadcrumb: [Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Find an app or app file using code search

Use code search in ServiceNow Studio to search through all applications and tables on an instance to locate a specific app, app file, or code snippet.

## About this task

Use code search for troubleshooting issues on an instance. For example, if a client script automatically updates a record incorrectly and displays an error message, search for the error message to find where it is being generated. For a detailed example, see the Community article on [Using Code Search to make developing on the platform easier](https://www.servicenow.com/community/developer-blog/using-code-search-to-make-developing-on-the-platform-easier/ba-p/2265789).

## Before you begin

Role required: admin or delegated\_developer

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the search bar, select the **Activate code search** toggle.

3.  Enter the code snippet to search for in the search bar.

4.  Specify whether to search all apps or a specific app.

    -   Select **Select all** to search all apps on the instance for the code snippet.
    -   Select **Select specific app** and enter the name of the app in the search bar that appears.
5.  Limit the search to a table by entering the table name in the **File types / tables** field.

    Only tables in the same scope are available. For a list of supported file types, see [ServiceNow Studio supported file types using code search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sn-studio-file-types.md).

6.  Select **View results** to run the search.

    The results open in a new **Code search** tab inside ServiceNow Studio.

7.  Expand the script type to review for the code snippet.

    For example, expand the **Notification** section to view all code search results in notification scripts, or the **Access control** section to view all instances of code related to roles and security.

    For a list of types of scripts, see [Available script types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/r_17Scripts.md).

8.  Expand the name of an individual script to view the matching code and its corresponding line number.

    Each script that contains the code snippet appears in an expandable section that displays the number of times the code appears in the script.

9.  Select **open file** to view the complete script.

    The complete script opens in a new tab in ServiceNow Studio.


**Parent Topic:**[Applications in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/working-with-apps-in-servicenow-studio.md)

