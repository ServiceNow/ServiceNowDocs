---
title: Apply overlays to the baseline controls
description: You can include overlays to the baseline control objectives in the Authorization Package using either addition, subtraction, or a custom action.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [View package details in CAM Workspace, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Apply overlays to the baseline controls

You can include overlays to the baseline control objectives in the Authorization Package using either addition, subtraction, or a custom action.

## Before you begin

Role required: sn\_irm\_cont\_auth.authorization\_official, sn\_irm\_cont\_auth.information\_owner, sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.info\_system\_sec\_officer, sn\_irm\_cont\_auth.sec\_control\_assessor, sn\_irm\_cont\_auth.system\_owner, sn\_irm\_cont\_auth.scheduler, sn\_irm\_cont\_auth.system\_user, sn\_irm\_cont\_auth.executive\_read, and sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **CAM Workspace**.

2.  To navigate to the Lists page, select the lists icon \(![Lists icon](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  From the Authorization packages in the RMF list, select an authorization package record.

4.  Select **Overlays** to Add, Edit, or Remove the overlays to the Authorization Package.

    The Authorization Package must be in the **Select** step to add policies to overlays.

    1.  Select **Add** to add a policy to the overlay.

        The **Add overlay** pop-up window appears.

    2.  Enter at least two characters in the **Policy** field to view and select from the list of available policies.

        **Note:** Only policies with the source CAM: Control Overlay, that are in the Published state, and that contain control objectives will appear in the **Policy** drop-down field.

        ![Adding overlay.](../image/auth-package-add-overlay-page.png)

    3.  Choose one of the following actions to apply the overlay to the Authorization Package.

        -   **Addition**: Select addition to add the control objectives from the policy to the baseline controls.

            **Note:** All control objectives are added based on their reference ID.

            -   If a control objective with the same reference ID already exists in the baseline controls, the **Behavior** will be set to **Matching** and the **Action** will be **Skip**. The skip action will not add any control objectives to the baseline controls from the overlay policy that you selected.
            -   If the overlay policy contains a control objective with a reference ID that differs from the baseline control, the **Behavior** will be set to **Distinct** and the **Action** will be **Create new**. The new control objective\(s\) from the overlay policy is added to the baseline control with the source as Control Overlay.![Policy added to the overlay.](../image/auth-package-overlay-addition-page.png)
        -   **Subtraction**: Select Subtraction to move control objectives with matching reference IDs between the selected overlay policy and the baseline controls to the Not Applicable Controls state.

            **Note:**

            -   If a control objective with the same reference ID already exists in the baseline controls:

                -   **Behavior** is set to **Matching**
                -   **Action** is **Move to N/A**

                    These matching control objectives between the selected overlay and the baseline controls will appear in the **Not Applicable Controls** tab.

                    In this scenario, the source of the baseline control remains the same. The justification field of baseline control is updated to indicate this change.

                    You can also manually select control objectives in the **Not Applicable Controls** tab and use **Return to Baseline Control** to move them back to the baseline controls in the authorization package.

                ![Policy moved to NA.](../image/auth-package-overlay-subtraction-page.png)

            -   If the overlay policy contains a control objective with a reference ID that differs from the baseline control:
                -   **Behavior** is set to **Distinct**
                -   **Action** is **Skip**

                    The skip action will not move any control objectives to the not applicable state from the baseline controls.

        -   **Custom Action**: Select **Custom Action** following are the available actions:
            -   **For matching records** \(the reference ID is same as in the baseline controls and the selected overlay policy\):

                -   **Override**: Replaces the baseline control objective with the one from the selected overlay policy.
                -   **Move to N/A**: Moves the control objective with the matching reference ID to the Not Applicable state.
                -   **Skip**: Ignores the matching record; no changes will be made to the Authorization Package from the selected policy.
                ![Custom matching records.](../image/auth-package-custom-overlay-matching-page.png)

            -   **For distinct records** \(reference ID does not exist in baseline controls\):

                -   **Create new**: Adds the new control objective from the selected overlay policy to the Authorization Package.
                -   **Skip**: Ignores the distinct record; it will not be added to the Authorization Package.
                ![Custom distinct records.](../image/auth-package-custom-overlay-distinct-page.png)

        **Note:** For existing baseline controls, if the overlay policy contains a Hybrid, Inherited, or Common control objective, the action will be skipped by default. The behavior will also be Hybrid, Inherited, or Common accordingly.

    4.  Select **Edit** from the **Overlay Controls** list view page to modify an overlay available in the list.

        **Note:** Only listed overlays can be edited. The previously selected policy action is applied by default, and you must select a different operation to proceed with the update.

    5.  Click **Submit** to apply the **Addition**, **Subtraction**, or **Custom Action** operation on the policy.


**Parent Topic:**[View package details in CAM Workspace](auth-package-overview-ws.md)

