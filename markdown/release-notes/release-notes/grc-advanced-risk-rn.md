---
title: Advanced Risk release notes
description: The ServiceNow Advanced Risk application enables you to identify, analyze, evaluate, treat, and monitor risks that could impact your organization in achieving its business objectives. Advanced Risk was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
---

# Advanced Risk release notes

The ServiceNow® Advanced Risk application enables you to identify, analyze, evaluate, treat, and monitor risks that could impact your organization in achieving its business objectives. Advanced Risk was enhanced and updated in the Xanadu release.

## Advanced Risk highlights for the Xanadu release

-   Create multidimensional entities by combining two or more entities from different entity classes and manage risks and controls for such composite entities.
-   Perform assessment on multiple risks and controls by creating a risk assessment project.
-   Use a uniform workflow for all types of risk response strategies, enable dynamic approvals using GRC: Approver Configurator, and create multiple strategies with various action items for each risk response plan.
-   Link the open risk response tasks or copy the tasks along with the risk response strategy from the previous assessment when reassessing the risk.
-   Create an issue or link an existing open issue as an outcome of the risk assessment.
-   Respond to risk identification questionnaires with an improved user experience using Smart Assessment Engine.
-   Reopen closed risk events to identify and address overlooked or underestimated risks, updating existing risk events instead of creating new risk events.

