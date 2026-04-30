---
title: View CMS block tags
description: View CMS block tags, which are used for advanced block creation and site flexibility.
locale: en-US
release: zurich
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# View CMS block tags

View CMS block tags, which are used for advanced block creation and site flexibility.

## Before you begin

Role required: content\_admin or admin

## About this task

It is constructed as `<g:content_block> {{Jelly_Tags|Jelly]]` and can be used in either of the following ways.

-   To display a block inside a block
-   To display a block inside a layout

The tag appears in the format, &lt;g:content\_block type="&lt;type&gt;" id="&lt;sys\_id&gt;"/&gt;.

An example of the block tag is included in the ESS Portal sample site.

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Design** &gt; **Frames**.

2.  Click **cms\_admin\_home\_frame**.

3.  View the code.

    ```
    <style>
    
    DIV.cms_administration_home {
    	background: url(gray_${current_page.getURLSuffix()}.pngx) no-repeat right top;
    }
    
    </style>
    
    
    <div class="cms_administration_home">
       ${body}
    <br/>
    <!-- Would you like to pivot off of parent page instead?  try this snippet 
       <j:if test="${current_page.getParentPage().getURLSuffix()=='administration'}">
          <g:content_block type="content_block_menu" id="7afc342def002000914304167b2256ac"/>
       </j:if>
         The defaults use the page URL suffix to define sub menus
    -->
       <j:if test="${current_page.getURLSuffix()=='administration'}">
          <g:content_block type="content_block_menu" id="7afc342def002000914304167b2256ac"/>
       </j:if>
       <j:if test="${current_page.getURLSuffix()=='community_inspired'}">
          <g:requires name="ess.portal.globals.jsdbx" />
          <g:content_block type="content_block_menu" id="ccd4b8c7efb70000914304167b22566e"/>
       </j:if>
    <br/>
    </div>
    ```

4.  To see what the page looks like, navigate to the ESS Portal administration page.

    For example, `http://instance name.service-now.com/ess/administration.do`.


**Parent Topic:**[Content blocks](../concept/c_ContentBlocks.md)

**Related topics**  


[Configure a content block](t_CreateAContentBlock.md)

[Types of content blocks](../reference/r_TypesOfContentBlocks.md)

[Content Management and the Apache Jelly engine](../reference/r_ContentManagementAndJelly.md)

[Content blocks](../concept/c_ContentBlocks.md)

[Configure a header block](t_HeaderBlock.md)

[Configure a static HTML block](t_StaticHTMLBlock.md)

[Format an image as a static HTML block](t_AddAnImageAsAStaticHTMLBlock.md)

[Configure dynamic blocks](t_CreateADynamicBlock.md)

[Catalog cart block](../concept/c_CatalogCartBlock.md)

[Integrate Live Feed with CMS](t_AddLiveFeedToIFrame.md)

[Configure Flash movie blocks](t_FlashMovieBlock.md)

[Configure a detailed content block](t_DetailedContentBlock.md)

[Configure iFrames](t_IFrame.md)

