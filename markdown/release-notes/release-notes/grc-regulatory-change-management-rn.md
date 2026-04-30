---
title: Regulatory Change Management release notes
description: The ServiceNow Regulatory Change Management application enables you to check upcoming regulatory changes, assess their impact, and implement risk and compliance-related changes. Regulatory Change Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-08-25"
reading_time_minutes: 5
---

# Regulatory Change Management release notes

The ServiceNow® Regulatory Change Management application enables you to check upcoming regulatory changes, assess their impact, and implement risk and compliance-related changes. Regulatory Change Management was enhanced and updated in the Zurich release.

## Regulatory Change Management highlights for the Zurich release

-   Add multiple regulatory tasks or source document import tasks to a regulatory alert to manage the associated compliance activities efficiently. You can help to ensure that each task aligns with the regulatory requirements to maintain structured tracking and accountability.
-   Close a regulatory task during the Implementation state after you verify that all required actions and documentation are complete. You can also confirm that no pending activities remain before you close a task.
-   Change the workflow of a regulatory task to reflect the updated compliance procedures or organizational processes.
-   Create action tasks when a regulatory task is in the New, Work in Progress, or Implementation states to drive progress. You can also assign responsibilities to help ensure that the compliance actions are executed in a timely manner.
-   Close regulatory alerts manually when all associated tasks and compliance obligations have been successfully addressed. You can verify that each related item meets the closure criteria before confirming that the alert is resolved.

See [Regulatory Change Management](https://www.servicenow.com/docs/access?context=reg-change-mgmt-landing-page&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) for more information.

**Important:** Regulatory Change Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Now Assist for Integrated Risk Management \(IRM\)](now-assist-for-irm-rn.md)**

    You can review the Now Assist for Integrated Risk Management \(IRM\) release notes for full descriptions of the Now Assist in Regulatory Change Management \(RCM\) features.

-   **[Add multiple regulatory tasks](https://www.servicenow.com/docs/access?context=regulatory-change-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Add multiple regulatory tasks to an alert. Each task can represent a distinct area of impact or required action. By organizing work into separate change tasks, your teams can assign responsibilities, track progress, and manage dependencies more effectively.

-   **[Add multiple source document import tasks](https://www.servicenow.com/docs/access?context=source-document-import-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Associate multiple source document import tasks with one regulatory alert to simplify the management and tracking of your regulatory content ingestion. Each import task adds the relevant documents to the regulatory library to help ensure that all source materials that are related to the alert are accurately captured and organized. You can help to improve traceability throughout the regulatory change management process.

-   **[Close a regulatory task](https://www.servicenow.com/docs/access?context=regulatory-change-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Close a regulatory task automatically when it's approved. You can also manually close a regulatory task while it's in the Implementation state, if all the associated action tasks are completed and closed. By closing a task manually, you get flexibility in managing the regulatory changes that don’t require formal approval workflows.

-   **[Reopen action tasks](https://www.servicenow.com/docs/access?context=action-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Reopen the action tasks for a regulatory task when it's rejected and transitions back to the Implementation state. You can review and rework the tasks to address the feedback or incorporate the updated requirements. You can also modify and resubmit the reopened action tasks so that the implementation aligns with regulatory expectations before you resubmit the change task.

-   **[Close a regulatory alert](https://www.servicenow.com/docs/access?context=list-view-of-reg-alerts&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Close a regulatory alert manually after all the associated regulatory tasks are complete. By closing the alert, you help to ensure accurate record-keeping by signaling that a compliance life-cycle for the specific regulatory alert is complete.

-   **[Work on action tasks](https://www.servicenow.com/docs/access?context=action-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Initiate and complete the action tasks independently without requiring prior approval from users who are assigned with the `sn_grc_reg_change.manager` role. You can execute assigned responsibilities in a timely manner and reduce unnecessary approval bottlenecks. The access to action tasks remains governed by user permissions and role-based access controls to ensure proper accountability and oversight.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Default column list](https://www.servicenow.com/docs/access?context=action-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Starting with the Zurich release, the default column configuration for regulatory tasks and action tasks, linked to a regulatory alert, has been updated. This change enhances usability and ensures better visibility of the key information that is relevant to each task type.


## Changed in this release

-   **Administrator role enhancements**

    After upgrading to version 21.1.x, if you have a feature admin role you can now complete tasks that were initially reserved for users with the broader administrator role.

-   **Read-only field enhancements**

    Starting with version 21.1.x, the following Regulatory Change Management plugins have security enhancements for read-only fields in this release:

    -   GRC: Taxonomy management \[com.sn\_grc\_taxonomy\]
    -   GRC: Regulatory Change Management integration with RSS Feeds \[com.sn\_grc\_rcm\_rssfeed\]
    -   GRC: Regulatory Change Management \[com.sn\_grc\_reg\_change\]
    -   GRC Case Management Core \[com.sn\_grc\_case\_mgmt\]
    -   GRC integration with Thomson Reuters Regulatory Intelligence \[com.sn\_grc\_int\_tr\]
    -   Regulatory Agency Library \[com.sn\_reg\_body\_mgmt\]
-   **[Tasks widget](https://www.servicenow.com/docs/access?context=list-view-of-reg-alerts&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    The overview page of a regulatory alert includes a newly added Tasks widget that enables you to get more visibility into related activities. This widget displays the total number of associated action tasks and change tasks that are linked to the specific regulatory alert. By using this widget, you can assess the level of effort that is required for compliance.

-   **[Workflow of regulatory task](https://www.servicenow.com/docs/access?context=reg-change-task&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    A regulatory task progresses through the following states:

    -   New
    -   Work In Progress
    -   Implementation
    -   Awaiting Approval \(optional\)
    -   Completed
    While in the Implementation state, requesting approval is optional. If all associated action tasks are completed, the regulatory task can be closed directly from the Implementation state without requiring additional approval.

-   **[Workflow of source document import task](https://www.servicenow.com/docs/access?context=reg-change-task&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    A source document task progresses through the following states:

    -   New
    -   Ready to Import
    -   Work In Progress
    -   Implementation
    -   Completed.
-   **[Create action tasks](https://www.servicenow.com/docs/access?context=manage-reg-action-tasks&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    You can create action tasks for a regulatory task when the task is in any of the following states:

    -   New
    -   Work in Progress
    -   Implementation
    You can now break down a regulatory task into smaller, manageable components so that you can more efficiently track and execute the required activities. You can plan, assign, and monitor tasks now in a structured manner that supports your compliance objectives and regulatory requirements.


## Activation information

Install Regulatory Change Management and Now Assist for IRM by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Governance, Risk, and Compliance release notes](grc-rn-landing.md)

