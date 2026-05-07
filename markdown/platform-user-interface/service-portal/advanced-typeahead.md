---
title: Create an advanced typeahead template
description: Configure the way typeahead results display with an advanced template.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Define a search source, Zing search in Service Portal, Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Create an advanced typeahead template

Configure the way typeahead results display with an advanced template.

## Before you begin

**Note:** Search suggestions replaces typeahead search in Service Portal. Update the **glide.service\_portal.search\_as\_you\_type\_behavior** system property to change this behavior. For more information, see [Enable and disable search suggestions](https://www.servicenow.com/docs/access?context=enable-search-suggestions&version=australia&pubname=australia-platform-administration&ft:locale=en-US). Service Portal search widgets automatically use whichever feature you enable.

Role required: admin

## Procedure

1.  Complete the required fields in [Define a search source](add-table-search-source.md).

2.  In the **Typeahead** tab of the **Search Source** record, select the **Advanced typeahead config** check box.

3.  In the **Typeahead template** field, add an HTML template.

    This example uses AngularJS bindings to display service catalog images in the typeahead results.

    ```
    <i class="ta-img" ng-if="match.model.type=='sc'" style="background-image:url('{{match.model.picture}}')"></i> 
    <i class="ta-img" ng-if="match.model.type=='sc_guide'" style="background-image:url('{{match.model.picture}}')"></i> 
    <i class="ta-icon fa fa-file-text-o" ng-if="match.model.type=='sc_content' && match.model.content_type == 'kb'"></i> 
    <strong ng-if="match.model.type=='sc_content' && match.model.content_type == 'external'">➚</strong> 
    <span ng-bind-html="match.label | uibTypeaheadHighlight:query"></span>
    ```

4.  Click **Update**.

    Typeahead results display beside the image defined in the service catalog record.

    ![Typeahead showing results for search term "apple".](../image/adv-typeahead-result.png)


**Parent Topic:**[Define a search source](add-table-search-source.md)

