---
title: Activate an EDL for Palo Alto Networks Next-Generation Firewall with a change request
description: If configured, the ServiceNow change request form is used to activate the External Dynamic List \(EDL\). This option is recommended if your firewall administrator is also using the ServiceNow AI Platform for firewall policy or rule changes. The EDL is activated automatically and ready to receive EDL entries upon closure of the ServiceNow AI Platform change request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/paloalto\_sncr\_edl.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Activate an EDL for Palo Alto Networks Next-Generation Firewall, Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Activate an EDL for Palo Alto Networks Next-Generation Firewall with a change request

If configured, the ServiceNow change request form is used to activate the External Dynamic List \(EDL\). This option is recommended if your firewall administrator is also using the ServiceNow AI Platform for firewall policy or rule changes. The EDL is activated automatically and ready to receive EDL entries upon closure of the ServiceNow AI Platform change request.

## Before you begin

**Note:** The figures in the following section are shown with **Tabbed forms** selected in System Settings. For more information about selecting and clearing tabbed forms, see the section titled Display tabbed forms in Configuring the form layout on the [ServiceNow Product Documentation website](https://www.servicenow.com/docs).

Role required: sn\_si.admin for approving the change request and change tasks

Palo Alto Networks firewall administrator for completing configuration tasks in Palo Alto Networks

## About this task

If configured, monitor your ServiceNow AI Platform change request and assign any tasks that are required to configure the Palo Alto Networks Next-Generation Firewall. After these tasks are completed, close the ServiceNow AI Platform change request to activate the EDL automatically.

## Procedure

1.  Navigate to **All** &gt; **Palo Alto Networks NGFW Integration** &gt; **Firewall EDL Configuration**.

2.  Select the EDL module and select an EDL in the **Name** column.

3.  In the open EDL record, select the change request number in the Change Requests related list.

    The change request record is displayed. The **Description** field lists the retrieval URL used to configure the Palo Alto Networks EDL. Details about mapping the EDL to the appropriate Palo Alto Networks Next-Generation Firewall policy are also included. In the **Short description** field, a comment indicates that there is a request to add a new EDL.

4.  In the upper-right corner of the record, select **Request Approval**.

    The State changes to Assess, and a message is displayed that the change request is waiting for approval.

5.  To complete the change request and activate the EDL, follow the steps to assign the tasks and close the change request.

    1.  If not displayed, open the change request and select the **Change Tasks** tab.

    2.  Select the task associated with creating the EDL object to open it.

    3.  On the record that is displayed, assign the task to the Palo Alto Networks firewall administrator, and select **Update**.

        The firewall administrator is notified and creates the EDL object in the Palo Alto Networks Next-Generation Firewall.

        To create the EDL object, the ServiceNow AI Platform retrieval URL is copied in Palo Alto Networks at **External Dynamic Lists** &gt; **Create Lists** &gt; **Source**.

    4.  After you have verified that the EDL object has been created in Palo Alto Networks, in the ServiceNow AI Platform, navigate to the change request associated with creating the EDL object and select **Close task**.

        On the task record for this example, `CTASK0010037` was closed for this task.

    5.  Navigate to the Change Tasks tab and select the task for assigning a firewall policy to the EDL Object.

        The status for `CTASK0010037` is `Closed`.

    6.  Open the record and assign the next task.

        After the task has been assigned, in Palo Alto Networks, the firewall administrator navigates to the **Policies** tab to assign the policy.

    7.  In the **Name** column, locate and select the security policy rule you want to add the EDL to, for example, **ServiceNow ip edl list**.

    8.  In the Security Policy Rule dialog box, select the **Destination** tab to add an EDL in the **Destination Address** field.

    9.  To view all the available EDLs, select the **Add** icon.

    10. Select **OK**.

    11. After you have verified that the EDL object has been assigned to a security policy, in the ServiceNow AI Platform, navigate to the change request, open the task associated with assigning the EDL object, and select **Close task**.

        After both tasks are closed, the change request is ready for approval.

    12. On the change request record, select the **Approvers** related list, and select an item in the **State** column to open the request used for creating the EDL.

    13. On the open approval request form, select **Approve**.

        The change request state moves to Scheduled.

    14. Select **Implement**.

    15. Select the **Closure Information** related tab and enter notes to close the request.

        An entry in this field is required to close the change request.

        After the change request is closed, the EDL is activated automatically. If you have not verified that the EDL is activated, navigate to **Palo Alto Networks NGFW Integration** &gt; **Firewall EDL Configuration**.

        In the Active column in the list, note that the status for the EDL is \(`true`\).

        In the Name column, select the EDL name, and in the open record, note that the **Active** check box is also selected.

    The EDL is now ready to accept EDL entries.


## What to do next

Submit EDL entries from a security incident or from the blocklist.

**Parent Topic:**[Activate an EDL for Palo Alto Networks Next-Generation Firewall](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/paloalto-activate-edl.md)

