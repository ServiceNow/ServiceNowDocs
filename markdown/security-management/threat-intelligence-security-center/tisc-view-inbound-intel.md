---
title: Viewing Inbound Intelligence
description: Use this section to view all inbound intelligence sharing records. Review the intelligence data and take necessary actions to approve or reject them.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Viewing Threat Intelligence External Sharing, Administer, Threat Intelligence Security Center, Security Operations]
---

# Viewing Inbound Intelligence

Use this section to view all inbound intelligence sharing records. Review the intelligence data and take necessary actions to approve or reject them.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intelligence Sharing**.

2.  Select **Inbound Intelligence** &gt; **All**

    The inbound intelligence page displays the inbound intelligence records received by the systems from the external parties that are in the process for sharing intelligence. It displays the following sub sections:

    -   **All**: Displays all the inbound intelligence sharing records that were received by the system across multiple profiles.
    -   **Pending Approvals**: Displays the inbound intelligence records that are pending for approvals.
    -   **My Approvals**: Displays the inbound intelligence records that are awaiting your approval.

        **Note:** You can directly **Approve** or **Reject** from My Approvals section list view. Select the desired option from the split button view and approve or reject by providing a reason.

    Select the appropriate section and consider taking the necessary action for each inbound intelligence record.

3.  Select any inbound intelligence record to view the details.

    All the records that are received as part of the intelligence record are available under the **Inbound Intelligence Records** section.

4.  Select **Approve** to approve the sharing record.

    The Approve Inbound Intelligence is displayed.

5.  Add any comments, if necessary.

6.  Open any record that is awaiting your review.

    1.  Select **Approve** button to approve the inbound intelligence record.

        A confirmation message is displayed indicating that the inbound intelligence record is approved.

        **Note:**

        Notifications are triggered based on the rules configured within each profile. Once you approve or reject a sharing record, an email will be sent if email notifications are enabled for the profile. If no email is configured, no notification will be sent.

7.  Additionally, select **Reject** button if you want to reject the inbound intelligence record.

    **Note:**

    email samples for both approval and rejection of a sharing record:

    -   **Email notification on approval**: Your request for inbound intelligence data is approved.
    -   **Email notification on rejection**: Your request for inbound intelligence data: \{sharing record number\} is rejected. You can view the rejected sharing record using the given link.

**Parent Topic:**[Viewing Threat Intelligence External Sharing](../concept/tisc-intel-sharing-module.md)

**Related topics**  


[Viewing Outbound Intelligence](tisc-view-outbound-intel.md)

[Viewing TAXII Collections](tisc-view-taxii-collections.md)

