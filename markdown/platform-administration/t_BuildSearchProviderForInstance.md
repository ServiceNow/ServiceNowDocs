---
title: Build a search provider for your instance
description: ServiceNow Search Providers allow you search and our Forums from the IE and Firefox search bar.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Supported integration interfaces, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# Build a search provider for your instance

ServiceNow Search Providers allow you search and our Forums from the IE and Firefox search bar.

## About this task

In Firefox 3.x you can also assign a keyword to each Search Provider and access them from the address bar. For example, assign w to the wiki search provider and you can search the wiki for Business Rules by typing: `w business rules` in the address bar.

![](../image/SearchProviders.png "Search Bar")

## Procedure

1.  Create an opensearch description document. You can review the OpenSearch standards for details on additional attributes of this document such as including an icon.

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
    	<ShortName>Demo Search</ShortName>
    	<Description>Demo Search provider</Description>
    	<InputEncoding>UTF-8</InputEncoding>
    	<Url type="text/html" template="https://www.service-now.com/demo/nav_to.do?
    	uri=incident_list.do?sysparm_query=active%3Dtrue^123TEXTQUERY321%3D{searchTerms}"/>
    	</OpenSearchDescription>
    ```

2.  Save the file to a web server with xml extension. The method used to install doesn't allow local file calls.

3.  Create a simple html page to install the provider.

    ```
    <a href="javascript:window.external.AddSearchProvider('http://yourServer/yourFile.xml');
    " title="MySearch" name="ServiceNow Custom Search">Add ServiceNow Custom Search Provider</a>
    
    ```

    You could try running the JavaScript command from the browser location box instead of using the html file. This works with FF not IE.


**Parent Topic:**[Supported integration interfaces](../../vendor-specific-integrations/reference/r_SupportedIntegrationInterfaces.md)

