---
title: Industrial Guided Tasks release notes
description: The ServiceNow Industrial Guided Tasks \(IGT\) application enables structured and guided execution of operational tasks using step-by-step digital workflows. IGT helps you maintain consistent work quality, safety compliance, and traceable execution. Industrial Guided Tasks is a new application in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Industrial Guided Tasks release notes

The ServiceNow® Industrial Guided Tasks \(IGT\) application enables structured and guided execution of operational tasks using step-by-step digital workflows. IGT helps you maintain consistent work quality, safety compliance, and traceable execution. Industrial Guided Tasks is a new application in the Australia release.

## Industrial Guided Tasks highlights for the Australia release

-   Design structured digital workflows faster with an enhanced guided task authoring experience.
-   Evaluate task outcomes accurately using a smart assessment engine with scoring rules, conditional logic, and validation.
-   Improve frontline execution with usability features such as barcode or QR scanning, step‑by‑step guidance, and offline support.
-   Track guided tasks through their full life cycle using intuitive workflow states that support clearer governance and audit readiness.
-   Extend task governance across the ICW suite through integrations with Industrial Standards, ICW Mobile, and ICW Core.

See [Exploring Industrial Guided Tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/exploring-industrial-guided-tasks.md) for more information.

**Important:** Industrial Guided Tasks is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Industrial Guided Tasks features

-   **[Authoring Guided Tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/task-authoring-configuration-settings.md)**

    Design structured workflows with sections, steps, assessments, and conditional paths by using an authoring interface that enforces consistency and quality.

    Built‑in rules help to maintain consistency by following correct steps sequence, naming, and safety requirements. Authors can preview the guided tasks’ end‑user experience before publishing.

-   **[Assessment-driven scoring, evaluation, and execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/scoring-industrial-guided-tasks.md)**

    Capture and evaluate task data by using multiple assessment types, including numeric inputs, selections, measurements, and conditional evaluations. Supports multiple assessment types including numeric inputs, selections, measurements, and conditional evaluations.

    Automatic scoring determines the following task outcomes based on configured thresholds: Successful, Unsuccessful, or Not Scored. Assessment data is captured for reporting, quality control, and continuous improvement.

-   **[Automation and Smart Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/industrial-guided-tasks-reference.md)**

    Reduce manual intervention by configuring automation features that trigger follow‑up work, standard tasks, or actions based on assessment results.

    Complex logic can route execution flows, creating dynamic experiences that adapt to operator input. This reduces manual intervention and maintains consistent responses to equipment or process conditions. You need an additional plugin to use this functionality.

    Template capabilities for duplication of task structures.

-   **[Easy accessibility and execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/execute-igt-icw-mobile.md)**

    Execute guided tasks through a clean step‑by‑step interface that supports images, instructions, validations, and attachments for accurate task completion.

    Integrated barcode or QR scanning helps identify parts, equipment, or materials during task execution.

    Offline access to guided tasks in the ICW mobile application. Offline mode minimizes interruption in your work, even in low‑connectivity industrial environments.

-   **[IGT Lifecycle Governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/industrial-guided-task-life-cycle.md)**

    Govern your guided tasks through separated life-cycle states that provide clearer oversight and a better audit trail.

    Review and approval workflows helps in maintaining quality, safety, and operational standards of guided tasks before release. Historical versions are archived for audits, root cause analysis \(RCA\) investigations, and long‑term reporting.

-   **[Create standards using templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/creating-standards-from-templates.md)**

    Accelerate guided task creation by duplicating existing tasks or using them as reusable templates.

    Structural components such as steps, assessments, and conditional logic can be reused across multiple workflows, which maintains consistency while reducing authoring time.


## Activation information

Industrial Guided Tasks is automatically installed when you install Industrial Connected Workforce Mobile Experience as part of the ICW Foundational SKU. You can request ICW Mobile from the ServiceNow Store.

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    Industrial Guided Task \(sn\_icw\_igt\): Contains the Industrial Guided Tasks application.


## Related ServiceNow applications and features

-   **[Industrial Connected Workforce Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/industrial-connected-workforce-core-landing-page.md)**

    ServiceNow® Industrial Connected Workforce \(ICW\) Core provides the foundational data models, workflows, and governance structures that power the entire Industrial Connected Workforce suite. ICW Core standardizes how organizations, equipment hierarchies, calendars, worker profiles, and industrial records are represented across applications. All other ICW applications rely on ICW Core for consistent execution, shared services, and data interoperability.

-   **[Industrial Standards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/industrial-standards-landing-page.md)**

    Industrial Standards enables organizations to define, publish, and manage operational standards such as standard operating procedures \(SOPs\), inspections, and CIL routines. Industrial Standards provides version control, reusable templates, and automated scheduling to maintain consistent and compliant work execution. Other ICW applications use these standards as the authoritative source for task generation and operational guidance.

-   **[Industrial Connected Workforce Mobile Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/icw-mobile-exp-landing-page.md)**

    Industrial Guided Tasks \(IGT\) provides the structured, step‑by‑step workflows that operators execute on the shop floor using the ICW Mobile. It acts as the primary execution channel for IGT, enabling workers to perform guided tasks with features like barcode/QR scanning, offline support, and attachment capture. In this way, ICW Mobile makes sure that the detailed guidance authored in IGT reaches frontline workers in a format optimized for real‑world industrial environments.


**Parent Topic:**[Industrial Connected Workforce release notes](industrial-connected-workforce-rn-landing.md)

