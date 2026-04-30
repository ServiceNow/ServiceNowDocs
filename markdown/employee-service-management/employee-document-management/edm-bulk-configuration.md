---
title: Configuring employee document management bulk import with source document repository
description: Use Employee Document Import Configuration to identify and communicate with the source document repository. The source document repository is where you currently store your employee documents.To import employee documents, map the source employee documents from your local document repository or third-party cloud-based repository to Employee Document Management.Use Employee Document Import Jobs to create a Verify source step. Verify is required to validate the connection between your local directory or your third-party, cloud-based document repository and Employee Document Management. The Verify source step also validates that source employee files are there to be processed.Use Employee Document Import Jobs to create or edit the Stage Directory source step.Use Employee Document Import Jobs to create or edit the stage file source step. Stage file is required to stage your source employee documents from your third-party, cloud-based document repository.Use Employee Document Import Jobs to create or edit the capture source step. Capture is required to import your source employee documents from your local or third-party, cloud-based document repository.
locale: en-US
release: xanadu
product: Employee Document Management
classification: employee-document-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 15
breadcrumb: [Employee document management bulk imports, Using Employee Document Management, Employee Document Management, HR Service Delivery, Employee Service Management]
---

# Configuring employee document management bulk import with source document repository

Use Employee Document Import Configuration to identify and communicate with the source document repository. The source document repository is where you currently store your employee documents.

## Before you begin

Role required: sn\_hr\_ef.admin, sn\_hr\_ef.document\_import

## About this task

Before you can move your employee documents from your source document repository, you must:

-   Identify the type of repository you are pulling documents from.
-   Identify the URL and credentials from the repository you are pulling documents from. Or, identify the directory you are pulling documents from.
-   Test to make sure that there is communication from your source repository and Employee Document Management.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Bulk Import** &gt; **Import Configuration**.

2.  Fill in the fields on the form.

<table id="table_mrq_k1s_cgb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A descriptive name that identifies your employee document bulk upload configuration.

</td></tr><tr><td>

Source type

</td><td>

Identifies the source you are moving employee documents from.-   Local: The source employee document repository is local.
-   URL: The source employee document repository is cloud-based.


</td></tr><tr><td>

Host

</td><td>

Appears when **Local** is selected from **Source type**.

The IP address of the local source employee document repository you are pulling from. When pulling from a local directory, the IP address of the source connected via the MID server.

</td></tr><tr><td>

URL

</td><td>

Appears when **URL** is selected from **Source Type**.The URL of the source third-party, cloud-based document repository.

</td></tr><tr><td>

Directory

</td><td>

The directory in the source employee document repository you are pulling from. For Local source type, you can specify a recursive directory structure.

 For third-party, cloud-based \(URL\) source type, you can only specify the root directory.

 **Note:** If you have multiple directories in your third-party, cloud-based repository, a separate Employee Document Import Configuration is required for each one. Use the **Clone Configuration** button to make cloning easier.

</td></tr><tr><td>

Staging record state

</td><td>

The state assigned to the imported employee document staging records before being inserted into the employee documents. -   Draft: Allows you to verify the staging records prior to inserting into the employee documents.

**Note:** Use the **Draft** state as the default in a testing environment when adjusting your mapping configurations. Employee documents that have a **Draft** state must be changed to **Ready** before the Capture step can process it.

-   Ready: When the staging records for employee documents are accurate and does not require verification, use this state. You can still fix any errors that occur. The state changes to Error when verification cannot be confirmed.

**Note:** Use the Ready state as the default in a production environment after testing ensures that your mapping configurations are error-free. Employee documents in the Ready state process automatically in the Capture step.

</td></tr><tr><td>

Credential alias

</td><td>

The connection and credential alias ID that labels a credential or connection record. The credential alias is required to connect to the local source document repository.The credential alias is configured from the local document repository.

 The credentials to access the local document repository are stored on the instance and tagged with the alias.

