---
title: System content management
description: Most of the content in a CMS site is managed in different locations throughout the system.
locale: en-US
release: australia
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Content Management design, Content Management System, Configure UIs and portals, Configure user experiences]
---

# System content management

Most of the content in a CMS site is managed in different locations throughout the system.

For example, if you are building a knowledge website, the pages and blocks exist in CMS, but the knowledge articles are authored and managed in the Knowledge application. The same is true for any other type of content you plan to leverage. It is important to take time to understand the table structure of data to become acquainted with content.

Links to content are typically static, however, take time to look at the document tree and review how field values are formatted for use within the CMS. To understand the information provided below, right-click within forms in the platform and select **Show XML** to view the document tree for the referenced table. To see the table values for each field, right-click the form label and choose **Show - \(field name\)** or **Configure Dictionary** for reference.

Look at several internet news sites for ideas on how to format dynamic list data and also the full article detail. Research blog sites, shopping sites, and any other site you find easy to use, as layout and usability design can be time-consuming. If you find a site that inspires you, emulate it in your design.

-   This [New York Times example](http://www.nytimes.com/pages/todayspaper/index.html) has two separate list formats.
-   The [CNN example](http://www.cnn.com/WORLD/) has several list formats on the page.
-   Several different list formats are used on the ServiceNow website.

## Knowledge articles - kb\_knowledge table

When you right-click and select **Show XML** on any form within the system, the document tree for the referenced database table becomes reference-able. Review the following selected subset of the document tree so you can acquaint yourself with the content readily available to your site design.

```
<kb_knowledge> 
  <active>true </active> 
  <author display_value= "First Last Name" >Use this field value if author name is important </author> 
  <short_description>Use this field value as the link to the full article detail </short_description>   
  <description>Provide this field value as a 1-2 sentence summary of the article </description>   
  <number>Unique ID can be leveraged in a number of different ways </number> 
  <published>Published time stamp of the article  </published> 
  <rating>This field value provides a 1 to 5 star rating similar to iTunes </rating> 
  <sys_updated_on>Add to supplement article published timestamp </sys_updated_on> 
  <sys_view_count>8 </sys_view_count> 
  <topic>Useful field value in creating hierarchical breadcrumbs </topic> 
  <category>Also useful in organizing articles hierarchically  </category> 
  <use_count>Use this similar to Facebook's "like" feedback, answer to the question was this useful </use_count> 
</ kb_knowledge>
```

```
<?xml version= "1.0" encoding= "utf-8" ?>
<j:jelly trim = "false" xmlns:j = "jelly:core" xmlns:g = "glide" xmlns:j2 = "null" xmlns:g2 = "null" >
 
<div class = "cms_knowledge_list customer_success" >
 <g:for_each_record file = "${current}" max = "${jvar_max_entries}" ><br /><table cellspacing = "0" cellpadding = "0" border = "0" class = "background_transparent" >
  <tr><td class = "cms_knowledge_list_image" >
  <j:if test = "${current.u_logo.getDisplayValue() != ''}" >  
   <div class = "knowledge_article_logo" >
     <a href = "knowledge.do?sysparm_document_key=kb_knowledge,${current.sys_id}" > 
       <img src = "${current.u_logo.getDisplayValue()}" alt = "${current.text}" width = "110px" /> 
     </a>  
   </div>
  </j:if>
  </td>
  <td width = "100%" >
  <a href = "knowledge.do?sysparm_document_key=kb_knowledge,${current.sys_id}" target = "_top" >
    <span class = "cms_knowledge_list_link" >${current.short_description}</span>
  </a>
  <p class = "kb_description" > "${current.description}"
  <!--${SP}-${SP}<span class="cms_knowledge_list_author">${current.author.first_name}${SP}${current.author.last_name}</span>-->
  </p>
  </td></tr><tr>
  <td width = "100%" colspan = "2" class = "kb_learn_more" >
  <p class = "kb_learn_more" >
    <a href = "knowledge.do?sysparm_document_key=kb_knowledge,${current.sys_id}" >Learn More</a>
  </p></td></tr></table>
 
</g:for_each_record></div>
 
</j:jelly>
```

**Parent Topic:**[Content Management design](c_ContentManagementPlanning.md)

