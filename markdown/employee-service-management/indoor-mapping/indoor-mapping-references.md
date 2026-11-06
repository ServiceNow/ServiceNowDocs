---
title: Indoor Mapping references
description: Find reference information for Indoor Mapping, including common terminology, installed roles, tables, and scheduled jobs, sync properties, bulk upload and import fields, map printing options, and troubleshooting guidance for common issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/indoor-mapping/indoor-mapping-references.html
release: australia
product: Indoor Mapping
classification: indoor-mapping
topic_type: concept
last_updated: "2026-10-18"
reading_time_minutes: 3
breadcrumb: [Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Indoor Mapping references

Find reference information for Indoor Mapping, including common terminology, installed roles, tables, and scheduled jobs, sync properties, bulk upload and import fields, map printing options, and troubleshooting guidance for common issues.

## What you can find in this section

-   Terms, roles, tables, and scheduled jobs: [Indoor Mapping terminology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/indoor-mapping-common-terminology.md) and [Map components installed with Indoor Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/components-installed-with-indoor-mapping.md).
-   Data migration and synchronization: [Snapshot Impacted tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/snapshot-ind-mapping-tables.md) and [Enhanced Sync Properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/enhanced-sync-properties.md).
-   Import and upload fields: [Floor map import group form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/import-group-form.md) and [Bulk upload Excel columns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/bulk-template-columns.md).
-   Printing: [Map printing options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/map-printing-options.md).
-   Troubleshooting: [Resolving cloning issues in Indoor Mapping instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/troubleshooting-clone-issues.md)and [Places display on the wrong floor in Manage Directions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/troubleshooting-floors-overlap-manage-directions.md).

## Tips for troubleshooting Indoor Mapping issues

-   Check the data before you change the source files. Some issues that look like CAD or georeferencing problems are caused by field values on the map records, so confirm the records first to avoid unnecessary re-imports.
-   Test on one record first. Apply a fix to a single record, verify the result in Map Studio, and then update the remaining records.
-   Test changes in a non-production instance before you apply them to production.
-   Before you clone an instance, preserve the data in the Font, Layer, Outdoor style, and Tile tables to prevent missing attachments and data discrepancies in the target instance.
-   Use [Map components installed with Indoor Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/components-installed-with-indoor-mapping.md) to look up table names, roles, and scheduled jobs when you filter records or verify access.

1.  [Map components installed with Indoor Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/components-installed-with-indoor-mapping.md)  
Several types of components are installed with the Indoor Mapping application, including user roles, tables, and scheduled jobs.
2.  [Indoor Mapping terminology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/indoor-mapping-common-terminology.md)  
Key terms used in Indoor Mapping.
3.  [Snapshot Impacted tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/snapshot-ind-mapping-tables.md)  
Few Indoor Mapping and Workplace Indoor Mapping tables are impacted during the snapshot process when the Indoor Mapping backup data is migrated to Workplace Service Delivery instances.
4.  [Map printing options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/map-printing-options.md)  
The map printing options provide configurations for the page format, font, icons, collision, legend, and timestamps.
5.  [Floor map import group form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/import-group-form.md)  
You can specify details about the import group and select users who must be notified of the import progress.
6.  [Enhanced Sync Properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/enhanced-sync-properties.md)  
You can define the behavior of sync operations by configuring the Enhanced Sync properties.
7.  [Bulk upload Excel columns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/bulk-template-columns.md)  
Use the bulk upload template to provide information about your campuses, buildings, and floors.
8.  [Resolving cloning issues in Indoor Mapping instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/troubleshooting-clone-issues.md)  
After cloning an Indoor Mapping source instance to a target instance, workplace administrators may observe missing attachments and data discrepancies in their target instance.
9.  [Places display on the wrong floor in Manage Directions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/troubleshooting-floors-overlap-manage-directions.md)  
In Indoor Mapping Map Studio, floors appear to overlap when a place record has both Floor and Campus values.

**Parent Topic:**[Indoor Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/indoor-mapping/Indoor-mapping.md)

