---
title: Configure iFrames
description: An iFrame embeds a URL on a page within a frame. It can embed external pages or render ServiceNow content.
locale: en-US
release: australia
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Types of content blocks, Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Configure iFrames

An iFrame embeds a URL on a page within a frame. It can embed external pages or render ServiceNow content.

## Before you begin

Role required: content\_admin or admin

## About this task

Configure an iFrame with forms you create in the instance and link to the page in which the iFrame resides.

**Note:** Do not add any type of report, such as a calendar, to iFrames. For more information on adding a report directly onto a page without using iFrames, see [Embedding reports in Jelly](https://www.servicenow.com/docs/access?context=c_EmbeddingReportsInJelly&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

**Note:** To deliver ServiceNow content from a web page, see [Service Portal](../../../build/service-portal/concept/c_ServicePortal.md) instead.

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Specialty Content** &gt; **iFrames**.

2.  Click **New**.

3.  Complete the iFrame form fields.

<table id="table_snn_mgc_gr"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Type a unique name for the iFrame block.

</td></tr><tr><td>

Frame name

</td><td>

Type a name for the frame on the page. When you use iFrames to present ServiceNow content such as forms or lists, the frame name must be `gsft_main`. This name allows links within the iFrame to open within the iFrame.

</td></tr><tr><td>

URL

</td><td>

Enter the URL to display in the iFrame. If you use the iFrame to display ServiceNow content, start with the page name and do not include the base instance part of the URL. For example, to show the list of requested items, the URL is:`sc_req_item_list.do`

 Queries can be applied to the URL. For instance, to display a list of open requested items, the URL is:

 `sc_req_item_list.do?sysparm_query=active=true`

 For more information, see [Navigate to a record or module using a URL](../../../use/navigation/task/navigate-using-url.md).

</td></tr><tr><td>

Sizing

</td><td>

Select an option for iFrame block size.**Note:** The **Expand to fit content** choice only works with ServiceNow content. If Fixed Size is selected, height and width fields are displayed for you to enter the size in pixels.

</td></tr></tbody>
</table>    **Note:** Some browsers suppress iFrames because they use an X-Frame-Options header value of SAMEORIGIN. The X–Frame-Options header was introduced in Internet Explorer 8 RC1, to help detect and prevent frame-based redressing. The SAMEORIGIN value causes the browser to render a blank page instead of the target page of the &lt;frame&gt; or &lt;iframe&gt; when the frame target is not on the same origin as the page itself. Support for this header has been implemented in Safari 4.0, Chrome 4.1.249.1042, and Firefox 3.6.9 and above.


-   **[Integrate Live Feed with CMS](t_AddLiveFeedToIFrame.md)**  
You can provide access to Live Feed from pages built in the Content Management System \(CMS\). For example, allow an end user to access your company feed via the ESS portal.
-   **[iFrame methods](../concept/c_IFrameMethods.md)**  
The following examples show how system records are pulled into an iFrame that is placed on a content page.

**Parent Topic:**[Types of content blocks](../reference/r_TypesOfContentBlocks.md)

**Related topics**  


[Configure a header block](t_HeaderBlock.md)

[Create a navigation menu block](t_CreateNavigationMenuBlock.md)

[Configure dynamic blocks](t_CreateADynamicBlock.md)

[Customize the list block](t_DefineTheListBlock.md)

[Configure a static HTML block](t_StaticHTMLBlock.md)

[Configure Flash movie blocks](t_FlashMovieBlock.md)

[Configure content links](t_ConfigureContentLinks.md)

[Configure a detailed content block](t_DetailedContentBlock.md)

[Content blocks](../concept/c_ContentBlocks.md)

[Configure a content block](t_CreateAContentBlock.md)

