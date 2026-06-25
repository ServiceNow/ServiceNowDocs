---
title: Smart assessments in Privacy Case Management
description: Utilize the Smart Assessment Engine to perform smart assessments on privacy case action tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/smart-assessment-for-privacy-action-tasks.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Privacy Case Management, Privacy Management, Governance, Risk, and Compliance]
---

# Smart assessments in Privacy Case Management

Utilize the Smart Assessment Engine to perform smart assessments on privacy case action tasks.

Using the abilities of the Smart Assessment Engine, you can empower the privacy teams to initiate privacy case assessments. These assessments assist privacy case analysts in identifying impacted and related areas during a privacy case investigation. They also help determine whether employees in your organization adhere to the required regulations. The analyst can then collect observations and evidence from the stakeholders and arrive at a resolution. The Smart Assessment Engine provides numerous benefits some of which are listed as follows:

-   Configuring the assessment templates
-   Identifying the assessment responders
-   Defining the due date for responding to the assessment

In the Assessment Workspace, you can view the templates available for Privacy Case Management. You must ensure that the assessment template category is set to **Privacy Case Assessment** and the assessment targets are set to **Action task** and **Privacy case**. Only the assessment templates that are published are available for performing the assessments.

You can publish a new version of a smart assessment template when its questionnaire, response options, or automations must change. Each version keeps a complete change history. Only one version is published at a time, so new assessments stay consistent. New assessments use the latest published version, while in-progress assessments finish against the version they were created with. For more information, see [Create a version of a privacy assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/create-new-smart-asmt-version.md).

For more information about Smart Assessment Engine, refer to [Exploring Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/smart-assessment-engine-cf-explore.md)

## Pre-requisites to enable smart assessment in Privacy Case Management

-   **Smart assessment scoped applications**

    The base system ships the GRC smart assessment template to the users when the Privacy Case Management plugin is installed. However, the following scoped applications are required:

    1.  Smart Assessment core \(sn\_smart\_asmt\)
    2.  Smart assessment Migration tools \(sn\_smart\_asmt\_mig\). For more information, see [Migrate a legacy metric type to an assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-tmplt-migrate-metrics-to.md)
    3.  Smart Assessment Connected \(sn\_smart\_asmt\_conn\)
    4.  Smart Assessment Designer \(sn\_smart\_asmt\_desg\). For more information, see [Using the template designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-template-designer.md)
-   **Enable smart assessments system property**

    The administrator sets the **sn\_grc\_case\_mgmt.enable\_smart\_assessments** system property to **true** for the privacy case manager to assess the action tasks using the smart assessment method.

-   **Migrate the template**

    Create a new template in Smart Assessment Engine. For more information, see [Creating an assessment template from legacy assessment metric types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-migrating.md).


To get started with smart assessments, the privacy case administrator \(sn\_comp\_case.compliance\_case\_admin\), configures the assessment questionnaire. When an action task moves from the **Draft** state to the **Assigned** state, the assessment is sent. Based on the assessment results, appropriate remediation measures are identified and implemented. To learn more about how to configure a questionnaire in the [Exploring Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/smart-assessment-engine-cf-explore.md), refer to [Configuring Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/smart-assessment-engine-cf-config.md). To learn how to perform smart assessment on action tasks, refer to [Perform smart assessment on action tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/compliance-case-management/perform-smart-assessment-on-action-task.md).

