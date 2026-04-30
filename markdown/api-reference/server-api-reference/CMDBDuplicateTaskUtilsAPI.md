---
title: CMDBDuplicateTaskUtils - Global
description: The CMDBDuplicateTaskUtils script include provides methods to create a de-duplication task that contains duplicate configuration items \(CIs\) that are of independent type.Creates an instance of the CMDBDuplicateTaskUtils class.Create a de-duplication task in which the sys\_ids of duplicate CIs are specified.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CMDBDuplicateTaskUtils- Global

The CMDBDuplicateTaskUtils script include provides methods to create a de-duplication task that contains duplicate configuration items \(CIs\) that are of independent type.

A de-duplication task can only contain Configuration Management Database \(CMDB\) CIs that are not in another de-duplication task.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CMDBDuplicateTaskUtils - CMDBDuplicateTaskUtils\(\)

Creates an instance of the CMDBDuplicateTaskUtils class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
/**
 * CMDBDeduplicateTaskUtil().createDeduplicateTask() example
 * 
 * OVERVIEW
 * 
 * This script will allow you to search the CMDB
 * for records that may be duplicates based on the field
 * and filter definitions of your chosing
 * 
 */

try {

    //SET INITIAL VARIABLES

    //Set the table that you would like to check for duplicates - note this MUST be a CMDB table
    var cmdbTable = 'cmdb_ci';

    //Add a filter as an encoded query if desired - only objects within this filter will be matched
    // this query filters items are Apple computers located in New York (NY)
    var filterQuery = 'sys_class_name=cmdb_ci_computer^sys_class_name=cmdb_ci_computer^manufacturer=b7e9e843c0a80169009a5a485bb2a2b5^sys_class_name=cmdb_ci_computer^manufacturer=b7e9e843c0a80169009a5a485bb2a2b5^locationLIKENY';

    //Which field shall we use to check for duplicates?
    var matchField = 'name';

    //Do matches need to have the same cmdb_ci class? - This prevents child device types from matching if enabled i.e. Computer, Server
    var sameClass = true;

    //Should empty values be excluded from match?
    var excludeEmpty = true;

    //Minimum number of duplicates required to create a de-duplication task - must be at least 2
    var numberOfMatches = 2;


    //USE GLIDE AGGREGATE TO IDENTIFY POSSIBLE DUPLICATES

    var dupeSetAgg = new GlideAggregate(cmdbTable);
    if (filterQuery) dupeSetAgg.addEncodedQuery(filterQuery);
    dupeSetAgg.addAggregate('COUNT', matchField);
    dupeSetAgg.orderByAggregate('COUNT', matchField);
    dupeSetAgg.groupBy(matchField);
    if (sameClass) dupeSetAgg.groupBy('sys_class_name');
    if (excludeEmpty) dupeSetAgg.addNotNullQuery(matchField);

    //Group by domain if domain separation is enabled (prevent matches across domains)
    if (gs.getProperty('glide.sys.domain.partitioning') == 'true') dupeSetAgg.groupBy('sys_domain');

    //Must have at least 2 CI records that match
    if (numberOfMatches < 2) numberOfMatches = 2;
    dupeSetAgg.addHaving('COUNT', matchField, '>=', parseInt(numberOfMatches));

    dupeSetAgg.query();


    //LOOP THROUGH EACH SET OF MATCHES

    while (dupeSetAgg.next()) {
        var dupeRecordCount = dupeSetAgg.getAggregate('COUNT', matchField);
        var dupeRecordsList = [];
        var dupeAggQuery = dupeSetAgg.getAggregateEncodedQuery();
        var dedupeShortDesc = 'Found ' + dupeRecordCount + ' records where ' + matchField + ' = ' + dupeSetAgg.getValue(matchField) + '\n';
        var dedupeDescription = '';

        gs.log(dedupeShortDesc, 'Dedupe Task Script');

        //Prepare notes - Header row
        dedupeDescription += 'NAME | CREATED ON | UPDATED ON'


        //GATHER ADDITIONAL DEVICE DETAILS (NEED SYS_IDs)

        var dupeDevices = new GlideRecord(cmdbTable);
        dupeDevices.addEncodedQuery(dupeAggQuery); //Use the exact query that the aggregate used for this group
        dupeDevices.query();

        while (dupeDevices.next()) {
            var devName = dupeDevices.getValue('name');
            var devCreated = dupeDevices.getDisplayValue('sys_created_on');
            var devUpdated = dupeDevices.getDisplayValue('sys_updated_on');
            var devId = dupeDevices.getUniqueValue();

            //Add CI to notes
            dedupeDescription += '\n' + devName + ' | ' + devCreated + ' | ' + devUpdated;

            //Add sys_id to list of matched records for this group
            dupeRecordsList.push(devId);
        }
        gs.log(dedupeDescription, 'Dedupe Task Script');


        //CREATE DEDUPLICATION TASK

        //Convert array to string - .createDuplicateTask() expects a comma separated string
        var deviceIdString = dupeRecordsList.join();

        var dedupeUtil = new CMDBDuplicateTaskUtils();
        var dedupeTaskId = dedupeUtil.createDuplicateTask(deviceIdString);


        //UPDATE DEDUPLICATION TASK - ADD DETAILS

        if (dedupeTaskId) {

            var dedupeTask = new GlideRecord('reconcile_duplicate_task');
            dedupeTask.get(dedupeTaskId);
            dedupeTask.setValue('short_description', dedupeShortDesc);
            dedupeTask.work_notes = dedupeDescription;
            dedupeTask.update();

            gs.log('>>>Created de-duplication task ' + dedupeTask.getValue('number') + ' for ' + devName, 'Dedupe Task Script');

        }

    }

} catch (er) {
    gs.log(er, 'Dedupe Task Script');

}
```

Output \(unique sys\_id\):

```
Dedupe Task Script: Found 2 records where name = MacBook Pro 15"

