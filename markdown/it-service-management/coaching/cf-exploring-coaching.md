---
title: Exploring Coaching
description: Review and assess the quality of your teams' completed interactions and tasks. Based on these assessments, you can assign course items for your teams. When they complete the training, the skills associated with it get added to their skills set.
locale: en-US
release: australia
product: Coaching
classification: coaching
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Coaching, IT Service Management]
---

# Exploring Coaching

Review and assess the quality of your teams' completed interactions and tasks. Based on these assessments, you can assign course items for your teams. When they complete the training, the skills associated with it get added to their skills set.

## Coaching overview

Coach your teams to train your employees to improve their skill set and enhance the quality of their service.

## Coaching users

<table id="table_nqm_rvp_2fb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Roles inherited

</th></tr></thead><tbody><tr><td>

sn\_coaching.trainee\[Coaching trainee\]

</td><td>

Able to view coaching assessments to which they belong.

 Able to add work notes in a coaching assessment by clicking **Review Assessments**.

</td><td>

-   skill\_user
-   survey\_reader
-   pa\_viewer

</td></tr><tr><td>

sn\_coaching.coach\[Coaching coach\]

</td><td>

Able to read and write coaching assessments assigned to the coach group to which they belong.

 Able to assign a training and virtual coaches to a coaching opportunity.

**Note:** The Coaching coach is not able to create a coaching opportunity.

</td><td>

-   sn\_coaching.trainee
-   pa\_viewer
-   sn\_lc.catalog\_manager

</td></tr><tr><td>

sn\_coaching.admin\[Coaching admin\]

</td><td>

Able to perform all functions.

</td><td>

-   sn\_coaching.coach
-   survey\_admin
-   sn\_cim\_improvement\_requester
-   sn\_lc.learning\_admin

</td></tr><tr><td>

Learning catalog group manager \[sn\_lc.catalog\_group\_manager\]

</td><td>

Grants administrative rights to create, read, or update learning libraries based on groups.

</td><td>

-   sn\_lc.task\_creator
-   sn\_lc.content\_writer

</td></tr></tbody>
</table>## Coaching workflow

The image shows a high-level workflow on how coaching admins set up Coaching, and how managers and agents use Coaching.

**Note:** You can use Predictive Intelligence when you use Coaching with [Workforce Optimization for ITSM](../../configurable-workforce-optimization-itsm/reference/workforce-optimization-itsm-landing-page.md).

![Coaching workflow](../../coaching/image/coaching-workflow.png "Assessing and training agents with Coaching with Learning")

1.  Coach admins set conditions in coaching opportunities that trigger an assessment. They can also define surveys used to assess agent performance.
2.  The system generates the assessment along with the survey, if defined, and assigns it to the coach.
3.  The coach assesses agents' ability to resolve incidents and the quality of their service. They also assign training tasks to agents based on the assessment.
4.  The trainee completes the assigned training tasks to address skill gaps and enhance skills set.
5.  The coach uses surveys to apply consistent, measurable scores across teams or tasks to evaluate them.
6.  Overall, the Coaching workflow helps agents enhance their skills set and the quality of their service.
7.  Predictive Intelligence uses supervised and unsupervised solutions definitions to recommend skills based on the work the agent has completed.

## Coaching benefits

<table id="table_b14_mmh_scc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Set up Coaching

</td><td>

Set up coaching opportunities, learning content, virtual coaches, and surveys.

</td><td>

Coach admin

</td></tr><tr><td>

Assess trainees and coach them.

</td><td>

-   Assess trainees' ability to resolve incidents.
-   Assign training tasks to agents based on assessments.
-   Use surveys to evaluate the trainees.

</td><td>

Coach or manager

</td></tr><tr><td>

Get trained to enhance your skills set.

</td><td>

Take assigned training tasks to address skill gaps.

</td><td>

Coaching trainee

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using Coaching, see:

-   [About Coaching](cf-coaching-overview.md)
-   [Setting up Coaching and surveys](cf-setting-up-coaching.md)
-   [Managing your coaching assessments](cf-getting-coached.md)
-   [Coaching reference](../reference/cf-coaching-reference.md)

