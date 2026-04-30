---
title: FireEye Additional Actions on Endpoint
description: FireEye integration supports running additional actions beyond the gold standard actions.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [FireEye Endpoint Security integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# FireEye Additional Actions on Endpoint

FireEye integration supports running additional actions beyond the gold standard actions.

These actions comprise of Triage Acquisition and Data Acquisitions. Out of the box, two data acquisitions are supported:

-   Comprehensive Investigative Details Script
-   Standard Investigative Details Script

In addition, Triage Acquisition is also supported out of the box. All these three are created by default along with the source. The customers can also create their own actions i.e., Data acquisitions from the FireEye Additional Actions Module.\[1\] The maximum file size supported for FireEye Additional Actions is 1024, and this value can be configured by changing **com.glide.attachment.max\_size**, and the default timeout is 120 minutes that can be configured from the FireEye Default Setting page.

## Comprehensive Investigative Details Script

Enables collecting all forensic and investigative artifacts from the endpoint but is the most prohibitively expensive option. This configuration is ideal for situations where there will only be one window for collecting data from the endpoint in question, and the ability to acquire more data cannot be guaranteed later. So, use this action with caution.

## Standard Investigative Details Script

Enables the most common options for collecting forensic and investigative artifacts from an endpoint. Meant to be the primary response tool when you have suspicion that an endpoint may be compromised and need to perform a deep dive analysis of that endpoint. Aims to strike a balance between collecting the most relevant and valuable data whilst avoiding the costly options that can be collected later once further investigation proves them necessary.

## Triage Acquisition

Triage collections contain information from within the lookback cache as well as additional forensic audit information, such as URL download history, file download history, process and ports listings, and standard system information. You might want to examine such information when anomalous network traffic is detected, and you want more visibility into endpoint actions.

## Maintaining Data Acquisition Scripts on FireEye

Data acquisition requests \(sometimes referred to as Live Response requests\) allow you to acquire any data you need from a single running endpoint. Using the Data Acquisition Scripts page on FireEye, you can create, edit, copy, and delete the data acquisitions scripts used for data acquisition requests.

## Accessing the Data Acquisition Scripts Page on FireEye

To access the Data Acquisition Scripts page:

1.  Navigate to Endpoint Security web user interface.
2.  Select Data Acquisition Scripts on the Admin menu.

## Creating a Script on FireEye

To create a data acquisition script:

1.  Select **Data Acquisition Scripts** &gt; **Admin** menu of the Endpoint Security web user interface.
2.  Click **Create Script**.
3.  Enter a name for the new script in the **Script Name** field.
4.  Optionally, enter a description of the script.
5.  Select the operating system to which the script applies. You can only select a single operating system on the Create Script dialog.
6.  Click **Create** to start the script definition.
7.  Select an acquisition data type in the **Add an acquisition type**drop-down box and click **Add**. Options for the acquisition type you requested appear to the right of the script list.
8.  Supply values for the acquisition type options or use the default values that are already selected. The Web UI does not warn you or remove tabs, spaces, or unwanted characters \(such as \\n\) in your specifications.
9.  Repeat the previous 2 steps to request additional data for the data acquisition script. Some acquisition data types are available only once for a script, while others can be specified more than once. After adding an acquisition type to a script, the list of acquisition types available in the **Add an acquisition type**drop-down box adjusts appropriately.
10. To remove an acquisition data type from the script, click the x icon \( \) on the acquisition tab on the left side of the page.

**Note:** This integration does not support **Allow Edits before acquiring** option while creating scripts. So, ensure that the check box is unchecked.

## Exporting a Script from FireEye

You can export a data acquisition script to a JSON file. To export a data acquisition script:

1.  Select **Data Acquisition Scripts** &gt; **Admin** of the Endpoint Security web user interface.
2.  Select Data Acquisition Scripts on the Admin menu.
3.  Select the script you want to export on the left side of the page.
4.  select **Actions** &gt; **Export Script**.
5.  A JSON file is downloaded to your computer. The JSON file name includes the operating system so you can easily determine which scripts are for which operating system.

## Creating a new Data Acquisition Action in the ServiceNow AI Platform

To create a new action, follow these steps:

1.  Navigate to **FireEye Integration** &gt; **FireEye Additional Actions**. The FireEye Additional Actions list is displayed.
2.  Click **New**. The form for the new action is displayed.
3.  Fill out of the form.

<table id="table_ffn_bht_frb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Action Name

</td><td>

Name of the FireEye action that is performed. This name helps you identify the Action type and describe it.

</td></tr><tr><td>

Acquisition

</td><td>

An acquisition obtains the data to analyze. This is a read only field, and is defaulted to Data Acquisition.

</td></tr><tr><td>

Source

</td><td>

Name of the FireEye source. Only configured sources are available from the choice list.

</td></tr><tr><td>

Capability

</td><td>

This is a read only field and is populated with Run Additional Action\(s\) capability

</td></tr><tr><td>

Acquisition Type

</td><td>

Type of acquisition action that needs to be obtained, and analyzed.

</td></tr><tr><td>

Active

</td><td>

This indicates that the Action is active.

</td></tr><tr><td>

Require Approval

</td><td>

When you enable the Require Approval option, the Approvers field is available on the form. After you submit a request, approval is required from the group to complete the request.

</td></tr><tr><td>

Display tag

</td><td>

Type of operation system such as Windows, Mac, Linux for adding scripts.**Note:** Only one type of OS is supported currently. You can create one action per operating system. For other operating systems, create new actions as required.

</td></tr><tr><td>

Scripts

</td><td>

Imported script from FireEye needs to be provided for the selected OS Type. Only one script can be added to each OS type.

</td></tr></tbody>
</table>4.  Click **Submit**.

## Triggering Data Acquisitions from Security Incident

The Additional actions created can be run via the Related Link called **Run Additional Action\(s\) on Endpoint** on the security incident.

**Note:** **Allow Edits before acquiring** FireEye functionality is not supported for the Additional Actions on Endpoint.

