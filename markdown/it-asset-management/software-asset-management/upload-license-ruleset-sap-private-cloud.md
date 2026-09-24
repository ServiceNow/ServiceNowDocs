---
title: Upload the license ruleset for SAP S/4HANA Private Cloud
description: Upload the license ruleset file to your SAP system to enable Full Usage Equivalent \(FUE\) user classification for SAP S/4HANA Cloud, Private Edition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/upload-license-ruleset-sap-private-cloud.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Set up SAP integration to establish a connection with SAP, Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management, Asset Management]
---

# Upload the license ruleset for SAP S/4HANA Private Cloud

Upload the license ruleset file to your SAP system to enable Full Usage Equivalent \(FUE\) user classification for SAP S/4HANA Cloud, Private Edition.

## Before you begin

-   Deploy the SAP S/4HANA Private Cloud satellite transport on your SAP system. For more information, see [Deploy the ABAP program for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/import-abap-program-sap.md).
-   Obtain the `License_Ruleset.xlsx` template file from the [ServiceNow Store](https://me.sap.com/notes/3113382) download package.

Role required: SAP Basis administrator

## About this task

**Note:** Use this task only for SAP S/4HANA Cloud, Private Edition deployments. If your SAP system already has a compatible license ruleset stored, skip this task. The existing ruleset is used automatically during FUE user classification.

The license ruleset defines the classification rules that the SAP user classification program \(`SLIM_USER_CLF_HELP`\) uses to determine the FUE license type for each user. The ruleset maps SAP roles and transaction codes to Named User Types — Developer \(GA\), Advanced \(GB\), Core \(GC\), and Self-Service \(GD\). This upload is a one-time setup step. After the ruleset is stored in your SAP system, the classification program runs automatically on a schedule without requiring manual input.

## Procedure

1.  Log on to your SAP S/4HANA Private Cloud system using SAP log in details.

2.  In the **command** field, enter transaction code `SA38` and press **Enter**.

3.  In the **Program** field, enter `SLIM_USER_CLF_HELP` and select **Execute**.

4.  On the SAP License Administration Workbench screen, select **Manage Rulesets &amp; Results**.

5.  Select **Upload Ruleset**.

6.  Browse to the location of the `License_Ruleset.xlsx` file and select it.

    **Warning:** The file must be named exactly `License_Ruleset.xlsx`. Renaming the file can cause errors during processing in the SAP database.

7.  Select **Upload** to store the ruleset in the SAP system.

    Verify that a success message is displayed confirming that the ruleset has been stored.


## Result

The license ruleset is stored in the SAP system and is available for use by the FUE user classification program. The classification program uses this ruleset to assign each SAP user a target Named User Type during scheduled data collection runs.

## What to do next

After uploading the ruleset, export the Root CA certificate from your SAP system. For more information, see [Export the Root CA certificate from SAP for Private Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/export-root-ca-cert-sap-private-cloud.md).

**Parent Topic:**[Set up SAP integration to establish a connection with SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/setup-sap-integration.md)

