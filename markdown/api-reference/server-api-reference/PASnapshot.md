---
title: PASnapshot - Scoped
description: The PASnapshot API enables you to query information about Performance Analytics snapshots. Snapshots are the lists of records \(sys\_ids\) that are collected at the time that the scores for those records are collected. A snapshot is made only for automated indicators with Collect records selected.Compares records in snapshots for a specified indicator at multiple dates, such as to identify records included in one snapshot but not the other.Returns the query used to compare records in snapshots for a specified indicator at multiple dates.Returns the sys\_id values for all records contained in the snapshot for a specified indicator at the specified date.Returns the query used to generate the snapshot for a specified indicator at the specified date.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# PASnapshot- Scoped

The PASnapshot API enables you to query information about Performance Analytics snapshots. Snapshots are the lists of records \(sys\_ids\) that are collected at the time that the scores for those records are collected. A snapshot is made only for automated indicators with **Collect records** selected.

You can query information about a snapshot at a certain date using the indicator sys\_id and date, and perform comparisons between snapshots for an indicator at different dates.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## PASnapshot - getCompareIDs\(String sys\_id, Number date1, Number date2, String type\)

Compares records in snapshots for a specified indicator at multiple dates, such as to identify records included in one snapshot but not the other.

<table id="table_jrk_qcq_nw" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

String

</td><td>

Indicator's sys\_id.

</td></tr><tr><td>

date1

</td><td>

Number

</td><td>

Date of the first snapshot.Format: yyyymmdd

</td></tr><tr><td>

date2

</td><td>

Number

</td><td>

Date of the second snapshot.Format: yyyymmdd

</td></tr><tr><td>

type

</td><td>

String

</td><td>

Data to retrieve. Valid values:

-   all1: all records in the first snapshot
-   all2: all records in the second snapshot
-   shared: records that are in both snapshots
-   movedin: records that are in the first snapshot, but not the second
-   movedout: records that are in the second snapshot, but not the first

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|A comma-separated list of sys\_id values.|

```
var snapshot2 = PASnapshot.getCompareIDs('fb007202d7130100b96d45a3ce6103b4', 20160430, 20160531, 'shared');
gs.info(snapshot2);
```

Output:

```
*** Script: 09c01200d7002100b81145a3ce6103ab,19c01200d7002100b81145a3ce6103e9,fcc01200d7002100b81145a3ce61035b,….
```

## PASnapshot - getCompareQuery\(String sys\_id, Number date1, Number date2, String type\)

Returns the query used to compare records in snapshots for a specified indicator at multiple dates.

<table id="table_tgw_sbq_nw" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

String

</td><td>

Indicator's sys\_id.

</td></tr><tr><td>

date1

</td><td>

Number

</td><td>

Date of the first snapshot.Format: yyyymmdd

</td></tr><tr><td>

date2

</td><td>

Number

</td><td>

Date of the second snapshot.Format: yyyymmdd

</td></tr><tr><td>

type

</td><td>

String

</td><td>

Specifies what data to retrieve.Valid values:

-   all1: all records in the first snapshot
-   all2: all records in the second snapshot
-   shared: records that are in both snapshots
-   movedin: records that are in the second snapshot, but not the first
-   movedout: records that are in the first snapshot, but not the second

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|The table, view, and encoded query as a JSON string.|

```
var snapshot4 = PASnapshot.getCompareQuery('fb007202d7130100b96d45a3ce6103b4', 20160530, 20160531, 'all1');
gs.info(snapshot4);

```

Output:

```
*** Script: {
  "view":"",
  "query":"sys_idINjavascript:new PAUtils().getCompareSnapshotIDs(\"fb007202d7130100b96d45a3ce6103b4\",
  \"20160530\",
  \"20160531\",
  \"all1\")",
  "table":"incident"
}
```

## PASnapshot - getIDs\(String sys\_id, Number date\)

Returns the sys\_id values for all records contained in the snapshot for a specified indicator at the specified date.

<table id="table_knc_xbq_nw" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

String

</td><td>

Indicator's sys\_id.

</td></tr><tr><td>

date

</td><td>

Number

</td><td>

Date when the snapshot was taken.Format: yyyymmdd

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|A comma-separated list of sys\_id values.|

```
var snapshot1 = PASnapshot.getIDs('fb007202d7130100b96d45a3ce6103b4', 20160530);
gs.info(snapshot1);
```

Output:

```
*** Script: 09c01200d7002100b81145a3ce6103ab,19c01200d7002100b81145a3ce6103e9,fcc01200d7002100b81145a3ce61035b,….
```

## PASnapshot - getQuery\(String sys\_id, Number date\)

Returns the query used to generate the snapshot for a specified indicator at the specified date.

<table id="table_pth_pbq_nw" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

String

</td><td>

Indicator's sys\_id.

</td></tr><tr><td>

date

</td><td>

Number

</td><td>

Date the snapshot was taken.Format: yyyymmdd

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|The table, view, and encoded query as a JSON string.|

```
var snapshot3 = PASnapshot.getQuery('fb007202d7130100b96d45a3ce6103b4', 20160530);
gs.info(snapshot3);
```

Output:

```
*** Script: {
  "view":"",
  "query":"sys_idINjavascript:new PAUtils().getSnapshotIDs(\"fb007202d7130100b96d45a3ce6103b4\",
  \"20160530\")",
  "table":"incident"
}
```

