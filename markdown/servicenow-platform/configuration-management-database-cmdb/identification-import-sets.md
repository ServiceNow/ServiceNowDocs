---
title: Applying IRE to Import Sets
description: You can apply CMDB Identification and Reconciliation Engine \(IRE\) processes when Import Sets are used to import CIs into the CMDB. CI identification can prevent duplicate CIs in the CMDB, which Import Sets might otherwise cause.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Applying IRE to Import Sets

You can apply CMDB Identification and Reconciliation Engine \(IRE\) processes when Import Sets are used to import CIs into the CMDB. CI identification can prevent duplicate CIs in the CMDB, which Import Sets might otherwise cause.

Populating CMDB tables using Import Sets can inadvertently result in duplicate CIs when multiple imported records are identical to an existing CI. To minimize this duplication, you can apply CMDB Identification and Reconciliation processes to Import Sets when importing new records into CMDB tables.

## Transform map script

In the onBefore transform map script for an import set, add a call to the CMDBTransformUtil API, similar to the following code sample:

```
(function runTransformScript(source, map, log, target) {
// Call CMDB API to do Identification and Reconciliation of current row
var cmdbUtil = new CMDBTransformUtil();
cmdbUtil.setDataSource('ImportSet');
cmdbUtil.identifyAndReconcile(source, map, log);
ignore = true;

if (cmdbUtil.hasError()) {
        var errorMessage = cmdbUtil.getError();
        log.error(errorMessage);
} else {
        log.info('IE Output Payload: ' + cmdbUtil.getOutputPayload());
        log.info('Imported CI: ' + cmdbUtil.getOutputRecordSysId());
}

})(source, map, log, target);
```

The `ignore = true` code phrase prevents Import Sets from creating the same record again after it is processed by the identification engine.

## Process

The identification engine performs identification of each source record before it is inserted into the CMDB. The identification engine determines if the record is a duplicate of an existing CI, and then:

-   If not duplicate: Inserts the record to the target table.
-   If duplicate: Updates the existing CI in the CMDB, with data from the source record.

The CMDBTransformUtil API pre-processes the source data, then passes the input values to the identification engine with import set being the data source by default. The CMDBTransformUtil API supports a target field that is a reference field in the same manner that Import Sets supports it. The CMDBTransformUtil API also supports a source script, evaluating source scripts to determine the target value which is then passed to the identification engine. For more information, see Creating a field map.

## Specify multiple target tables for an import set

You can configure each record in an import set with its own target table. Then, instead of inserting all the transformed records into a single target table, the records are inserted into the different target tables that are specified per record. For example, you might need to insert some records from the import set to the Computer class and other records to the Server class.

When importing data using Import Sets, incorporate the following steps:

-   In the data source file, add a target table column. Use a string such as "MyTable" to label the column header. In each record row, enter the target table for the record, as a valid CMDB class name such as "cmdb\_ci\_computer".
-   After you **Auto Map Matching Fields** on the Table Transform Map form, add a field map for the added target table column to establish a relationship between classes and the target tables in the CMDB.
    1.  In the **Field Map** related list on the Table Transform Map form, click **New**.
    2.  Set **Source field** to the header of the target table column that you added in the data source file, such as `MyTable`.
    3.  Set **Target field** to **Class**.
    4.  Click **Submit**.

When you configure an import set with multiple target tables as described in the steps above, the **Target table** that is specified on the Table Transform Map form is not used.

## Restrictions

The following restrictions apply:

-   An import set should be associated with a single transform map. While adding a call to the CMDBTransformUtil API, ensure that still a single transform map exists for the import set.
-   The CMDBTransformUtil API does not check if mandatory fields have values when used with Import Sets . Regardless of how **enforce mandatory fields** is set in the transform map, data import fails if a mandatory field does not have a value.
-   CI Identification and Reconciliation cannot be applied to Import Sets for dependent CIs \(CIs with dependent identification rules\).

**Parent Topic:**[CMDB Identification and Reconciliation \(IRE\)](c_CMDBIdentifyandReconcile.md)

**Related topics**  


[bundle-crint.t_CreateATransformMap]

