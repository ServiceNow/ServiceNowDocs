---
title: Copy Splunk Enterprise Security profiles from one instance to another using export/import functionality
description: You can export and import Splunk Enterprise Security profiles settings from one ServiceNow AI Platform instance to a different ServiceNow AI Platform instance.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Copy Splunk Enterprise Security profiles from one instance to another using export/import functionality

You can export and import Splunk Enterprise Security profiles settings from one ServiceNow AI Platform instance to a different ServiceNow AI Platform instance.

## Before you begin

The settings you can export and import include profile name, correlation rules, mappings, filters, aggregation criteria, field translations, fetched sample data, scheduling, and configuration tile source information.

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

This functionality allows the security administrator to copy profiles that have been tested and verified on one ServiceNow AI Platform instance, for example on non-production, to another ServiceNow AI Platform instance, for example production, without the need to redo all configuration settings. The settings that are exported and imported include profile name, correlation rules, mappings, filters, aggregation criteria, field translations, fetched sample data, scheduling, and configuration tile source information.

**Note:** When you export a manual event forwarding profile type, the attachment data used for the sample field mapping is copied, however, the attachment file itself is not exported.

## Procedure

1.  Navigate to **All** &gt; **Splunk ES Integration** &gt; **Splunk ES Event Profiles**.

2.  Select a profile that you want to export to another ServiceNow AI Platform instance.

    You can select multiple profiles for export.

3.  From the Actions menu, click **Export**.

4.  Once the export complete message appears, click **Download**.

    The following illustration shows exporting a profile \(SplunkES3profile\) from the ServiceNow AI Platform instance \(psand.service-now.com\).

    ![Exporting Splunk profile data.](../image/splunk-profile-export.gif)

    The exported payload.xml file is downloaded on your computer. The file contains the profile name, correlation rules, mappings, filters, aggregation criteria, field translations, fetched sample data, scheduling, and configuration tile source information. When you select and download multiple profiles, they appear in the same payload.xml file.

    You can now proceed to import the profile in another ServiceNow AI Platform instance.

5.  Navigate to **Splunk ES Integration** &gt; **Splunk ES Event Profiles**.

6.  Click **Import**.

7.  Click **Choose file** and select the xml file on your computer.

8.  Click **Upload**.

9.  Click **Close and Reload Profiles**.

    The following illustration shows importing a profile \(SplunkES3profile\) from the ServiceNow AI Platform instance \(psand.service-now.com\) to the ServiceNow AI Platform instance \(ppsand.service-now.com\).

    ![Importing a Splunk Profile.](../image/splunk-profile-import.gif)

    You have successfully imported the profile from another ServiceNow AI Platform instance.

    Verify that the exported Source \(Splunk API account and Splunk server URL\) and MID Server configuration settings are valid and available in imported ServiceNow AI Platform instance. Update your Splunk Enterprise Security configuration if required.

10. Verify the MID Server settings after your import a profile.

11. Navigate to **Security Operations** &gt; **Integration Configurations**.

12. Select the Splunk Enterprise Security configuration tile, and click **Update**.

13. Review and update the Source and MID Server details as required.


