---
title: Connecting EAP with Collaborative Work Management
description: Enhance visibility and streamline planning for your Agile teams by connecting Enterprise Agile Planning \(EAP\) with Collaborative Work Management \(CWM\).
locale: en-US
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2025-11-18"
reading_time_minutes: 3
breadcrumb: [Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Connecting EAP with Collaborative Work Management

Enhance visibility and streamline planning for your Agile teams by connecting Enterprise Agile Planning \(EAP\) with Collaborative Work Management \(CWM\).

## Overview of EAP-CWM connection

The EAP-CWM integration enables organizations to connect strategic program planning with team-level execution in a single system, eliminating silos and improving delivery predictability.

Using EAP, program managers and release train engineers can define Program Increment \(PI\) objectives, align Epics, Features, and Stories, create sprints for teams, and manage cross-team dependencies. After completing a PI, they can conduct PI retrospectives and update roadmaps for the next cycle. These capabilities ensure that enterprise priorities are clearly structured and traceable across all levels.

By linking EAP to CWM, product owners and team members can plan and execute sprints, manage agile stories alongside operational tasks such as incidents, track progress, and hold team-level retrospectives, all within the same workspace.

This connection between the applications reduces context switching and ensures that both planned and unplanned work is accounted for, without losing alignment to strategic goals. The result is end-to-end transparency where leadership can track progress against PI goals through EAP, while teams maintain flexibility to adapt to changing priorities.

## Workflow of EAP-CWM integration

1.  EAP admin connects an EAP team to CWM. See [Connect an EAP team with CWM](../task/connect-an-eap-team-with-cwm.md).
2.  A new Space and Board are created for this EAP team in the CWM workspace.
3.  Existing work items assigned to this EAP team are brought over to the newly created CWM Board through Connected Work filters.
4.  Sprint planning view is enabled for this CWM Board where the existing work items and sprints are automatically shown.
5.  Check team's access to CWM and provide the CWM user \[sn\_cwm.cwm\_user\] to all team members.
6.  EAP team can start creating more work, manage current work, and update progress directly from the CWM Board. See [Sprint planning in CWM](../../collab-work-mgmt/concept/agile-sprint-planning-in-cwm.md).
7.  The team's progress and work status is reflected back on the Team dashboard in the EAP workspace. See [EAP Agile Team dashboard](eap-agile-team-dashboard.md)

## Creating or managing sprints for EAP teams in CWM

For EAP teams integrated with CWM, existing sprints and their scheduled work automatically sync to CWM. These details are displayed in the Sprint Planning view on the CWM Board.

As the team progresses through assigned work, they can update the work status directly in the Sprints section. The sprint can be marked **Complete** from this view and any incomplete work items can be moved either to the backlog or the next sprint, if it exists.

New sprints for the team must be created in EAP. After creating new sprints in EAP, they will sync to CWM, allowing the team to schedule work into these sprints from CWM.

**Note:** Sprints for EAP teams are not created directly at the Agile team level. Sprints are created automatically when a Planning Interval \(PI\) is defined for the parent Agile Release Train \(ART\) in EAP and sync to CWM automatically.

![Sprint planning view for EAP teams in CWM.](../images/eap-cwm-sprints.png)

**Related topics**  


[Collaborating with Spaces in CWM](../../collab-work-mgmt/concept/cwm-spaces.md)

[Managing work using Boards in CWM](../../collab-work-mgmt/concept/cwm-boards.md)

[Connected work in CWM](../../collab-work-mgmt/concept/unified-boards-for-connected-work-in-cwm.md)

[Sprint planning in CWM](../../collab-work-mgmt/concept/agile-sprint-planning-in-cwm.md)

[EAP Agile Team dashboard](eap-agile-team-dashboard.md)

