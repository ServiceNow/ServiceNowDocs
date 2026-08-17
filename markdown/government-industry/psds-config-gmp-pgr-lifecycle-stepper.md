---
title: Configure program lifecycle stepper
description: Control the visibility of the program lifecycle stepper on the Grant Program record page. The stepper is turned off by default and can be enabled at the instance level for deployments that follow a batch or competitive grant lifecycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-gmp-pgr-lifecycle-stepper.html
release: australia
topic_type: task
last_updated: "2026-06-23"
reading_time_minutes: 3
keywords: [program lifecycle stepper, grants management, stepper configuration]
breadcrumb: [Set up a grant program, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure program lifecycle stepper

Control the visibility of the program lifecycle stepper on the Grant Program record page. The stepper is turned off by default and can be enabled at the instance level for deployments that follow a batch or competitive grant lifecycle.

## About this task

The program lifecycle stepper displays six steps on the Grant Program record page: Preparing Program, Accepting Proposals, Evaluating, Awarding, Post-Award, and Closed. Each step reflects a stage in the grant program lifecycle. The steps advance automatically based on the program state. The stepper is turned off by default for all new and existing grant programs. An admin can enable the stepper by toggling on the Grant program Stepper system property for deployments where staged progression through the steps is meaningful.

When the stepper is enabled, all existing stepper behavior is preserved. When the stepper is turned off, no stepper component is rendered on the Grant Program record and the Grant Program playbook views.

Steps 1 through 4 advance automatically based on the program state. Steps 5 and 6 are inactive from Grants management version 1.41 onward. The steps in order are:

1.  Preparing Program
2.  Accepting Proposals
3.  Evaluating
4.  Awarding
5.  Post-Award \(inactive\)
6.  Closed \(inactive\)

Each step has one of the following display states:

-   **None**: The step hasn't started.
-   **Partial** \(Highlighted\): The step is in progress. This is the current active step.
-   **Done** \(Checkmark\): The step is complete. The program has advanced past this step.

\[Omitted image "psds-gm-stepper.png"\] Alt text: Grant program lifecycle stepper

The steps advance automatically based on the program state.

-   **Preparing Program**: The stepper displays Step 1 as partial \(in progress\) when the grant program state is `draft`. All other steps remain in the "None" state. This is the default display state when no valid program record is found.
-   **Accepting Proposals**: The stepper advances to Step 2 when the grant program state changes to `accepting_applications`. Step 1 is marked as done and Step 2 displays as partial.
-   **Evaluating**: The stepper advances to Step 3 when the grant program state changes to `applications_closed` and merit reviews take place. Steps 1 and 2 are marked as done and Step 3 displays as partial.
-   **Awarding**: The stepper advances to Step 4 only when the program state is `applications_closed` and all linked merit review tasks have reached a final state. The system checks every task for each proposal linked to the grant program and verifies that proposal's merit review task is in a final state. If all merit review tasks are final, Steps 1 through 3 are marked as done and Step 4 displays as partial. If even one merit review task remains open across the entire grant program, the stepper stays in step 3. At this stage, all the proposals are in the `ready_for_proposal` state.
-   **Post-Award** and **Closed** steps are turned off in the stepper UI as they are reserved for future use.

**Note:**

The configuration scope is per instance and not per individual grant program.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Public Sector Workspace**.

2.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

3.  Select **sn\_svc\_appl\_pgm\_mg.admin**.

4.  In the **Value** field, enter `true`.

5.  Select **Update**.


## Result

The program lifecycle stepper is now visible on all Grant Program record pages in the instance. The stepper displays the current program state: Preparing Program, Accepting Proposals, Evaluating, Awarding, Post-Award, and Closed.

**Parent Topic:**[Set up a grant program in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-config-gmp-grant-pgr.md)

**Previous topic:**[Configure the Spending Overview Widget and Filter pills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-gm-config-spending-overview-widget.md)

**Next topic:**[Install and configure the Social Benefits Playbook application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/configuring-social-benefit-playbook.md)

