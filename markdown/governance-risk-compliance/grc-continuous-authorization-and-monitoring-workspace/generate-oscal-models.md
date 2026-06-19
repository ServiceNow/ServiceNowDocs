---
title: Export OSCAL SSP
description: From the Authorization package overview record page, generate zip files and export the record's mapped content details in OSCAL format. To generate OSCAL SSP, the selected Authorization package must be in implemented state or after that. This action enables you to export your authorization package from CAM.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/generate-oscal-models.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Export in OSCAL format, CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export OSCAL SSP

From the Authorization package overview record page, generate zip files and export the record's mapped content details in OSCAL format. To generate OSCAL SSP, the selected Authorization package must be in implemented state or after that. This action enables you to export your authorization package from CAM.

## Before you begin

Role required:

-   CAM Administrator \(sn\_irm\_cont\_auth.admin\)
-   System Owner \(sn\_irm\_cont\_auth.system\_owner\)
-   Authorizing Official \(sn\_irm\_cont\_auth.authorization\_official\)
-   Information System Security Manager \(sn\_irm\_cont\_auth.info\_system\_sec\_manager\)
-   Information System Security Officer \(sn\_irm\_cont\_auth.info\_system\_sec\_officer\)

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select the List icon \(\[Omitted image "ws-list-icon.png"\] Alt text: List\).

3.  Select Authorization packages from the **RMF** list.

4.  From the list view, select the authorization package record for which to generate SSP files.

    **Note:** The authorization package must be in the Implement, Assess, Authorize, or Monitor state to generate OSCAL SSP.

5.  Select **Generate OSCAL**.

    A banner appears with the message: "The files are being generated. Please refresh the page after some time, then click 'Download OSCAL Files' to download the OSCAL files."

    The system starts generating OSCAL files asynchronously. This process takes a few minutes depending on package complexity. The **Download OSCAL Files** button appears when the process is complete.

6.  After the process is complete, select **Download OSCAL Files**.

    **Note:** Verify that the pop-up blocker is turned off for the URL so that the ZIP file is automatically downloaded to your local machine.

    A ZIP file is downloaded containing the following OSCAL files:

    -   Catalog JSON file
    -   Profile JSON file
    -   SSP JSON file
    -   Assessment Plan \(AP\) JSON file \(one per engagement\)
    -   Assessment Results \(AR\) JSON file \(one per engagement\)
    -   Overlay Catalog JSON file \(if overlays are configured. Also includes overlays from associated control tailoring requests\)
    -   POA&amp;M JSON file \(included if POA&amp;M items exist\)
    Additionally, if any diagrams attached to the respective fields and boundary for the package are linked to it, then they’re also available in the contents of the zip. The diagrams can be a catalog dataflow diagram, network architecture diagram, or an authorization boundary diagram, available as png files in the zip.

    You can validate these files using the OSCAL CLI validator and import them into other systems or share them with external auditors for assessment planning.

    To customize the OSCAL behavior for export, see the [OSCAL Model customization support \[KB1650397\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650397) article in the Now Support Knowledge Base.

    For more information on OSCAL import error, see the [OSCAL Import \[KB1794095\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1794095) article in the Now Support Knowledge Base.


**Parent Topic:**[Export in OSCAL format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-support-cam.md)

