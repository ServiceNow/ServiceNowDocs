---
title: Regulatory change tasks
description: When a regulatory alert is marked as applicable by the alert coordinator, manager, or administrator, the system initiates the creation of a regulatory change task. This task serves as a central point for stakeholders to determine the necessary modifications to organizational compliance practices.
locale: en-US
release: zurich
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Regulatory change tasks

When a regulatory alert is marked as applicable by the alert coordinator, manager, or administrator, the system initiates the creation of a regulatory change task. This task serves as a central point for stakeholders to determine the necessary modifications to organizational compliance practices.

The regulatory change task provides a structured process for evaluating regulatory updates and initiating corrective actions. Stakeholders use this task to identify what changes are required, which leads to the creation of one or more Action tasks. These action tasks represent the specific activities needed to implement the changes, such as updating relevant policies, controls, or risk statements within the regulatory library.

Each regulatory change task contains related [action tasks](action-tasks.md). The action tasks get created to fulfill the identified requirements. This hierarchical relationship ensures traceability and accountability throughout the change implementation process.

If you have the `sn_grc_reg_change.manager` role, you can assign regulatory change tasks to users with the `sn_grc_reg_change.user` role. The task includes key information such as the assigned group, the designated assignee, the approver, and other essential task details.

You can create multiple regulatory change tasks for a single regulatory alert. Each task can represent a distinct area of regulatory impact or a specific category of required action. This approach enables organizations to break down complex regulatory updates into manageable workstreams.

Organizing work into separate regulatory change tasks enables teams to assign responsibilities more accurately based on specific subject matter expertise. This structure enables clear monitoring of progress on each individual task component. Separate regulatory change tasks help identify and manage dependencies between related activities more effectively.

A structured task distribution improves collaboration across teams and ensures accountability throughout the process. This approach also supports the timely completion of all required compliance actions. Linking multiple regulatory change tasks to a single regulatory alert improves traceability across all related activities. This linking enables stakeholders to view how various aspects of the regulatory alert are being addressed.

A regulatory task gets closed automatically on approval, indicating that all required steps have been successfully completed. Alternatively, you can manually close a regulatory task while it is in the Implementation state when all associated action tasks have been completed and closed.

After completing all regulatory change tasks and their associated action tasks, you can close the related regulatory alert. Closure of the alert confirms that all required compliance obligations have been successfully fulfilled.

## Types of regulatory tasks

The following types of regulatory tasks are available in Regulatory Change Management:

-   Business Change- for example, implementing a new process to comply with updated anti-money laundering regulations.
-   Citation Amendment- for example, updating legal references in internal documentation due to changes in data protection laws like GDPR.
-   Control Update- for example, modifying access control procedures to meet new cybersecurity compliance requirements.
-   Policy Revision- for example, updating the organization's privacy policy to reflect changes in consent requirements under new regulatory guidance.
-   Regulatory Reporting- for example, preparing and submitting revised financial disclosures to a regulatory authority in response to new reporting standards.
-   Training Revision- for example, updating employee training modules to include recent changes in workplace harassment laws.
-   Others-For example, establishing a new governance framework to manage cross-border data transfers in response to emerging regulatory expectations.
-   None- Tasks that don’t fall under any specific predefined category, such as preliminary research or administrative setup tasks.

## New workflow of a regulatory task

Upgrade the following applications to get the new workflow:

-   GRC: Common Workspace Elements \(`sn_grc_workspace`\)
-   GRC: Regulatory Change Management \(`sn_grc_reg_change`\)

Starting with version 21.0.x, a regulatory task progresses through the following states:

-   New- The action task has been created but hasn’t yet been reviewed or acted upon. This is the initial placeholder for the task. Usually, a compliance analyst or a regulatory coordinator is responsible for reviewing and validating the task.
-   Work in Progress- The task is under active assessment. The task owner is analyzing regulatory requirements and identifying impacted areas, business processes, or required changes. The task assignee performs analysis, coordinates with stakeholders, and prepares the task for implementation.
-   Implementation- The necessary changes identified \(for example, policy updates, control modifications, or training revisions\) are being implemented. Action tasks may be created and assigned to specific impacted areas. Usually, the business process owner executes required changes.
-   Awaiting Approval \(optional\)- The implementation is complete and pending review or formal approval by designated stakeholders. This stage may be skipped if approval isn’t required. An approver like compliance manager validates that the task was completed correctly and meets regulatory requirements.
-   Closed- The task has been reviewed \(if applicable\), and all necessary actions are completed. The task is formally closed. A compliance analyst confirms that closure criteria are met and updates task status.

While in the Implementation state, requesting approval is optional. If all associated action tasks are completed, the regulatory task can be closed directly from the Implementation state without requiring additional approval.

**Note:** After the upgrade:

-   The first approval of a regulatory task in the Awaiting Approval state moves the task into the Implementation state.
-   The first rejection of a regulatory task in the Awaiting Approval state moves the task into a Work In Progress state.

## Create action tasks

Starting with version 21.0.x, you can create action tasks for a regulatory task when the task is in any of the following states:

-   New- The regulatory action task has been newly created and is pending initial review or planning. You can create action tasks at this stage, for example, predefine tasks for anticipated impacted areas.
-   In Progress- The action task is actively being worked on, and it includes analysis, defining impacted areas, and assigning responsibilities. Action tasks can be created and linked during this stage as findings and required actions are identified.
-   Closed- The regulatory task has been completed and formally closed. However, retrospective action tasks can still be added, such as documentation updates or follow-up audits. You can still create action tasks at this stage, useful for tracking late or follow-up actions.

You can break down a regulatory task into smaller, manageable components so that you can more efficiently track and execute the required activities. You can plan, assign, and monitor tasks now in a structured manner that supports your compliance objectives and regulatory requirements.

For example, a new data privacy law requires updates across multiple departments. You break down the regulatory task into smaller components such as updating the privacy policy, revising employee training, and implementing new data access controls. This breakdown of tasks enables each team to track and complete their assigned tasks efficiently.

