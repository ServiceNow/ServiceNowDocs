---
title: Risk Management Framework \(RMF\) step 4 - Assess implemented controls and document findings
description: After you have implemented controls, you can assess internal and external controls, generate Plans of Action and Milestones \(POA&amp;M\), and manage change requests and vulnerable items.
locale: en-US
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Risk Management Framework \(RMF\) step 4 - Assess implemented controls and document findings

After you have implemented controls, you can assess internal and external controls, generate Plans of Action and Milestones \(POA&amp;M\), and manage change requests and vulnerable items.

## Before you begin

Role required: sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.info\_system\_sec\_officer, sn\_irm\_cont\_auth.authorization\_official, sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.admin

## About this task

The Assess process is generally performed by a user other than the system owner or the personnel who implemented the controls.

The Assess state adds **Control Assessments** and **Risk Summary** related lists, as well as **POA&amp;M**, **Change Requests**, **Security Incidents**, and **Vulnerable Items** tabs to the Authorization Package form.

**Note:** CAM performance may slow when a high volume of Change Request, Incident records, or both is related to a single authorization package. If you experience long transaction response times, consider performing the procedures detailed in [KB0861865](https://support.servicenow.com/kb_view.do?sys_kb_id=6076cbb61b3b94508672ea89bd4bcbca).

## Procedure

1.  For an authorization package in the Implement state, select **Assess**.

    ![Transition to the Assess state](../image/assess.png)

    **Note:** An Audit Engagement is automatically created.

    To send the package back to the Implement state, select **Back to previous step**. The state of the engagement becomes Closed Incomplete. On selecting **Assess**, an engagement is created.

2.  Select the **Control Assessments** related list to view the Audit engagement.

    ![Control Assessments](../image/control-asmts.png)

    **Note:** The Audit Engagement is automatically assigned to the SCA.

3.  Select the engagement number to open it.

    Notice that the **Entities** tab is displaying the authorization boundary for the package.

    ![Tabs for assessment.](../image/entity.png)

4.  Select the **Controls** tab to view all the controls that your team implemented.

    ![Controls](../image/controls-tab.png)

5.  Select the **Test plans** tab.

    Test plans are automatically created for the control. For more information on test plans, see [Generate assessment procedure plans for a test plan](cam-assess-controls-assess-obj.md).

6.  Select the **Control tests** tab to view the tasks for assessing the controls.

    **Note:** The **Audit tasks** tab in the Default view is renamed as **Control tests** tab in the CAM view. The names of the related list labels vary and are specific to the Default view or CAM view. You can change the view by selecting the Additional actions icon \(![Additional actions menu icon.](../../../common/image/Form_MenuIcon.png)\).

    ![Control tests tab.](../image/cam-control-tests.png)

    For more information on test plans, see [Determine control effectiveness of a control test](cam-control-effectiveness-control-test.md).

    1.  Select a control test.

        ![Assessment procedures related list.](../image/cam-assessment-proc.png)

    2.  From the **Assessment procedures** list, select a record.

    3.  Select the **Attach File** link to attach an evidence document as a proof of the test.

7.  In the Default view, select an audit task and perform the Design Test and Operation Test to judge the control's effectiveness.

    For details on this process, see [Manage engagements](../../grc-audit/concept/c_Engagements.md).

    **Note:** Any issues that arise during the Assess phase appear in the **POA&amp;M** tab. Additionally, any open Change Requests or Vulnerable Items targeting the system elements in the package appear under those tabs.

8.  The system owner must review and document any POA&amp;M issues, change requests, and vulnerable items that potentially threaten your systems.


