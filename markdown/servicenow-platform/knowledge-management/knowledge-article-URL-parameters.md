---
title: Knowledge article URL parameters
description: You can add parameters to an article URL to view the latest version and an existing translation.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Knowledge Management Service Portal article view page features, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge article URL parameters

You can add parameters to an article URL to view the latest version and an existing translation.

## Knowledge article URL structure

The knowledge article URL appears in the following structures:

-   Accessed from **Service Portal**: `https://<instance-name>.service-now.com/kb?id=kb_article_view&sysparm_article=<article number>&sysparm_language=<language code>`

    For example, the URL `https://yourbusiness.service-now.com/kb?id=kb_article_view&sysparm_article=KB0010053&sysparm_language=EN` returns the article with the most recent version in the selected language, if the translation for the selected language exists.

    **Note:** If you open an article with sysparm\_article and sys\_kb\_id parameters that belong to different articles, the article loads based on a sysparm\_article.

-   Accessed from **Knowledge Base View \(kb\_view\) UI page**: `kb_view.do?sysparm_article=<article number>&sysparm_language=<language code>’`

    For example, the URL `https://yourbusiness.service-now.com/kb_view.do?sysparm_article=KB0010044&sysparm_language=en`returns the article with the most recent version in the selected language, if the translation for the selected language exists.


**Note:** The listed parameters can include the sys\_id in the url parameter.

## Parameters

The following parameters are available for knowledge article URLs.

|Parameter|Possible values|
|---------|---------------|
|sysparm\_article|Returns the most recent article version. For example, `https://yourbusiness.service-now.com/kb?id=kb_article_view&sysparm_article=KB0010053`.|
|sysparm\_language|Returns the most recent article version in the input language if a translation exists. For example, `https://yourbusiness.service-now.com/kb?id=kb_article_view&sys_id=3b07857187032100deddb882a2e3ec20&sysparm_language=EN`.|

**Parent Topic:**[Knowledge Management Service Portal article view page features](../concept/knowledge-service-portal-view.md)

