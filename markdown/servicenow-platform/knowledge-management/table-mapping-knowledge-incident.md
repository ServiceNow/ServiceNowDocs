---
title: Create field mapping from an incident to a knowledge article
description: Copy information from an incident into a knowledge article by creating custom mapping between the Incident table and the KCS article table.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Knowledge article creation from an incident, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create field mapping from an incident to a knowledge article

Copy information from an incident into a knowledge article by creating custom mapping between the Incident table and the KCS article table.

## Before you begin

Role required: admin

-   You must activate the Knowledge Advanced plugin \(com.snc.knowledge\_advanced\).
-   You must activate the KCS Article template.
    1.  Navigate to **Knowledge** &gt; **Administration** &gt; **Article Templates**.
    2.  Set the **Active** field to **true** for the KCS Article template.

## Procedure

1.  In the filter navigator, type `csm_table_map.list`.

2.  Click **New**.

3.  In the **Mapping Name** field, enter `Incident KCS Article`.

4.  In the **Source Table** field, enter `Incident`.

5.  In the **Target Table** field, enter `KCS Article`.

6.  Right-click the form header and **Save**.

7.  In the **Basic Field Mapping** related list, click **New**.

8.  Create mappings for the following fields.

    |Source Field|Target Field|
    |------------|------------|
    |Sys ID|Source Task|
    |Short description|Short description|
    |Resolution notes|Resolution|

    **Note:** You can create field mappings for more fields, as required.

    -   In the **Source** field, select the field in the source Incident table that contains the information to be copied to the field in the article template target table.
    -   In the **Target** field, select the field in the article template target table to which you need information copied to from the field in the source Incident table.
9.  To customize when and how the **Knowledge** check box is displayed, click the **Condition** tab.

10. To map fields using advanced scripts, select the **Advanced Field Mapping** check box.

11. On the **Advanced field Mapping** tab, paste in the following code.

    ```
    (function (source,target) {
        // Get the first comments from incident and use it as Issue description for article
        var notes = source.comments.getJournalEntry(-1);
        var entries = notes.split("\n\n");
        var comment = "";
        if(entries[entries.length-2]){
            comment = entries[entries.length-2];
            var part = comment.toString().indexOf(")");
            if(part != -1){
    comment = comment.toString().substring(part+2).replaceAll("\r\n","<br/>");
        }
        }if(comment)
            target.kb_issue = comment;
    })(source,target);
    ```

    The first comment on an incident is mapped to the **Issue Description** field in the knowledge article.

    **Note:** If the same source or target field is configured in both the basic and advanced field mappings, the advanced field mapping overrides the basic field mapping.

    If the fields configured in the basic and advanced field mapping are different, the field configurations in the advanced field mapping are appended to the field configurations in the basic field mapping.


**Parent Topic:**[Knowledge article creation from an incident](../concept/article-from-incident.md)

