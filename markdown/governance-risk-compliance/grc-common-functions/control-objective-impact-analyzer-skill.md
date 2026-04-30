---
title: Control Objective Impact Analyzer skill
description: Explore the Control objective impact analyzer skill that evaluates citation updates and determines which associated control objectives require attention.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-11-19"
reading_time_minutes: 1
keywords: [Control Objective Impact Analyzer]
breadcrumb: [Explore, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Control Objective Impact Analyzer skill

Explore the Control objective impact analyzer skill that evaluates citation updates and determines which associated control objectives require attention.

The Control Objective Impact Analyzer skill is designed to identify which control objectives are affected when a citation is modified. This functionality analyzes updates to citation descriptions or supplemental guidance and determines the impacted control objectives.

## Association between control objectives and citations

Citations and control objectives have a many-to-many relationship:

-   A single citation can be linked to multiple control objectives.
-   Each control objective can be associated with multiple citations.

When a user updates a citation, the Control Objective Impact Analyzer evaluates these changes to determine which linked control objectives require attention.

## How the skill works

When a citation is modified, the Control Objective Impact Analyzer performs the following steps:

1.  Analyzes citation details: The skill reviews the citation’s description and supplemental guidance to identify new or changed information.
2.  Evaluates associated control objectives: It then examines all control objectives linked to the modified citation, considering their descriptions, names, and supplemental guidance.
3.  Determines impacted control objectives: The skill identifies which control objectives are directly relevant to the changes. For instance, if a citation update adds details about password backup frequency, only control objectives pertaining to backup processes are identified.
4.  Generates impacted control objectives: The identified impacted control objectives are displayed in the **Change impacts** tab for user review.

After reviewing the impacted control objectives, users can trigger the Control Objective Change Agent to update descriptions and guidance as needed.

