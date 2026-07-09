---
title: Resolving cloning issues in Indoor Mapping instances
description: After cloning a Indoor Mapping source instance to a target instance, workplace administrators may observe missing attachments and data discrepancies in their target instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/indoor-mapping/troubleshooting-clone-issues.html
release: yokohama
product: Indoor Mapping
classification: indoor-mapping
topic_type: topic
last_updated: "2026-07-07"
reading_time_minutes: 2
breadcrumb: [Reference, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Resolving cloning issues in Indoor Mapping instances

After cloning a Indoor Mapping source instance to a target instance, workplace administrators may observe missing attachments and data discrepancies in their target instance.

## Symptom

Administrators can clone a source Indoor Mapping instance to a target Indoor Mapping instance. For more information, see cloning an instance.

Before cloning your Indoor Mapping source instance to a target instance, preserve data for each of the listed tables in your source instance. This helps in preventing missing data and attachments in your target Indoor Mapping cloned instance tables.

## Cause

Data discrepancies and missing attachment issues are observed after you have cloned your target instance. The System Clone \[clone\_instance\] record or Clone Request \[sn\_instance\_clone\_request\] record in the source instance excludes the Attachment \[sys\_attachment\] table and doesn't preserve data in the Font \[sn\_map\_core\_font\], Layer \[sn\_map\_core\_layer\], Outdoor style \[sn\_map\_core\_outdoor\_style\], and Tile \[sn\_map\_core\_tile\] tables.These issues also affect workplace experiences in Indoor Mapping Map Studio, Workplace Central, Workplace Reservation Management portal, Workplace Services Kiosk, Workplace Move Management, and Workplace Service Delivery for Mobile.

## Resolution

## Procedure

1.  Log in to your source instance.

2.  Export the list of records in each listed table as XML from the source instance:

    -   sn\_map\_core\_font
    -   sn\_map\_core\_outdoor\_style
    -   sn\_map\_core\_layer
    -   sn\_map\_core\_tile
    For more information, see [Export data from a list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/export-list-data.md).

3.  Log in to the target instance.

4.  In the target instance, update your application scope to Indoor Mapping.

5.  Import the XML files to the target instance.

    **Note:**

    After importing the XML files, it's observed sometimes that there's no data in the JSON files. The JSON files stored in the Styles \(style\) column of the Outdoor styles \[sn\_map\_core\_outdoor\_style\] show missing attachments. To prevent missing attachments and data discrepancies, perform steps 6-7.

    For more information about how to import XML files, see [Import data from XML](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/c_ExportAndImportXMLFiles.md).

6.  To avoid future clone issues, preserve data in the following tables:

    -   sn\_map\_core\_font
    -   sn\_map\_core\_outdoor\_style
    -   sn\_map\_core\_layer
    -   sn\_map\_core\_tile
7.  To preserve data in sn\_map\_core\_font, sn\_map\_core\_outdoor\_style, sn\_map\_core\_layer, and sn\_map\_core\_tile tables perform the following steps:

    1.  Log in to your source Indoor Mapping instance.
    2.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Definition** &gt; **Preserve data**.
    3.  Select **New**.
    4.  On the form, fill in the fields:

<table id="table_lc2_4vh_vjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Enter the following table information as required:-   **\[sn\_map\_core\_font\]**
-   **sn\_map\_core\_layer**
-   **sn\_map\_core\_outdoor\_style**
-   **sn\_map\_core\_tile**


</td></tr></tbody>
</table>    5.  Right-click the form header and select **Save**.
    6.  Add your clone profiles.
        1.  Navigate to Clone profiles related list.
        2.  Select **Edit**.
        3.  From the Collection slush bucket, add your clone profile\(s\) to the Clone Profile List slush bucket.
        4.  Select **Save**.

**Parent Topic:**[Indoor Mapping references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/indoor-mapping/indoor-mapping-references.md)

**Previous topic:**[Bulk upload Excel columns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/indoor-mapping/bulk-template-columns.md)

**Next topic:**[Workplace Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/workplace-central/workplace-central-feat.md)

