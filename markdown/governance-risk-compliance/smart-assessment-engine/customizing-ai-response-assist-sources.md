---
title: Customizing AI Response Assist sources
description: The Smart Assessment Response Assist skill refers to previous assessments and documents to generate suggestions. By default, the skill uses scope-based matching for previous assessments and the files attached to the assessment instance for documents. To use different sources for a specific template category, implement the Smart Assessment Response Assist scripted extension point.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/customizing-ai-response-assist-sources.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-06-10"
reading_time_minutes: 6
keywords: [scripted extension point, extension point, SmartAsmtResponseAssistExtensionPoint, AI Response Assist, Document Provider, customize AI sources]
breadcrumb: [Configure, Now Assist, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Customizing AI Response Assist sources

The Smart Assessment Response Assist skill refers to previous assessments and documents to generate suggestions. By default, the skill uses scope-based matching for previous assessments and the files attached to the assessment instance for documents. To use different sources for a specific template category, implement the Smart Assessment Response Assist scripted extension point.

## What a scripted extension point is

A scripted extension point is a ServiceNow platform mechanism that lets you extend the functionality of an application without modifying the application's core code.

For background on how scripted extension points work and how to implement them, see [Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md).

## Why SAE exposes this extension point

Smart Assessment Response Assist generates draft answers from two source types.

-   **Previous assessments**

    Past smart and classic assessments whose responses the skill can semantically match against the current questions.

-   **Documents**

    Files the skill can analyze for answer content \(SOC 2 reports, security policies, DPAs, vendor documentation, and so on\).


The Smart Assessment Engine exposes the Smart Assessment Response Assist scripted extension point so that upstream applications and customer developers can provide that selection logic per template category.

## Default behavior when no implementation is registered

If no scripted extension point implementation handles the assessment's template category, the skill uses the following default sources.

-   **Previous smart assessments**

    The skill considers a prior smart assessment only if its scope items are an exact match or a superset of the current assessment's scope items. The prior assessment must cover every scope item on the current assessment; it may include additional scope items, but it can't be missing any. Only completed assessments are considered.

-   **Previous classic assessments**

    The skill matches on the individual scope item. A classic assessment that targets one of the current assessment's scope item records is considered.

-   **Documents**

    The document picker is populated from the files attached directly to the assessment instance.


## The Smart Assessment Response Assist scripted extension point

To customize the sources for a template category, create a script include that extends the following extension point:

`sn_smart_ai_assist.SmartAsmtResponseAssistExtensionPoint`

The extension point exposes four methods. Implement `handles` plus any method whose default you want to override; you don't have to override every method.

-   **`handles(templateCategoryId)`**

    Returns a boolean. Use the supplied `templateCategoryId` \(sys ID of the `sn_smart_asmt_template_category` record\) to decide whether this implementation should be applied to assessments in that category. Return `true` only for the categories your implementation owns so that other implementations or the defaults handle the rest.

-   **`getPreviousSmartAssessmentIdsForResponseAssist(assessmentId)`**

    Returns a comma-separated string of smart assessment instance sys IDs that should be considered when fetching responses to previous questions. The default implementation returns the IDs filtered by the scope-item rule described earlier. Override this method to designate a different set of prior smart assessments.

-   **`getPreviousClassicAssessmentIdsForResponseAssist(assessmentId)`**

    Returns an object with two properties:

    -   `recordIds` — a comma-separated string of record sys IDs.
    -   `recordRefField` — the reference field on `asmt_assessment_instance_question` to use for filtering. The value must be either `'source_id'` or `'instance'`.
    The default implementation returns scope-item record IDs paired with `recordRefField: 'source_id'`.

-   **`getDocumentIdsForResponseAssist(assessmentId)`**

    Returns an array of document descriptor objects. Each descriptor identifies one attachment to add to the document picker and the source record the attachment belongs to. Each object has these properties:

    -   `attachmentId` — sys ID of the `sys_attachment` record.
    -   `documentName` — file name of the attachment.
    -   `sourceTableName` — name of the table the source record belongs to. Used with `sourceId` to look up the source record's display value through `GlideRecordSecure`, so the running user's ACLs gate the lookup. The resolved display value is then used as the source name shown to the user.
    -   `sourceId` — sys ID of the source record to display.
    The default implementation returns an empty array. Override this method to return documents from any location your application controls. Examples include a folder on a parent record, files indexed in a document management system, and attachments on related records.


## Override behavior

The way an override interacts with the defaults differs by source type:

-   **Previous assessments \(smart and classic\)**

    **Replace**. When your implementation's `handles` returns `true` for a category, the IDs returned by the previous-assessment methods replace the default scope-item filtering for that category. If a method returns an empty result, that source produces no suggestions for the category — the default isn't applied as a fallback. This is intentional, so that a customer who wants to suppress a source can do so by returning an empty result.

-   **Documents**

    **Additive**. The files attached directly to the assessment instance are always offered in the document picker. The documents returned by `getDocumentIdsForResponseAssist` are added on top of those attachments. Your implementation supplements the attached files; it doesn't replace them.


## Example skeleton

The following script include is a starting point for an implementation. It returns the default values; replace the bodies of the methods you want to customize.

```
var SmartAsmtResponseAssistExtensionPoint = Class.create();
SmartAsmtResponseAssistExtensionPoint.prototype = {
    initialize: function() {},

    /**
     * Function to check whether current implementation should be used for the given template category sysId.
     * @param templateCategoryId - sysId of the template category (sn_smart_asmt_template_category).
     * @returns {boolean}
     */
    handles: function(templateCategoryId) {},

    /**
     * Returns comma-separated smart assessment instance sys_ids that should be considered
     * while fetching response of previous questions for the given assessmentId.
     * Default implementation filters by scope items matching the target assessment.
     * @param {string} assessmentId - Assessment instance sys_id.
     * @returns {string} Comma-separated smart assessment sys_ids.
     */
    getPreviousSmartAssessmentIdsForResponseAssist: function(assessmentId) {
        return new sn_smart_ai_assist.SmartAsmtResponseAssistUtils().getScopeItemFilteredIdsForAssessment(assessmentId);
    },

    /**
     * Returns an object containing comma-separated sys_ids and the reference field
     * to use for filtering previous question responses for the given assessmentId.
     * Default implementation filters by scope item records matching the target assessment.
     * @param {string} assessmentId - Assessment instance sys_id.
     * @returns {Object} Object with the following properties:
     *   - {string} recordIds - Comma-separated record sys_ids.
     *   - {string} recordRefField - Reference field on asmt_assessment_instance_question
     *                               used for filtering. Must be one of 'source_id' or 'instance'.
     */
    getPreviousClassicAssessmentIdsForResponseAssist: function(assessmentId) {
        return {
            recordIds: new sn_smart_ai_assist.SmartAsmtResponseAssistUtils().getScopeRecordsFilteredIdsForClassicAssessment(assessmentId).join(','),
            recordRefField: 'source_id'
        };
    },

    /**
     * Returns an array of document descriptors for response assist.
     * Each descriptor identifies an attachment and the source record it belongs to.
     * @param {string} assessmentId - Sys ID of the current Smart assessment instance (sn_smart_asmt_instance).
     * @returns {Array<Object>} Array of document descriptor objects with the following properties:
     *   - {string} attachmentId    - Sys ID of the sys_attachment record.
     *   - {string} documentName    - File name of the attachment.
     *   - {string} sourceTableName - Name of the table the source record belongs to.
     *   - {string} sourceId        - Sys ID of the source record to display to the user.
     */
    getDocumentIdsForResponseAssist: function(assessmentId) {
        return [];
    },

    type: 'SmartAsmtResponseAssistExtensionPoint'
};
```

After you create the script include, register it as an implementation of `sn_smart_ai_assist.SmartAsmtResponseAssistExtensionPoint`. For end-to-end steps on registering an implementation, see [Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md).

**Related topics**  


[Smart Assessment response assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/ai-generated-responses-for-smart-assessment.md)

[Configure Now Assist for Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/configure-now-assist-for-smart-assessment-engine.md)

