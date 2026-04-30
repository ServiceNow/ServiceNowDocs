---
title: Properties for Employee Document Management application
description: Activating the Employee Document Management \[com.sn\_employee\_document\_management\] plugin adds the following properties.
locale: en-US
release: yokohama
product: Employee Document Management
classification: employee-document-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Reference - Employee Document Management, Employee Document Management, HR Service Delivery, Employee Service Management]
---

# Properties for Employee Document Management application

Activating the Employee Document Management \[com.sn\_employee\_document\_management\] plugin adds the following properties.

Properties control the behavior of the Employee Document Management application.

For optimal system performance and depending on your internal processes, employee documentation is purged based on the security policy established by your company.

<table id="table_w4v_2nn_bdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_hr\_ef.enable\_document\_viewer \(Enable "Document Viewer" to preview documents\)

</td><td>

Enables document viewer to view documents of type \(.docx, .txt, .png, .xls, and so on\) directly from Employee Document Management.The default value is **Yes**.

**Note:** If **No** is checked, you can still download the document and view it locally.

</td></tr><tr><td>

sn\_hr\_ef.enable\_download\_multiple \(Enable "Download" UI Action to download multiple employee documents in a zip file.\)

</td><td>

Lets you download multiple employee documents from Employee Documents list into a .zip file.The default value is **Yes**.

</td></tr><tr><td>

sn\_hr\_ef.max\_file\_size \(Maximum file upload size in megabytes:\)

</td><td>

The maximum file size of a document you can upload. The default is 30 megabytes.You can change this value, but system performance can be affected.

</td></tr><tr><td>

sn\_hr\_ef.purge\_stride\_length \(The frequency in days that purge dates will be recalculated for Employee documents.\)

</td><td>

Determines the stride value for recalculating the purge dates for employee documents. The stride value determines the range of values that can be assigned to every user \[sys\_user\] record that has associated employee documents.

 For example, if 30 is entered, the range of values that can be randomly assigned is from 1 through 30. When the Refresh Purge Dates for Employee Documents scheduled job runs, based on the current date, it determines the stride value. Any user record assigned that stride value has their employee documents purge date recalculated.

 Also, purge dates are recalculated for employee documents that match the following requirements:

-   Employee document is active.
-   There are no legal holds or purge holds on the employee document.
-   The stride value for the user record matches the stride value for the current date.

 The number you enter determines the stride value range. For example, Entering a 1 indicates that there is no stride range and the purge recalculation is performed for all employee documents daily.

 Entering a larger number ensures that system performance is optimal since large companies can have large amounts of documents.

 The default value is **30** and can be modified.

</td></tr><tr><td>

sn\_hr\_ef.purge\_authorization\_interval \(The number of days before the next month a purge notification is sent \(value between 1-30\):\)

</td><td>

The number of days before the beginning of the month for the purge notification to be sent out. The Purge Notification Daily Job scheduled job uses this value to determine when to send a purge notification or authorization.

 The default value is **7** and can be changed.

</td></tr><tr><td>

sn\_hr\_ef.enable\_purge\_logs \(Enable purge logs to log the files deleted during document purge.\)

</td><td>

Indicates if you want a purge log to be created for deleted documents. A purge log lists all deleted documents with the fields you specify in the **These fields will be included in the purge logs if enabled** field.The default value is **Yes**.

 **Note:** The purge log is created after the Purge employee documents scheduled job runs. This job runs daily by default.

</td></tr><tr><td>

sn\_hr\_ef.purge\_log\_fields\_to\_include \(These fields will be included in the purge logs if enabled.\)

</td><td>

If you checked **Yes** for the **Enable purge logs to log the files deleted during document purge** field, enter the fields you want to appear in the purge logs. Separate the fields with a comma.

 Purge logs can be downloaded into a .csv file.

 The default values are: **employee, hr\_case**.

**Note:** The purge log is created after the Purge employee documents scheduled job runs. This job runs daily by default.

</td></tr></tbody>
</table>**Parent Topic:**[Reference - Employee Document Management](../concept/reference-employee-document-management.md)

**Related topics**  


[Components installed with Employee Document Management](installed-w-employee-doc-mngemnt.md)