Dedupe Task Script: NAME | CREATED ON | UPDATED ON
MacBook Pro 15" | 2012-02-18 00:14:21 | 2021-12-17 04:28:17
MacBook Pro 15" | 2012-02-18 00:14:37 | 2021-12-17 04:28:21
MacBook Pro 15" | 2012-02-18 00:14:29 | 2021-12-17 04:28:31
...
MacBook Pro 15" | 2012-02-18 00:14:36 | 2021-12-17 04:30:17
MacBook Pro 15" | 2012-02-18 00:14:32 | 2021-12-17 04:30:14
MacBook Pro 15" | 2012-02-18 00:14:19 | 2021-12-17 04:30:14
Dedupe Task Script: >>>Created de-duplication task DUP0001002 for MacBook Pro 15"
```

## CMDBDuplicateTaskUtils - createDuplicateTask\(String sysIDs\)

Create a de-duplication task in which the sys\_ids of duplicate CIs are specified.

|Name|Type|Description|
|----|----|-----------|
|sysIDs|String|A comma-separated list of sys\_ids for which to create a de-duplication task.|

<table id="table_jkd_gt3_2db" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

The sys\_id of the created de-duplication task. Returns null if:

-   The input string is empty.
-   The input parameter contains a sys\_id that is not in the cmdb\_ci table.
-   The input parameter contains a sys\_id that is in an open de-duplication task

</td></tr></tbody>
</table>```
// where <sys-id1> and <sys-id2> are sys_IDs of CIs in the cmdb_ci table
var sysIDs = '<sys-id1>,<sys-id2>';
var dupTaskUtil = new CMDBDuplicateTaskUtils();
var deDupTaskID = dupTaskUtil.createDuplicateTask(sysIDs);
gs.info(deDupTaskID);
```

Output \(unique sys\_id\):

```
04c53e2c1bac411079e52131604bcba9
```

