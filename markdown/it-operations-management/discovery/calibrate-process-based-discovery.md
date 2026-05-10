---
title: Calibrate fingerprint-based discovery
description: Fine-tune discovering applications based on processes, if the discovery results are not satisfactory.Fingerprint-based discovery relies on Predictive Intelligence for generating suggestions for discovery. If the Application Fingerprints dashboard does not display any suggestions, ensure that the Predictive Intelligence is configured correctly.Adjust definitions of process-based suggestions before starting discovery. Typically, you need to fine-tune automatically generated suggestions if the accuracy is less than 100%. Predictive Intelligence creates suggestions and provides the accuracy estimate for each suggestion. The lack of accuracy may result in the failure to discover required applications or the discovery of wrong applications in addition to the correctly discovered applications.Fine-tune the regular expression in the classifier rule to make discovery results more precise. Predictive Intelligence extracts regular expressions from processes and assigns them to classifier rules as part of creating suggestions. If you are not satisfied with the discovery results or the suggestion accuracy is lower than 100%, modify the regular expression.By default, the fingerprint-based discovery is enabled. Disable application discovery based on processes, if Predictive Intelligence does not generate enough processes.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Discover applications based on fingerprints, Running discoveries in your network, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Calibrate fingerprint-based discovery

Fine-tune discovering applications based on processes, if the discovery results are not satisfactory.

Modify default settings for fingerprint-based discovery if this feature does not generate any suggestions or does not generate. In addition, you may also fine-tune the generated suggestions to make them relevant and useful.

## Ensure that the fingerprint-based discovery generates suggestions

Fingerprint-based discovery relies on Predictive Intelligence for generating suggestions for discovery. If the **Application Fingerprints** dashboard does not display any suggestions, ensure that the Predictive Intelligence is configured correctly.

### Before you begin

Confirm that fingerprint-based discovery remains enabled, since it is enabled by default. To verify, navigate to **All** &gt; **System Properties** &gt; **All Properties**. Check that the **sys\_property process.clustering.appfingerprint.enabled** property does not appear on the list.

Role required: discovery\_admin

### About this task

If the **Application Fingerprints** dashboard does not display any suggestions, perform the following steps. After every action, check if the issue persists.

### Procedure

1.  Ensure that Predictive Intelligence is installed and active.

    1.  Navigate to **System Definition** &gt; **Plugins**.

    2.  Search for **Predictive Intelligence**.

    3.  Verify that the Predictive Intelligence plugin is installed.

        ![Checking the Predictive Intelligence plugin status](../image/pi-installed.png)

        If Predictive Intelligence is not installed, click the **Install** button.

    4.  Click the **Predictive Intelligence** tile.

    5.  On the Predictive Intelligence form, verify that the **Status** is **Active**.

        If the status is **Inactive**, click the **Activate/Repair** link under **Related Links**.

2.  Ensure that the scheduled job controlling the fingerprint-based discovery, is enabled and configured correctly.

    1.  Navigate to **System Definition** &gt; **Scheduled Jobs**.

    2.  Select the **Applications suggestion - ITOM Autodisco** scheduled job from the list.

    3.  Ensure that the **Active** check box is selected.

    4.  Check that the discovery frequency is set to one hour as shown in the following example:

        ![Ensuring that the scheduled job for the fingerprint-based discovery is active](../image/fingerprint-based-scheduled-job-active.png)

3.  Check that the clustering solution responsible for grouping processes into suggestions is active.

    1.  Enter `ml_solution.list` in the **Filter navigator** field of the **Navigation** panel.

        The **ML Solutions** tab displays all solutions, including clustering solutions.

    2.  Identify clustering solutions by checking the **Table** column.

        The system saves clustering solutions in the Virtual running processes \[v\_cmdb\_running\_process\] table.

    3.  If there are several clustering solutions, identify the latest solution by the timestamp in the **Update** column.

        Alternatively, you can use the number that the system appends to the solution name to identify the latest solution.![Identifying the latest clustering solution by appended number in the name.](../image/pi-clustering-solution-identification.png)

    4.  Verify that the **State** value is **Solution Complete** and **Progress** is at **100%**.

        ![Verify that the clustering solution is active.](../image/pi-clustering-solution.png)

    5.  If the State value is not Solution Complete, configure Predictive Intelligence as described in [Configuration tips for Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/troubleshooting-predictive-intelligence.md).

