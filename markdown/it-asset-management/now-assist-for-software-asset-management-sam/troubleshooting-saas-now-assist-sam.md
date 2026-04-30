---
title: Generate troubleshooting guidance for SaaS integrations by using Now Assist for SAM
description: Generate error messages and detailed guidance to troubleshoot runtime job failures for SaaS integrations. These recommendations enable you to resolve common configuration issues and reduce downtime.
locale: en-US
release: zurich
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: task
last_updated: "2026-01-30"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Generate troubleshooting guidance for SaaS integrations by using Now Assist for SAM

Generate error messages and detailed guidance to troubleshoot runtime job failures for SaaS integrations. These recommendations enable you to resolve common configuration issues and reduce downtime.

## Before you begin

Role required: sam\_integrator

## About this task

Now Assist for SAM generates the troubleshooting guidance for all SaaS integrations by enabling dynamic debug-level logging for flow actions and validating connections. The troubleshooting guidance is available for both existing and new SaaS integrations.

## Procedure

1.  Navigate to **Workspace** &gt; **Software Asset Workspace** &gt; **License operations**.

2.  Select **User subscription** and then select **Direct integration profiles**.

3.  Generate troubleshooting guidance.

<table id="choicetable_azy_b5f_g3c"><thead><tr><th align="left" id="d293662e106">

Integration

</th><th align="left" id="d293662e109">

Action

</th></tr></thead><tbody><tr><td id="d293662e115">

**Existing**

</td><td>

1.  Select the integration profile from the Direct integration profiles list.

An error message is displayed on the Integration Profile form indicating that the scheduled job failed to complete successfully.

2.  Select **Troubleshoot** on the error message.

The Now Assist for SAM application generates the troubleshooting details that contain the error summary and suggested resolutions. Each error that's listed in the Error Summary section has a corresponding troubleshooting guidance in the Suggested Resolutions section.

</td></tr><tr><td id="d293662e143">

**New**

</td><td>

1.  Select **New**.
2.  Select an integration type from the drop-down list.
3.  Select **Continue**.
4.  On the Integration profile form, enter a unique and descriptive **Display name**.
5.  Verify the required user roles or API permissions specified under various subflows and select **Save**.
6.  Select the preview icon ![](../../../common/image/Form_ReferenceLookupIcon.png) next to the **Connection &amp; Credential** field.
7.  Enter connection and credential details for this integration profile by selecting the **Create New Connection &amp; Credential** related link.
8.  Select **Create**.
9.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

The ServiceNow instance displays an error message stating that the connection validation isn't successful.

10. Select **Troubleshoot** on the error message.

The Now Assist for SAM application generates the troubleshooting details that contain the error summary and suggested resolutions. Each error that's listed in the Error Summary section has a corresponding troubleshooting guidance in the Suggested Resolutions section.

</td></tr></tbody>
</table>    ![Error summary and troubleshooting guidance for SaaS integration](../image/now-assist-troubleshooting.png)

4.  Use the suggested resolutions and select **Validate Connection.**

    If the connection validation isn't successful, you can select the **Troubleshoot** button to regenerate the error summary and resolution guidance.

5.  After the connection validation is successful, publish the integration profile by selecting **Publish**.


**Parent Topic:**[Using generative AI skills in Now Assist for SAM](../concept/using-now-assist-sam.md)

