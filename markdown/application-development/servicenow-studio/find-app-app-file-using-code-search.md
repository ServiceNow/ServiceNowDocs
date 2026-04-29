---
title: Find an app or app file using code search
description: Find an app or app file using code search in ServiceNow Studio. Code search enables you to search through all applications and tables on your instance to find what you're looking for.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with applications, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Find an app or app file using code search

Find an app or app file using code search in ServiceNow Studio. Code search enables you to search through all applications and tables on your instance to find what you're looking for.

## About this task

You can use code search for troubleshooting issues on your instance. For example, if a client script automatically updates a record incorrectly and displays an error message, you can perform a code search for the error message to find out where it's being generated. For a detailed example of using code search to troubleshoot, see the Community article on [Using Code Search to make developing on the platform easier](https://www.servicenow.com/community/developer-blog/using-code-search-to-make-developing-on-the-platform-easier/ba-p/2265789).

## Before you begin

Role required: admin or delegated developer

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  In the search bar, select the **Activate code search** toggle.

3.  Enter the code snippet you're looking for in the search bar.

4.  Specify whether to search all apps or a specific app.

    -   Choose **Select all** to search all apps on the instance for the code snippet.
    -   Choose **Select specific app** and then enter the name of the app in the search bar that appears.
5.  Limit the search to a table by entering the name of the table in the **File types / tables** field.

    Only tables in the same scope are available. For a list of supported file types, see [ServiceNow Studio supported file types using code search](../reference/sn-studio-file-types.md).

6.  Run the search by selecting **View results**.

    The results open in a new **Code search** tab inside ServiceNow Studio.

7.  Expand the type of script that you want to review for the code snippet.

    For example, you can expand the **Notification** section to view all code search results in notification scripts, or the **Access control** section to view all instances of code related to roles and security.

    For a list of types of scripts, see [Available script types](https://www.servicenow.com/docs/access?context=r_17Scripts&version=australia&pubname=australia-api-reference&ft:locale=en-US).

8.  View the code you searched for and its corresponding line number by expanding the name of the individual script within the section you're viewing.

    Each script that contains the code snippet appears in an expandable section that displays the number of times the code appears in the script.

9.  View the whole script that contains the code by selecting **open file**.

    The complete script appears in a new tab in ServiceNow Studio.


**Parent Topic:**[Working with applications in ServiceNow Studio](../concept/working-with-apps-in-servicenow-studio.md)