</td></tr><tr><td>

Domain

</td><td>

Automatically populated via domain separation and identifies the specific domain you are configuring employee documentation bulk uploads for.

</td></tr><tr><td>

Log mapping

</td><td>

Indicates that you want to write debug statements to the system log during the staging phase. Log mapping provides an easier debugging of mapping. Recommended when first configuring bulk imports during the testing phase.

</td></tr></tbody>
</table>    **Note:** For more information on credentials and aliases, see [Introduction to credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

    For more information on domain separation, see [Domain Separation and HR Service Delivery](../concept/hr-domain-separation.md).

3.  Select **Save**, **Submit**, or **Update**.

    The Employee Document Import Sources and Employee Document Import Map tabs appear.


**Parent Topic:**[Employee document management bulk imports](../concept/edm-bulk-uploads.md)

## Create or edit import configuration

To import employee documents, map the source employee documents from your local document repository or third-party cloud-based repository to Employee Document Management.

### Before you begin

Role required: sn\_hr\_ef.document\_import

### About this task

For a local document repository, name mapping acquires file meta data from the file name.

### Procedure

1.  From **Employee Document Import Configuration** form, click the **Employee Document Import Map** tab.

2.  Click **New** or on an existing import configuration.

3.  Fill in the form.

<table id="table_cmt_nkz_4fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration

</td><td>

The name of the employee document bulk import configuration. See [Configuring employee document management bulk import with source document repository](edm-bulk-configuration.md#).

</td></tr><tr><td>

Mapping type

</td><td>

Defines how you are locating the source employee documents within your source document repository.-   Field: Indicates that within an array of information about your source document you want to identify a specific part of the array to map.
-   Value: Indicates that you are identifying a specific term within an array of information from your source document you want to map.


</td></tr><tr><td>

Regex

</td><td>

The regular expression string that identifies files you want to include from the source repository.For example, \(\\w+\)\_\(\\w+\)\_\(\\w+\).\(\\w+\) matches file names that contain alphanumeric, underscore, and a period. Once you have identified specific parts of information in the array, you can then map it.

 The more consistent your existing naming convention, the easier to locate your employee documents from your source repository,

</td></tr><tr><td>

Replace

</td><td>

The information you want the source employee document to contain when imported to Employee Document Management. For example, the array for your source employee document has school. You want the new value to equal transcripts for document type. Enter:

-   Replace: transcripts
-   Mapped element: docType
-   Source element: school
**Note:** You can also use regular expressions \(RegEx\) to define the replacement value. When using RegEx, use a regular expression test site to ensure correct parsing.

</td></tr><tr><td>

Mapped element

</td><td>

Determines what meta data field is acquired and the value included in the final staging record created.Fields from the Import Document Staging \[sn\_hr\_ef\_import\_staging\] table that you want to map your source employee documents to.

 The base system provides the following fields you can map your source employee documents to:

-   docType: Document type
-   fileName: File name
-   employee: Employee name


</td></tr><tr><td>

Source element

</td><td>

The field or value from a local or third-party cloud-based employee document repository you want to map to Employee Document Management.For example, if your source file name contains the employee name, you can use the employee name as the source element and use the Mapped element of employee.

</td></tr><tr><td>

Filter regex

</td><td>

A regular expression sequence that matches text found in the array from your source employee document repository. Use this field to refine your identification of source employee documents.

</td></tr><tr><td>

Filter field

</td><td>

Locates specific text found in the array of information returned from the source repository when files matching the Regex are imported. **Note:** You can also use regular expressions \(RegEx\) to define the replacement value. When using RegEx, use a regular expression test site to ensure correct parsing.

 Use this field to help refine the information you want mapped.

 For example, to import only files with a file name formatted first\_last\_xxx.pdf \(abel\_tuter\_tuition.pdf\):

-   Regex: \(\\w+\)\_\(\\w+\)\_\(\\w+\).\(\\w+\)
-   Mapped element: fileName
-   Source element: fileName
-   Filter field: .pdf


</td></tr></tbody>
</table>    -   **File name example**

        The example file name is abel\_tuter\_tuition.pdf.

        To find and extract the file name from the source repository, see this example:

        ![Import Map — File name](../image/import-map-filename.png)

        The import map is looking for a source element called fileName.

        The import map is going to translate this source element to a mapped element called fileName.

        The Regex is looking for the format of the file name first\_last\_xxx.pdf.

    -   **File name to employee name example**

        From the file name, the employee name is extracted. Employee name is a requirement for Employee Document Management.

        ![Import Map — Employee Name](../image/import-map-employee.png)

        The import map is looking for a source element called fileName.

        The import map is going to translate this source element to a mapped element called employee.

        The Regex is looking for the format of the file name to be first\_last\_tuition.pdf \(\\w+\)\_\(\\w+\)\_\(\\w+\).\(\\w+\).

        It replaces the original file name with first.last \($1.$2\)

    -   **File name to document type example**

        From the file name, the document type is extracted. Document type is a requirement for Employee Document Management.

        ![Import Map — docType](../image/import-map-doctype.png)

        The import map is looking for a source element called fileName.

        The import map is going to translate this source element to a mapped element called docType.

        The Regex is looking for the format of the file name to be first\_last\_tuition.pdf \(\\w+\)\_\(\\w+\)\_\(\\w+\).\(\\w+\).

        It creates a docType of tuition \($3\).

4.  Click **Submit** or **Update**.


## Create or edit the verify source step

Use Employee Document Import Jobs to create a Verify source step. Verify is required to validate the connection between your local directory or your third-party, cloud-based document repository and Employee Document Management. The Verify source step also validates that source employee files are there to be processed.

### Before you begin

Role required: sn\_hr\_ef.admin, sn\_hr\_ef.document\_import

### About this task

The base system provides a sample Verify source step you can use as a model.

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Import Configuration**.

2.  Click an existing Import Configuration record.

3.  From the Employee Document Import Source tab, click an existing Verify source step or **New**.

4.  Fill in or edit the form.

<table id="table_oz3_53c_2gb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration

</td><td>

A descriptive name that identifies your employee document bulk upload configuration.

</td></tr><tr><td>

Source step

</td><td>

The import step that makes up the import job. Select Verify.Verify: Ensures the connection between the Employee Document instance and source repository \(third-party cloud-based or local\) is configured correctly and can communicate.

</td></tr><tr><td>

Import type

</td><td>

The import type that drives the source step. You can select the method that drives the source step. -   Sub flow: A workflow launched by another workflow to drive the import step. See [Workflows used as subflows](https://www.servicenow.com/docs/access?context=workflows-as-subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
-   Flow action: The Flow Designer action that drives the import step. See [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).
-   Workflow: An automated way to provide a multi-step process. See [Workflow](https://www.servicenow.com/docs/access?context=c_WorkflowOverview&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
-   Script: Use to automate the import step. See [Scripts](https://www.servicenow.com/docs/access?context=c_Script&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).


</td></tr><tr><td>

Application

</td><td>

The application the import source is used in.

</td></tr><tr><td>

Domain

</td><td>

Automatically populated via domain separation and identifies the specific domain you are configuring employee documentation bulk uploads for.

</td></tr><tr><td>

Sub FlowAction

 Workflow

 Script

</td><td>

The subflow, flow action, workflow, or script that launches the source step based on the import type. For example, if you are using Flow Action as your Import type, the Action drop-down appears to select the action you previously created.

</td></tr></tbody>
</table>5.  Click **Submit** or **Update**.

6.  Click the **Start verify configuration** related link to start the verify job.

    The **Employee Document Import Jobs** tab appears with the Verify job in the **Queued** state.

7.  Reload the form to see if the import step validated.

    Validated indicates that the credentials are correct, the directory is valid, and shows the number of source employee files found in the directory.


## Create or edit the stage directory lookup source step

Use Employee Document Import Jobs to create or edit the Stage Directory source step.

### Before you begin

Role required: sn\_hr\_ef.admin, sn\_hr\_ef.document\_import

### About this task

Stage directory is required to locate your source employee documents from your local or third-party, cloud-based document repository. This step also uses the mapping to parse file names and create a record in the staging table for each of the files with the parsed data.

The base system provides a sample Stage - Directory source step you can use as a model.

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Import Configuration**.

2.  Click an existing Import Configuration record.

3.  From the Employee Document Import Source tab, click an existing Stage - Directory source step or **New**.

4.  Fill in or edit the form.

<table id="table_oz3_53c_2gb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration

</td><td>

A descriptive name that identifies your employee document bulk upload configuration. The name comes from the Employee Document Import Configuration. See [Configuring employee document management bulk import with source document repository](edm-bulk-configuration.md#).

</td></tr><tr><td>

Source step

</td><td>

The import step that makes up the import job. Select Stage - Directory.Stage — Directory: Ensures that the employee documents from the source repository are located and mapped correctly.

</td></tr><tr><td>

Import type

</td><td>

The import type that drives the source step. You can select the method that drives the source step. -   Sub flow: A workflow launched by another workflow to drive the import step. See [Workflows used as subflows](https://www.servicenow.com/docs/access?context=workflows-as-subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
-   Flow action: The Flow Designer action that drives the import step. See [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).
-   Workflow: An automated way to provide a multi-step process. See [Workflow](https://www.servicenow.com/docs/access?context=c_WorkflowOverview&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
-   Script: Use to automate the import step. See [Scripts](https://www.servicenow.com/docs/access?context=c_Script&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).


</td></tr><tr><td>

Application

</td><td>

The application the import source is used in.

</td></tr><tr><td>

Domain

</td><td>

Automatically populated via domain separation and identifies the specific domain you are configuring employee documentation bulk uploads for.

</td></tr><tr><td>

Sub FlowAction

 Workflow

 Script

</td><td>

The subflow, flow action, workflow, or script that launches the source step based on the import type. For example, if you are using Flow Action as your Import type, the Action drop-down appears to select the action you previously created.

</td></tr></tbody>
</table>5.  Click **Submit** or **Update**.


## Create or edit the stage file source step

Use Employee Document Import Jobs to create or edit the stage file source step. Stage file is required to stage your source employee documents from your third-party, cloud-based document repository.

### Before you begin

Role required: sn\_hr\_ef.admin, sn\_hr\_ef.document\_import

### About this task

The base system provides a sample Stage - File source step you can use as a model.

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Import Configuration**.

2.  Click an existing Import Configuration record.

3.  From the Employee Document Import Source tab, click an existing Stage - File source step or **New**.

4.  Fill in or edit the form.

<table id="table_oz3_53c_2gb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration

</td><td>

A descriptive name that identifies your employee document bulk upload configuration. The name comes from the Employee Document Import Configuration. See [Configuring employee document management bulk import with source document repository](edm-bulk-configuration.md#).

</td></tr><tr><td>

Source step

</td><td>

The import step that makes up the import job. Select Stage - File.Stage — File: Ensures that the employee documents from the source repository are located and mapped correctly.

</td></tr><tr><td>

Import type

</td><td>

The import type that drives the source step. You can select the method that drives the source step. -   Sub flow: A workflow launched by another workflow to drive the import step. See [Workflows used as subflows](https://www.servicenow.com/docs/access?context=workflows-as-subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
-   Flow action: The Flow Designer action that drives the import step. See [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).
-   Workflow: An automated way to provide a multi-step process. See [Workflow](https://www.servicenow.com/docs/access?context=c_WorkflowOverview&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
-   Script: Use to automate the import step. See [Scripts](https://www.servicenow.com/docs/access?context=c_Script&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).


</td></tr><tr><td>

Application

</td><td>

The application the import source is used in.

</td></tr><tr><td>

Domain

</td><td>

Automatically populated via domain separation and identifies the specific domain you are configuring employee documentation bulk uploads for.

</td></tr><tr><td>

Sub FlowAction

 Workflow

 Script

</td><td>

The subflow, flow action, workflow, or script that launches the source step based on the import type. For example, if you are using Flow Action as your Import type, the Action drop-down appears to select the action you previously created.

</td></tr></tbody>
</table>5.  Click **Submit** or **Update**.

6.  Click the **Start staging job** related link.

    The staging job verifies that the source document directory and source files can be staged. The **Employee Document Import Jobs** tab appears with the Stage import step in the **Queued** state.

7.  Reload the form to see if the Stage import step completed.

    The **Employee Document Staging** tab appears. You can view all source documents that are in the staging table and make corrections if necessary. See [Correcting employee documents in the staging table](edm-doc-staging.md).

8.  Change staged documents that have a state of **Draft** to **Ready**.

    Staged documents must be in **Ready** state for it to be picked up in the **Capture** step. You can change the state by checking all staged documents that have a **Draft** state and selecting **Ready for import** from **Action on selected rows** or opening a specific staged document and selecting **Ready for Import**.


## Create or edit capture source step

Use Employee Document Import Jobs to create or edit the capture source step. Capture is required to import your source employee documents from your local or third-party, cloud-based document repository.

### Before you begin

Role required: sn\_hr\_ef.admin, sn\_hr\_ef.document\_import

### About this task

The base system provides a sample Capture source step you can use as a model. The example for the local document repository provides a sample script that can be used.

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Import Configuration**.

2.  Click an existing Import Configuration record.

3.  From the Employee Document Import Source tab, click an existing Capture source step or **New**.

4.  Fill in or edit the form.

<table id="table_oz3_53c_2gb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration

</td><td>

A descriptive name that identifies your employee document bulk upload configuration. The name comes from the Employee Document Import Configuration. See [Configuring employee document management bulk import with source document repository](edm-bulk-configuration.md#).

</td></tr><tr><td>

Source step

</td><td>

The import step that makes up the import job. Select Verify.

 Capture: Ensures that the employee documents from the source repository are imported to Employee Document Management.

</td></tr><tr><td>

Import type

</td><td>

The import type that drives the source step. You can select the method that drives the source step. -   Sub flow: A workflow launched by another workflow to drive the import step. See [Workflows used as subflows](https://www.servicenow.com/docs/access?context=workflows-as-subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
-   Flow action: The Flow Designer action that drives the import step. See [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).
-   Workflow: An automated way to provide a multi-step process. See [Workflow](https://www.servicenow.com/docs/access?context=c_WorkflowOverview&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
-   Script: Use to automate the import step. See [Scripts](https://www.servicenow.com/docs/access?context=c_Script&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).


</td></tr><tr><td>

Application

</td><td>

The application the import source is used in.

</td></tr><tr><td>

Domain

</td><td>

Automatically populated via domain separation and identifies the specific domain you are configuring employee documentation bulk uploads for.

</td></tr><tr><td>

Sub FlowAction

 Workflow

 Script

</td><td>

The subflow, flow action, workflow, or script that launches the source step based on the import type. For example, if you are using Flow Action as your Import type, the Action drop-down appears to select the action you previously created.

</td></tr></tbody>
</table>5.  Click **Submit** or **Update**.

    Run the Capture job after the Verify configuration and Staging jobs have run successfully.

6.  Click the **Start capture job** related link.

    The capture job imports the source documents into Employee Document Management. The **Employee Document Import Jobs** tab appears with the Stage import step in the **Queued** state.

7.  Reload the form to see if the Stage import step completed and have a state of **Complete**.


