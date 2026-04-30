---
title: Example: set up a GitHub search source
description: Set up an advanced search source that queries data from an external website.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Define a search source, Zing search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Example: set up a GitHub search source

Set up an advanced search source that queries data from an external website.

## Before you begin

Role required: none

To create an advanced search source, you need authenticated access to an external website via a REST API and basic knowledge of [AngularJS](https://angularjs.org/).

## Procedure

1.  In the platform UI, navigate to **Service Portal** &gt; **Portals** and select the portal you want to add search sources to.

2.  From the Search Sources related list, click **New**.

3.  Create a name and ID for the search source.

    The ID should be unique, and should not include any spaces or special characters.

4.  On the **Data Source** tab, select the **Is scripted source** check box.

5.  Add content to the data fetch script field.

    To set up a GitHub integration:

    ```
    (function(query) {
        var results = [];
        /* Calculate your results here. */
        var url = "https://api.github.com/search/repositories?q=" + encodeURI(query);
        var ws = new GlideHTTPRequest(url);
        ws.setBasicAuth("YOUR_USERNAME_HERE", "YOUR_PASSWORD_HERE");
        var jsonOutput = ws.get();
        if (jsonOutput) {
            var response = new JSON().decode(jsonOutput.getBody());
            results = response.items;
            results.forEach(function(result) {
                result.url = result.svn_url;
                result.target = "_blank";
                result.primary = result.full_name;
            });
        }
    
        return results;
    })(query);
    ```

    **Note:** In the preceding example, `ws.setBasicAuth` requires a username and password for the external resource. For more detail, see [GlideHTTPRequest - Global](https://www.servicenow.com/docs/access?context=GlideHTTPRequestAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

6.  Use the Search page template to customize the way the search results display.

    ```
    <div>
      <div class="pull-right">
        <strong>{{item.language}}</strong>
        <a ng-href="{{item.svn_url}}/stargazers" target="_blank" class="m-l-sm"><span class="fa fa-star m-r-xs"></span>{{item.stargazers_count}}</a>
        <a ng-href="{{item.svn_url}}/network" target="_blank" class="m-l-sm"><span class="fa fa-code-fork m-r-xs"></span>{{item.forks}}</a>
      </div>
      <a ng-href="{{item.svn_url}}" target="_blank" class="h4 text-primary m-b-sm block">
        <span ng-bind-html="highlight(item.full_name, data.q)"></span>
      </a>
      <p>{{item.description}}</p>
      <p>Updated <sn-time-ago timestamp="item.updated_at"></sn-time-ago> ago</p>
    </div>
    ```


**Parent Topic:**[Define a search source](add-table-search-source.md)

