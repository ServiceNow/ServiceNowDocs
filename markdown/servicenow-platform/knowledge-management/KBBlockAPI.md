---
title: KBBlock - Global
description: The KBBlock API is included with knowledge blocks \[com.snc.knowledge\_blocks\] as a script include. It provides methods to use with the knowledge blocks feature, such as integration with a custom knowledge article viewer.Instantiates a KBBlock object in a global application.Gets knowledge articles with relevant knowledge block content that a user has access to read.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating a custom search or knowledge article viewer with knowledge blocks, Using knowledge blocks, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# KBBlock - Global

The `KBBlock` API is included with knowledge blocks \[com.snc.knowledge\_blocks\] as a script include. It provides methods to use with the knowledge blocks feature, such as integration with a custom knowledge article viewer.

**Parent Topic:**[Integrating a custom search or knowledge article viewer with knowledge blocks](integrating-with-custom-search-or-knowledge-article-viewer.md)

## KBBlock - KBBlock\(\)

Instantiates a KBBlock object in a global application.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## KBBlock - getArticleContent\(GlideRecord knowledgeRecord\)

Gets knowledge articles with relevant knowledge block content that a user has access to read.

If you have activated the knowledge blocks feature and are using a custom knowledge article viewer with your application, your viewer may not display articles that expand the relevant block content. To expand block content that a user has access to read, you must call the `getArticleContent()` method inside your custom viewer.

|Name|Type|Description|
|----|----|-----------|
|knowledgeRecord|GlideRecord|GlideRecord of the knowledge article to display.|

|Type|Description|
|----|-----------|
|String|Knowledge article with relevant knowledge block content that a user has access to read.|

### Integrating a custom knowledge article viewer with knowledge blocks

```

// This function returns the article text with expanded block content.
function getArticleText(kbSysId) {
  var knowledgeRecord = new GlideRecord('kb_knowledge');
  var kbText='';
  if(knowledgeRecord.get(kbSysId)) {
    if(new GlidePluginManager().isActive('com.snc.knowledge_blocks')) {
      kbText = new KBBlock();
      kbText.getArticleContent(knowledgeRecord);
    }
    else
      kbText = knowledgeRecord.getValue('text');
    }
  return kbText;
}

// This is an example of how to call the function defined above.
var kbText = getArticleText('01a1ca5b6710130038876c3b5685efd3');
```

