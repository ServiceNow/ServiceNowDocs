---
title: Create a narrative disclosure on remote storage
description: Create an ESG Management narrative disclosure for your organization and store it on remote storage such as Microsoft SharePoint. Disclosures can be of several types such as ESG report, annual report, and so on.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Disclosures in Operational Sustainability Management \(formerly ESG Management\), Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create a narrative disclosure on remote storage

Create an ESG Management narrative disclosure for your organization and store it on remote storage such as Microsoft SharePoint. Disclosures can be of several types such as ESG report, annual report, and so on.

## Before you begin

Ensure that you follow the procedure to integrate the ServiceNow® instance and Microsoft OneDrive. Refer to [Setup Microsoft OneDrive for Document Services](https://www.servicenow.com/docs/access?context=configure-ms-onedrive-doc-services&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and [Connecting to Microsoft Sharepoint \[KB1646310\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1646310%20) article in the Now Support Knowledge Base.

Role required: sn\_esg.reporting\_disclosure\_manager or sn\_esg.program\_manager

## About this task

When you create a disclosure, you can specify if you want to save the disclosure on your local system or on some remote storage such as Microsoft SharePoint. The disclosure that is created serves as the primary document. This procedure provides the instructions for creating a narrative disclosure on remote storage.

**Note:** After you create a disclosure, you must not use Ctrl+A and delete to delete the content in the Disclosure document. If this is done, the metrics associated with the document would not be deleted and will be tracked. Ensure that the custom properties Document ID and Disclosure Number are not updated or deleted after the disclosure document is created.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Lists** &gt; **Disclosures** &gt; **Narrative disclosures**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_FloorForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Identification number for the disclosure. This field is automatically set.

</td></tr><tr><td>

State

</td><td>

State of the disclosure. This field is automatically set to **Draft**.

</td></tr><tr><td>

Name

</td><td>

Name of the disclosure.

</td></tr><tr><td>

Description

</td><td>

Description of the disclosure.

</td></tr><tr><td>

Type

</td><td>

Type of disclosure. The choices are as follows:-   **Annual report**
-   **ESG report**
-   **Regulatory and framework**
-   **Request for information**
-   **Ratings and indices**
-   **Supplier questionnaire**
-   **Others**
**Note:** If a template is available, the disclosure document is created based on the template. Otherwise a blank document is created.

</td></tr><tr><td>

Owner

</td><td>

User responsible to move the disclosure to different states and perform actions such as synchronizing the disclosure. **Note:** Only users with the sn\_esg.reporting\_disclosure\_manager role can be selected in this field.

</td></tr><tr><td>

Upload to remote storage

</td><td>

Option to decide if the disclosure must be stored on remote storage such Microsoft SharePoint. If this option is selected, the Remote storage section appears on the form.

</td></tr><tr><td>

Data classification

</td><td>

Classification of the disclosure information. The choices are as follows:-   **Public**: Determines if the disclosure will be made public.
-   **Private**: Determines if the disclosure must remain private.


</td></tr><tr><td>

Approvers

</td><td>

Users who must approve the disclosure. **Note:** Only users with the sn\_esg.reporting\_disclosure\_manager role can be selected in this field.

</td></tr><tr><td class="sub-head" colspan="2">

**Remote storage**

</td></tr><tr><td>

Storage type

</td><td>

Location of where the disclosure must be stored. The available option is **Sharepoint**. If this option is selected, a blank document is created.

</td></tr><tr><td>

Document path

</td><td>

Path on Microsoft SharePoint in the user’s home folder. This field appears only when the **Upload to remote storage** option is selected.

</td></tr><tr><td>

Collaborators

</td><td>

Users who contribute to the disclosure document. This field appears only when the **Upload to remote storage** option is selected. **Note:** Only users with the sn\_esg.reporting\_disclosure\_manager role can be selected in this field.

</td></tr></tbody>
</table>4.  To save the disclosure, select **Save**.

    Ensure that the custom properties, Document ID and Disclosure Number of the disclosure documents for a disclosure record are not updated or deleted.

5.  To open and edit the document that is created, **Open document**.

    To insert data points in the document, open the add-in in the Word document. For details, refer to [Import data in to a Microsoft Word disclosure report](import-data-into-ms-word.md). If the link does not open the disclosure, see the [Troubleshooting checklist for narrative disclosures \[KB1702819\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1702819) article in the Now Support Knowledge Base.

6.  Close the document before syncing data.

    Before you perform the next step, wait for one minute for the data to reflect in the tracking table.

7.  Select **Sync disclosure data** to synchronize any modifications made to the disclosure document, ensuring that the changes are reflected on the Overview page under Disclosure summary.

    The **Sync disclosure data** button is only available if the **Storage type** field is set to **Sharepoint**.

8.  To move the disclosure to the next state, select **Move to Work in Progress**.

9.  To request approval from the necessary approvers, select **Request Approval**.


**Parent Topic:**[Disclosures in Operational Sustainability Management \(formerly ESG Management\)](../concept/esg-disclosures.md)

