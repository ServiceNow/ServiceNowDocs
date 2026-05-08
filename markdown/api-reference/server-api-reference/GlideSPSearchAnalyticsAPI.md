---
title: GlideSPSearchAnalytics - Global
description: The GlideSPSearchAnalytics API provides methods to generate search analytics from custom ServiceNow search widgets.Sends search data to the Search Event \[sys\_search\_event\], Search Event per source \[sys\_search\_source\_event\], and Search Signal Event \[sys\_search\_signal\_event\] tables for search results, or to the Search Result Clicked \[sys\_search\_result\_clicked\] and Search Signal Result Event \[sys\_search\_signal\_result\_event\] tables when a user clicks a search result.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSPSearchAnalytics- Global

The GlideSPSearchAnalytics API provides methods to generate search analytics from custom ServiceNow search widgets.

By default, the Search Events \[sys\_search\_event\] and Search Source Events \[sys\_search\_source\_event\] tables collect search data from base system search widgets. However, custom search widgets do not benefit from this feature. Use this API in the server script of custom search widgets in global environments to send search data to the search events tables. Generate relevant search suggestions for your users and monitor search analytics to understand what your users are searching for and whether they're finding what they need.

This API collects the following search data:

-   Searched terms
-   Rank of clicked items
-   Filters used to refine search results
-   Table names and record identifiers from the first page of search results
-   Search results clicked, including browser and location

Search Suggestions is a ServiceNow AI Platform feature. For more information, see Search Suggestions.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideSPSearchAnalytics - publish\(String payload\)

Sends search data to the Search Event \[sys\_search\_event\], Search Event per source \[sys\_search\_source\_event\], and Search Signal Event \[sys\_search\_signal\_event\] tables for search results, or to the Search Result Clicked \[sys\_search\_result\_clicked\] and Search Signal Result Event \[sys\_search\_signal\_result\_event\] tables when a user clicks a search result.

<table id="table_hdc_hvn_plb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

payload

</td><td>

String

</td><td>

JSON payload in String format containing the search data to send to the Search Event \[sys\_search\_event\], Search Event per source \[sys\_search\_source\_event\], and Search Signal Event \[sys\_search\_signal\_event\] tables for search results, or to the Search Result Clicked \[sys\_search\_result\_clicked\] and Search Signal Result Event \[sys\_search\_signal\_result\_event\] tables when a user clicks a search result. Structure the payload as key-value pairs according to the type of search data you would like to collect. -   Collect data when the user searches for a term:
    -   `query`: String. The query being searched.
    -   `portal_id`: String. Sys\_id of the portal record from the Service Portals \[sp\_portal\] table.
    -   `page_id`: String. Sys\_id of the page record from the Pages \[sp\_page\] table.
    -   `results_per_source`: Array. Number of results returned from each search source.
        -   `source_id`: String. Sys\_id of the search source record from the Search Sources \[sp\_search\_source\] table.
        -   `number_of_results`: Number. Number of results returned from the query for the specific search source.
    -   `ais_profile`: String. Sys\_id of the search profile applied to the search. Only applicable for searches made with the AI Search engine.
    -   `search_results`: Array. Results returned in the first page of search results.
        -   `record_id`: String. Sys\_id of the search result record.
        -   `table_name`: String. Name of the table in which the search result record was found.
    -   `refinement_occurred`: Boolean. True if the user filtered the search results; otherwise false.
-   Collect data when a user refines their search results:
    -   `query`: String. The query being searched.
    -   `portal_id`: String. Sys\_id of the portal record from the Service Portals \[sp\_portal\] table.
    -   `page_id`: String. Sys\_id of the page record from the Pages \[sp\_page\] table.
    -   `refinement_occurred`: Boolean. True if the user filtered the search results; otherwise false.
-   Collect the rank of the search result that the user selected.
    -   `query`: String. The query being searched.
    -   `portal_id`: String. Sys\_id of the portal record from the Service Portals \[sp\_portal\] table.
    -   `click_rank`: Number. Rank of the item the user selected. For example, if the user clicked the third item in a list of search results, the value is `3`.
-   Collect information on the search result that the user clicks. Data logs to the Search Result Clicked \[sys\_search\_result\_clicked\] table.
    -   `query`: String. The query being searched.
    -   `portal_id`: String. Sys\_id of the portal record from the Service Portals \[sp\_portal\] table.
    -   `page_id`: String. Sys\_id of the page record from the Pages \[sp\_page\] table.
    -   `results_per_source`: Array. Number of results returned from each search source.
        -   `source_id`: String. Sys\_id of the search source record from the Search Sources \[sp\_search\_source\] table.
        -   `number_of_results`: Number. Number of results returned from the query for the specific search source.
    -   `refinement_occurred`: Boolean. True if the user filtered the search results; otherwise false.
    -   `click_rank`: Number. Rank of the item the user selected. For example, if the user clicked the third item in a list of search results, the value is `3`.
    -   `browser_info`: String. Logs browser name, version, and platform.
    -   `location`: Float. Logs latitude and longitude coordinates of the user location.
    -   `result_clicked_sys_id`: String. Sys\_id of the result the user selected.
    -   `label_description`: String. Description of the result that the user selected.
    -   `source_table`: String. Name of the source table containing the selected result.
    -   `ais_doc_id`: String. Underscore-separated name of the source table and sys\_id of the result record for each result the user selected. For example, if the user clicked a result from the Knowledge \[kb\_knowledge\] table, the value is of the form `kb_knowledge_3020c9b14843210e9db4b5b08b9a712d`. Only applicable for searches made with the AI Search engine.
