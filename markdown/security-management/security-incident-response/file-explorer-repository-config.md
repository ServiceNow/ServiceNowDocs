---
title: Configure File Explorer repository drive
description: Configure the File Explorer repository drive to establish a connection between your MSIM workspace and Microsoft SharePoint, enabling team members to manage incident documents centrally.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/file-explorer-repository-config.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure File Explorer Component, Configure, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure File Explorer repository drive

Configure the File Explorer repository drive to establish a connection between your MSIM workspace and Microsoft SharePoint, enabling team members to manage incident documents centrally.

## Before you begin

Role required: sn\_msi.workspace\_admin

## Procedure

1.  Navigate to **All** &gt; **Major Security Incident** &gt; **File Explorer** &gt; **File Repository Configuration**.

2.  On the form, fill in the fields.

<table id="table_xcc_rjh_zpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the file repository record that identifies the usage. For example, MSIM.

</td></tr><tr><td>

Provider

</td><td>

Name of the provider that is the third-party file hosting repository provider. For example, Microsoft SharePoint.

</td></tr><tr><td colspan="2">

**Properties**

</td></tr><tr><td>

Site URL Path

</td><td>

Enter a Microsoft SharePoint URL with a specific site path. Provide only the relative path to the site and a complete site URL may not be required. For example, Sites/MSIM.

</td></tr><tr><td>

Document Library Name

</td><td>

Create a document library under the Microsoft SharePoint site and provide the same document library name here.

</td></tr><tr><td>

Graph Connection

</td><td>

Select the File Explorer Graph tenant record. For more information on the tenant connection configuration, see [Microsoft SharePoint spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/sharepoint-online-spoke.md).

</td></tr><tr><td>

Rest Connection

</td><td>

Select the File Explorer REST tenant record. For more information on the tenant connection configuration, see [Microsoft SharePoint spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/sharepoint-online-spoke.md).

</td></tr></tbody>
</table>3.  Select **Save**.

4.  Select the **Test Connection** tab to test the connection and validate the file repository drive configuration properties.

    **Note:** Before **Activating** the file repository, make sure that the corresponding document library at Microsoft SharePoint doesn't have any folder or file data.

5.  Select **Activate** to activate the file repository. Select **OK** on the confirmation pop-up.

    **Note:** The **Activate** button appears on the form only when all of the following conditions are met:

    -   The **Provider** field is set to Microsoft SharePoint.
    -   The **Graph Connection** and **REST Connection** fields are configured with valid Microsoft SharePoint tenant records.
    -   The record has been saved and validated successfully. The system resolves the Microsoft SharePoint Site ID automatically during validation. If validation fails, the Activate button does not appear.
6.  Select the **Troubleshooting** check box to verify the file repository **Execution Details** and verify the **Fetch State** is complete and make sure that the Microsoft SharePoint Drive Subscriptions is created and state is complete.

    **Note:** Using the **Test Connection** button, either MSI Administrator or MSI Manager can only validate the file repository configuration.


**Parent Topic:**[Configure File Explorer Component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/file-explorer.md)

