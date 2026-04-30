---
title: View links between system elements and URLs
description: You can view the links between your system elements and their URLs to render more specific content within your site.
locale: en-US
release: xanadu
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Content Management integration points, Content Management System, Configure UIs and portals, Configure user experiences]
---

# View links between system elements and URLs

You can view the links between your system elements and their URLs to render more specific content within your site.

## Before you begin

Role required: content\_admin or admin

## About this task

See the [Navigate to a record or module using a URL](../../../use/navigation/task/navigate-using-url.md) page for an overview of URL syntax in the ServiceNow platform.

The Incidents list offers a quick example of viewing a form within its own tab. This viewing method illustrates how to append the URL string to render more specific content within your site.

## Procedure

1.  Navigate to**Incident** &gt; **All**.

2.  Right-click in a blank area within the content frame and select **Open Frame in New Window** or **Open Frame in New Tab**.

    The URL returned looks similar to this example.

    `<instance_name>/incident_list.do?sysparm_userpref_module=b55b4ab0c0a80009007a9c0f03fb4da9`

    The URL is comprised of the following elements.

    -   `incident_list.do?` is the call to the list with no parameters passed into it. Explore context menu options and list filtering variations to see how the URL string is appended with each action.
    -   `incident_list.do?sysparm_query=&sysparm_view=ess` is an example of how the view is passed in the URL string.
    -   `incident_list.do?sysparm_query=GROUPBYactive&sysparm_view=` is how the URL looks when the **group by** option is chosen from the context menu.
    -   `incident_list.do?sysparm_query=category%3Dsoftware` is the result of applying a **category is software** filter to the list.
    Explore all the options available within the right-click menu. Click through to the Incident form itself \(incident.do\) to see what the URL string does when parameters are passed into it.


-   **[Element link examples](../concept/c_Examples.md)**  
View examples that show how to create a site pointing to various system data in several different data tables.
-   **[Page source view](../reference/r_PageSourceView.md)**  
Use the tools available in your browser to view the frame source page and understand what URL address bars pass between system frame sets.

**Parent Topic:**[Content Management integration points](../concept/c_CMSIntegrationPoints.md)

