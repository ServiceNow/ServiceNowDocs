---
title: KBPortalServiceImpl - Global
description: The KBPortalServiceImpl API is included with Knowledge Management V3 \[com.snc.knowledge3\] as a script include. It provides methods to use with knowledge, such as integration with a custom search.Instantiates a KBPortalServiceImpl object in a global application.Returns search results based on keywords from the knowledge article and from relevant knowledge block content that the user has access to read.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrating a custom search or knowledge article viewer with knowledge blocks, Using knowledge blocks, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# KBPortalServiceImpl - Global

The `KBPortalServiceImpl` API is included with Knowledge Management V3 \[com.snc.knowledge3\] as a script include. It provides methods to use with knowledge, such as integration with a custom search.

**Parent Topic:**[Integrating a custom search or knowledge article viewer with knowledge blocks](integrating-with-custom-search-or-knowledge-article-viewer.md)

## KBPortalServiceImpl - KBPortalServiceImpl\(\)

Instantiates a KBPortalServiceImpl object in a global application.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## KBPortalServiceImpl - getResultData\(Object request\)

Returns search results based on keywords from the knowledge article and from relevant knowledge block content that the user has access to read.

If you have activated the knowledge blocks feature and are using a custom search for knowledge with your application, your search may not return relevant articles when keywords are contained in the blocks. To return search results based on keywords from the article and from relevant block content that the user has access to read, you must call the `getResultData()` method inside your custom search.

|Name|Type|Description|
|----|----|-----------|
|request|Object|JSON object to refine the search.|

|Type|Description|
|----|-----------|
|Object|Array of search results in JSON format based on keywords from the knowledge article and from relevant knowledge block content that the user has access to read.|

### Integrating a custom search with knowledge blocks

```
function doKeywordSearch(queryText, count, queryLocation) {
  var results = [];
  
  // To set up the request.
  var request = {
    keyword: queryText,
    language: "",

    // To pass data to filter on different metadata.
    variables: {
      kb_knowledge_base: ['Knowledge'],
      kb_category: '',
      author: ['']
    },
 
    // Provide the following.
    context: gs.getProperty('glide.knowman.sp.search_context', 'Knowledge Search'),
    resource: 'Knowledge',
    order: "relevancy,true",

    // Provide the pagination variables.
    start: queryLocation,
    end: queryLocation+count,

    attachment: false,

    // Provide any additional metadata you want to include in your results.
    knowledge_fields: [
      "number",
      "sys_id",
      "published"
    ]
  };

  // To execute the search.
  var response = new KBPortalServiceImpl();
  response.getResultData(request);

  // To send the search results back to the UI or to store results in your object.
  for (var i = 0; i < response.results.length; i++) {
    result = response.results[i];
    var article = {};
    article.sys_id = result.meta.sys_id.display_value;
    article.number = result.meta.number.display_value;
    article.short_description = article.short_description;
    article.title = result.title;
    article.published = result.meta.published.display_value;
    article.publishedUTC = result.meta.published.display_value;
    article.text = article.text;
    article.score = result.meta.score;
    article.label = article.short_description;
    article.shortDescription = article.short_description;
    results.push(article);
  }

  return results;
}
```

