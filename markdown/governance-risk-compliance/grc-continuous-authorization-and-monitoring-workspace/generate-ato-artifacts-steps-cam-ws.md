---
title: Generate ATO artifacts
description: From the Authorization package overview record page, generate Authority to Operate \(ATO\) artifacts in Microsoft Word format. This action enables you to download your ATO artifacts from CAM.
locale: en-US
release: xanadu
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2024-12-11"
reading_time_minutes: 3
breadcrumb: [ATO artifacts for an authorization package, Continuous authorization and monitoring tasks in the CAM Workspace, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Generate ATO artifacts

From the Authorization package overview record page, generate Authority to Operate \(ATO\) artifacts in Microsoft Word format. This action enables you to download your ATO artifacts from CAM.

## Before you begin

Role required:

-   sn\_irm\_cont\_auth.admin
-   sn\_irm\_cont\_auth.authorization\_official
-   sn\_irm\_cont\_auth.info\_system\_sec\_manager
-   sn\_irm\_cont\_auth.info\_system\_sec\_officer
-   sn\_irm\_cont\_auth.system\_owner

**Important:**

-   Set up the ServiceNow Document designer for Word plugin before you create a Microsoft Word template and generate the ATO artifacts reports.

    For more information, see [Install the ServiceNow Document Designer add-in](../../grc-common/task/install-document-designer.md).

-   Verify using which report type you want to generate the respective ATO artifacts.

    For more information, see [Continuous Authorization and Monitoring system properties](../../grc-cam/reference/cam-system-properties.md).


## Procedure

1.  Navigate to **All** &gt; **CAM Workspace**.

2.  To navigate to the Lists page, select the lists icon \(![Lists icon.](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  From the Authorization packages in the RMF list, select an authorization package record for which you want to generate the reports.

    **Important:** To generate ATO artifacts, the reports must be in the following state:

<table id="simpletable_khg_4dk_b2c"><thead><tr><th>

State

</th><th>

ATO artifacts

</th></tr></thead><tbody><tr><td>

Implement, Assess, Authorize, or Monitor

</td><td>

-   SSP
-   POA&amp;M
 **Note:**

-   The repetition property "com.snc.word\_doc\_api.max\_repetitions" in the Document designer plugin must be set to 200 to generate an SSP report successfully. For more information, see [Reference information for Document designer](../../grc-common/reference/properties-for-document-designer.md).
-   For authorization packages with medium or high data limits, increase the number of records to 200 in the template configuration to generate the SSP report successfully. For more information, see [Create content configurations for CAM](../../grc-cam/reference/cam-create-content-configurations.md).


</td></tr><tr><td>

Assess, Authorize, or Monitor

</td><td>

-   SAP
-   SAR


</td></tr><tr><td>

Authorize or Monitor

</td><td>

-   ATO Letter
-   Executive Summary


</td></tr></tbody>
</table>4.  To generate an SSP report for the package, select **Generate SSP**.

5.  To generate the following report, select the drop-down action icon \(![Drop-down actions icon](../image/cam-ato-artifacts-dropdown-icon.png)\):

    -   To generate an SAR report for the package, select **Generate SAR**.
    -   To generate an POA&amp;M report for the package, select **Generate POA&amp;M**.
    -   To generate an SAP report for the package, select **Generate SAP**.
    -   To generate an ATO letter report for the package, select **Generate ATO Letter**.
    -   To generate an Executive Summary report for the package, select **Generate Executive Summary**.
    ![Generate ATO artifact UI actions.](../image/cam-ato-artifacts.png)

6.  Select **Proceed**.

    After the Microsoft Word file is generated, a banner message states that the report has been generated successfully.

    **Note:** When generating a report from an HTML template, the screen remains displayed after you select **Proceed** until the report is fully generated.

    When generating a report from a Word template, the **Proceed** screen disappears, and the report generation takes place in the background.

7.  Close the message and select the attachment in the sidebar.

    The Microsoft Word document is also attached to the **Authorization** section of the package in the **Details** related list. You can also select the download icon next to the report to download the file.

8.  Select the more actions icon \(![More actions icon](../../grc-workspace-risk/image/icon-more-actions-risk.png)\) next to the file with a **.docx** extension and select the **Download** option.

    The downloaded file opens in a Microsoft Word format with all the details. The report is also attached in the **Activity** section of the package with the timestamp and the user who generated it.

    To use the functionality of Generate ATO artifacts for an authorization package using the HTML template, see the [Configurations Required to Enable Report Generation for Authorization Package in CAM Workspace \[KB1649486\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1649486) article in the Now Support knowledge base.


