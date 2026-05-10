---
title: Copying responses from previous assessments
description: You can copy responses from previous assessments to save time and reduce repetition.
locale: en-US
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Respond to assessments, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Copying responses from previous assessments

You can copy responses from previous assessments to save time and reduce repetition.

## Copy smart assessment responses action

If you have the flow designer \[flow\_designer\] or system admin privileges, you can add the Copy smart assessment responses Workflow Studio action to your flows and subflows. This flow action enables you to reuse responses from a previous assessment.

The following table shows the Copy smart assessment responses action form.

|Field|Description|
|-----|-----------|
|Source Assessment \[Smart assessment instance\]|Assessment that you’re copying responses from for reuse. You must use the assessment instance record reference for this selection.|
|Target assessment \[Smart assessment instance\]|Assessment that you’re copying responses into. You must use the assessment instance record reference for this selection.|

Both the source assessment that you’re copying from and the target assessment for reusing responses must be based on the same template. The target assessment must be in an Open state. After this flow action is implemented, the answers from the source assessment are automatically available as answers for the assessor's responses.

For more information on adding actions to flows in Workflow Studio, see [Create a flow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-flow.md).

