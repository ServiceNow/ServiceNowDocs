---
title: Integrating with SAP Ariba
description: Integrating your Software Asset Management application with the SAP Ariba application enables you to track your software subscriptions and reclaim unused licenses.Before setting up an SAP Ariba integration profile, generate and download reports for all users who are currently using SAP Ariba licenses.Create an SAP Ariba integration profile to track software subscriptions and optimize licensing for your SAP Ariba applications.
locale: en-US
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with SAP Ariba

Integrating your Software Asset Management application with the SAP Ariba application enables you to track your software subscriptions and reclaim unused licenses.

**Important:**

This integration retrieves user subscription details, tracks last login date, and identifies low-usage for the following SAP Ariba applications:

-   Ariba Sourcing
-   Ariba Supplier Performance Management
-   Ariba Contract Management

## Download reports for SAP Ariba users consuming licenses

Before setting up an SAP Ariba integration profile, generate and download reports for all users who are currently using SAP Ariba licenses.

### Before you begin

Role required: SAP Ariba admin

### About this task

For setting up an SAP Ariba integration profile, the following SAP Ariba reports are required.

-   Sourcing - User Names and Permissions
-   Contract Usage Reports
-   Number of Users Creating Projects
-   Supplier Performance Managements \(SPM\) Project Report

### Procedure

