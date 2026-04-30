---
title: Run the fix script to enable decimal quantities for services
description: After upgrading to Yokohama Patch 12 or Zurich Patch 6, if you are unable to specify decimal quantities for services, you must run a background fix script to enable support for decimal quantities.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-02-20"
reading_time_minutes: 1
breadcrumb: [Decimal quantity support for service-based purchases in Shopping Hub, My purchases on Shopping Hub, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Run the fix script to enable decimal quantities for services

After upgrading to Yokohama Patch 12 or Zurich Patch 6, if you are unable to specify decimal quantities for services, you must run a background fix script to enable support for decimal quantities.

## Before you begin

Role required: sn\_shop.procurement\_administrator

## About this task

If you upgraded to Yokohama Patch 12 or Zurich Patch 6 and cannot specify decimal quantities for services, run this script from the Scripts - Background module. The script converts the quantity field type from integer to decimal and updates the field scale to four decimal places.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scripts - Background**.

2.  In the **Run script \(JavaScript executed on server\)** section, paste the following code:

    ```
    (function() {
       var tableName = 'sn_spend_sdc_service_request_line';
       var columnName = 'new_purchased_quantity';
       if (pm.isZboot()) {
           return;
       }
       try {
           var updated = GlideFixStuff.fixTypeFromIntegerToDecimalCaseLineQuantityItem(tableName, columnName);
           if (!updated) {
               gs.info('Cannot update type from integer to decimal for field ' + columnName);
               return;
           }
           updateScale();
       } catch (ex) {
           gs.info('Cannot update type from integer to decimal with error ' + JSON.stringify(ex));
           return;
       }
       function updateScale() {
           var desiredScale = 4;
           var dictGR = new GlideRecord('sys_dictionary');
           var query = 'name=' + tableName + '^elementIN' + columnName;
           var fieldName;
           dictGR.addEncodedQuery(query);
           dictGR.query();
           if (dictGR.next()) {
               try {
                   var attrbiuteArray = [];
                   var currentAttributes = dictGR.attributes;
                   if (currentAttributes != '') {
                       attrbiuteArray = currentAttributes.split(',');
                   }
                   var currentMaxLength = dictGR.max_length;
                   fieldName = dictGR.element;
                   var newMaxLength = currentMaxLength + desiredScale;
                   dictGR.max_length = newMaxLength;
                   attrbiuteArray.push("scale=" + desiredScale);
                   dictGR.attributes = attrbiuteArray.join(',');
                   dictGR.update();
                   dictGR.max_length = newMaxLength + 1;
                   dictGR.update();
                   gs.info('Updated max length twice for field ' + fieldName);
               } catch (ex) {
                   gs.info('Cannot update scale attribute due to error : ' + JSON.stringify(ex));
                   gs.error('Error updating max length attribute for field {0}. No update performed.', fieldName);
               }
           }
       }
    })();
    ```

3.  Deselect the **Record for rollback?** check box.

4.  Select **Run Script**.


**Parent Topic:**[Decimal quantity support for service-based purchases in Shopping Hub](../concept/decimal-support-services.md)

