---
title: View upload status for Software Bill of Materials files
description: Check the upload status for the Software Bill of Materials \(SBOM\) files that you upload in the BOM Queue module in the Software Bill of Materials \(SBOM\) Workspace. Track the files that you upload successfully, your upload history, and errors.
locale: en-US
release: yokohama
product: SBOM Core
classification: sbom-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Viewing reports and dashboards in the Software Bill of Materials workspace, Uploading and viewing your SBOM files in the SBOM Workspace, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# View upload status for Software Bill of Materials files

Check the upload status for the Software Bill of Materials \(SBOM\) files that you upload in the BOM Queue module in the Software Bill of Materials \(SBOM\) Workspace. Track the files that you upload successfully, your upload history, and errors.

## Before you begin

Role required: sn\_sbom\_resp.sbom\_analyst

## Procedure

1.  View your upload status.

    The method you use to view your upload status depends on the applications you have installed.

<table id="table_kfc_nqs_ydc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SBOM Core

</td><td>

1.  Navigate to **All** &gt; **SBOM Core** &gt; **BOM Ingestion Status**.
2.  On the Bill of Materials list, review the columns such **Status**, **BOM generation time**, and **Created** columns for details.


</td></tr><tr><td>

SBOM Response

</td><td>

1.  Navigate to **All** &gt; **SBOM Workspace** &gt; **BOM Queue**.
2.  Select a visualization card to review the following details for the categories of your uploaded files:
    -   BOM updates in the last 30 days - Total BOM entities uploaded and parsed successfully over the past 30 days.
    -   Upload source - Total of successfully uploaded SBOM files and a breakdown of the methods used to ingest them \(API or manual\).
    -   Upload errors by category - Top five categories of upload errors. If no data appears on this visualization, all of your SBOM files uploaded successfully.


</td></tr></tbody>
</table>    The status information in the Bill of Materials table \[sn\_sbom\_doc\_list\] and the BOM Queue module both include BOM formats, ingestion Status, and BOM generation time. The Status column for BOM ingestion includes the following states:

    -   Queued - SBOM data has been uploaded.
    -   Processing - The component data is being processed as part of the import.
    -   Processed - Data ingestion has been successfully completed.
    -   Error - An error has occurred during processing.
    In addition to the status of your uploaded files, you can view lists of components you've ingested by selecting a BOM entity record.

2.  Access more information about errors and upload status by selecting the gear icon ![Gear icon](../../../../reuse/icons/product-icons/gear-changes-outline-24.svg) and adding fields such as **Error category** and **Error detail**.


