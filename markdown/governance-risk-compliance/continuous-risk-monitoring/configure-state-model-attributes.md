---
title: Add existing attributes to a GRC workflow state
description: Add existing Governance, Risk, and Compliance state model attributes to add special capabilities to workflow steps without custom code. Attributes control features like approval requirements, report generation, and Open Security Controls Assessment Language \(OSCAL\) file exports for specific workflow states.
locale: en-US
release: yokohama
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 1
breadcrumb: [GRC state model configuration, CAM workflow configuration, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Add existing attributes to a GRC workflow state

Add existing Governance, Risk, and Compliance state model attributes to add special capabilities to workflow steps without custom code. Attributes control features like approval requirements, report generation, and Open Security Controls Assessment Language \(OSCAL\) file exports for specific workflow states.

## Before you begin

With CAM, you get the following attributes:

-   **Generate ATO Letter**: Generates Authority to Operate \(ATO\) letter document.
-   **Generate Executive Summary**: Generate an Executive Summary document.
-   **Generate OSCAL SSP**: Generate an OSCAL format System Security Plan \(SSP\).
-   **Generate POAM**: Generate a Plan of Action and Milestones \(POA&amp;M\) document.
-   **Generate SAP**: Generate a Security Assessment Plan \(SAP\) document.
-   **Generate SAR**: Generate a Security Assessment Report \(SAR\) document.
-   **Generate SSP**: Generate a System Security Plan \(SSP\) document.
-   Required approval: Requires approval before proceeding to the next step.

**Note:** To configure state model attributes with the CAM specific attributes, perform the tasks in this topic. To create a new state model attribute, see [Create a new state model attribute](configure-new-state-model-attributes.md).

Role required: sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization and Monitoring** &gt; **Administration** &gt; **GRC State Models**.

2.  Open the state model record that contains workflow states.

3.  On the **GRC workflow states** related list, select the workflow state for which you want to add the existing attribute.

4.  On the selected workflow state record, select **State Model Attributes** tab.

    ![State model attributes tab.](../image/WF-state-edit-attributes2.png)

5.  To add the existing attributes, select **Edit**.

6.  Select attribute from the **Collection** list.

    ![Editing state model attribute.](../image/WF-state-edit-attributes1.png)

7.  Select the right arrow icon \(&gt;\) to move selected attribute to the **State Model Attributes List** on the right.

8.  To remove an attribute, select attribute in the **State Model Attributes List** on the right panel and select the left arrow icon \(&lt;\).

9.  Select **Save** to save the attribute.


## Result

State model attributes are configured and control the functionality available at specific workflow steps. You can see the appropriate buttons and features based on the attributes assigned to each workflow state.

