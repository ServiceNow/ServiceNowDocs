---
title: Test security incidents and approve requests for the isolate host
description: The test and preview step permits you to validate that the host isolation and remove host isolation workflow results are returned as expected for the profile.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/mcafee-epo-test-incident-ih.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
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

1.  If the Test Incident page is not displayed, select **Test Incident** in the progress bar.

    The Test Incident page is displayed for your profile.

2.  To the right of the top field, select the search icon to select a security incident to preview.

3.  In the Number column of the list that is displayed, select an item that you want to display in the preview.

    Only security incidents that match the criteria you set for the profile are displayed.

    The security incidents are displayed on the page.

4.  Repeat steps 2 and 3 until all the incidents that you want to preview are displayed in the fields.

    Select up to five security incidents for the preview.

5.  Select **McAfee ePO Preview** to view the security incidents.

    The incidents created for the security event conditions that match your profile are displayed in tabs.

    **Note:** If you leave the Test Incident page at this point, your security incidents are cleared from these fields.

6.  Select a tab, and, on the security incident, scroll to view the work notes.

7.  If you're a user in an approval group, follow these steps to process a request.

    1.  Navigate to **My Approvals** in your instance.

        The approvals list is displayed.

    2.  In the State column, select an item to open the approval record.

    3.  In the Approval record that is displayed, select **Approve** or **Reject**.

        After you process the request, the workflow may take a few moments to run. On the record at the top, a message is displayed as shown in the following figure if the transaction takes more than a few seconds.

        After a few moments, in the approval record that is displayed, the State column changes from `Requested` to `Approved`. No additional approvals are required to isolate the host machine for this request. If the request is rejected, the host is not isolated and the request remains pending. As a user with the sn\_si.analyst role, if the request is rejected, you're required to submit a new request if you still wish to isolate the endpoint.

        The request to isolate the host machine in the preceding figure is approved.

    4.  Navigate to **Security Incident** &gt; **Incidents** &gt; **Show All Incidents** and, in the Number column, select an entry to open the security incident that you're working with.

        On the security incident that is displayed, the Isolate Host - Completed™ tag replaces the Isolate Host - Initiated™ tag. The host isolation workflow for this example is successful.

        Work notes on the security incident also indicate that the host isolation is completed, and the approver, Mary admin™, is listed.

        **Important:** Although the security tag and work notes on the security incident indicate that a successful isolate host workflow is completed, return to your McAfee ePO console and verify that the host machine is isolated from your network.

        After you have completed your investigation on the asset, launch the Remove Isolation workflow from the Host Isolation Entries™ table in your ServiceNow AI Platform® instance to return the host to the network.

8.  To remove the host from quarantine and return it to the network, follow these steps.

    1.  If the McAfee ePO Isolate Host Entries table is not displayed, navigate to **McAfee epO Integration** &gt; **Mcafee epO integration Isolate Host Entries**.

        The Isolate Host Entries list is displayed. At the top of the list in the Status column, search for the asset you isolated.

    2.  In the Added date column, select the item to open the record.

        The Isolate Host Entries record is displayed. An audit trail for all the actions associated with the security incident is displayed in the work notes. In the following figure, the last entry in the work notes is a successful host isolation. The date the quarantine is completed is displayed in the **Added date** field \(`2019-01-03 14:04:17`\).

    3.  Select **Remove Isolation** to launch the workflow to restore the machine to the network.

        The Isolate Host Entry record is displayed. On the top of the record, a message indicates that the request was submitted. The Status changes from **Isolated** to **Pending Approval**, and a work note is logged. In this case, the System Administrator has requested that the machine is restored to the network.

    4.  After you're notified of the request, as a user with approval permission for host isolation, navigate to **My Approvals** in your instance and open the record for the remove isolation request.

    5.  Select **Approve** to approve the request and return the asset to the network.

        Alternatively, select **Reject** to keep the request in the pending approval state. If a request is rejected, a new request must be submitted to isolate the host. After you approve the request to remove the host isolation, the tag on the security incident is removed. Work notes create an audit trail for the remove isolation request.

        The security tag and work notes on the security incident indicate that the remove host isolation workflow is successfully completed. To verify that the host is back on the network, return to your McAfee ePO console and verify that the host machine is now active.

9.  Choose one to continue.

    |Option|Description|
    |------|-----------|
    |**Previous**|Return to the Configuration step for the profile. If you're not satisfied with the test and preview results, continue configuring the profile settings.|
    |**Finish**|Complete the configuration. You're prompted to confirm activation.|


**Parent Topic:**[McAfee ePO integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/mcaffee-epo-overview-arch.md)

**Previous topic:**[Test security incidents to initiate malware scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/mcafee-epo-test-incident-malscan.md)

**Next topic:**[Edit the start and completion tag names and colors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/mcafee-epo-edit-security-tag.md)

