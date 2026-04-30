---
title: Discover applications based on fingerprints
description: Discover applications based on suggestions based on ServiceNow Predictive Intelligence. Predictive Intelligence automatically classifies and categorizes the discovered running processes, as application fingerprints, and provides suggestions. ITOM Visibility uses Predictive Intelligence to perform initial analysis of discovered processes and suggest applications that you might want to discover. When using this method, ITOM Visibility automatically creates a Configuration Management Database \(CMDB\) configuration item \(CI\) class, a classifier, or a pattern for the new application CI class.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Running discoveries in your network, Discovery, ITOM Visibility, IT Operations Management]
---

# Discover applications based on fingerprints

Discover applications based on suggestions based on ServiceNow Predictive Intelligence. Predictive Intelligence automatically classifies and categorizes the discovered running processes, as application fingerprints, and provides suggestions. ITOM Visibility uses Predictive Intelligence to perform initial analysis of discovered processes and suggest applications that you might want to discover. When using this method, ITOM Visibility automatically creates a Configuration Management Database \(CMDB\) configuration item \(CI\) class, a classifier, or a pattern for the new application CI class.

## Before you begin

Perform horizontal discovery on all relevant IP ranges as described in [Convert IP networks into Discovery range sets](../concept/c_NetworkDiscovery.md#). Provide all the relevant credentials for ITOM Visibility access to the applications and devices that you want to discover.

Role required: discovery\_admin

## About this task

Discovering applications using fingerprints is especially useful when you can't use patterns available by default or from the ServiceNow Store. For example, when you want to discover non-standard, home-grown applications or brand new applications.

The Discovery feature of ITOM Visibility uses application dependency-mapping \(ADM\) to detect processes running on TCP ports and discover applications that run these processes. When you discover applications based on fingerprints, you take it a step further. The fingerprint-based discovery method analyzes processes that ADM hasn't used for discovery.

Fingerprint-based discovery uses algorithms to identify running processes and organizes them into groups. These process groups become suggested applications or candidates. You review suggested applications and choose which ones to discover. The list of suggested applications is refreshed every hour.

Patterns created during the fingerprint discovery are used for both horizontal and top-down discovery. For Service Mapping to run such a pattern correctly, define when to run this pattern. You do that by defining before or after which other pattern Service Mapping should run this new pattern.

When you discover an application based on an application suggestion, the fingerprint-based discovery performs the following steps:

1.  The fingerprint-based discovery creates a CMDB CI class for the new application. The new CI class extends the Application \[cmdb\_ci\_appl\] CI class and by default uses the process group name for the suggested CI class display name.
2.  The fingerprint-based discovery creates a process classifier for the application group you chose to discover. ADM uses the new process classifier to trigger the new pattern created for the CI class. The priority of the classifier is lower to ensure that the system first uses the default patterns available with ITOM Visibility or custom patterns.
3.  The fingerprint-based discovery creates a discovery pattern of the application type for the new CI class. **Enforce Process Classification** is enabled to make sure that the MID Server runs this pattern only if the process identified on a CI matches the classification criteria for this pattern.

    **Note:** The Service Mapping user interface refers to CI classes as CI types.

4.  ADM uses the classifier to trigger the horizontal discovery of the application CI.
5.  ADM triggers discovery using the new pattern.
6.  After the pattern completes discovery, it writes the discovered application CI into the relevant CMDB table.

By default, the fingerprint-based discovery is enabled.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Home**.

2.  Click **Application Fingerprints**.

    The **Application Fingerprints** dashboard opens.

3.  Review suggested applications in one of the following ways:

    -   On the **Top Suggestions** pie chart, view the top suggestions arranged by the number of processes making up these suggestions. The process count is reflected by the size of the chart segment. Click the segment to see its corresponding suggestions in a filtered list. To remove a suggestion from the chart, click the suggestion name in the chart legend.
    -   To view only suggestions for application servers, click the **Suggested Application Servers** tile. The filtered list of suggestions for application servers is displayed.
    -   Alternatively, click **All suggestions**. The unfiltered list of all suggestions is displayed.
4.  Click the relevant suggestion in the **Suggested Group Name**, for example **python**.

    The suggestion details open in the **Application Suggestion** form.

5.  Review the suggestion details, paying attention to the following parameters:

<table id="table_xjs_crm_3lb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Suggested Group Name

</td><td>

The name ITOM Visibility generates for the suggestion. This field is pre-populated, but you can modify it if necessary.

</td></tr><tr><td>

Extended Group Name

</td><td>

The top 10 key words that provide more information about the process. Predictive Intelligence extracts these key words from the process.

</td></tr><tr><td>

Suggested CMDB CI class

</td><td>

The name of the CMDB CI class that the ADM creates, if you choose to discover the suggested application.

</td></tr><tr><td>

Process Count

</td><td>

The number of discovered processes that this suggestion is based on.

</td></tr><tr><td>

View Processes

</td><td>

Click to view sample processes that this suggestion is based on. The overall number of processes may be larger and starts from one thousand. The number of sample processes you can view by default is one hundred.

</td></tr><tr><td>

Accuracy

</td><td>

A validation algorithm checks the quality of the prediction. The algorithm analyzes the regular expression \(ReGex\) parameter of the processes in this suggestion and other suggestions \(application groups\). Pick suggestions with higher rule accuracy. If the accuracy is low, you may adjust the process ReGex definition manually, as described in [Adjust regular expression used for fingerprint-based discovery](../concept/calibrate-process-based-discovery.md#).

 **Note:** Do not modify the accuracy value manually.

</td></tr><tr><td>

Process Classifier

</td><td>

The suggested regular expression used in the classifier. If defined, ADM uses this regular expression during horizontal discovery.

</td></tr><tr><td>

Ignore Rule

</td><td>

The name of the process that was excluded from discovery using the **Ignore** action.

</td></tr></tbody>
</table>6.  If this suggestion is not relevant and you do not want to use it for discovery, perform one of the following actions:

    -   To exclude processes from horizontal discovery, click **Ignore**.

        This process is added to the Process Handlers \[discovery\_proc\_handler\] table with the **Classify parameter** set to false. Discovery stops checking the classifier for the excluded process and does not discover the CI on which these processes run.

    -   To remove this suggestion from the suggestion list, click **Delete**.

        The suggestion disappears from the list. If Predictive Intelligence adds new processes to a deleted suggestion, it reappears in this list.

7.  Click **Discover Application**.

    The fingerprint-based discovery discovers an application CI for the selected suggestion.

8.  On the **Application Fingerprints** dashboard, check that the discovered application appears under **Created Applications**.

    ![Discovered Python application.](../image/fingerprint-dashboard-created-apps-example.png)

9.  Configure the running order for the automatically created pattern:

    1.  Click the process classifier next to the new application.

        The Process Classification form opens.

    2.  On the Triggers probes tab, click the pattern link.

        ![Click the automatically generated pattern.](../image/triggers-probes-pattern.png)

        The pattern form opens.

    3.  Select the order in which this pattern always runs:

        -   **Before**
        -   **After**
    4.  Then select the other applicable pattern.

        **Note:** If you are not sure what the right order is or you are not planning on using this automatically generated pattern for top-down discovery, configure the run order to **After All**.

    5.  Click **Save**.

10. Click the process classifier next to the new application to see the classifier and the pattern that the fingerprint-based discovery creates for this application CI.

11. If the discovery result is not satisfactory, [calibrate the fingerprint-based discovery feature](../concept/calibrate-process-based-discovery.md#).


**Related topics**  


[Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Application Fingerprints dashboard](../../../use/dashboards/application-content-packs/discovery-application-fingerprint-dashboard.md)

