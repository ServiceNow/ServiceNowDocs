---
title: Configure the preview text setting for a standard article template
description: Configure the preview text setting to customize the default preview text for a standard article template.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure knowledge article templates, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the preview text setting for a standard article template

Configure the preview text setting to customize the default preview text for a standard article template.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  On the Script Includes page, in the **Name** field, enter `ArticleTemplateUtilSNC`.

3.  Open the ArticleTemplateUtilSNC record.

4.  On the ArticleTemplateUtilSNC page, copy the following code from the **Script** field.

    ```
    setPreviewTextForStandardArticle: function(){
                  return null;
           },
    ```

5.  On the Script Includes page, in the **Name** field, enter `ArticleTemplateUtil`.

6.  Open the ArticleTemplateUtil record.

7.  On the ArticleTemplateUtil page, modify the code in the **Script** field by pasting the copied code as shown.

    ```
    var ArticleTemplateUtil = Class.create();
                     ArticleTemplateUtil.prototype = Object.extendsObject(ArticleTemplateUtilSNC,{
                     type: 'ArticleTemplateUtil',
    		    setPreviewTextForStandardArticle: function(){
                             return null;
                     },
                     });
    ```

8.  In the **Script** field, remove `null` and enter a preview text.

9.  Select **Update**.


## Result

The modified preview text displayed on the standard article template selector.

## Example

The following code is modified to show custom preview text. You can also include HTML tags to modify the appearance of preview text.

```
var ArticleTemplateUtil = Class.create();
                 ArticleTemplateUtil.prototype = Object.extendsObject(ArticleTemplateUtilSNC,{
                 type: 'ArticleTemplateUtil',
		    setPreviewTextForStandardArticle: function(){
                         return 'Demo for standard article';
                 },
                 });
```

**Parent Topic:**[Configure knowledge article templates](../concept/configure-knowledge-article-templates.md)

