---
title: Guided Decision Playbook Migration
description: Guided decisions are an activity type within a playbook that presents users with a series of structured questions. Based on the user's answers, the decision branches to a recommended action — such as a resolution path, a next step, or an escalation.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-07-06"
reading_time_minutes: 3
keywords: [Guided decisions]
---

# Guided Decision Playbook Migration

Guided decisions are an activity type within a playbook that presents users with a series of structured questions. Based on the user's answers, the decision branches to a recommended action — such as a resolution path, a next step, or an escalation.

**Note:**

Guided Decision Trees are being replaced by Guided Decision Playbooks. When you migrate a tree, each piece of it becomes a specific Playbook activity. Understanding this mapping helps to review migrated playbooks and make sure everything converts as expected.

## GDT to activity mapping

A Guided Decision Tree has four main parts. Each one becomes an activity \(or activities\) in a Guided Decision Playbook.

**Decision Node becomes Questionnaire + Decision activities.**

A Decision Node is where the tree asks questions and branches based on the answers. In a playbook, this splits into two activities:

-   A Questionnaire activity collects the answers from the user.
-   A Decision activity routes the user down different paths based on those answers.

They are separate because playbooks separate the "asking" step from the "routing" step. The Questionnaire gathers the input. The Decision activity then evaluates that input and chooses which path to take next.

**Guidance Node becomes a Guidance activity**

A Guidance Node is where the tree shows the user advice, next steps, or an action to complete. In a playbook, this becomes a single Guidance activity. The activity points at the same guidance record the tree used, so the content written remains the same.

**Linking Node becomes a Launch Nested Playbook activity**

A Linking Node is where a tree references another tree—a nested tree. In a playbook, this becomes a Launch Nested Playbook activity. That activity launches the migrated playbook that corresponds to the tree you were linking to. If the linked tree hasn't been migrated yet, the migration utility handles it first, ensuring the nested launch points to an existing playbook.

**Output Node becomes a Set Playbook Outputs activity**

An Output Node is where a tree defines the final values it passes back \(its outputs\). In a playbook, this becomes a Set Playbook Outputs activity. Each output node gets converted, so the playbook produces the same output values the guided decision tree did.

**Paths become decision conditions**

Paths are the branches between nodes in a tree. They activate when conditions are met. In a playbook, each path becomes a branch on the Decision activity, and the condition logic is translated so the Decision activity knows when to take that branch.

## Migrated playbook structure

Every migrated playbook follows the same shape, whether it launches directly or runs nested inside another playbook, allowing the same field references to work at any depth.

Each migrated playbook starts with two inputs:

-   context\_record\_table\_name \(the table name of that record\)
-   context\_record\_sys\_id \(the sys\_id of the record running the playbook\)

The first activity in every migrated playbook is a Look Up Record activity. It takes those two inputs and turns them into an actual record object. Everything that comes after \(Questionnaire, Guidance, Decision activities\) reads field values from that record.

This is because a migrated playbook is standalone—it doesn't have a trigger record the way a guided decision tree does. Instead, it receives the record information as plain text strings \(the sys\_id and table name\), and the Look Up Record activity resolves them back into real data. Nested playbooks pass the same inputs straight through unchanged, allowing the same field references to work at any depth without special handling at any level.

**Note:**

Do not delete the Look Up Record activity, as downstream activities depend on it.

After migration, administrators can manually configure where the playbook renders \(Playbooks, Recommended Actions, Portal, etc.\), enable setting the Guided layout, and re-point Portal launches to the new playbook.

## Who uses them

When opening a draft playbook, the expected structure becomes clear—Decision Nodes appear as Questionnaire plus Decision activities, Guidance Nodes become Guidance activities, nested links become Launch Nested Playbook activities, and the Look Up Record activity sits first. Understanding the migrated playbook structure allows you to validate the conversion worked correctly and identify any issues that need manual fixes.

-   **For administrators and implementation partners:** This mapping helps when reviewing migrated playbooks and validating that the conversion produced the expected result. If an implementation partner reviews a migrated playbook and notices a branch is missing a condition or a field reference didn't resolve, they can identify it, check the migration log, and the issue can be fixed manually before publishing.
-   **For agents, fulfillers, and technicians:** The playbook runs in Configurable Workspace. The migration preserves the functionality—the playbook works the same way as the tree it replaced, just built on the newer Playbook platform.