See [Advanced Risk Assessment](https://www.servicenow.com/docs/access?context=advanced-risk-assessment&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Advanced Risk is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Create multidimensional entities](https://www.servicenow.com/docs/access?context=create-composite-entity-ws&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Create multidimensional entities by combining two or more entities from different entity classes using the Composite Entity Management application. You can create multidimensional entity classes with a composite entity structure, such as Company \| Department \| Business Process. After defining the composite entity class, you can create composite entity that operates as a standalone entity. This feature enables you to manage risk and compliance workflows at the composite entity level, providing visibility into the combined risk and compliance posture.

    **Note:** Composite entity classes can be created in both the classic UI and the Risk Workspace. The creation of composite entities is supported only in Risk Workspace.

-   **[Assess multiple risks and controls simultaneously](https://www.servicenow.com/docs/access?context=risk-assessment-project&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Create a risk assessment project to perform bulk assessments on multiple risks and controls, enabling assessors to evaluate them in a single project. This approach reduces time and effort, confirms consistency across multiple assessments, and provides a more comprehensive view of risks and controls within the same project. You can scope multiple risks related to the assessable entity within the project and perform assessments.

    **Note:** Assessment of multiple risks and controls is supported only in Risk Workspace.

-   **[Addition of new roles](https://www.servicenow.com/docs/access?context=risk-assessment-project&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    The following roles related to risk assessment project were added:

    -   Risk assessment project reader \[sn\_risk\_advanced.risk\_asmt\_project\_reader\]: Provides read only access to the risk assessment projects.
    -   Risk assessment project user \[sn\_risk\_advanced.risk\_asmt\_project\_user\]: Provides the ability to create risk assessment projects and update or delete only the projects created by the user.
    -   Risk assessment project manager \[sn\_risk\_advanced.risk\_asmt\_project\_manager\]: Provides the ability to create, update, and delete any risk assessment projects.
-   **[Enhanced risk response workflow](https://www.servicenow.com/docs/access?context=workflow-of-risk-response-task&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Streamline your risk response workflow with the following enhancements:

    -   Use a uniform workflow for all types of risk response tasks. A standardized workflow for risk response tasks enhances the management of all types of risk response tasks, promotes consistency, and reduces the need for customization.
    -   Configure multiple levels of approvals for the risk response tasks using the approval configurator. By default, a single level of approval is enabled for all types of risk response tasks, where the risk owner can approve the tasks. These approvals can be configured based on requirements.
    -   Reject a risk response task and move it to the work in progress state without closing it. This feature helps the risk response task owner to modify the response strategy if the approver is unsatisfied with the response.
    -   Create action items with an independent workflow and link them to the risk response tasks when they are in the Draft or Work in progress state.

        **Note:** You can create risk response action items for all types of risk responses except for Risk acceptance tasks.

    -   Copy risk response plans from the previous risk assessment to the current risk assessment while reassessing.
    -   Link an open risk response task from the previous assessment to the current risk assessment while reassessing. You can also edit or remove an existing risk response task.
-   **[Issue linking with risk assessments](https://www.servicenow.com/docs/access?context=perform-ara-workspace&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Streamline your risk assessments with the following enhancements:

    -   Enable the issue linking option on the Risk Assessment Methodology \(RAM\) form to create an issue or link an existing open issue with the risk assessment.
    -   View issue details from the configurable issue card available on the risk assessment.
    -   Identify newly created issues from existing linked issues with a visual differentiator on the issue card.
    -   Edit or remove issues.
-   **[Enhanced risk event task workflow](https://www.servicenow.com/docs/access?context=manage-risk-events&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Streamline your risk event workflow with the following enhancements:

    -   Use a uniform and enhanced workflow for the risk event tasks. A standardized workflow enhances the management of risk event tasks.
    -   Configure multiple levels of approvals for the risk event tasks using the approval configurator.
    -   Reject a risk event task and move it to the work in progress state without closing it. This feature helps the risk event task owner to modify the risk event if the approver is unsatisfied.
-   **[Improved user experience for risk identification questionnaire using Smart Assessment Engine](https://www.servicenow.com/docs/access?context=configure-risk-identification-form&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Respond to the risk identification questionnaires from the [Assessment Workspace](https://www.servicenow.com/docs/access?context=sae-asmnt-workspace&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US) with an interactive and intuitive user experience. Risk admin can select between classic and smart assessment questionnaire in the risk identification configuration without making it a forced behavior. You can migrate an existing risk identification template to the Smart Assessment Engine application. You can also create risk identification templates in the [Assessment Workspace](https://www.servicenow.com/docs/access?context=sae-asmnt-workspace&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

    **Note:** Only published assessment templates with a Risk Identification category are available for selection on the Risk Identification Configuration form.

-   **[Configuring currency conversion dates](https://www.servicenow.com/docs/access?context=advanced-risk-properties&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Define currency conversion dates for the risk event entries in the system properties. This feature enhances the accuracy of net loss calculations by enabling you to select specific dates for currency conversion rather than relying solely on the date of impact. You can select a currency conversion date at the system property level from the following options:

    -   Risk event entry date
    -   First loss entry date
    -   Last loss entry date
    -   First recovery entry date
    -   Last recovery entry date
    -   Custom date
    **Note:** You can also override the defined currency conversion dates in the risk response template configuration. These changes apply to both new and ongoing risk event workflows.

-   **[Reopen closed risk events](https://www.servicenow.com/docs/access?context=reopen-a-risk-event&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Reopen closed risk events to update existing risk events with new discoveries, losses, or relevant information without creating new risk events. This feature saves time and effort, offering flexibility and boosting efficiency in managing risk events. You can reopen a risk event individually or in bulk.

-   **Miscellaneous enhancements and improvements**

    Streamline your processes with the following enhancements:

    -   Notify the risk assessor with a notification email when a risk assessment is approved or rejected.
    -   Define a specific group as the respondent type in the Feedback Integration Configuration form when the target record doesn't have a user or group. For more information, see [Configure a feedback integration](https://www.servicenow.com/docs/access?context=configure-feedback-integration&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).
    -   Configure a single currency mode for advanced risk assessments. This feature displays all financial values in the selected single currency, confirming consistency and clarity in all fields. For more information, see [Single-currency mode](https://www.servicenow.com/docs/access?context=single-currency-mode&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
    -   View the completion date of the most recent risk identification in the new field **Last completed date**, added to the Risk Identification form. For more information, see [Set up risk identification integration](https://www.servicenow.com/docs/access?context=configure-risk-identification-form&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

## UI changes

-   **Risk assessment column labels**

    The following risk assessment column labels were renamed to avoid any confusion caused by duplicate names:

    -   Computed control effectiveness \(control\_computed\_effectiveness\) was renamed Computed control effectiveness rating.
    -   Computed inherent risk \(inherent\_computed\_risk\) was renamed Computed inherent rating.
    -   Computed residual risk \(residual\_computed\_risk\) was renamed Computed residual rating.
    -   Computed target risk \(target\_computed\_risk\) was renamed Computed target rating.
    -   Control effectiveness \(summary\_control\_effectiveness\) was renamed Control effectiveness rating.
    -   Control effectiveness when overridden \(control\_effectiveness\_when\_overridden\) was renamed Control effectiveness rating when overridden.
    -   Inherent risk \(summary\_inherent\_risk\) was renamed Inherent rating.
    -   Override computed score \(override\_calculated\_inherent\_score\) was renamed Override computed inherent score.
    -   Override computed score \(override\_calculated\_residual\_score\) was renamed Override computed residual score.
    -   Override computed score \(override\_calculated\_target\_score\) was renamed Override computed target score.
    -   Residual risk \(summary\_residual\_risk\) was renamed Residual rating.
    -   Residual risk when overridden \(residual\_risk\_when\_overridden\) was renamed Residual rating when overridden.
    -   Target risk \(summary\_target\_risk\) was renamed Target rating.
    -   Target risk when overridden \(target\_risk\_when\_overridden\) was renamed Target rating when overridden.
    -   Comments \(target\_justification\) was renamed Comments for target risk.
    -   Comments \(inherent\_justification\) was renamed Comments for inherent risk.
    -   Comments \(control\_justification\) was renamed Comments for control effectiveness.
    -   Comments \(residual\_justification\) was renamed Comments for residual risk.
    -   Comments \(approver\_comments\) was renamed Approver comments.
    -   Comments \(risk\_response\_justification\) was renamed Comments for risk response.

## Deprecations

-   The Risk portal has been deprecated, and a navigation link has been added to access the new Risk portal.

## Activation information

Install Advanced Risk by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[GRC Risk Management](https://www.servicenow.com/docs/access?context=grc-risk-overview&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    Use the Risk Management with the ServiceNow® Advanced Risk application to identify and monitor high-impact risks, improve your risk-based decision-making, and reduce reaction time from days to minutes.

-   **[GRC Risk Workspace](https://www.servicenow.com/docs/access?context=risk-workspace&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US)**

    The Risk Workspace with the ServiceNow® Advanced Risk application provides a simplified user experience with a single-pane view for all your risk-related activities.


**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

