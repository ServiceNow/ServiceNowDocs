---
title: Export OSCAL POA&amp;M
description: Generate zip files Plan of Action and Milestones \(POA&amp;M\) data in Open Security Controls Assessment Language \(OSCAL\) JSON format from the Authorization package overview record page. The authorization package must be in Implement state or later, and a POA&amp;M file must link to the selected authorization package.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/export-oscal-poa-m.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-12-01"
reading_time_minutes: 2
breadcrumb: [Export in OSCAL format, CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export OSCAL POA&amp;M

Generate zip files Plan of Action and Milestones \(POA&amp;M\) data in Open Security Controls Assessment Language \(OSCAL\) JSON format from the Authorization package overview record page. The authorization package must be in Implement state or later, and a POA&amp;M file must link to the selected authorization package.

## Before you begin

Role required:

-   CAM Administrator \(sn\_irm\_cont\_auth.admin\)
-   System Owner \(sn\_irm\_cont\_auth.system\_owner\)
-   Authorizing Official \(sn\_irm\_cont\_auth.authorization\_official\)
-   Information System Security Manager \(sn\_irm\_cont\_auth.info\_system\_sec\_manager\)
-   Information System Security Officer \(sn\_irm\_cont\_auth.info\_system\_sec\_officer\)

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace** and then select the \[Omitted image "ws-list-icon.png"\] Alt text: Lists icon. icon.

2.  Select **Authorization packages** from the **RMF** list.

3.  From the list view, select the authorization package record for which you want to generate a POA&amp;M file.

    **Note:** The authorization package must be in the Implement, Assess, Authorize, or Monitor state to generate OSCAL POA&amp;M.

4.  To export OSCAL POA&amp;M, select **Generate OSCAL**.

    **Note:** To generate the OSCAL POA&amp;M, the POA&amp;M file must be linked to the selected Authorization package.

    A banner appears with the message: "The files are being generated. Please refresh the page after some time, then click 'Download OSCAL Files' to download the OSCAL files."

    The system starts generating OSCAL files asynchronously. This process takes a few minutes depending on package complexity. The **Download OSCAL Files** button appears when the process is complete.

5.  After the process is complete, select **Download OSCAL Files**.

    **Note:** Verify that the pop-up blocker is turned off for the URL so that the ZIP file is automatically downloaded to your local machine.

    A ZIP file is downloaded containing the following OSCAL files:

    -   Catalog JSON file
    -   Profile JSON file
    -   SSP JSON file
    -   Overlay Catalog JSON file \(if overlays are configured. Also includes overlays from associated control tailoring requests\)
    -   POA&amp;M JSON file \(included if POA&amp;M items exist\)
    -   Assessment Plan \(AP\) JSON file \(one per engagement\)
    -   Assessment Results \(AR\) JSON file \(one per engagement\)
    You can validate these files using the OSCAL CLI validator and import them into other systems or share them with external auditors for assessment planning.

    To customize the OSCAL behavior for export, see the [OSCAL Model customization support \[KB1650397\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650397) article in the Now Support Knowledge Base.

    For more information on OSCAL import error, see the [OSCAL Import \[KB1794095\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1794095) article in the Now Support Knowledge Base.


**Parent Topic:**[Export in OSCAL format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-support-cam.md)

