---
title: Places display on the wrong floor in Manage Directions
description: In Indoor Mapping Map Studio, floors appear to overlap when a place record has both Floor and Campus values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/indoor-mapping/troubleshooting-floors-overlap-manage-directions.html
release: australia
product: Indoor Mapping
classification: indoor-mapping
topic_type: topic
last_updated: "2026-10-18"
reading_time_minutes: 2
keywords: [indoor mapping, Manage Directions, floors overlap, sn\_map\_core\_place]
breadcrumb: [Reference, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Places display on the wrong floor in Manage Directions

In Indoor Mapping Map Studio, floors appear to overlap when a place record has both Floor and Campus values.

## Symptom

In a multifloor building, when you select Floor 2 in Manage Directions, room markers and places that belong to Floor 1 also display. The floors look as though they were imported on top of each other.

The CAD files, floor assignments, and generated floor geometry are correct.

## Cause

The Place request that Map Studio sends returns Indoor Mapping place records that match the selected floor or the campus. If a floor-specific place record in the Place \[sn\_map\_core\_place\] table has both the **Floor** and **Campus** fields populated, the record also qualifies as a campus-level place. As a result, Map Studio returns it when you select a different floor.

The record in the Space \[sn\_wsd\_core\_space\] table isn't the cause. It must keep its full location hierarchy of campus, building, floor, and space.

## Resolution

## Procedure

1.  In the Place \[sn\_map\_core\_place\] table, filter the list by using the following encoded query:

    This step identifies the affected place records.

    ```
    active=true^floorISNOTEMPTY^campusISNOTEMPTY
    ```

    These records are candidates for investigation. Not every record that matches is incorrect.

2.  To list the matching records by using a script, run the following read-only background script:

    ```
    var gr = new GlideRecord('sn_map_core_place');
    gr.addQuery('active', true);
    gr.addNotNullQuery('floor');
    gr.addNotNullQuery('campus');
    gr.query();
    
    while (gr.next()) {
      gs.info(
        'Place=' + gr.getValue('name') +
        ' | Floor=' + gr.getDisplayValue('floor') +
        ' | Campus=' + gr.getDisplayValue('campus') +
        ' | Source=' + gr.getDisplayValue('source')
      );
    }
    ```

3.  Open one affected place record and verify that:

    -   The place is floor-specific.
    -   The **Floor** value is correct.
    -   The AutoCAD source is correct.
    -   The geometry is correct.
    -   The hierarchy of the corresponding record in the Space \[sn\_wsd\_core\_space\] table is correct.
4.  On the place record, clear the **Campus** field and leave the **Floor** field populated, and then save the record.

    **Warning:** Clear the **Campus** field only on records in the Place \[sn\_map\_core\_place\] table. Don't clear it on records in the Space \[sn\_wsd\_core\_space\] table. Test the change in a non-production instance before you apply it to production.

5.  Refresh Map Studio and select each floor of the building to test the change.

    The place displays on its assigned floor and doesn't display on other floors.

6.  If the test is successful, repeat steps 3 to 5 for the remaining affected place records.


**Parent Topic:**[Indoor Mapping references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/indoor-mapping-references.md)

**Previous topic:**[Resolving cloning issues in Indoor Mapping instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/troubleshooting-clone-issues.md)

**Next topic:**[Workplace Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-central/workplace-central-feat.md)

