---
title: View package details in CAM Workspace
description: Use the authorization package overview page to view documents and evidence that help you to assess your organization's security posture.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# View package details in CAM Workspace

Use the authorization package overview page to view documents and evidence that help you to assess your organization's security posture.

## Before you begin

Role required:

-   sn\_irm\_cont\_auth.authorization\_official
-   sn\_irm\_cont\_auth.information\_owner
-   sn\_irm\_cont\_auth.info\_system\_sec\_manager
-   sn\_irm\_cont\_auth.info\_system\_sec\_officer
-   sn\_irm\_cont\_auth.sec\_control\_assessor
-   sn\_irm\_cont\_auth.system\_owner
-   sn\_irm\_cont\_auth.scheduler
-   sn\_irm\_cont\_auth.system\_user
-   sn\_irm\_cont\_auth.admin
-   sn\_irm\_cont\_auth.executive\_read

## Procedure

1.  Navigate to **All** &gt; **CAM Workspace**.

2.  To navigate to the Lists page, select the lists icon \(![Lists icon](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  From the Authorization packages in the RMF list, select an authorization package record.

    The stepper component displays the current state of the package, and the roadmap to reach the Monitor state.

    ![Authorization package overview page.](../image/auth-package-overview.png)

    -   **Compliance summary**

        Displays the total number of controls contained in this package. Breakup counts of inherited control and not applicable controls of the package are also displayed. The **Controls implemented** contain the percentage of controls in the Monitor state.

        **Note:**

        -   You cannot move control objectives with the same reference ID from the baseline controls list to the not applicable controls.
        -   When you select two control objectives with the same reference ID from the **Not Applicable Controls** list, the **Return to Baseline Control** action is disabled.
        -   You cannot move control objectives with the same reference ID from baseline controls to not applicable controls, or from not applicable controls to baseline controls.
    -   **Control allocation**

        Controls grouped by family and categorized as system specific and hybrid.

    -   **Overview**

        Displays the total count of Controls, Control tests, and POA&amp;Ms and their status.

    -   **Details**

        More granular details of controls in control requirement widget, control tests details in assessment procedures widget.

        In the **Details** tab when the authorization package moves to the **Authorize** step you can view the following details:

        -   **Next Authorization Date**: This date is generated when the Authorization Package is moved to the Authorize step. The next authorization date will be set to three years from the date the package is moved to this step.
        -   **Next Engagement Date**: The next engagement date is prepopulated based on the number of days defined on the **System Properties** page. For more information, see [Continuous Authorization and Monitoring system properties](../../grc-cam/reference/cam-components-installed.md#).

            On this date, a new engagement is created with controls, test plans carried over from previous engagements, and newly associated control tests and assessment procedures.

4.  Select the sidebar icon \(![Sidebar icon](../../grc-workspace-compliance/image/pc-ws-sidebar-icon.png)\).

    The Highlighted details section displays:

    -   The privacy sensitive system status of the package.
    -   The link to the boundary, if selected, helps you to navigate to the authorization boundary to which this package is associated.
    -   The **Impact** card shows the confidentiality, integrity, and availability status of the package, based on which the **Impact** of the package is determined.
    -   The users who have a key role to play in updating the authorization package are also listed.
5.  To view the relationship between the selected authorization package and all its associated objects in a distinct visualization, select **360° view**.

    **360° view** is added in the Overview pages of Authorization Boundary, Authorization Package, Control, Control objective, Control overlays, Control test, Test template, Test plan, Engagements, and in the Details pages of Indicator, Indicator Template, and POA&amp;Ms.

    ![360° view of all the elements associated with the authorization package.](../image/apack-cam-ws-360-view.png)

6.  Select **Generate SSP** to generate a System Security Plan \(SSP\).

    You can also generate ATO artifact reports such as Security Assessment Report \(SAR\) and Plan of Actions and Milestones \(POA&amp;Ms\) by selecting the more actions icon \(![More actions icon](../../grc-workspace-risk/image/icon-more-actions-risk.png)\).

    For more information on CAM ATO artifacts, see [ATO artifacts for an authorization package](../concept/generate-ato-artifacts-cam-ws.md).

7.  To generate OSCAL SSP, select the **Export OSCAL SSP** option from the more actions icon \(![More actions icon](../../grc-workspace-risk/image/icon-more-actions-risk.png)\).

    For more information, see [Export in OSCAL format](../concept/oscal-support-cam.md) and [Export OSCAL SSP](generate-oscal-models.md).

8.  To move to the previous step of the authorization package and to update any details, select the **Back to previous step** option from the more actions icon \(![More actions icon](../../../common/image/icon-ellipses.png)\).

    All actions that are done when you moved to the current state are reversed if you opt the **Back to previous step** action. For example, if the package is in Implement state, then when it moves back to Select state all the existing controls that are generated are retired. In the Select state, you can revisit the baseline controls and take necessary actions if required. However, this operation can only be done by a Continuous Authorization and Monitoring administrator \(sn\_irm\_cont\_auth.admin\).

9.  To view the controls related to the authorization package, select the **Controls** related list.

    1.  Select a control from the list.

        In the Continuous Authorization and Monitoring application, you can view the control's allocation category in the header of the control's Overview page. **Control allocation** is either System specific or Hybrid.

    2.  Select the sidebar icon \(![Sidebar icon](../../grc-workspace-compliance/image/pc-ws-sidebar-icon.png)\) to view the NIST reference details.

    3.  Select the **Details** related list.

        The family to which the control objective of the control belongs can be known by the **Family** and **Family ID** fields. These fields are read only in the Control form.

        The **Control allocation** list in the authorization package overview page displays the controls grouped by their families segregated into system specific and hybrid.

10. Select **Add** to add the selected control objectives to the baseline controls.

    **Note:** When adding control objectives, you cannot select multiple control objectives with the same reference ID to add to the baseline controls. You cannot add a control objective if its reference ID already exists in the baseline controls list.![Selecting multiple control objectives.](../image/add-baseline-controls-auth-pack.png)

11. To inherit the requirements for a baseline control, select only one control objective in the **Baseline Controls** tab.

    You must have one self implemented requirement and the remaining requirements can be inherited from common control providers.

    The package must be in the **Select** state. Only common control providers with control requirements can be used to create hybrid controls.

    1.  Select **Create Hybrid**.

        The Create Hybrid Control pop-up lists the packages in groups.

        ![Create hybrid control popup.](../image/cam-ws-create-control-hybrid.png)

    2.  Enter a package in the **Authorization Package \(Optional\)** field.

        You can enter all the packages that you require, from which you can select the requirements.

    3.  Select the requirements from the package groupings, leaving one or more requirements for self implementation for that control.

        You’re creating a hybrid control, for which the requirement is inherited from the package that you selected.

    4.  Select **Add**.

12. To navigate to the associated control objective, select the link to the control objective in the sidebar.

    The Reference for the control objective, sourced by NIST, is captured as **Source ID** in the header of the control objective.

    The controls are grouped as a **Family**, and abbreviated with an ID that is defined as **Family ID**. These fields are editable and help you to identify the group to which the control belongs and are used in the Control allocation section for reporting purpose. The content for Family and Family ID is updated based on NIST 800-53. For more information, see [Control Requirement Details View](../../grc-cam/reference/cam-cr-control-form.md).

    1.  Select the Related control objectives related list.

        All control objectives that have an impact in the implementation of the package but belong to different families are grouped as Related control objectives. These control objectives are sourced by NIST. All related controls in a package based on the mapped control objectives are linked as Related control objectives.

        Related controls related list contains controls from the related control objective with the same entity.

    2.  To add related control objectives, select **Add**.

    3.  Select the control objectives and select **Add**.

        The list shows those control objectives that aren’t already added to the related control objectives list of the package.


-   **[Apply overlays to the baseline controls](apply-overlay-to-baseline.md)**  
You can include overlays to the baseline control objectives in the Authorization Package using either addition, subtraction, or a custom action.
-   **[Request control trailoring](../concept/request-control-trailoring.md)**  
Control tailoring requests enable you to modify the baseline controls for an authorization package after the Select step without reverting the package or disrupting ongoing assessments. You can add new controls, change control applicability status, or update hybrid and inherited control configurations while maintaining the current workflow step and preserving unaffected controls.

**Parent Topic:**[Continuous authorization and monitoring tasks in the CAM Workspace](../concept/cam-ws-continuous-auth-monitor.md)

