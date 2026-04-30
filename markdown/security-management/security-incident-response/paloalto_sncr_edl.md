---
title: Activate an EDL for Palo Alto Networks Next-Generation Firewall with a change request
description: If configured, the ServiceNow change request form is used to activate the External Dynamic List \(EDL\). This option is recommended if your firewall administrator is also using the ServiceNow AI Platform for firewall policy or rule changes. The EDL is activated automatically and ready to receive EDL entries upon closure of the ServiceNow AI Platform change request.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Activate an EDL, Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Activate an EDL for Palo Alto Networks Next-Generation Firewall with a change request

If configured, the ServiceNow change request form is used to activate the External Dynamic List \(EDL\). This option is recommended if your firewall administrator is also using the ServiceNow AI Platform for firewall policy or rule changes. The EDL is activated automatically and ready to receive EDL entries upon closure of the ServiceNow AI Platform change request.

## Before you begin

**Note:** The figures in the following section are shown with **Tabbed forms** selected in System Settings. For more information about selecting and clearing tabbed forms, see the section titled Display tabbed forms in Configuring the form layout on the [ServiceNow Product Documentation website](https://servicenow.com/docs).

Role required: sn\_si.admin for approving the change request and change tasks

Palo Alto Networks firewall administrator for completing configuration tasks in Palo Alto Networks

## About this task

If configured, monitor your ServiceNow AI Platform change request and assign any tasks that are required to configure the Palo Alto Networks Next-Generation Firewall. After these tasks are completed, close the ServiceNow AI Platform change request to activate the EDL automatically.

## Procedure

1.  Navigate to **All** &gt; **Palo Alto Networks NGFW Integration** &gt; **Firewall EDL Configuration**.

    ![Select Firewall EDL Configuration module.](../image/4-30-fedl-nav.png)

2.  Select the EDL module and click an EDL in the **Name** column.

    ![Select an EDL from the Name column.](../image/4-30-edl-arrow.png)

3.  In the open EDL record, click the change request number in the Change Requests related list.

    ![Task: Select the change request.](../image/4-30-edl-app-notactive.png)

    The change request record is displayed. The **Description** field lists the retrieval URL used to configure the Palo Alto Networks EDL. Details about mapping the EDL to the appropriate Palo Alto Networks Next-Generation Firewall policy are also included. In the **Short description** field, a comment indicates that there is a request to add a new EDL.

    ![Work notes with text requesting the addition of a new EDL.](../image/4-30-apprv-1-shrtdescr.png)

4.  In the upper-right corner of the record, click **Request Approval**.

    The State changes to Assess, and a message is displayed that the change request is waiting for approval.

    ![Change request in Assess state.](../image/4-30-apprv-2.png)

5.  To complete the change request and activate the EDL, follow the steps to assign the tasks and close the change request.

    1.  If not displayed, open the change request and select the **Change Tasks** tab.

        ![Change Tasks tab on the change request.](../image/4-30-apprv-task-1.png)

    2.  Click the task associated with creating the EDL object to open it.

        ![Task to create the EDL Object highlighted.](../image/4-30-apprv-task-1-first.png)

    3.  On the record that is displayed, assign the task to the Palo Alto Networks firewall administrator, and click **Update**.

        The firewall administrator is notified and creates the EDL object in the Palo Alto Networks Next-Generation Firewall.

        To create the EDL object, the ServiceNow AI Platform retrieval URL is copied in Palo Alto Networks at **External Dynamic Lists** &gt; **Create Lists** &gt; **Source**.

        ![Task: Copy Retrieval URL to create the EDL object.](../image/4-30-pa-1-dialog-5-7.png)

        Image is used by permission and is PRIVILEGED and PROPRIETARY.

    4.  After you have verified that the EDL object has been created in Palo Alto Networks, in the ServiceNow AI Platform, navigate to the change request associated with creating the EDL object and click **Close task**.

        On the task record for this example, `CTASK0010037` was closed for this task.

    5.  Navigate to the Change Tasks tab and click the task for assigning a firewall policy to the EDL Object.

        ![Task: Assign EDL to a firewall policy highlighted.](../image/4-30-apprv-task-2-a.png)

        The status for `CTASK0010037` is `Closed`.

    6.  Open the record and assign the next task.

        After the task has been assigned, in Palo Alto Networks, the firewall administrator navigates to the **Policies** tab to assign the policy.

        ![Task to navigate to Policies in Palo Alto Networks.](../image/4-30-pa-2-box.png)

        Image is used by permission and is PRIVILEGED and PROPRIETARY.

    7.  In the **Name** column, locate and click the security policy rule you want to add the EDL to, for example, **ServiceNow ip edl list**.

        ![Task to select an EDL.](../image/4-30-pa-2-arrow.png)

        Image is used by permission and is PRIVILEGED and PROPRIETARY.

    8.  In the Security Policy Rule dialog box, select the **Destination** tab to add an EDL in the **Destination Address** field.

    9.  To view all the available EDLs, click the **Add** icon.

        ![Task to select Destination Address.](../image/4-30-obj-to-policy-pa.png)

        Image is used by permission and is PRIVILEGED and PROPRIETARY.

    10. Click **OK**.

    11. After you have verified that the EDL object has been assigned to a security policy, in the ServiceNow AI Platform, navigate to the change request, open the task associated with assigning the EDL object, and click **Close task**.

        After both tasks are closed, the change request is ready for approval.

    12. On the change request record, click the **Approvers** related list, and select an item in the **State** column to open the request used for creating the EDL.

        ![Approval requests for security incident admin listed on change request.](../image/4-30-paloalto-my-approvals-4-2-cropped.png)

    13. On the open approval request form, click **Approve**.

        The change request state moves to Scheduled.

        ![Change request in Scheduled state.](../image/4-30-apprv-3.png)

    14. Click **Implement**.

    15. Click the **Closure Information** related tab and enter notes to close the request.

        An entry in this field is required to close the change request.

        ![Close notes entered and change request completed.](../image/edl-apprv-closenotes.png)

        After the change request is closed, the EDL is activated automatically. If you have not verified that the EDL is activated, navigate to **Palo Alto Networks NGFW Integration** &gt; **Firewall EDL Configuration**.

        In the Active column in the list, note that the status for the EDL is \(`true`\).

        ![Activated EDL in Firewall EDL Configuration list.](../image/4-30-edl-list-active-callout.png)

        In the Name column, click the EDL name, and in the open record, note that the **Active** check box is also selected.

        ![EDL activated with check box selected on EDL record.](../image/4-30-apprv-4.png)

    The EDL is now ready to accept EDL entries.


## What to do next

Submit EDL entries from a security incident or from the blocklist.

**Parent Topic:**[Activate an EDL](paloalto-activate-edl.md)

