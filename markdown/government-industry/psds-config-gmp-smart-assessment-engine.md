---
title: Configure the Smart Assessment Engine for Grants Management
description: Create a new Smart Assessment template, which would show up in the compliance assessment field in the proposal playbook. The Smart assessment template is used to collect compliance information from applicants during proposal submission.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure PaCE Eligibility Framework Engine, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure the Smart Assessment Engine for Grants Management

Create a new Smart Assessment template, which would show up in the compliance assessment field in the proposal playbook. The Smart assessment template is used to collect compliance information from applicants during proposal submission.

## Before you begin

Role required: admin, sn\_smart\_asmt.assessment\_reader, sn\_smart\_asmt.template\_manager, sn\_gsm\_grnt\_mgmt.program\_manager, sn\_gsm\_grnt\_mgmt.grant\_director

Verify your scope is set to **Global**.

## About this task

The Smart Assessment Engine \(SAE\) streamlines and automates assessment processes, and supports various assessment types.

You can create assessment templates for grants compliance, and add instructions, questions, and reference information by using the template designer in the Smart Assessment Engine application. Smart assessments can help you to evaluate various situations, aspects, or records.

## Procedure

1.  Navigate to **All** &gt; **Smart Assessment Engine** &gt; **Administration** &gt; **Template Categories**.

2.  Select **New** to create a template category.

3.  On the form, fill in the fields.

    In the Category role field, enter `sn_smart_asmt.template_manager`.

4.  Select **Submit**.

5.  Navigate to **Workspaces** &gt; **Assessment Workspace**

6.  Select **New Template**, and on the form, fill in the fields.

    In the Assessment targets field, enter **Grants Management Case**.

7.  Navigate to the **Questions** tab and select **Add section**.

    ![Smart assessment engine.](../image/psds-gmp-smart-engine-questions-tab.png)

8.  On the form, fill in the details for the section, then select **Save**.

9.  Select **Add question**, and add a Single Select Drop-down Question of your choice.

    Repeat until you have added all of your desired questions.

10. Select **Publish**.


## Result

The template is now published, and can be selected in the compliance assessment activity of the Grants Setup Playbook. It is used to collect compliance information from applicants during proposal submission.

**Parent Topic:**[Configure PaCE Eligibility Framework Engine for use with Grants Management](psds-config-gmp-pace.md)

**Previous topic:**[Configure PaCE Restricted Caller Access Privileges \(RCA\)](psds-config-gmp-rca.md)

**Next topic:**[Configure the Reviewer Service Portal](psds-config-reviewer-service-portal.md)

