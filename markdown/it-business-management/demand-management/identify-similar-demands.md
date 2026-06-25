---
title: Identify similar records using Now Assist for Strategic Portfolio Management \(SPM\)
description: Detect similar demand records using the identify similar records Now Assist skill. This skill detects similar demand records based on contextual similarity in the name, description, and business case content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/demand-management/identify-similar-demands.html
release: australia
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist skill, Now Assist, Gen AI, Generative AI, SPM, Strategic Portfolio Management, Identify similar demand records]
breadcrumb: [Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Identify similar records using Now Assist for Strategic Portfolio Management \(SPM\)

Detect similar demand records using the identify similar records Now Assist skill. This skill detects similar demand records based on contextual similarity in the name, description, and business case content.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

If you have custom roles that require access to this skill, update the ACLs \(access control lists\) for those roles that require access. For more information, see [Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md).

Role required: it\_demand\_user

## Procedure

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **Create New**.

    Alternatively, you can create a demand from **Self-Service** &gt; **Demands** &gt; **Create New**.

2.  On the Demand form, fill in the **Name**, **Description**, and **Business case** fields.

    For a description of the field names, see [Demand form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-management/demand-form.md).

3.  Select **Save**.

4.  Select the **Identify similar demands** button to detect similar demand records.


## Result

The similar demands identified by Now Assist are displayed in the top banner and the Similar Demands related list.

\[Omitted image "similar-demand-new-color.png"\] Alt text: List of similar records identified by Now Assist.

**Note:**

-   If any similar records are present on the demand record, the related list is updated to display the list of identified similar records.
-   If there are no identified similar records for a demand, a message is displayed to convey the same and the related list remains empty.

## What to do next

View the full details of the identified similar demand records by selecting the demand number link from the Similar Demands related list.

**Parent Topic:**[Use Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-management/r_UsingDemandManagement.md)

**Related topics**  


[Assess demands]()

[Create a demand]()

[View demands]()

[Add details to demands]()

[RIDAC \(Risk, Issue, Decision, Action, and Request Changes\) records for a demand]()

[Reset a demand to Draft state]()

[Delete demands]()

[Move and resize a demand]()

[Train the similarity solution for Demand Management to find similar demands]()

[PPM PIWB template - Find similar demands]()

[Summarize demands with demand summarization skill]()

[Associate AI systems with demands]()

