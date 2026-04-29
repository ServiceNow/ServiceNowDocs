---
title: Create field mapping from an HR case to a knowledge article
description: Copy information from an HR case into a knowledge article by creating custom mapping between the HR case table and the KCS article table.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Enable actionable knowledge feedback, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create field mapping from an HR case to a knowledge article

Copy information from an HR case into a knowledge article by creating custom mapping between the HR case table and the KCS article table.

## Before you begin

Role required: admin

-   Ensure that the Knowledge Advanced plugin \(com.snc.knowledge\_advanced\) is active.
-   Ensure that the Developer Application is set to **Human Resources: Core**.
-   Ensure that the KCS Article template is active.
    1.  Navigate to **Knowledge** &gt; **Administration** &gt; **Article Templates**.
    2.  Set the **Active** field to **true** for the KCS Article template.

## Procedure

1.  In the filter navigator, type `csm_table_map.list`.

2.  Click **New**.

3.  In the **Mapping Name** field, enter `HR Case KCS Article`.

4.  In the **Source Table** field, enter `HR Case`.

5.  In the **Target Table** field, enter `KCS Article`.

6.  Right-click the form header and **Save**.

7.  In the **Basic Field Mapping** related list, click **New**.

8.  Create mappings for the following fields.

    |Source Field|Target Field|
    |------------|------------|
    |Sys ID|Source Task|
    |Short description|Short description|
    |Close notes|Resolution|
    |Description|Cause|

    **Note:** You can create field mappings for more fields, as required.

    -   In the **Source** field, select the field in the source HR Case table that contains the information to be copied to the field in the article template target table.
    -   In the **Target** field, select the field in the article template target table to which you need information copied to from the field in the source Incident table.
9.  To customize when and how the **Knowledge** check box is displayed, click the **Condition** tab.

10. To map fields using advanced scripts, select the **Advanced Field Mapping** check box.

11. On the **Advanced field Mapping** tab, paste in the following code.

    ```
    (function (source) {
       // Get the first comments from HR case and use it as Issue description for article
       target.short_description=source.short_description+“”;
       target.kb_resolution=source.close_notes+“”;
       target.kb_cause=source.description+“”;
      var notes = source.comments.getJournalEntry(-1);
      var entries = notes.split(“\n\n”);
      var comment = “”;
      if(entries[entries.length-2]){
          comment = entries[entries.length-2];
          var part = comment.toString().indexOf(“)”);
          if(part != -1){
    comment = comment.toString().substring(part+2).replaceAll(“\r\n”,“<br/>“);
      }
      }if(comment)
          target.kb_issue = comment;
    
       //Only if selected article type is active
       var tem =  new GlideRecord("kb_article_template");
       tem.addQuery("child_table","kb_template_kcs_article");
       tem.addActiveQuery();
       tem.query();
       if(!tem.hasNext())
           return false;
    
       //Do not allow to create the knowledge again
       var now_GR = new GlideRecord("kb_knowledge");
       gr.addQuery("source",source.sys_id);
       gr.query();
       if(gr.next())
           return false;
    
       return true;
    })(source);
    ```

    The first comment on an HR case is mapped to the **Issue Description** field in the knowledge article.

    **Note:** If the same source or target field is configured in both the basic and advanced field mappings, the advanced field mapping overrides the basic field mapping.

    If the fields configured in the basic and advanced field mapping are different, the field configurations in the advanced field mapping are appended to the field configurations in the basic field mapping.


**Parent Topic:**[Enable actionable knowledge feedback](configure-act-know-feedback-properties.md)

