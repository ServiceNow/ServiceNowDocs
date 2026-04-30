---
title: Enforcing unique numbering
description: Although duplicate numbers are rare, numbering does not enforce uniqueness, by default.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Record numbering, Customize, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Enforcing unique numbering

Although duplicate numbers are rare, numbering does not enforce uniqueness, by default.

To enforce uniqueness, you can:

-   Create a before business rule on insert only to check for duplicate values and replace duplicates with the next available number.
-   Enable a unique index on the table. For more information, see [Create a table index](../../table-administration/task/t_CreateCustomIndex.md).

    **Note:** While unique indexes ensure data integrity they also prevent any insert involving a duplicate number. This may cause unexpected errors during data entry.


## Sample business rule

This sample script can be used as part of a before business rule on insert only to check for duplicate numbers and replace them with the next available number. The following script references a script created in [Configure left padding of a system number in a table](../task/t_RenumberingRecords.md).

```javascript
var curNum = current.number + '';
 
if(curNum) {
 
  var recordClass = current.getRecordClassName();
  var now_GR = new GlideRecord(recordClass);
  now_GR.addQuery('number', curNum);
  now_GR.setLimit(1);  
  now_GR.query();
 
  if(now_GR.getRowCount() > 0) {
    var newNum = getNextObjNumberPadded();
    gs.addInfoMessage("The number " + current.number + " was already used by another " +
     recordClass + ". The " + recordClass + " number has been changed to " + newNum);
    current.number = newNum;
  }
}

```

**Parent Topic:**[Record numbering](c_ManagingRecordNumbering.md)

**Related topics**  


[Business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

