---
title: Automation opportunities
description: LEAP groups similar incidents into automation opportunities and uses AI to generate resolution artifacts that help reduce manual effort and repeat incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/automation-opportunities.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2026-05-12"
reading_time_minutes: 1
keywords: [automation opportunities, LEAP, incident resolution]
breadcrumb: [Explore, Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# Automation opportunities

LEAP groups similar incidents into automation opportunities and uses AI to generate resolution artifacts that help reduce manual effort and repeat incidents.

An automation opportunity is a group of similar incidents that LEAP identifies through AI-driven analysis. For each group, LEAP generates resolution artifacts — such as resolution steps, knowledge base articles, problem records, and playbooks — that operators can use to resolve recurring incidents faster.

## Automation opportunity lifecycle

When the Group Action Framework \(GAF\) process re-runs, it can identify new patterns in incident data. If remapping is successful, LEAP archives automation opportunities that contain resolution steps and transfers their artifacts to newly identified opportunities. Archived automation opportunities are hidden by default in the user interface to help you focus on actionable opportunities.

The automation opportunity details page displays banner messages that indicate the archiving and remapping status:

-   Archived automation opportunities display a message indicating that artifacts were remapped to a new opportunity, with a link to the new opportunity
-   New automation opportunities that received artifacts display a message indicating the source archived opportunity, with a link to the archived opportunity

The Action Insights panel on the details page also shows the relationship between archived and new automation opportunities.

## Managing automation opportunities

The automation opportunity details page provides tools to review and act on identified opportunities. From this page you can:

-   Review the incidents grouped into the opportunity
-   Generate or regenerate resolution steps, knowledge base articles, problem records, and playbooks
-   Create sub-groups for large opportunities to produce more targeted resolutions
-   Track missed opportunities where automation artifacts were available but not used