4.  Check that the clustering solution created enough process groups, which become suggestions.

    1.  Navigate to **System Definition** &gt; **Tables** and locate the Virtual running processes \[v\_cmdb\_running\_process\] table.

    2.  Check that there are more than 1000 records in this table.

    3.  If there are less than 1000 processes, discover more processes by running horizontal discovery on additional IP ranges or subnets.

    4.  If there are still less than 1000 processes after discovering additional IP ranges or subnets, [disable the fingerprint-based discovery](calibrate-process-based-discovery.md#).

5.  Check that the **Application suggestion - ITOM Autodisco** transaction is not slow-loading, as described in [View and kill active transaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/platform-performance/t_ViewAndKillAnActiveTransaction.md).

    If this transaction is running for a long time, kill it.


## Fine-tune suggestions for fingerprint-based discovery

Adjust definitions of process-based suggestions before starting discovery. Typically, you need to fine-tune automatically generated suggestions if the accuracy is less than 100%. Predictive Intelligence creates suggestions and provides the accuracy estimate for each suggestion. The lack of accuracy may result in the failure to discover required applications or the discovery of wrong applications in addition to the correctly discovered applications.

### Before you begin

Role required: discovery\_admin

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Home**.

2.  Select **Application Fingerprints**.

    The **Application Fingerprints** dashboard opens.

3.  Navigate to the list of suggestions by one of the following methods:

    -   On the **Top Suggestions** pie chart, view the top suggestions arranged by the number of processes making up these suggestions.
    -   To view only suggestions for application servers, select the **Suggested Application Servers** tile. The filtered list of suggestions for application servers is displayed. This list is also filtered to display only suggestions whose accuracy is 100%.
    -   Alternatively, select **All suggestions**. The unfiltered list of all suggestions is displayed.
4.  In the Application Suggestions list, select the relevant suggestion in the **Suggested Group Name** column.

    The Application Suggestion form opens.

    ![The Application Suggestion form](../image/fingerprint-application-suggestion-fine-tune.png)

5.  To change the name used for the fingerprint-based application, enter the preferred name in the **Name** field.

    For example, many applications run java processes and the suggested group name for these groups is **java**. You may want to assign a name that better describes the application that you want to discover using this suggestion \(for example, `java_myweblogic`\).

6.  To change the name used for the CI class, enter the preferred CI class name in the **Suggested CMDB CI Class** field.

7.  To fine-tune the classifier rule, change the regular expressions in the **Suggested Classifier Rule** field.

    For example, add version information to the regular expression for discovering a Tomcat application: `.*tomcat.* -Dopss.*version=12.1.3.*`

8.  Click **Update**.

9.  If you are not sure how to change the classifier rule, fine-tune it after performing the initial discovery as described in [Adjust regular expression used for fingerprint-based discovery](calibrate-process-based-discovery.md#).


## Adjust regular expression used for fingerprint-based discovery

Fine-tune the regular expression in the classifier rule to make discovery results more precise. Predictive Intelligence extracts regular expressions from processes and assigns them to classifier rules as part of creating suggestions. If you are not satisfied with the discovery results or the suggestion accuracy is lower than 100%, modify the regular expression.

### Before you begin

Role required: discovery\_admin

### Procedure

1.  Navigate to **All** &gt; **Application** &gt; **Module**.

2.  Click **Discover Application**.

    The fingerprint-based discovery finds the application and creates a CI class, a classifier, and a pattern.

3.  On the **Application Suggestions** list, click the newly created process classifier.

    The Process Classification form opens.

    ![Adjusting the regular expression.](../image/process-classification-fine-tune-example1.png)

4.  In the **Parameters** value field under **Condition**, notice the regular expression automatically selected by Predictive Intelligence.

    In this example, it is **."-DweblogicName=."**

5.  Click **Padlock** icon ![Padlock icon](../../event-management/image/lock-icon.png) next to **Test with**.

6.  Click the **Look up** icon ![Search icon](../../../administer/field-administration/image/SearchIconHeisenberg.png) to select the server on which you want to test additional regular expressions.

    The list of all discovered servers opens.

7.  Select the sever that runs the application that you want to discover using the customized classifier.

    The selected server appears in the **Test with** field.

8.  Right-click the header of the Process Classification form and select **Save**.

    The system runs a test and displays the results on the **Test results** tab at the bottom of the page.

    ![Adjusting the regular expression and choosing the server for testing it.](../image/process-classification-fine-tune-example2.png)

9.  On the Test results tab, check the processes that were discovered using the regular expressions configured for this classifier.

10. Adjust the regular expression in the Parameters value field under **Conditions**.

    For example, make it more generic: `"weblogic."`

11. Right-click the header of the Process Classification form and select **Save**.

    The system runs the test again and displays the results on the **Test results** tab at the bottom of the page.

12. On the Test results tab, verify that the fingerprint discovery found the applications as you expected.


## Disable fingerprint-based discovery

By default, the fingerprint-based discovery is enabled. Disable application discovery based on processes, if Predictive Intelligence does not generate enough processes.

### Before you begin

Role required: discovery\_admin

### Procedure

1.  Add the system property **sys\_property process.clustering.appfingerprint.enabled** as described in [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

2.  To disable, enter `false` in the **Value** field.

3.  To enable the fingerprint-based discovery again, change the **Value** field to `true`.


**Related topics**  


[KB0826261: Advanced configuration and troubleshooting of fingerprint-based discovery](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsysparm_article%3DKB0826261%26sysparm_stack%3D%26sysparm_view%3D)

[Troubleshooting Guide for ML Connection Suggestions](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0963421)

