---
title: Test security incidents to initiate malware scan
description: After you configure a profile for the malware scan, test the profile and view the security incidents that match the settings of your profile. Preview the scan results on the related lists of a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Test security incidents to initiate malware scan

After you configure a profile for the malware scan, test the profile and view the security incidents that match the settings of your profile. Preview the scan results on the related lists of a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.

## Before you begin

Role required: sn\_si.admin

## About this task

As a user with the sn\_si.admin role, verify that the profile with the malware scan capability is invoked and that the scan search results match what is expected with a preview of the related lists on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident. The preview permits you to validate that scan results are returned as expected for the profile.

## Procedure

1.  If the Test Incident page is not displayed, click **Test Incident** in the progress bar.

    The Test Incident page is displayed for your profile. For this example, the Initiate Malware Scan profile you created and configured in the preceding sections is displayed.

    ![Test Incident page of a McAfee Capability Profile.](../image/mcafee-im-test-1.png)

2.  To the right of the top field, click the search icon to select a security incident to display on the preview.

    ![Search symbol highlighted.](../image/mcafee-im-test-2.png)

    Only security incidents that match the profile criteria are displayed.

3.  In the Number column of the list that is displayed, select an item that you want to display in the preview.

    ![List of security incidents.](../image/mcafee-im-test-3.png)

    The security incident number is displayed in the field.

    ![Security incident number displayed in search field.](../image/mcafee-im-test-3-result.png)

4.  Repeat steps 2 and 3 until all the incidents that you want to preview are displayed in the fields.

    Select up to five security incidents for the preview.

5.  Click **McAfee ePO Preview**.

    ![McAfee ePO Preview button highlighted.](../image/mcafee-im-test-4.png)

    The security incidents that match the event conditions of your profile are displayed. After the page has loaded, on the bottom of the page, tabs are displayed for each security incident.

    ![Security incident displayed on tab.](../image/mcafee-im-test-5.png)

6.  Scroll to view the work notes.

    **Note:** The list threat events workflow is part of the scan. For more information about creating a profile with the malware scan capability, see [Create a capability profile](mcafee-epo-create-profile.md).

    ![Work notes logging when capability tasks are initiated and successfully completed.](../image/mcafee-im-worknotes.png)

    Scans are sometimes scheduled to run during after peak working hours to minimize their impact to users on the network. The scan may not complete immediately. In this case, on the top of the security incident, a security tag is displayed indicating that the scan is scheduled. Refer to the work notes for status on the workflow. The work notes list when workflows start and are successfully completed. For this example, the work notes in the following figure show that the scan started, and that it successfully completed. The List Threat Events capability was also started and successfully completed as part of the scan.

    The following figure shows an example of a security tag on the related security incident.

    ![On security incident, McAfee ePO Scan Scheduled security tag.](../image/mcafee-im-test-6.png)

    On the security incident, after the scan is successfully completed, the scheduled tag is automatically replaced by the completed tag.

    ![On security incident, McAfee ePO Scan Complete security tag.](../image/mcafee-im-si-tag-cmplt.png)

7.  After you verify that the scan is successfully completed, on the security incident, scroll to view the Related Links and click **Show all Related Lists**.

    ![Show All Related Lists link highlighted.](../image/mcafee-im-test-7.png)

    The Threat Event Results and Threat Event Details list are displayed as tabs.

8.  If the Threat Event Details list is not selected, select it to view the results.

    ![Threat Event Results tab with results selected.](../image/mcafee-im-threat-resutls-tab.png)

9.  Click an item in the Source column to open a record and view the enrichment data.

    ![Threat Event Result record.](../image/mcafee-im-threat_event_result-rcd.png)

    The enrichment data includes the following information.

    -   The CI field value that was matched during the scan.
    -   Last Check-in Date with time zone. This data refers to when in local time the most current data was from pulled from the McAfee ePO console.
    -   Raw data
    You have successfully verified that the scan workflow successfully completed for security incidents that matched the auto-trigger criteria that you set for this profile.

10. Choose one to continue.

    |Option|Description|
    |------|-----------|
    |**Previous**|Return to the Configuration step for the profile. If you are not satisfied with the test and preview results, continue configuring the profile settings.|
    |**Finish**|Complete the configuration. You are prompted to confirm activation.|


**Parent Topic:**[McAfee ePO integration](../concept/mcaffee-epo-overview-arch.md)

**Previous topic:**[Using McAfee ePO integration in Analyst Workspace](using-mcafee-integration-aws.md)

**Next topic:**[Test security incidents and approve requests for the isolate host](mcafee-epo-test-incident-ih.md)

