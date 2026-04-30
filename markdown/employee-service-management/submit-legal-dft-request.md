---
title: Submit a digital forensic request
description: Submit a legal request to access data of current or former employees for internal investigation or litigation reasons.Add a custodian and related data source details in your digital forensic request.Add a non-custodial data and related search source details in your digital forensic request.Upload a Microsoft Excel or CSV file containing custodial and non-custodial data to quickly add multiple records in a digital forensic request in one go.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Requests, Legal Digital Forensics, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Submit a digital forensic request

Submit a legal request to access data of current or former employees for internal investigation or litigation reasons.

## Before you begin

Role required: sn\_lg\_ops.legal\_user

## Procedure

1.  Navigate to **All** &gt; **Employee Center**.

    **Note:** If you are using Legal Service Portal, you can submit a legal request by navigating to the Legal Service Portal portal and selecting a request from the **Service Catalog**.

2.  Select **Legal services** from the header.

3.  Select **Browse Legal services**.

4.  Search for the digital forensic request item.

5.  Click **Digital Forensic Request**.

6.  On the form, fill in the fields.

<table id="table_DFT_request_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add this request to

</td><td>

Option to associate the legal request with an existing legal matter or to a new legal matter.-   **Existing matter**: Option to associate the legal request with an existing legal matter.

Only current legal matters that you have permission to access appear in the list.

-   **New matter**: Option to create a new legal matter and associate the legal request with it.


</td></tr><tr><td>

Existing matter

</td><td>

List of existing legal matters to associate with the legal request.Only current legal matters that you have permission to access appear in the list.

 This field appears only when the **Existing matter** option is selected.

</td></tr><tr><td>

Name of new matter

</td><td>

Name of the new legal matter.This field appears only when the **New matter** option is selected.

</td></tr><tr><td>

Activity request

</td><td>

Short description of the request.

</td></tr><tr><td>

Detailed description

</td><td>

Detail information of the request, for example, details of the suspicious activities by the custodians or details of the litigation.

</td></tr><tr><td>

Custodial data

</td><td>