-   Collect data when a user searches for a term and collect the rank of the search result that the user clicked:
    -   `query`: String. The query being searched.
    -   `portal_id`: String. Sys\_id of the portal record from the Service Portals \[sp\_portal\] table.
    -   `page_id`: String. Sys\_id of the page record from the Pages \[sp\_page\] table.
    -   `results_per_source`: Array. Number of results returned from each search source.
        -   `source_id`: String. Sys\_id of the search source record from the Search Sources \[sp\_search\_source\] table.
        -   `number_of_results`: Number. Number of results returned from the query for the specific search source.
    -   `ais_profile`: String. Sys\_id of the search profile applied to the search. Only applicable for searches made with the AI Search engine.
    -   `search_results`: Array. Summary of records returned in the first page of search results.
        -   `record_id`: String. Sys\_id of the search result record.
        -   `table_name`: String. Name of the table in which the search result record was found.
    -   `click_rank`: Number. Rank of the item the user selected. For example, if the user clicked the third item in a list of search results, the value is `3`.
    -   `ais_doc_id`: String. Underscore-separated name of the source table and sys\_id of the result record for each result the user selected. For example, if the user clicked a result from the Knowledge \[kb\_knowledge\] table, the value is of the form `kb_knowledge_3020c9b14843210e9db4b5b08b9a712d`. Only applicable for searches made with the AI Search engine.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example passes direct search data to the search analytics tables.

```
var searchObject = new GlideSPSearchAnalytics();
var payload = {
  'query': 'how do i get a new computer',
  'portal_id': '81b75d3147032100ba13a5554ee4902b',
  'page_id': '87466b63c3223100c8b837659bba8feb',
  'results_per_source': [{
    'source_id': 'bf2c4c15b3a31300e64be12b86a8dcb7',
    'number_of_results': 2,
  }, {
    'source_id': 'c96eb1686721220023c82e08f585efff',
    'number_of_results': 1
  }],
  'refinement': false,
  'search_results': [{
    'record_id': 'KB Article 1',
    'table_name': 'knowledge'
  }, {
    'record_id': 'KB Article 2',
    'table_name': 'knowledge'
  }, {
    'record_id': 'Employee Help',
    'table_name': 'userportal'
  }]
};
var directSearchData = searchObject.publish(JSON.stringify(payload));
```

This example dynamically collects direct search data from a custom search widget and passes it to the search analytics tables.

```
//client script
var payload = {
  query: this.data.query,
  portal_id: this.data.portalID,
  page_id: this.data.pageID,
  results_per_source: getSearchSources(),
  refinement_occurred: false,
};
var payloadObject = {
  action: "TestAction",
  payload: payload,
};
c.server.get(payloadObject);
```

```
//server script
if (input && input.action === "TestAction") {
  input.action = "";
  var textSearchAnalytics = new GlideSPSearchAnalytics().publish(JSON.stringify(input.payload));
  return;
}
```

This example collects direct search-results-clicked data from a custom search widget and passes it to the search analytics \[sys\_search\_result\_clicked\] table.

```
//client script
function setUserLocationCoords(cb) {
  var onSuccess = function(pos) {
    return cb({
      latitude: pos.coords.latitude,
      longitude: pos.coords.longitude,
    });
  };
  var onError = function() {
    return cb({
      latitude: null,
      longitude: null,
    });
  };
  return window.navigator.geolocation.getCurrentPosition(onSuccess, onError, {
    enableHighAccuracy: true,
  });
}

function trackSearchResultClicked(resultClicked, rank) {
  if (!rank || rank < 1) return;
  var c = $scope;
  var query = _.get(c.data, "q");
  var results = _.get(c.data, "results", []);
  var result = results.find(function(e) {
    return e.primary.trim() === resultClicked.trim();
  });
  var description = result.name != null ? result.name : result.primary;
  var sourceTable = result.table != null ? result.table : null;
  var payloadObject = {
    action: "TestAction",
    payload: {
      query: query,
      portal_id: c.portal.sys_id,
      page_id: $scope.page && $scope.page.id,
      results_per_source: getSearchSources(c),
      refinement_occurred: false,
      click_rank: rank,
      browser_info: $window.navigator.userAgent,
      location: {},
      result_clicked_sys_id: result.sys_id,
      label_description: description,
      source_table: sourceTable,
    },
  };
  setUserLocationCoords(function(coords) {
    payloadObject.payload.location.latitude = coords.latitude;
    payloadObject.payload.location.longitude = coords.longitude;
    $window.spSearchAnalytics = {
      query: query,
      refinement_occurred: false,
    };
    c.server.get(payloadObject);
  });
}
// Event delegation for Updating click rank
$(".panel").on("click", ".result-item a", function(e) {
  var index = $(e.currentTarget).parent().parent().data("index");
  var resultClicked = e.currentTarget.innerText;
  trackSearchResultClicked(resultClicked, index + 1);
});
```

```
// server script
if (input && input.action === "TestAction") {
  input.action = "";
  var textSearchAnalytics = new GlideSPSearchAnalytics().publish(JSON.stringify(input.payload));
  return;
}
```

