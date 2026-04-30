---
title: Navigate to a record or module using a URL
description: Users can navigate to a record or module directly by using a URL. This topic explains the URL schema by which the system renders pages.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Navigate to a record or module using a URL

Users can navigate to a record or module directly by using a URL. This topic explains the URL schema by which the system renders pages.

## Before you begin

Role required: admin

## About this task

**Note:** The `sysparm_query` page parameter behaves differently for a list versus a form.

-   List: Returns records that match the query conditions.
-   Form \(with sys\_id=-1 specified\): Applies the values to the new record.

## Procedure

1.  To access the unique, secure web address for each instance, enter the default format: `https://<instancename>.service-now.com`.

    **Note:** To display a custom base URL in email notifications, set the **glide.email.override.url** property. For more information, see [Advanced email properties](https://www.servicenow.com/docs/access?context=r_AdditionalProperties&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

2.  For other URL displays, enter one of the following schemas:

<table id="table_ocs_m3y_h1b"><thead><tr><th>

Action

</th><th>

Schema

</th></tr></thead><tbody><tr><td>

To display the page in the standard interface, with the banner frame on top and the application navigator on the left

</td><td>

`nav_to.do?uri=`

</td></tr><tr><td>

To open a form, list, UI page, or other page

</td><td>

`<page name>.do?`

</td></tr><tr><td>

To view a list

</td><td>

`<table name>_list.do`

</td></tr><tr><td>

To open a record in form view

</td><td>

`<sys_id>`

</td></tr><tr><td>

To create a new record

</td><td>

`sys_id` is -1.

</td></tr><tr><td>

To specify a query, view, redirection page, and more.

</td><td>

`<page parameters>`

 Parameters include the following examples:

-   `sysparm_view=ess`: Specifies a view \(ess\).
-   `sysparm_query=number=INC00040`: Specifies a query \(number is INC00040\).
-   `sysparm_query=priority=2^active=true`: Specifies a complex query with two terms \(priority is 2 and active is true\).
-   `sysparm_query=priority=2^active=true^EQ^GROUPBYcategory`: Groups query results \(by category\).
-   `sysparm_order=number`: Specifies the field by which to sort \(number\).
-   `sysparm_order_direction=desc`: Specifies a sort order \(descending\).
-   `sysparm_force_row_count=5`: Limits the maximum number of results \(5 records\).
-   `sysparm_result_view=viewname`: Specifies the view for search results.


</td></tr><tr><td>

To specify a file format. \(CSV, XML, PDF, or UNL \(Unload\)\)

</td><td>

`%26CSV`

</td></tr><tr><td>

To separate page parameters

</td><td>

`&`

</td></tr><tr><td>

To build multiple term queries or specify multiple field values

</td><td>

`^`\(carat\)

</td></tr><tr><td>

 

</td><td>

 

</td></tr></tbody>
</table>
-   **[Enable tiny URL support](t_EnableTinyURLSupport.md)**  
The default URLs by which the system renders pages may exceed the character limit of some browsers, resulting in an error message. You can enable tiny URL support, which generates shortened internal URLs, to help prevent this error.
-   **[Examples of navigating by URL](../reference/r_NavigatingByURLExamples.md)**  
A list of example URLs that demonstrate ways to open pages in the ServiceNow application.

**Parent Topic:**[Forms in the classic environment](../../using-forms/concept/c_UsingForms.md)

**Related topics**  


[Page navigation by URL](../../../build/service-portal/concept/navigate-by-portal-url.md)