Employees on whose data you are requesting the investigation. Also provide other investigation details for a custodian—search keywords, data sources, and search period.For more information, see [Add a custodian to a digital forensic request](submit-legal-dft-request.md#).

</td></tr><tr><td>

Non-custodial data

</td><td>

Resources and assets, such as server, laptop, mobile, or cloud storage, on which you are requesting the investigation. Also provide other investigation details for a non-custodian—search keywords, data sources, and search period.For more information, see [Add a non-custodial data to a digital forensic request](submit-legal-dft-request.md#).

</td></tr><tr><td>

Bulk upload

</td><td>

Export multiple custodian and non-custodial data from a file.For more information on uploading the data from a file, see [Add custodial and non-custodial data from a file](submit-legal-dft-request.md#).

</td></tr><tr><td>

Activities requested

</td><td>

Type of actions required on the data for the investigation.-   Preserve: Secure the original data from the source devices in compliance with departmental guidelines to protect and preserve the evidence.
-   Collect: Acquire the digital evidence that may be relevant to the investigation. Collection might involve activities such as imaging storage devices, or copying or printing of the digital information.
-   Review: Conduct an in-depth, systematic examination of the facts in the collected digital evidence related to the investigation.
-   Present: Document and present the relevant information and findings of the examination in an appropriate format to stakeholders.


</td></tr><tr><td>

Third party reference ID

</td><td>

Reference to a legal matter ID stored in your other matter management system.

</td></tr><tr><td>

Third party reference system

</td><td>

Reference to your other matter management system.

</td></tr><tr><td>

Preferred completion date and time

</td><td>

Date by which the investigation must be complete. The date and time is based on the time zone you are in while requesting.

</td></tr></tbody>
</table>7.  Click **Submit**.


## Result

-   A digital forensic request is created in the New state.
-   The Standard Ticket page displays that has the following tabs to perform different tasks:
    -   Activity: Track the activity history of the request and post messages for the fulfiller working on the request.
    -   Attachments or Documents: Upload and manage the documents in the legal request.

        **Note:** If the external storage option is enabled, the **Documents** tab is displayed. Otherwise, the **Attachments** tab is displayed.

    -   Custodial data: View existing custodial details. You can also export the data to a file.
    -   Non-custodial data: View existing non-custodial details. You can also export the data to a file.
    -   Request Details: Review request details.
-   If you [uploaded custodial and non-custodial data from an Excel or CSV file](submit-legal-dft-request.md#), the file is attached as a reference document to the request.

    The number of records successfully uploaded from the file into the request is posted as additional comments in the Activity tab on the Standard Ticket page.

    If a record from the file isn't added to the request, an error log file is added in the Activity tab. You can review the reason for failure in the error log file, fix the errors in your file, and upload it again by [editing the request](modify-legal-dft-request.md).

-   For each custodian added in the request, a record is created in the Custodial Data \[sn\_lg\_forensics\_custodial\_data\] table. If a legal profile record for each custodian is not already present in the Legal Profile \[sn\_lg\_ops\_legal\_profile\] table, a corresponding record is created.
-   For each non-custodial data added in the request, a record is created in the Non Custodial Data \[sn\_lg\_forensics\_non\_custodial\_data\] table.

## What to do next

On the Standard Ticket page, you can update request details, add comments, manage custodial and non-custodial data, upload supporting documents, or cancel the request. For more information, see [Update a submitted digital forensic request](modify-legal-dft-request.md).

Any member from the digital forensic team can triage and assign the request to themselves or to any other member in the group. Once the request is assigned, an approval flow is triggered. The flow creates an approval record for each custodial and non-custodial added in the digital forensic request. These approval records are assigned to the privacy team in the legal department. Any member from the legal privacy team can approve the request. After the approval, a digital forensic team member to whom the legal request is assigned can start working on the request. For more information, see [Work on a digital forensic request](work-on-legal-dft-request.md).

**Note:**

The approval details appear under the **Approvals** tab on the Standard Ticket page.

**Parent Topic:**[Submitting digital forensics requests](../concept/submitting-legal-dft-request.md)

## Add a custodian to a digital forensic request

Add a custodian and related data source details in your digital forensic request.

### Before you begin

Role required: sn\_lg\_ops.legal\_user

### Procedure

1.  On the Digital Forensic Request intake form, in the Custodial data section, click **Add**.

2.  On the Add Row dialog box, fill in the fields.

<table id="table_custo_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Custodian name

</td><td>

Name of the custodian on whose digital assets you are requesting a digital forensic investigation.

</td></tr><tr><td>

Data source

</td><td>

Source \(hardware or software\) from which the data for investigation is to be collected.

</td></tr><tr><td>

Other data sources

</td><td>

Source \(hardware or software\), not listed in the **Data source** field, from which the data for investigation is to be collected.This field appears only when **Other** is selected from **Data source**.

</td></tr><tr><td>

Keywords

</td><td>

Terms to look for within the data collected from the custodian data sources.You can provide multiple search terms each separated by a comma.

</td></tr><tr><td>

Filter start date

</td><td>

Start date of the digital forensics investigation period. The digital forensic team member would check for the search terms in the data from this date onwards.

</td></tr><tr><td>

Filter end date

</td><td>

End date of the digital forensics investigation period. The digital forensic team member would check for the search terms in the data until this date.

</td></tr><tr><td>

Additional information

</td><td>

Additional details about the custodial data that would be helpful in resolving the request.

</td></tr></tbody>
</table>3.  Click **Add**.

    The custodian record appears in the Custodial data list on the Digital Forensic Request intake form.


## Add a non-custodial data to a digital forensic request

Add a non-custodial data and related search source details in your digital forensic request.

### Before you begin

Role required: sn\_lg\_ops.legal\_user

### Procedure

1.  On the Digital Forensic Request intake form, in the Non-custodial data section, click **Add**.

2.  On the Add Row dialog box, fill in the fields.

<table id="table_non_custo_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Non-custodial details

</td><td>

Details of the non-custodial data on which you are requesting a digital forensic investigation. For example, you can enter details such as model number, serial number, or product name of the non-custodial data.

</td></tr><tr><td>

Data source

</td><td>

Source from which the data for investigation is to be collected.

</td></tr><tr><td>

Other data sources

</td><td>

Source \(hardware or software\), not listed in the **Data source** field, from which the data for investigation is to be collected.This field appears only when **Other** is selected from **Data source**.

</td></tr><tr><td>

Search location/File path

</td><td>

Location of the folder or file from where the data for investigation is to be collected. For example, a URL on a cloud storage or a folder or file in a system.

</td></tr><tr><td>

Keywords

</td><td>

Terms to look for within the data collected from the data sources.You can provide multiple search terms each separated by a comma.

</td></tr><tr><td>

Filter start date

</td><td>

Start date of the digital forensics investigation period. The digital forensic team member would check for the search terms in the data from this date onwards.

</td></tr><tr><td>

Filter end date

</td><td>

End date of the digital forensics investigation period. The digital forensic team member would check for the search terms in the data until this date.

</td></tr><tr><td>

Additional information

</td><td>

Additional details about the non-custodial data that would be helpful in resolving the request.

</td></tr></tbody>
</table>3.  Click **Add**.

    The non-custodial record appears in the Non-custodial data list on the Digital Forensic Request intake form.


## Add custodial and non-custodial data from a file

Upload a Microsoft Excel or CSV file containing custodial and non-custodial data to quickly add multiple records in a digital forensic request in one go.

### Before you begin

Role required: sn\_lg\_ops.legal\_user

### About this task

Use a file with a predefined format available on the digital forensics request page to upload custodial and non-custodial data.

### Procedure

1.  Download the template file with the predefined columns and add custodial and non-custodial details.

    1.  Click the **Download an upload template here** link to download the Excel file template.

        The template file contains sample records for custodial and non-custodial data. During import, the columns marked as Not applicable in the file are ignored.

    2.  Review the sample data in the downloaded Excel file and add custodial and non-custodial details in the same format, and then save.

2.  On the Digital Forensic Request intake form, in the Bulk Upload section, click **Upload**.

3.  Browse and select the Excel file containing the custodial and non-custodial data.

    The file is attached to the request. The data from the file is uploaded into the request when you submit the request.


