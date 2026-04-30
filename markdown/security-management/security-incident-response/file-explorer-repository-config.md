---
title: Configure File Explorer Repository Drive
description: The Microsoft SharePoint connector provides various capabilities to be implemented in Microsoft SharePoint File Explorer features by managing and tracking the file metadata.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure File Explorer Component, Configure, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure File Explorer Repository Drive

The Microsoft SharePoint connector provides various capabilities to be implemented in Microsoft SharePoint File Explorer features by managing and tracking the file metadata.

## Before you begin

Role required: sn\_msi.workspace\_admin

## Procedure

1.  Navigate to **All** &gt; **Major Security Incident** &gt; **File Explorer** &gt; **File Repository Configuration**.

2.  Fill the following fields as described in the following table:

<table id="table_xcc_rjh_zpb"><thead><tr><th>

Field Name

</th><th>

Field Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the file repository record that identifies the usage. For example, MSIM.

</td></tr><tr><td>

Provider

</td><td>

Name of the provider that is the third-party file hosting repository provider. For example,Microsoft SharePoint.

</td></tr><tr><td colspan="2">

**Properties**

</td></tr><tr><td>

Site URL Path

</td><td>

Enter a Microsoft SharePoint URL with a specific site path. Provide only the relative path to the site and a complete site URL may not be required. For example, Sites/MSIM.

</td></tr><tr><td>

Document Library Name

</td><td>

Create a document library under the Microsoft SharePoint site and provide the same document library name here.This would be the same document library that you created in the Microsoft SharePoint Connector Drive setup.

</td></tr><tr><td>

Graph Connection

</td><td>

Select the File Explorer Graph tenant record. For more information on the tenant connection configuration, see [Microsoft SharePoint spoke](https://www.servicenow.com/docs/access?context=sharepoint-online-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

</td></tr><tr><td>

Rest Connection

</td><td>

Select the File Explorer REST tenant record. For more information on the tenant connection configuration, see [Microsoft SharePoint spoke](https://www.servicenow.com/docs/access?context=sharepoint-online-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

</td></tr></tbody>
</table>3.  Select **Save**.

4.  Click **Test Connection** tab to test the connection and validate the file repository drive configuration properties.

    **Note:** Before **Activating** the file repository, make sure that the corresponding document library at Microsoft SharePoint doesn't have any folder or file data.

5.  Click **Activate** to activate the file repository.

    ![File Repository Drive](../image/file-explorer-drive-config.png)

6.  Select the **Troubleshooting** check box to verify the file repository **Execution Details** and verify the **Fetch State** is complete and make sure that the Microsoft SharePoint Drive Subscriptions is created and state is complete.

    ![File explorer execution details](../image/file-exp-drive-execution-details.png)

    **Note:** Using the **Test Connection** button, either MSI Administrator or MSI Manager can only validate the file repository configuration.


**Parent Topic:**[Configure File Explorer Component](../concept/file-explorer.md)

