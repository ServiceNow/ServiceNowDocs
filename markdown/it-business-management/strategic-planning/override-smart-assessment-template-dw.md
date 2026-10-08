---
title: Use a custom smart assessment template for demands
description: Point the automatic demand to smart assessment trigger at a custom template by overriding the predefined DemandSmartAssessmentUtils script include provided for this customization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/override-smart-assessment-template-dw.html
release: brazil
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 1
keywords: [smart assessment template override, DemandSmartAssessmentUtils, change assessment template]
breadcrumb: [Configure, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Use a custom smart assessment template for demands

Point the automatic demand to smart assessment trigger at a custom template by overriding the predefined **DemandSmartAssessmentUtils** script include provided for this customization.

## Before you begin

A custom assessment template is created. For more information, see [Create an assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/sae-asmnt-template-create.md)

Role required: admin

**Warning:** The template's questions feed specific score fields on the demand \(Size, Strategic Alignment, Risk, ROI, Cost\) through metric mappings built for the predefined demand assessment template. A different template's questions and metrics aren't automatically remapped to those score fields, so scoring can silently stop working unless the replacement template is built with matching metrics. Test thoroughly in a non-production instance before doing this in production.

## About this task

The demand to screening trigger, the assessment completion check, and assessment score population all use one hardcoded template ID. The predefined **DemandSmartAssessmentUtils** script include is provided to override this template ID and other behavior in the base implementation. This helps to keep the base implementation as-is without modifying it directly.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Search for `DemandSmartAssessmentUtils`.

3.  Select the link in the alert to edit the record in the **Portfolio Planning** application scope.

    \[Omitted image "demand-smart-assess-script.png"\] Alt text: Hyperlink to edit the script include.

4.  Add a **SMART\_ASMT\_TEMPLATE\_ID** property to the object passed to **Object.extendsObject** and set to your template's sys\_id.

    As shipped, the script include has no overrides:

    ```
    var DemandSmartAssessmentUtils = Class.create();
    DemandSmartAssessmentUtils.prototype = Object.extendsObject(DemandSmartAssessmentUtilsSNC, {
        type: 'DemandSmartAssessmentUtils'
    });
    ```

    Add the override:

    ```
    var DemandSmartAssessmentUtils = Class.create();
    DemandSmartAssessmentUtils.prototype = Object.extendsObject(DemandSmartAssessmentUtilsSNC, {
        SMART_ASMT_TEMPLATE_ID: '<your_template_sys_id>',
        type: 'DemandSmartAssessmentUtils'
    });
    ```

5.  Add an override to the smart assessment metric map to support your template.

    ```
    SMART_ASMT_SECTION_METRIC_MAP: {
            '6a5bcff4ff27031090efffffffffff98': 'score_size',
            'e25bcff4ff27031090efffffffffff91': 'score_strategic_allignment',
            'ae5bcff4ff27031090efffffffffff94': 'score_risk',
            '6e5bcff4ff27031090efffffffffff89': 'score_value',
            '665bcff4ff27031090efffffffffff84': 'score_cost'
        },
    ```

6.  Select **Update**.


## Result

New smart assessments triggered for demands now use the specified template. For more information about a template's expected sections, questions, and weights, see [Assess demands with smart assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/strategic-planning/smart-assessments-overview.md).

