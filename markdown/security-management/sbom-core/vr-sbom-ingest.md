---
title: Upload Software Bill of Materials files manually
description: Upload Software Bill of Materials \(SBOM\) files manually.
locale: en-US
release: australia
product: SBOM Core
classification: sbom-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Software Bill of Materials, Unified Security Exposure Management, Security Operations]
---

# Upload Software Bill of Materials files manually

Upload Software Bill of Materials \(SBOM\) files manually.

## Before you begin

Starting with version 4.0, SBOM Core supports:

-   XML and JSON in versions 1.0 - 1.6 of CycloneDX.
-   JSON in versions 2.2 - 2.3 of SPDX.

Role required: sn\_sbom\_core.sbom\_ingest

## Procedure

1.  Upload files manually.

    The method you use to upload your files depends on whether you have the SBOM Core or SBOM Response applications installed.

<table id="choicetable_xcf_543_czb"><thead><tr><th align="left" id="d138463e90">

Option

</th><th align="left" id="d138463e93">

Description

</th></tr></thead><tbody><tr><td id="d138463e99">

**If you have installed SBOM Core**

</td><td>

1.  Navigate to **SBOM Core** &gt; **BOM Ingestion Status**.
2.  On the Bill of Materials list select **New**.
3.  Select the **Click to add** link.

You can upload one SBOM file at a time.

4.  Select **Choose file** and locate the file you want.

The file name is displayed on the Choose an attachment file page.

5.  Select **OK**.


</td></tr><tr><td id="d138463e157">

**If you have installed SBOM Response starting with v4.0**

</td><td>

1.  Navigate to **All** &gt; **Workspaces** &gt; **SBOM Workspace** &gt; **BOM Queue**.
2.  Select **Upload BOM**.

The Upload SBOM file modal is displayed.

3.  Select the **Attach file** link.
4.  Locate the file you want and select **Open**.

After your file uploads, a link for the file is displayed along with three icons that provide you with the following options:

    -   Download the file.
    -   Edit the file name.
    -   Delete the file from the upload.
5.  Select **Upload** to continue.

You can upload one SBOM file at a time.

6.  \(Optional\) Select a Business application and a Product model from the lists.

These values help you associate this SBOM to a business application or product model in your organization. This information is displayed on the BOM entity record after upload.

7.  Select **Upload**.

The BOM queue page is displayed and the file is listed on the SBOM ingestion section along with upload status other information about the file.

</td></tr></tbody>
</table>2.  Upload SBOM files imported by the [Veracode Vulnerability Integration](../../veracode/concept/veracode-vuln-integration.md).

    **Note:** You can upload Veracode files in CycloneDX \(JSON and XML\) and SPDX \(XML\) formats only if you have installed and activated the Veracode integration with Application Vulnerability Response. See the [Veracode Vulnerability Integration](../../veracode/concept/veracode-vuln-integration.md) for more information.


## Result

After an SBOM is successfully processed, where you view the upload status depends on the applications you are using.

-   If you are using SBOM Response, the BOM Entity record is displayed on the SBOM Ingestion Status list in the BOM Queue module in the SBOM Workspace.
-   If you are using SBOM Core, navigate to **SBOM Core** &gt; **BOM Ingestion Status**.

**Related topics**  


[Uploading Software Bill of Materials files using a REST API](../concept/vr-sbom-preparing-upload.md)

