---
title: Test security incidents and approve requests for the isolate host
description: The test and preview step permits you to validate that the host isolation and remove host isolation workflow results are returned as expected for the profile.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Test security incidents and approve requests for the isolate host

The test and preview step permits you to validate that the host isolation and remove host isolation workflow results are returned as expected for the profile.

## Before you begin

Role required: sn\_si.admin

## About this task

During this step of the configuration, as a user with the sn\_si.admin role, verify that the profile you configured with the isolate host capability returns security incidents and matching asset IDs as expected. View the actual ServiceNow AI Platform Security Incident Response \(SIR\) security incidents that are created when security event conditions occur that match the settings of your profile.

After a request to isolate a host machine is submitted, as a user with an approver role, process the request.

## Procedure

1.  If the Test Incident page is not displayed, click **Test Incident** in the progress bar.

    ![Test Incident page of a McAfee Capability Profile.](../image/mcafee-test-incident1.png)

    The Test Incident page is displayed for your profile. For this example, the Isolate Host™ profile you created and configured in the preceding sections is displayed.

2.  To the right of the top field, click the search icon to select a security incident to preview.

    ![Search symbol highlighted.](../image/mcafee-test-incident1-callout.png)

3.  In the Number column of the list that is displayed, select an item that you want to display in the preview.

    Only security incidents that match the criteria you set for the profile are displayed.

    ![List of security incidents.](../image/mcafee-test-incident2a.png)

    The security incidents are displayed on the page.

4.  Repeat steps 2 and 3 until all the incidents that you want to preview are displayed in the fields.

    Select up to five security incidents for the preview.

5.  Click **McAfee ePO Preview** to view the security incidents.

    ![McAfee ePO Preview button highlighted.](../image/mcafee-test-incident-clk-preview.png)

    The incidents created for the security event conditions that match your profile are displayed in tabs.

    **Note:** If you leave the Test Incident page at this point, your security incidents are cleared from these fields.

    ![Security incidents displayed on tabs.](../image/mcafee-test-incident-4.png)

6.  Select a tab, and, on the security incident, scroll to view the work notes.

    ![Work notes logging when capability tasks are initiated and successfully completed.](../image/mcafee-ih-notes-pending.png)

    For this example, SIR0010021 from the preceding image is selected. The work notes list that the isolate host workflow is started. Because the **Require Approval** option is enabled for this profile, the work notes indicate that the request is `pending approval`.

    On the top of the incident, the security tag is displayed that indicates the request is initiated \(`Isolate Host - Initiated`\).

    ![Security incident with Isolate Host Queued tag displayed.](../image/mcafee-que-tag.png)

    You have successfully located security incidents that match your profile for the Isolate Host capability and viewed a security incident.

