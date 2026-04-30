---
title: Search Scripted Post-processors form
description: The Search Scripted Post-processors form contains information about post-processing scripts defined in search application configurations for AI Search. Use this form when creating or modifying search scripted post-processors.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer]
---

# Search Scripted Post-processors form

The Search Scripted Post-processors form contains information about post-processing scripts defined in search application configurations for AI Search. Use this form when creating or modifying search scripted post-processors.

For details on creating or editing search scripted post-processors, see [Using search scripted post-processors in AI Search application configurations](../concept/script-post-process-ais.md#).

<table id="table_jwr_5vb_5nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Option to activate the search script post-processor.

</td></tr><tr><td>

Name

</td><td>

Name for the search script post-processor.

</td></tr><tr><td>

Application

</td><td>

Application scope for the search script post-processor. This field is automatically set.

</td></tr><tr><td>

Type

</td><td>

Type of record the search script post-processor operates on. Valid values:

-   **Genius Result**: Script operates on a Genius Result answer record.
-   **Search Result**: Script operates on a search result record.

</td></tr><tr><td>

Post processing script

</td><td>

Server-side script function that takes a record object as its parameter. When the search scripted post-processor is linked to a search application configuration, search results reflect changes made to the record object in this script function. As an example, this post-processing script function operates on search results from the kb\_knowledge table, transforming sys\_updated\_on date field values into a human-readable format:

```
function process(record) {

    var transformableTables = ['kb_knowledge'];
    var transformableDateFields = ['sys_updated_on'];

    var table = record.getTable();

    // Terminate early if possible, to avoid unnecessary overhead
    if (transformableTables.indexOf(table) === -1)
        return;

    function transformToHumanFriendlyDate(rawDate) {
        // Time gaps in ms
        var MINUTE_GAP = 60000;
        var HOUR_GAP = 3600000;
        var DAY_GAP = 86400000;
        var WEEK_GAP = 604800000;
        var MONTH_GAP = 2592000000;
        var YEAR_GAP = 31536000000;

        var gap = new Date().getTime() - rawDate;
        if (gap < MINUTE_GAP) {
            return gs.getMessage('Just Now');
        } else if (gap > MINUTE_GAP && gap < 2 * MINUTE_GAP) {
            return gs.getMessage('1 minute ago');
        } else if (gap < HOUR_GAP) {
            return gs.getMessage('{0} minutes ago', '' + Math.floor(gap / MINUTE_GAP));
        } else if (gap > HOUR_GAP && gap < 2 * HOUR_GAP) {
            return gs.getMessage('1 hour ago');
        } else if (gap < DAY_GAP) {
            return gs.getMessage('{0} hours ago', '' + Math.floor(gap / HOUR_GAP));
        } else if (gap > DAY_GAP && gap < 2 * DAY_GAP) {
            return gs.getMessage('1 day ago');
        } else if (gap < WEEK_GAP) {
            return gs.getMessage('{0} days ago', '' + Math.floor(gap / DAY_GAP));
        } else if (gap > WEEK_GAP && gap < 2 * WEEK_GAP) {
            return gs.getMessage('1 week ago');
        } else if (gap < MONTH_GAP) {
            return gs.getMessage('{0} weeks ago', '' + Math.floor(gap / WEEK_GAP));
        } else if (gap > MONTH_GAP && gap < 2 * MONTH_GAP) {
            return gs.getMessage('1 month ago');
        } else if (gap < YEAR_GAP) {
            return gs.getMessage('{0} months ago', '' + Math.floor(gap / MONTH_GAP));
        } else if (gap > YEAR_GAP && gap < 2 * YEAR_GAP) {
            return gs.getMessage('1 year ago');
        } else {
            return gs.getMessage('{0} years ago', '' + Math.floor(gap / YEAR_GAP));
        }
    }

    for (var i = 0; i < transformableDateFields.length; i++) {
        var fieldName = transformableDateFields[i];
        var updatedDateField = record.getField(fieldName);
        if (updatedDateField !== null) {
            var updatedDateRaw = updatedDateField.getValue();
            if (updatedDateRaw != null) {
                var humanFriendlyDate = transformToHumanFriendlyDate(updatedDateRaw);
                updatedDateField.setDisplayValue(humanFriendlyDate);
            }
        }
    }
}
```

**Note:** The UI displays an overview of API methods usable in the post-processing script function.

 You can copy code from an existing post-processor script to use as a starting point for your own script function. To access existing post-processor scripts, open the Search Scripted Post-processors \[sys\_search\_scripted\_processor\] table in list view by following these steps:

1.  Select **All**.
2.  In the Filter field, enter `sys_search_scripted_processor.list`.
3.  Press Enter.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

