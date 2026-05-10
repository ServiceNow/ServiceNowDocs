---
title: Quick start tests for Assessments and Surveys
description: Validate that Assessments and Surveys still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Quick start tests for Assessments and Surveys

Validate that Assessments and Surveys still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

Assessments and Surveys quick start tests require activating the Automated Test Framework for Survey plugin \(com.glide.automated\_testing\_impl. Survey\).

**Note:** In the Australia release, all the buttons on the assessments or surveys cards have been removed. To run the Automated Test Framework tests successfully, the **Click the Take Survey button** step must be replaced with **Click the Survey card** for all tests that have this step.

|Name|Description|Release version|
|----|-----------|---------------|
|Survey: Basic Platform Based Test|Create a survey using Platform UI actions.|Madrid|
|Survey: Platform test for Dynamic Validation|Validate a survey dynamically.|Madrid|
|Survey: Clone Action|Clone a survey and validate the records of the original survey and the cloned survey.|New York|
|Survey: Question Bank Flow|Verify the addition of a question bank to a survey.|New York|
|Survey: Survey Creator Work Flow|Survey creator can create a survey and assign to the user who can take the survey and submit it.|New York|
|Assessment: Assign assessment to assessor|Assign an assessment to an assessor and verify that the instance is created for the assessor.|Orlando|
|Assessment: Create assessment as survey creator|Create an assignment as a survey creator.|Orlando|
|Assessment: Scale and Template support|Create, publish, and assign the assessment. Then take the assessment.|Rome|
|Assessment: Basic test flow|Verify the basic flow of an assessment.|Orlando|

**Parent Topic:**[Assessments and Surveys](../../assessments/concept/assessments-surveys-landing-page.md)

**Related topics**  


[Quick start tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/quick-start-tests.md)

