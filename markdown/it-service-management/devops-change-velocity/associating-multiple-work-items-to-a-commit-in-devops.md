---
title: Associating multiple work items to a commit in DevOps
description: Multiple work items for a commit are supported in DevOps for Azure DevOps, Bitbucket, GitHub, and GitLab.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Associating multiple work items to a commit in DevOps

Multiple work items for a commit are supported in DevOps for Azure DevOps, Bitbucket, GitHub, and GitLab.

Work item syntax in the commit message can be customized to reflect the processes in your organization using the DevopsCommitMessageParserSNC script include in the **System Definition &gt; Script Includes** module.

In order to link the commits with work items, the work item native ID is extracted from the commit message. In the base system, DevOps supports following commit message formats:

```
/**
     * Supported patterns
     * Colon pattern 
         * Sample supported formats: 
             *   1. STRY1,STRY2: Additional bug fixes
             *   2. STRY1 , STRY2 : Additional bug fixes
             *   3. STRY1, STRY2 : Additional bug fixes
     * Hash pattern 
         * Sample supported formats: 
             *   1. Fixes for #STRY1, #STRY2, #STRY3
             *   2. Fixes @$#3 and #1 work item
             *   3. Fixes for #STRY1 #STRY2 #STRY3
             *   4. Fixes for AB#123
     * Jira pattern
         * Sample supported formats: 
             *   1. JRA-123 fixed
             *   2. JRA-123 JRA-234 JRA-345 resolved
     */
```

If you want to add support for additional message formats to meet the processes in your organization, you can add a custom logic in the `DevopsCommitMessageParser` script include by navigating to the **System Definition &gt; Script Includes** module. `DevopsCommitMessageParser` script include extends from `DevopsCommitMessageParserSNC`. The `DevopsCommitMessageParserSNC` has three regular expressions defined for identifying work item native IDs for supported message formats in the base system. See the following example to include a new custom message format that has work item native IDs in square brackets.

```
var DevopsCommitMessageParser = Class.create();
DevopsCommitMessageParser.prototype = Object.extendsObject(DevopsCommitMessageParserSNC, {
    initialize: function() {
        DevopsCommitMessageParserSNC.prototype.initialize.call(this);
        this._customPattern = /\[(.*?)\]/g; // The regex pattern to match the words written inside square brackets.
        // Example commits message to match this custom pattern is : "[STRY1], [STRY2] Additional bug fixes"
    },
    getWorkitemsFromCommitMessage: function(message, branchName) {
        var workitems = [];
        // We first call the getWorkitemsFromCommitMessage method from the parent class to get the matching workitems ids for OOB formats
        var defaultWI = DevopsCommitMessageParserSNC.prototype.getWorkitemsFromCommitMessage.call(this, message, branchName);
        if (!gs.nil(defaultWI) && defaultWI.length > 0) {
            workitems = workitems.concat(defaultWI);
        }
        // Now call your custom method that returns an array of workitem native IDs matching custom pattern
        var customWI = this.getWIFromCustomPattern(message);
        if (!gs.nil(customWI) && customWI.length > 0) {
            workitems = workitems.concat(customWI);
        }
        // getUniqueWorkItems method from parent class removes duplicates from the workitems array
        workitems = this.getUniqueWorkItems(workitems);
        // return the final list
        return workitems;
    },
    getWIFromCustomPattern: function(message) {
        var wi = [];
        var l;
        var match;
        var matches = message.match(this._customPattern);
        if (gs.nil(matches))
            return wi;
        for (var i = 0; i < matches.length; i++) {
            l = matches[i].length;
            match = matches[i].substring(1, l - 1); // trim the brackets
            wi.push(match);
        }
        return wi;
    },
    type: 'DevopsCommitMessageParser'
});
```

Linking work items to a commit using the Azure DevOps user interface is also supported in DevOps. ![Link work item to a commit in Azure DevOps](../image/commit-workitem-association.png)

You can view the list of associated work items in the DevOps Commit record, and in the Pipeline UI.

**Parent Topic:**[Managing DevOps Change Velocity](using-devops-change-velocity.md)