1.  Log in to [SAP Ariba portal](https://s1.ariba.com/Buyer/Main/ad/loginPage/SSOActions?awsso_cc=YXdzc29fcnU6YUhSMGNITTZMeTl6TVM1aGNtbGlZUzVqYjIwdlFuVjVaWEl2VFdGcGJqOXlaV0ZzYlQxaVkyOXVaV1JsYlc5cGJtRmliM2c9O3JlYWxtOlltTnZibVZrWlcxdmFXNWhZbTk0O2F3c3NvX2x1OmFIUjBjSE02THk5ek1TNWhjbWxpWVM1amIyMHZRblY1WlhJdlRXRnBiaTloWkM5amJHbGxiblJNYjJkdmRYUXZVMU5QUVdOMGFXOXVjdz09O2F3c3NvX2FwOlFuVjVaWEk9O2F3c3NvX2FyaWQ6TVRjeU9UYzFNakExTURJek1RPT07YXdzc29fa3U6YUhSMGNITTZMeTl6TVM1aGNtbGlZUzVqYjIwdlFuVjVaWEl2VFdGcGJpOWhaQzlqYkdsbGJuUkxaV1Z3UVd4cGRtVXZVMU5QUVdOMGFXOXVjdz09O2F3c3NvX2ZsOk1RPT0%3D%3AODEL3qhULrVEX%2BWtoW%2Bc5639RBg%3D&awsso_ap=Buyer&awsso_hpk=true&awsso_st=1&passwordadapter=PasswordAdapter1&realm=bconedemoinabox&awsr=true) with your admin credentials.

2.  On the home page, expand the **Manage** drop-down list.

    ![SAP Ariba home page.](../image/ariba-home-page.png)

3.  Select **Prepackaged Reports**.

    **Tip:** If you don’t find this menu item directly under the **Manage** drop-down list, select **More...** and then select **Prepackaged Reports** from the Reports section.

4.  Download the Sourcing - User Names and Permissions, Contract Usage Reports, and Number of Users Creating Projects reports.

    1.  On the Prepackaged Reports page, search for and select **System and Benchmark Usage Reports** and then select **Open**.

    2.  On the System and Benchmark Usage Reports page, select **System Usage Reports** and then select **Open**.

        The list of System Usage reports is displayed, where you can find Contract Usage Reports and Sourcing Usage Reports.

    3.  Save and export the Sourcing - User Names and Permissions report.

        1.  On the System Usage Reports page, expand the **Sourcing Usage Reports** drop-down list.

            The Sourcing-User and Permissions report is displayed.

        2.  Scroll down and select **Sourcing-User Names and Permissions** and then select **Open**.

            The Sourcing - User Names and Permissions report gets displayed.

        3.  Select **Save...**.

            As the Sourcing - User Names and Permissions report is a default report, you must not edit it.

        4.  On the Save Report page, select the **Current Project** field as **Personal Workspace**.

            **Important:** To change the file name when saving the report, provide the name in the format `Sourcing-User Names and Permissions`. You might include prefixes or suffixes as needed.

        5.  Select **Save**.
        6.  Export the saved report to your system in `.csv` format by selecting **Export**.
    4.  Save and export the Contract Usage Reports.

        1.  On the System Usage Reports page, search for and select **All Contract Workspaces** and then select **Open**.
        2.  On the All Contract Workspaces page, filter the report according to your requirements by selecting **Edit**.

            You can select a date range for the report you want to generate.

        3.  Add a field or a hierarchy from the General Contract Workspace list in the report by selecting the **Pivot Layout** step.

            For example, if you want to add the User Type field data to Detail Fields, select and hold \(or right-click\) it and then select **Detail Field**. You can add your required data to either Row Fields, Column Fields, or Detail Fields.

        4.  After your required fields are added, select **Next**.

            **Important:** If the **All Owners - User ID** field isn't included in the report, you must add it.

        5.  Select **Done**.

            In the **Pivot table** tab, the Detail View section displays the fields you have added in a tabular format.

            **Tip:** If you can’t see the fields that you selected, verify that you have selected the **Detail View** format.

        6.  Select **Save...**.
        7.  On the Save Report page, select the **Current Project** field as **Personal Workspace**.

            **Important:** To change the file name when saving the report, provide the name in the format `Contract Usage Reports`. You might include prefixes or suffixes as needed.

        8.  Select **Save**.
        9.  Export the saved report to your system in `.csv` format by selecting **Export**.
    5.  Save and export the Number of Users Creating Projects report.

        1.  On the System Usage Reports page, expand the **Sourcing Usage Reports** drop-down list and then select **Open**.

            The System Usage Reports are displayed.

        2.  Expand **Sourcing Usage Reports** and scroll down.

            You can view Number of Users Creating Projects.

        3.  Select **Number of Users Creating Projects** and then select **Open**.
        4.  On the Number of Users Creating Projects page, filter the report according to your requirements by selecting **Edit**.

            You can select a date range for the report you want to generate.

        5.  Add a field or a hierarchy from the Sourcing Project list in the report by selecting the **Pivot Layout** step.

            For example, if you want to add the Start Date field data, select and hold \(or right-click\) it and then select **Row Field**. You can add your required data to either Row Fields, Column Fields, or Detail Fields.

        6.  After your required fields are added, select **Next**.

            **Important:** If the **All Owners - User ID** field isn't included in the report, you must add it.

        7.  Select **Done**.

            In the **Pivot table** tab, the Detail View section displays the fields you have added in a tabular format.

            **Tip:** If you can’t see the fields that you selected, verify that you have selected the **Detail View** format.

        8.  Select **Save...**.
        9.  On the Save Report page, select the **Current Project** field as **Personal Workspace**.

            **Important:** To change the file name when saving the report, provide the name in the format `Number of Users Creating Projects`. You might include prefixes or suffixes as needed.

        10. Select **Save**.
        11. Export the saved report to your system in `.csv` format by selecting **Export**.
5.  Save and export the SPM Project Report.

    1.  On the Prepackaged Reports page, search for and select **Supplier Performance Management Reports** and then select **Open**.

    2.  On the Supplier Performance Management Reports page, select **SPM Project Report** and then select **Open**.

    3.  Select a date range for which you want the report and select **View Report**.

        **Tip:** If you can’t see the fields that you selected, verify that you have selected the **Detail View** format.

    4.  Filter the report according to your requirements by selecting **Edit**.

    5.  Add a field or a hierarchy from the SPM Project list in the report by selecting the **Pivot Layout** step.

        For example, if you want the Calendar data in Column Fields, select and hold \(or right-click\) it and then select **Column Field**. You can add your required data to Row Fields, Column Fields, or Detail Fields.

    6.  After your required fields are added, select **Next**.

        **Important:** If the **All Owners - User ID** field isn't included in the report, you must add it.

    7.  Select **Done**.

        In the **Pivot table** tab, the Detail View section displays the fields you have added in a tabular format.

        **Tip:** If you can’t see the fields that you selected, verify that you have selected the **Detail View** format.

    8.  Select **Save...**.

    9.  On the Save Report page, select the **Current Project** field as **Personal Workspace**.

        **Important:** To change the file name when saving the report, provide the name in the format `SPM Project Report`. You might include prefixes or suffixes as needed.

    10. Select **Save**.

    11. Export the saved report to your system in `.csv` format by selecting **Export**.


## Create an SAP Ariba integration profile

Create an SAP Ariba integration profile to track software subscriptions and optimize licensing for your SAP Ariba applications.

### Before you begin

The Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) must be installed from the [ServiceNow Store](https://store.servicenow.com/).

For publishing the integration profile, change the application scope to **Global**.

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the SAP Ariba integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d87598e797">

Interface

</th><th align="left" id="d87598e800">

Action

</th></tr></thead><tbody><tr><td id="d87598e806">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **SAP Ariba Integration Profile**.


</td></tr><tr><td id="d87598e848">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **SAP Ariba** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_yrz_yrr_gdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the integration profile. For example, `Ariba Integration`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile. -   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to `Ariba Subscription`.

</td></tr></tbody>
</table>3.  View the required user roles or API permissions to minimize security risks and optimize SaaS licenses.

    In the Download Subscription Subflow section, verify that the **Subflow** field is set to**SAP Ariba Download Subscriptions**. The **Download subscriptions** check box is selected by default and you can't clear it.

4.  Select **Save**.

5.  After the integration profile is saved, upload the attachments by selecting the **Attach** icon ![](../../contract-management/image/attachments-icon.png).

6.  On the Attachments pane, drag or select the files in the `.csv` format that you want to upload one by one or together.

    **Important:** Upload the SAP Ariba reports regularly to view the most recent data.

    After the files are uploaded successfully, the Subscription Stagings \[samp\_subscription\_staging\] table gets populated with the uploaded data.

7.  Select **Publish**.

    After the integration profile is published, the files attached to the profile are deleted automatically.


### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

After creating an integration profile, view information about the profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**. You can select an integration profile to view the following related lists. If the following related lists aren't visible for an integration profile in the default view, you can select the custom integration view from the Details tab:

-   Software Models
-   Unrecognized Subscription Identifiers
-   Scheduled Jobs
-   Scheduled Job Results
-   Software Subscriptions
-   Subscription Identifier Exclusion Rule
-   Subscription User Exclusion Rule

After creating an integration profile, you can define subscription exclusion rules to keep certain subscriptions from license cost calculations. For more information, see [Subscription exclusions for SaaS and SSO applications](subscription-exclusions.md#).

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../reuse/create-child-alias-saas.md).

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation in Software Asset Management classic](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

