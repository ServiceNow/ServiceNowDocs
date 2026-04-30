---
title: Content management and Jelly code examples
description: Code examples
locale: en-US
release: yokohama
product: Content Management System
classification: content-management-system
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Content Management and the Apache Jelly engine, Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Content management and Jelly code examples

Code examples

-   **Header Example Code**

    This dynamic content block needs to be active and have the "Two Phase" option clicked. The g:requires tag is including the UI script defined in the system whose name is "servicenow.website.globals". The file extension in the call is .jsdbx and is used only in the call to the UI script, not in the name of the script in the system. For JSDBX, the file being called is a JavaScript\(.js\) defined within the database \(db\) that needs to be cached \(x\).

    ```
    <?xml version= "1.0" encoding= "utf-8" ?><j:jelly trim = "false" xmlns:j = "jelly:core" xmlns:g = "glide" xmlns:j2 = "null" xmlns:g2 = "null" >
     
        <g:requires name = "servicenow.website.globals.jsdbx" />
     
    </j:jelly>
    ```

-   **Page Title and Description Example Code**

    This dynamic content block needs to be active. There are two actions within this code snippet. First is a forward-looking string container that allows site translation, the $\{gs.getMessage\('Your Text'\)\} string call\). The second action pulls in the page title and description, $\{current\_page.getName\(\)\} and $\{current\_page.getDescription\(\)\}.

    ```
    <?xml version= "1.0" encoding= "utf-8" ?><j:jelly trim = "false" xmlns:j = "jelly:core" xmlns:g = "glide" xmlns:j2 = "null" xmlns:g2 = "null" >
     
    	<j:if test = "${current_page.getName()=='Solutions'}" ><h1 class = "page_name" > <b> <a href = "solutions.do?" title = "${gs.getMessage('Solutions')}" >${gs.getMessage('Solutions')}</a> </b> </h1><p class = "page_description" >
    	 	    ${current_page.getDescription()}
    		</p> <br /></j:if><j:if test = "${current_page.getName()=='IT 3.0'}" ><h1 class = "page_name" > <b> <a href = "solutions.do?" title = "${gs.getMessage('Solutions')}" >${gs.getMessage('Solutions')}</a> </b> | ${current_page.getName()}</h1><p class = "page_description" >
    	 	    ${current_page.getDescription()}
    		</p> <br /></j:if></j:jelly>
    ```

-   **List Block Pulling From Knowledge Articles Example Code**

    This code example contains one of the best tricks in the CMS. Using the type field with draws from a number of defined list definitions to make slight, or very dramatic changes, to list display. Because the UI is open to configuration and innovation, this is a good opportunity to use design skills. Anyone who can use HTML and CSS knows that a basic list can be turned into a float grid or be made inline. The combinations are limited only by what the designer can dream up and code.

    In the code example, there is a custom logo field \(u\_logo\) added to the Knowledge form. The custom field displays customer logos, partner logos, and award images on the awards page. There are a number of different sections that use this list definition so efficient reuse is taking place.

    -   div class="cms\_knowledge\_list customer\_success" - Begin by creating an outer container with a unique class name that can be used as a basis for CSS style selectors and rules. From the outer container, many of the child elements can be accessed for theming.
    -   &lt;g:for\_each\_record file="$\{current\}" max="$\{jvar\_max\_entries\}"&gt; - Loop for list creation that calls the selected table record and the entries set on the list form.
    -   &lt;a href="knowledge.do?sysparm\_document\_key=kb\_knowledge,$\{current.sys\_id\}"&gt;&lt;img src="$\{current.u\_logo.getDisplayValue\(\)\}" alt="$\{current.text\}" width="110px"/&gt; - Defines linking to the article detail in the knowledge base. For further reference, look at content types within the site definition and you will see some similarities. The knowledge.do? portion of the URL points to the knowledge detail page which \(as mentioned above\) is mandatory if you plan to call the knowledge base in your CMS site. The rest of the URL represents the syntax for calling a knowledge article by its sys\_id. Each and every item housed within the system has a unique sys\_id.
    -   &lt;ttt&gt;$\{SP\}-$\{SP\}$\{current.author.first\_name\}$\{SP\}$\{current.author.last\_name\}&lt;/tt&gt; - This example is commented out and not used, but it is still interesting in that it has a jelly call $\{SP\} and it pulls the knowledge article's author by first and last name.
    ```
    <?xml version= "1.0" encoding= "utf-8" ?><j:jelly trim = "false" xmlns:j = "jelly:core" xmlns:g = "glide" xmlns:j2 = "null" xmlns:g2 = "null" >
     
    <div class = "cms_knowledge_list customer_success" ><g:for_each_record file = "${current}" max = "${jvar_max_entries}" ><br /><table cellspacing = "0" cellpadding = "0" border = "0" class = "background_transparent" ><tr><td class = "cms_knowledge_list_image" ><j:if test = "${current.u_logo.getDisplayValue() != ''}" ><div class = "knowledge_article_logo" ><a href = "knowledge.do?sysparm_document_key=kb_knowledge,${current.sys_id}" > <img src = "${current.u_logo.getDisplayValue()}" alt = "${current.text}" width = "110px" /> </a></div></j:if>
     
    			</td><td width = "100%" ><a href = "knowledge.do?sysparm_document_key=kb_knowledge,${current.sys_id}" target = "_top" ><span class = "cms_knowledge_list_link" >${current.short_description}</span></a><p class = "kb_description" >
    					"${current.description}"
    				 <!--${SP}-${SP}<span class="cms_knowledge_list_author">${current.author.first_name}${SP}${current.author.last_name}</span>--></p></td></tr><tr><td width = "100%" colspan = "2" class = "kb_learn_more" ><p class = "kb_learn_more" ><a href = "knowledge.do?sysparm_document_key=kb_knowledge,${current.sys_id}" >Learn More</a></p></td></tr></table>
     
    </g:for_each_record></div>
     
    </j:jelly>
    ```


**Parent Topic:**[Content Management and the Apache Jelly engine](r_ContentManagementAndJelly.md)

**Related topics**  


[Content Management and the Apache Jelly engine](r_ContentManagementAndJelly.md)

