---
title: Tutorial: set up an external knowledge base search source
description: Define an advanced search source to return data from any source on the Internet. To understand the power of search sources, follow this tutorial to set up an external knowledge base search source.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 3
breadcrumb: [Define a search source, Zing search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Tutorial: set up an external knowledge base search source

Define an advanced search source to return data from any source on the Internet. To understand the power of search sources, follow this tutorial to set up an external knowledge base search source.

## Before you begin

Role required: none

To create an advanced search source, you need authenticated access to an external website via a REST API and basic knowledge of [AngularJS](https://angularjs.org/).

## About this task

In this integration, you will:

-   Create a data fetch script that uses the ServiceNow [Table API](https://developer.servicenow.com/app.do#!/rest_api_doc?v=paris&id=c_TableAPI) to query a knowledge base from another ServiceNow instance.
-   Decode the JSON response and define the fields that the search widget expects.
-   Update the search sources HTML template to open the search result in the external site.

## Procedure

1.  In the platform UI, navigate to **Service Portal** &gt; **Portals** and select the portal you want to add the search source to.

2.  From the **Search Sources** related list, click **New**.

3.  Create a name and ID for the search source.

    The ID should be unique, and should not include any spaces or special characters.

4.  On the **Data Source** tab, select the **Is scripted source** check box.

5.  Add content to the data fetch script field.

    1.  Define the search function to be executed by the instance.

        This example uses a [Recordless RESTMessageV2 example](https://www.servicenow.com/docs/access?context=r_RecordlessRESTMessageV2Example&version=australia&pubname=australia-api-reference&ft:locale=en-US), but you can modify this example to use a pre-configured [Outbound REST web service](https://www.servicenow.com/docs/access?context=c_OutboundRESTWebService&version=australia&pubname=australia-api-reference&ft:locale=en-US) if needed, or create a more secure authentication profile.

        ```
        (function(query) {  
        var results = [];  
        /* Calculate your results here. */ 
        var url= "https://myInstance.service-now.com/api/now/table/kb_knowledge?sysparm_query=GOTO123TEXTQUERY321%3D" + encodeURI(query) + "&sysparm_fields=sys_id%2Cnumber%2Cshort_description%2Ccategory%2Ctext";  
            var ws = new sn_ws.RESTMessageV2();
                ws.setBasicAuth("search_user", "search");  
                ws.setHttpMethod("get");  
                ws.setEndpoint(url);  
          
                var jsonOutput = ws.execute();  
        
        return results;  
        })(query);
        ```

        **Note:** In the preceding example, `ws.setBasicAuth` requires a username and password for the remote instance. For more detail, see [RESTMessageV2 - Scoped, Global](https://www.servicenow.com/docs/access?context=c_RESTMessageV2API&version=australia&pubname=australia-api-reference&ft:locale=en-US) .

    2.  Add an if statement to the data fetch script to decode the JSON object being returned, iterate over each result, and set expected fields.

        The final data fetch script:

        ```
        (function(query) {  
        var results = [];  
        /* Calculate your results here. */  
        var url= "https://<my-instance>.service-now.com/api/now/table/kb_knowledge?sysparm_query=GOTO123TEXTQUERY321%3D" + 
        encodeURI(query) + "&sysparm_fields=sys_id%2Cnumber%2Cshort_description%2Ccategory%2Ctext";  
        var ws = new sn_ws.RESTMessageV2();  
            ws.setBasicAuth("search_user", "search");  
            ws.setHttpMethod("get");  
            ws.setEndpoint(url);  
          
            var jsonOutput = ws.execute(); 
            if (jsonOutput) {  
                var response = new JSON().decode(jsonOutput.getBody());  
                results = response.result;  
                results.forEach(function(result) {  
                    result.url = "https://myInstance.service-now.com/kb_view.do?sysparm_article=" + result.number;            
                    result.target = "_blank";  
                    result.primary = result.short_description;  
                });  
            }  
        
            if (jsonOutput.haveError()){
                gs.addErrorMessage(jsonOutput.getErrorMessage());
            }
        
        return results;  
        })(query); 
        ```

        In this example, the following fields are set on the result object:

        -   **url**: If linking to an external site rather than opening the record in your ServiceNow instance, this defines where the link leads to.
        -   **target**: The target for the link. Set the target to `_blank` to open results in a new tab, otherwise leave it blank.
        -   **primary**: The primary field displayed in the search results.
6.  Update the search page template to open the search results in the external site.

    ```
    <div>
     <a href="https://myInstance.service-now.com/kb_view.do?sysparm_article={{item.number}}" target="_blank" class="h4 text-primary m-b-sm block">   
        <span ng-bind-html="highlight(item.primary, data.q)"></span>
      </a>
      <span class="text-muted" ng-repeat="f in item.fields | limitTo: 4">
        <span class="m-l-xs m-r-xs" ng-if="!$first"> &middot; </span>
        {{f.label}}: <span ng-bind-html="highlight(f.display_value, data.q)"></span>
      </span>
    </div>
    ```

7.  Click **Update**.


## Result

Test the external search in your portal. Results display under the name field value defined in step three.

![An external search source in the search page](../image/external-search-source-result.png)

Each search result opens in the external site defined in the search page template.

![A single search result from the external search source](../image/ext-knowledge-result.png)

**Parent Topic:**[Define a search source](add-table-search-source.md)

