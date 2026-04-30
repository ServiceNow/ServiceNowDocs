---
title: Export data in OSCAL format
description: From the Authorization package overview record page, generate zip files and export the record's mapped content details in OSCAL format. This action enables you to export your authorization package from CAM.
locale: en-US
release: xanadu
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exporting Catalog, Profile, and SSP in OSCAL format, Continuous authorization and monitoring tasks in the CAM Workspace, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export data in OSCAL format

From the Authorization package overview record page, generate zip files and export the record's mapped content details in OSCAL format. This action enables you to export your authorization package from CAM.

## Before you begin

Role required: sn\_irm\_cont\_auth.authorization\_official, sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.info\_system\_sec\_officer, sn\_irm\_cont\_auth.system\_owner

## Procedure

1.  Navigate to **All** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select the List icon \(![List](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Select Authorization packages from the **RMF** list.

4.  From the list view, select the authorization package record for which to generate SSP files.

    **Note:** The authorization package must be in Implement state to generate OSCAL SSP.

5.  Select the more actions icon \(![More actions icon.](../../grc-workspace-risk/image/icon-more-actions-risk.png)\) and then select the **Export OSCAL SSP** option from the list.

    A message appears stating that the OSCAL report is being processed and that the file will be exported. A zip is generated which contains JSON files along with some diagrams.

    **Note:** If you do not have the Integration Hub Pro entitlement that is not included in the CAM Workspace, then follow the steps in the [Generate OSCAL Models without zip \[KB1651422\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1651422) article in the Now Support Knowledge Base to generate the OSCAL models.

6.  Refresh the page and select the attachment icon \(![Attachment icon.](../../../common/image/Form_Attachment.png)\) in the sidebar.

7.  Select the action icon \(![More actions icon](../../grc-compliance-case-mgmt/image/more-actions-vertical-icon.png)\) in the oscal-ssp.zip and then select the **Download** option.

    ![Dowload oscal-ssp-zip from the sidebar.](../image/cam-oscal-ssp-zip.png)

8.  Right-click the zip file and select **Open** to extract the file contents from the oscal-ssp.zip.

    You can view the catalog.json, overlay-catalog.json, profile.json, ssp.json files. Additionally, if the authorization package has any diagrams that are mapped to it, then they are also available in the contents of the zip. The diagrams can be a catalog dataflow diagram, network architecture diagram, or an authorization boundary diagram, available as png files in the zip.

    **Note:** To customize the OSCAL support solution, see the [OSCAL Model customization support \[KB1650397\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650397) article in the Now Support Knowledge Base.


