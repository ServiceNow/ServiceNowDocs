---
title: Export SAP SuccessFactors Learning data for external content indexing
description: Export user, library and assignment, and training item data from your SAP SuccessFactors Learning environment. The SAP SuccessFactors external content connector needs this exported data to index your content and user permissions for search.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/export-sap-successfactors-data-external-content-indexing.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-06-02"
reading_time_minutes: 7
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [SAP SuccessFactors external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Export SAP SuccessFactors Learning data for external content indexing

Export user, library and assignment, and training item data from your SAP SuccessFactors Learning environment. The SAP SuccessFactors external content connector needs this exported data to index your content and user permissions for search.

## Before you begin

You need a non-production SAP SuccessFactors Learning environment configured to include the Learning Report Designer tool. To learn how to request Learning Report Designer configuration in a non-production environment, see the [2171592 - Process to enable the use of Plateau Report Designer \(PRD\) on Learning](https://userapps.support.sap.com/sap/support/knowledge/en/2171592) SAP support resource.

**Note:** Many SAP resources still refer to the Learning Report Designer using its legacy name, Plateau Report Designer.

In both the non-production SAP SuccessFactors Learning environment and the environment that you want the connector to retrieve data from, you need administrator accounts with the following report permissions:

-   Edit Report
-   Import/Export Reports
-   Publish/Unpublish Reports
-   Run \[report title\] Report
-   Run Unpublished Reports
-   Search Reports
-   View Report Query

For details on these report permissions in SAP SuccessFactors Learning, see the [Report Permissions](https://help.sap.com/docs/successfactors-learning/managing-sap-successfactors-learning-for-administrators/report-permissions) SAP Help Portal resource.

In the non-production SAP SuccessFactors Learning environment that has Learning Report Designer enabled, your administrator account needs the REPORT\_DEVELOPER role. For details on adding this role to an administrator account, see the [Setting up a Plateau Report Designer Account](https://help.sap.com/docs/successfactors-learning/managing-sap-successfactors-learning-for-administrators/setting-up-plateau-report-designer-account) SAP Help Portal resource.

The Learning Report Designer tool must be downloaded, installed on a Windows workstation with a 32-bit Java Runtime Environment \(JRE\), and configured to connect to your non-production SAP SuccessFactors Learning environment. To learn about these procedures, see the [Downloading Learning Report Designer](https://help.sap.com/docs/successfactors-learning/managing-sap-successfactors-learning-for-administrators/downloading-learning-report-designer) SAP Help Portal resource.

Role required: none

## About this task

Unlike most other external content connectors, the SAP SuccessFactors connector doesn't retrieve content and metadata directly from your source system.

Instead, the SAP SuccessFactors external content connector retrieves user, library and assignment, and training item data from three comma-separated value \(CSV\) files. These CSV data files are generated using custom reports that you run in your SAP SuccessFactors Learning environment. Your connector administrator needs these generated CSV data files to configure the SAP SuccessFactors external content connector.

Perform these steps to import the custom reports into your SAP SuccessFactors Learning environment and generate the three CSV data files required by the SAP SuccessFactors connector.

## Procedure

1.  On your Windows workstation that has Learning Report Designer installed, download the three custom report ZIP archive files attached to the [External Content Connector \(XCC\) for SAP SuccessFactors - Attach report SQL \[KB3047950\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3047950) article in the Now Support Knowledge Base.

2.  Start Learning Report Designer and use it to edit the SQL query for one of the three downloaded custom reports.

    1.  Navigate to **File** &gt; **Open File…**, then open the `Users_custom_report` report from the `Users_custom_report.zip` custom report ZIP archive file.

        To learn about opening a report in Learning Report Designer, see "Updating a System Report in Report Designer" steps 2–8 in the [Using Plateau Report Designer](https://help.sap.com/docs/SUPPORT_CONTENT/lm/3354618691.html) SAP Help Portal resource.

    2.  In the Data Explorer panel, expand the **Data Sets** section and double-click \(or use the keyboard shortcut\) to open the data set associated with the custom report query.

    3.  In the query editor, find this clause in the custom report's SQL query:

        ```sql
        (SELECT User_value
        FROM PA_STUD_USER c
        WHERE a.STUD_ID = c.STUD_ID (+)
        AND c.col_num = 10) as "Custom Column 10"
        ```

3.  In the Learning Report Designer query editor, edit the SQL query clause from the preceding step to reference the user mapping column for your SAP SuccessFactors Learning environment.

    Your user mapping column is the column with values that uniquely identify each user in your SAP SuccessFactors Learning environment. Values in this column might contain user IDs, email addresses, or some other uniquely identifying information.

    The SAP SuccessFactors connector uses values from your user mapping column to map users from your source system to users in your ServiceNow AI Platform® instance. This mapping is needed to preserve user access permissions for content indexed from your SAP SuccessFactors Learning environment.

    Your user mapping column may be a predefined column from the PA\_STUDENT table, such as EMAIL\_ADDR, or a custom column from the PA\_STUD\_USER table.

    -   If your user mapping column is a predefined column from the PA\_STUDENT table, replace the entire clause shown in the preceding step with this clause:

        ```sql
        a.EMAIL_ADDR AS "Email Address"
        ```

        Change the column name and alias in this clause to match your user mapping column. As an example, if your user mapping column is PA\_STUDENT.STUD\_ID, change the clause to refer to that column:

        ```sql
        a.STUD_ID AS "Student ID"
        ```

    -   If your user mapping column is a custom column from the PA\_STUD\_USER table, change the column number in the `c.col_num = 10` condition and the `"Custom Column 10"` alias to match the column number of your custom column. As an example, if your user mapping column is a custom column with column number 20, change the last line of the clause to `AND c.col_num = 20) as "Custom Column 20"`.
4.  Use Learning Report Designer to save the modified custom report.

    1.  Select **Save**.

    2.  In the Outline panel, select the modified report name, then select the **Zip** icon.

    3.  Save the modified report to the Workspace as a ZIP archive.

5.  Replace the downloaded `Users_custom_report.zip` custom report ZIP archive file with the modified copy that you saved in the preceding step.

6.  Use your administrator credentials to log in to the SAP SuccessFactors Learning environment that you want the connector to retrieve trainings data for.

7.  Import the custom reports from the downloaded and updated ZIP archives.

    For details on importing reports into your SAP SuccessFactors Learning environment, see the [Importing Reports](https://help.sap.com/docs/successfactors-learning/managing-sap-successfactors-learning-for-administrators/importing-reports) SAP Help Portal resource.

    Importing a report automatically grants you the Run \[report title\] Report permission for that report.

8.  Make the imported custom reports accessible to other users in your SAP SuccessFactors Learning environment.

    **Note:** This step is only required if you want the reports to be run by users other than the user who imported them. If you will run the custom reports from your administrator account, skip to the next step.

    1.  Publish the imported custom reports.

        Publishing a report makes it available to users who can access the report and who have the Run \[report title\] Report permission. Unpublished reports are only available to users who satisfy these conditions and who have the Run Unpublished Reports permission.

        To learn how to publish a SAP SuccessFactors Learning report, see the [Publishing a Report](https://help.sap.com/docs/successfactors-learning/managing-sap-successfactors-learning-for-administrators/publishing-report) SAP Help Portal resource.

    2.  For each of the imported custom reports, grant the Run \[report title\] Report permission to all users who will run the report.

        For details on the Run \[report title\] Report permission in SAP SuccessFactors Learning, see the [Report Permissions](https://help.sap.com/docs/successfactors-learning/managing-sap-successfactors-learning-for-administrators/report-permissions) SAP Help Portal resource.

9.  In SAP SuccessFactors Learning, run each of the imported custom reports, specifying CSV as the report format.

    To learn how to run a SAP SuccessFactors Learning report, see the [Running Reports in Learning](https://help.sap.com/docs/successfactors-learning/managing-sap-successfactors-learning-for-administrators/running-reports-in-learning) SAP Help Portal resource.


## Result

The custom reports generate CSV files that include current user data, library data, assignment data, and training item data from your selected SAP SuccessFactors Learning environment.

**Note:** The SAP SuccessFactors external content connector can't accept CSV data files that exceed the maximum attachment size specified by the value of the **com.glide.attachment.max\_size** system property. By default, this property limits the size of attachments to 1 Gb or less. For details on configuring this system property, see [Maximum allowed attachment size](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-max-allowed-attachment-size.md).

## What to do next

Provide the three CSV data files that you generated in step [9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/export-sap-successfactors-data-external-content-indexing.md) to your connector administrator.

Your connector administrator needs these three files to configure a SAP SuccessFactors external content connector to retrieve trainings from your SAP SuccessFactors Learning source system.

For details on creating and configuring a SAP SuccessFactors external content connector, see [Create a SAP SuccessFactors external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-ext-cont-connector-sap-successfactors.md).

**Note:** To update the user, library and assignment, and training item data available to the SAP SuccessFactors external content connector, repeat step [9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/export-sap-successfactors-data-external-content-indexing.md) and provide the three updated CSV data files to your connector administrator. To learn how to update the connector configuration to read these files, see [Update CSV data files for a SAP SuccessFactors external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/update-data-files-sap-successfactors-external-content-connector.md).

**Parent Topic:**[SAP SuccessFactors external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/sap-successfactors-external-content-connector.md)