7.  If you are a user in an approval group, follow these steps to process a request.

    1.  Navigate to **My Approvals** in your instance.

        For this example, the user name of the approver is Mary admin™.

        ![My Approvals module highlighted.](../image/mcafee-ih-maryapprv.png)

        The approvals list is displayed.

    2.  In the State column, click an item to open the approval record.

        ![In My approvals, Requested in State column highlighted.](../image/mcafee-ih-maryapprv1.png)

    3.  In the Approval record that is displayed, click **Approve** or **Reject**.

        ![On Approval record, Approve and Reject buttons highlighted.](../image/mcafee-ih-maryapprv2.png)

        After you process the request, the workflow may take a few moments to run. On the record at the top, a message is displayed as shown in the following figure if the transaction takes more than a few seconds.

        ![Transaction processing message.](../image/mcafee-transaction-msg-ih.png)

        After a few moments, in the approval record that is displayed, the State column changes from `Requested` to `Approved`. No additional approvals are required to isolate the host machine for this request. If the request is rejected, the host is not isolated and the request remains pending. As a user with the sn\_si.analyst role, if the request is rejected, you are required to submit a new request if you still wish to isolate the endpoint.

        ![In My Approvals, Approved displayed in State column.](../image/mcafee-ih-maryapprv3.png)

        The request to isolate the host machine in the preceding figure is approved.

    4.  Navigate to **Security Incident** &gt; **Incidents** &gt; **Show All Incidents** and, in the Number column, click an entry to open the security incident that you are working with.

        ![Show All Incidents highlighted in navigation panel.](../image/mcafee-ih-maryapprv-si.png)

        On the security incident that is displayed, the Isolate Host - Completed™ tag replaces the Isolate Host - Initiated™ tag. The host isolation workflow for this example is successful.

        ![On security incident, Host successfully Isolated security tag.](../image/mcafee-iso-tag.png)

        Work notes on the security incident also indicate that the host isolation is completed, and the approver, Mary admin™, is listed.

        ![Work notes logging when capability tasks are initiated and successfully completed.](../image/mcafee-ih-notes-isolated.png)

        **Important:** Although the security tag and work notes on the security incident indicate that a successful isolate host workflow is completed, return to your McAfee ePO console and verify that the host machine is isolated from your network.

        After you have completed your investigation on the asset, launch the Remove Isolation workflow from the Host Isolation Entries™ table in your ServiceNow AI Platform® instance to return the host to the network.

8.  To remove the host from quarantine and return it to the network, follow these steps.

    1.  If the McAfee ePO Isolate Host Entries table is not displayed, navigate to **McAfee epO Integration** &gt; **Mcafee epO integration Isolate Host Entries**.

        ![On McAfee ePO Isolate Host Entries table, Status column with Isolated highlighted.](../image/mcafee-uih-isolated-status.png)

        The Isolate Host Entries list is displayed. At the top of the list in the Status column, search for the asset you isolated.

    2.  In the Added date column, click the item to open the record.

        The Isolate Host Entries record is displayed. An audit trail for all the actions associated with the security incident is displayed in the work notes. In the following figure, the last entry in the work notes is a successful host isolation. The date the quarantine is completed is displayed in the **Added date** field \(`2019-01-03 14:04:17`\).

        ![Isolate Host Entries record.](../image/mcafee-uih-2.png)

    3.  Click **Remove Isolation** to launch the workflow to restore the machine to the network.

        The Isolate Host Entry record is displayed. On the top of the record, a message indicates that the request was submitted. The Status changes from **Isolated** to **Pending Approval**, and a work note is logged. In this case, the System Administrator has requested that the machine is restored to the network.

        ![Isolate Host Entry record with messages.](../image/mcafee-uih-3.png)

    4.  After you are notified of the request, as a user with approval permission for host isolation, navigate to **My Approvals** in your instance and open the record for the remove isolation request.

    5.  Click **Approve** to approve the request and return the asset to the network.

        Alternatively, click **Reject** to keep the request in the pending approval state. If a request is rejected, a new request must be submitted to isolate the host. After you approve the request to remove the host isolation, the tag on the security incident is removed. Work notes create an audit trail for the remove isolation request. For this example, the system administrator initiated and approved the request.

        ![Work notes logging when capability tasks are initiated and successfully completed.](../image/mcafee-remove-notes-cmplt.png)

        The security tag and work notes on the security incident indicate that the remove host isolation workflow is successfully completed. To verify that the host is back on the network, return to your McAfee ePO console and verify that the host machine is now active.

9.  Choose one to continue.

    |Option|Description|
    |------|-----------|
    |**Previous**|Return to the Configuration step for the profile. If you are not satisfied with the test and preview results, continue configuring the profile settings.|
    |**Finish**|Complete the configuration. You are prompted to confirm activation.|


**Parent Topic:**[McAfee ePO integration](../concept/mcaffee-epo-overview-arch.md)

**Previous topic:**[Test security incidents to initiate malware scan](mcafee-epo-test-incident-malscan.md)

**Next topic:**[Edit the start and completion tag names and colors](mcafee-epo-edit-security-tag.md)

